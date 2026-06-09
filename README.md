# videos-kling — Pipeline de B-Roll para VSL (Kling 3.0)

Fábrica reutilizable para generar **b-roll vertical 9:16** para VSLs con flujo **voz-primero**:
la voz grabada es la fuente de verdad del timing → transcripción → cortes reales → keyframe (imagen fija)
→ animación image-to-video con **Kling 3.0** → lipsync solo en tomas habladas → montaje con la voz pegada.
Subtítulos y música se agregan después en el editor.

## Proveedor por defecto — kie.ai ⭐

Desde 2026-06-09 el i2v **y** los keyframes se hacen por defecto en **kie.ai** (router económico,
mismo Kling 3.0 y nano-banana, sin marca de agua). **fal** y **PiAPI** quedan como alternativas.
Mismo método y mismos JSON entre proveedores — **no mezclar dentro de un mismo lote**.

| Paso       | kie.ai (default) ⭐                       | fal (alternativa)                        |
|------------|------------------------------------------|------------------------------------------|
| Keyframe   | `batch_keyframes_kie.mjs` (nano-banana)  | `batch_keyframes_fal.mjs` (nano-banana)  |
| Video i2v  | `batch_kling3_kie.mjs` (Kling 3.0)       | `batch_kling3.mjs` (Kling 3.0 v3 Pro)    |
| Subir img  | `upload_asset.mjs` (fal CDN)             | `upload_asset.mjs` (fal CDN)             |
| Montaje    | `assemble_voiced.mjs` (ffmpeg)           | `assemble_voiced.mjs` (ffmpeg)           |

Modelo extra de animación: `batch_kling26.mjs` (Kling 2.6 Pro vía fal, presupuesto / comparación).
`upload_asset.mjs` y `assemble_voiced.mjs` son compartidos por todos los proveedores.

## Requisitos

- Node.js 18+ (usa `fetch` y `stream/promises` nativos)
- [ffmpeg](https://ffmpeg.org/) en el PATH (para el montaje)
- Credenciales por variable de entorno:
  - `KIE_API_KEY` — proveedor por defecto (kie.ai)
  - `FAL_KEY` — alternativa fal, transcripción/lipsync y `upload_asset.mjs`
  - `PIAPI_KEY` — alternativa PiAPI (opcional)

```powershell
# PowerShell (Windows)
$env:KIE_API_KEY = "tu_clave"
$env:FAL_KEY     = "tu_clave"
```

## Instalación

```bash
npm install
```

## Flujo oficial (voz-primero) — ejemplo nombre = v4

```bash
# 1. El usuario graba la voz completa → "Videos a iterar/V4.mp3"

# 2. Transcribir (Whisper word-level)
node transcribe_fal.mjs "Videos a iterar/V4.mp3" v4 es      # → config/transcript_v4.json

# 3. Armar a mano config/cuts_v4.json = [{n,start,end,guion}] con los timestamps REALES

# 4. Cortar la voz por toma
node cut_audio.mjs config/cuts_v4.json "Videos a iterar/V4.mp3" audio/v4   # → audio/v4/seg_<n>.wav

# 5. Keyframes (kie.ai por defecto)
node batch_keyframes_kie.mjs config/keyframes_input_v4.json v4
#    → assets/v4/kf_<n>.png + config/kf_map_v4.json + config/batch_input_v4.json

# 6. Video i2v MUDO (kie.ai por defecto, std = 720p)
node batch_kling3_kie.mjs config/batch_input_v4.json clips/v4 std        # → clips/v4/raw_<n>.mp4

# 7. Lipsync SOLO en tomas con personaje hablando de frente
node batch_lipsync_fal.mjs config/lipsync_input_v4.json clips/v4_sync    # → clips/v4_sync/lip_<n>.mp4

# 8. Montaje con la voz pegada (no sobreescribe)
node assemble_voiced.mjs v4 "Videos a iterar/V4.mp3"                     # → output/final_v4_voiced.mp4
```

Los scripts de generación muestran una **tabla de aprobación con costo** y piden `OK` antes de gastar.

### Formato de los JSON

```json
// config/keyframes_input_<n>.json
[ { "n": "01", "prompt": "…", "refs": ["https://…"], "out": "kf_01.png" } ]

// config/batch_input_<n>.json
[ { "n": "01", "image_url": "https://…", "prompt": "…", "duration": 5 } ]

// config/lipsync_input_<n>.json
[ { "n": "01", "video": "clips/v4/raw_01.mp4", "audio": "audio/v4/seg_01.wav" } ]
```

## Precios de referencia

| Herramienta                          | Precio              | Nota                          |
|--------------------------------------|---------------------|-------------------------------|
| kie.ai nano-banana keyframe          | ~$0.02/img          | ½ de fal, default ⭐          |
| kie.ai Kling 3.0 i2v (std 720p)      | ~$0.07/s            | default ⭐ (70 cr/5s)         |
| fal nano-banana                      | ~$0.039/img         | alternativa                   |
| fal Kling 3.0 v3 Pro sin audio       | $0.112/s            | alternativa                   |
| fal Kling 2.6 Pro                    | $0.07/s             | presupuesto / comparación     |
| Kling LipSync                        | $0.014/5s           | solo tomas habladas           |
| PiAPI nano-banana-2 (1K)             | $0.06/img           | alternativa                   |
| PiAPI Kling 3.0 720p (std) sin audio | $0.10/s             | alternativa                   |

## Método y convenciones

El método completo (estructura de venta, roles de estilo, coherencia visual, animación aterrizada,
regla de duración de toma, control de gasto, flujo voz-primero) está documentado en [`CLAUDE.md`](./CLAUDE.md).

## Notas

- **Nunca** se sobreescribe un output anterior: cada video tiene su propio archivo (`output/final_<n>_voiced.mp4`).
- El packaging real **nunca** se inventa con IA: se sube la imagen real y se coloca en escena (nano-banana).
- Categoría salud: los claims son responsabilidad del operador; incluir disclaimer.
- Las keys de API van por variable de entorno y están excluidas del repo (ver `.gitignore`).
- Material pesado regenerable (`clips/`, `audio/`, `*.mp4`, frames extraídos) **no** se versiona; sí las voces `V<n>.mp3`.
```
