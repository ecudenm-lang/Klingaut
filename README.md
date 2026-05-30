# videos-kling — Pipeline de B-Roll para VSL (Kling 3.0)

Fábrica reutilizable para generar **b-roll vertical 9:16** para VSLs: keyframe (imagen fija) →
animación image-to-video con **Kling 3.0** → montaje con cortes secos, mudo, alineado a la voz.
La voz, subtítulos y música se agregan después en el editor.

Soporta **dos proveedores** para el mismo método, elegibles por video:

| Paso       | PiAPI (default)                      | fal (alternativa)                       |
|------------|--------------------------------------|------------------------------------------|
| Keyframe   | `batch_keyframes.mjs` (nano-banana-2)| `batch_keyframes_fal.mjs` (nano-banana)  |
| Video i2v  | `batch_piapi.mjs` (Kling 3.0)        | `batch_kling3.mjs` (Kling 3.0 v3 Pro)    |
| Subir img  | `upload_asset.mjs` (fal storage)     | `upload_asset.mjs` (fal storage)         |
| Montaje    | `assemble.mjs` (ffmpeg)              | `assemble.mjs` (ffmpeg)                  |

`upload_asset.mjs` y `assemble.mjs` son compartidos. No mezclar proveedores dentro de un mismo lote.

## Requisitos

- Node.js 18+ (usa `fetch` y `stream/promises` nativos)
- [ffmpeg](https://ffmpeg.org/) en el PATH (para `assemble.mjs`)
- Credenciales por variable de entorno:
  - `PIAPI_KEY` — para el pipeline PiAPI
  - `FAL_KEY` — para el pipeline fal y para `upload_asset.mjs`

```powershell
# PowerShell (Windows)
$env:PIAPI_KEY = "tu_clave"
$env:FAL_KEY   = "tu_clave"
```

## Instalación

```bash
npm install
```

## Uso

### 1. Subir imágenes locales (ambos proveedores)
nano-banana no acepta base64; las imágenes locales se suben a fal storage primero.
```bash
node upload_asset.mjs ./assets/packaging_real.png   # imprime la URL CDN
```

### 2. Keyframes
```bash
# PiAPI
node batch_keyframes.mjs keyframes_input.json assets/
# fal
node batch_keyframes_fal.mjs keyframes_input.json assets/
```
`keyframes_input.json`:
```json
[ { "n": "01", "prompt": "…", "refs": ["https://…"], "out": "kf_01.png" } ]
```

### 3. Video (image-to-video, Kling 3.0)
```bash
# PiAPI
node batch_piapi.mjs batch_input.json clips/
# fal
node batch_kling3.mjs batch_input.json clips_v3/
```
`batch_input.json`:
```json
[ { "n": "01", "image_url": "https://…", "prompt": "…", "duration": 5 } ]
```
Ambos scripts muestran una **tabla de aprobación con costo** y piden escribir `OK` antes de gastar.

### 4. Montaje
```bash
node assemble.mjs   # une los clips en orden → final_<shotlist>.mp4
```

## Precios de referencia

| Herramienta                         | Precio       |
|-------------------------------------|--------------|
| PiAPI nano-banana-2 (1K)            | $0.06/img    |
| PiAPI Kling 3.0 720p (std) sin audio| $0.10/s      |
| PiAPI Kling 3.0 1080p (pro) sin audio| $0.15/s     |
| fal nano-banana                     | ~$0.039/img  |
| fal Kling 3.0 v3 Pro sin audio      | $0.112/s     |

## Método y convenciones

El método completo (estructura de venta, roles de estilo, coherencia visual, animación aterrizada,
regla de duración de toma, control de gasto) está documentado en [`CLAUDE.md`](./CLAUDE.md).

## Notas

- **Nunca** se sobreescribe un output anterior: cada shotlist tiene su propio archivo.
- El packaging real **nunca** se inventa con IA: se sube la imagen real y se coloca en escena.
- Categoría salud: los claims son responsabilidad del operador; incluir disclaimer.
- Las keys de API van por variable de entorno y están excluidas del repo (ver `.gitignore`).
