# Pipeline de B-Roll para VSL — PiAPI + Kling 3.0
# Carpeta: videos-kling. Entorno separado de la fábrica fal/Kling 2.6 Pro en videos-broll.
# Propósito: probar Kling 3.0 (mejor calidad, multi-shot, audio nativo) y comparar contra fal.

═══════════════════════════════════════════════════════════
QUÉ ENTREGA
═══════════════════════════════════════════════════════════
Video vertical 9:16 montado: b-roll en orden, cortes secos, mudo, duración alineada a la voz.
Voz, subtítulos y música los pongo yo en el editor. Este pipeline solo hace el b-roll.
Entregables: final_<SHOTLIST>.mp4 + carpeta clips/ numerados + index_<SHOTLIST>.md.
NUNCA sobreescribir un output anterior — cada shotlist tiene su propio archivo.

═══════════════════════════════════════════════════════════
CÓMO SE USA (fábrica reutilizable)
═══════════════════════════════════════════════════════════
1. Para cada video nuevo me pasás un BRIEF + GUION + VO_DURATION (+ TIMECODES si los hay).
2. Yo aplico ESTE método al brief: segmento, genero keyframes, animo, monto.
3. El método NO cambia entre productos; solo cambia el brief.

═══════════════════════════════════════════════════════════
MÉTODO
═══════════════════════════════════════════════════════════

## A. FLUJO IMAGEN→VIDEO
KEYFRAME (imagen fija vertical 9:16 alta resolución) → ANIMAR con Kling 3.0 vía PiAPI.
Para tomas de producto: imagen REAL del packaging (NUNCA inventado con IA — sale falso).

## B. ESTRUCTURA DE VENTA
HOOK → AGITAR → AUTORIDAD → HISTORIA/CASO → MECANISMO (villano + solución) → ORIGEN/PRUEBA
→ TRANSFORMACIÓN → PRODUCTO → URGENCIA/GARANTÍA → CTA. No todos usan todas.

## C. ROLES DE ESTILO (uno por toma)
- STORY   → personaje/testimonio/experto. "Pixar-style 3D animation, warm cinematic lighting"
- SCIENCE → anatomía/moléculas/mecanismo. "hyperreal medical 3D render / scientific CGI"
- EMOTION → miedo/lucha/metáfora. "dark cinematic, dramatic lighting, moody"
- CONCEPT → producto sin marca. Ingredientes/cápsulas genéricas. El packaging real lo meto vía nano-banana o en editor.

## D. COHERENCIA VISUAL
- ANCLA DE ESTILO: una MISMA frase de render en TODOS los keyframes del video, definida en el brief.
- ACENTO DE COLOR compartido en todas las tomas (sutil en CGI clínico, protagonista en CONCEPT).
- Misma LENTE/tratamiento en todas.
- CONTRASTE intencional permitido (problema oscuro vs solución cálida) — no igualar todo.
- Personajes/objetos recurrentes: reusar su MISMO keyframe base.

## E. ANIMACIÓN ATERRIZADA (evitar "flotar en el vacío")
Cada prompt lleva:
1. ANCLAJE FÍSICO (mesa, suelo, mano — nunca el vacío).
2. ACCIÓN CON PROPÓSITO (gesto significativo, no solo "moverse/girar").
3. CÁMARA CONCRETA Y LENTA ("slow push-in", "slow pan"). Evitar "orbit".
negative_prompt: "floating in void, spinning, orbiting, weightless, screensaver, empty background,
static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry,
talking mouth closeup"

## F. LIPSYNC (voz va aparte)
Personajes en plano medio gesticulando; NO foco en boca. La palabra la lleva la voz + subtítulos.
Preferir animación estilizada sobre realistas hablando en primer plano.

## G. PRODUCTO REAL
Packaging NUNCA se inventa. Subir imagen real, colocarla en escena con nano-banana, después animar.
Describir el tipo según el brief (pouch/bolsa, frasco, caja).

## H. CONTROL DE GASTO
- Pedir OK antes de CADA generación de pago. NO reintentar sin avisar.
- Probar 1 toma antes de lanzar el lote.
- LOTES PARALELOS: mostrar tabla completa (toma | prompt | costo) y esperar OK — todo se cobra de golpe.

## I. REGLA DE DURACIÓN DE TOMA (versión OPTIMIZADA PARA AHORRO)
Kling entrega clips ~4.8-4.9 s reales cuando se piden "5 s". En vez de subir todo a "10 s", combinar:

| Tramo de voz     | duration | Nota |
|------------------|----------|------|
| ≤ 5.5 s          | "5"      | Si necesita 5.0–5.5 s: congelar último frame 0.1–0.5 s en editor. Imperceptible, ahorra $0.50/toma. |
| 5.5 s – 10 s     | "10"     | $1.00/clip — solo cuando realmente necesario. |
| > 10 s           | PARTIR   | Dividir en 2 tomas con planos distintos. |

POR QUÉ 5.5 Y NO 5.0: Estirar 0.1–0.5 s del último frame (freeze frame en Premiere/CapCut) no se nota
porque es el último instante antes del corte. Estirar > 0.5 s sí se nota — ahí usar "10".
AHORRO TÍPICO: un VSL de 14 tomas con 5 "casi 5 s" = ~$2.50 extra innecesarios sin esta regla.
NOTA PARA EL EDITOR: el index_<SHOTLIST>.md indica las tomas que necesitan freeze frame y cuántos
segundos estirar. Es 1 click en la mayoría de editores.

═══════════════════════════════════════════════════════════
HERRAMIENTAS PiAPI (usar EXACTAMENTE así)
═══════════════════════════════════════════════════════════

### KEYFRAME — Nano Banana 2 vía PiAPI
Endpoint: POST https://api.piapi.ai/api/v1/task
Body:
{
  "model": "gemini",
  "task_type": "nano-banana-2",
  "input": {
    "prompt": "...",
    "aspect_ratio": "9:16",
    "output_format": "png",
    "resolution": "1K",
    "safety_level": "high",
    "image_urls": ["https://..."]   ← SOLO si hay imagen de referencia (array, NO base64, NO string)
  }
}
Headers: x-api-key: <PIAPI_KEY>
Costo: $0.06/imagen (1K). nano-banana-pro existe pero cuesta $0.105 — usar nano-banana-2.
IMPORTANTE: NO acepta base64. Para imágenes locales: subir a fal storage primero.
Output URL: data.output.image_url (ephemeral — descargar y re-subir a CDN antes de animar).

### VIDEO — Kling 3.0 image-to-video vía PiAPI
Endpoint: POST https://api.piapi.ai/api/v1/task
Body:
{
  "model": "kling",
  "task_type": "video_generation",
  "input": {
    "version": "3.0",
    "mode": "std",          ← "std" = 720p, "pro" = 1080p. NO existe "i2v" ni campo "resolution".
    "image_url": "<URL del keyframe>",
    "prompt": "<prompt animación>",
    "duration": 5,          ← INTEGER (no string). El modo i2v se activa con image_url, no con mode.
    "aspect_ratio": "9:16",
    "enable_audio": false
  }
}
Headers: x-api-key: <PIAPI_KEY>
Devuelve task_id INMEDIATAMENTE → polling con GET /api/v1/task/{task_id} hasta status=completed.
Video URL en respuesta: data.output.video como STRING DIRECTO (no .resource ni .resource_without_watermark).
Costo: 720p sin audio = $0.10/s = $0.50 por clip de 5s. (1080p mode "pro" = $0.75/clip)

### PARALELO
PiAPI es ASÍNCRONO NATIVO — sin cola, sin límite visible de concurrencia.
Disparar TODOS los task POSTs casi al mismo tiempo (Promise.all sobre el array de shots), guardar
los task_ids, hacer polling de todos hasta que cada uno esté completed, descargar.

═══════════════════════════════════════════════════════════
PRECIOS REALES (verificados mayo 2026 desde piapi.ai/kling-3-0)
═══════════════════════════════════════════════════════════
| Herramienta                    | Precio       | Nota                              |
|--------------------------------|--------------|-----------------------------------|
| nano-banana-2 keyframe (1K)    | $0.06/img    | model:"gemini" task:"nano-banana-2" — DEFAULT |
| nano-banana-pro keyframe (1K)  | $0.105/img   | model:"gemini" task:"nano-banana-pro" — NO usar |
| Kling 3.0 720p sin audio       | $0.10/s      | $0.50 clip 5s — DEFAULT producción (mode:"std") |
| Kling 3.0 720p con audio       | $0.15/s      | NO usar (voz va aparte)           |
| Kling 3.0 1080p sin audio      | $0.15/s      | $0.75 clip 5s — héroe/producto (mode:"pro") |
| Kling 3.0 1080p con audio      | $0.20/s      | NO usar                           |

═══════════════════════════════════════════════════════════
CUMPLIMIENTO
═══════════════════════════════════════════════════════════
No inventar credenciales médicas, testimonios ni aprobaciones oficiales.
Categoría salud (diabetes): claims fuertes son responsabilidad del operador, incluir disclaimer.

═══════════════════════════════════════════════════════════
QUÉ DEBE TRAER UN BRIEF
═══════════════════════════════════════════════════════════
- Producto: nombre, qué es, ingrediente clave, tipo de packaging real + imagen del producto.
- Avatar/cliente objetivo e idioma.
- Guion + VO_DURATION + TIMECODES (idealmente).
- ANCLA DE ESTILO de ese video.
- ACENTO DE COLOR de la marca.
- Personajes recurrentes y sus descripciones.
- Paletas por "mundo" si hay contraste intencional.
- Claims permitidos y disclaimer.

═══════════════════════════════════════════════════════════
SEGUNDO PROVEEDOR — fal (alternativa a PiAPI, mismo método)
═══════════════════════════════════════════════════════════
Esta carpeta soporta DOS proveedores para el MISMO método (sección MÉTODO arriba no cambia).
Elegir uno por video según calidad/precio/disponibilidad. NO mezclar dentro de un mismo lote.

| Paso       | PiAPI (default de esta carpeta) | fal (alternativa)              |
|------------|---------------------------------|--------------------------------|
| Keyframe   | batch_keyframes.mjs (nano-banana-2) | batch_keyframes_fal.mjs (nano-banana) |
| Video i2v  | batch_piapi.mjs (Kling 3.0)     | batch_kling3.mjs (Kling 3.0 v3 Pro) |
| Subir img  | upload_asset.mjs (fal storage)  | upload_asset.mjs (fal storage) |
| Montaje    | assemble.mjs (ffmpeg)           | assemble.mjs (ffmpeg)          |

NOTA: upload_asset.mjs y assemble.mjs son compartidos por ambos proveedores.
El PiAPI también usa fal storage para subir imágenes locales (nano-banana no acepta base64).

### Credenciales (variables de entorno)
- PiAPI:  PIAPI_KEY
- fal:    FAL_KEY
Nunca commitear las keys. Van por env var, no en archivos.

### fal — VIDEO: batch_kling3.mjs
USO:  node batch_kling3.mjs [batch_input.json] [clips_dir]   (default clips_dir = clips_v3/)
- endpoint: fal-ai/kling-video/v3/pro/image-to-video
- campo de imagen: start_image_url (NO image_url como en PiAPI)
- generate_audio forzado a false (mudo, voz va aparte)
- duration: entero 3–15
- precio: $0.112/s sin audio (Kling 3.0 Pro / 1080p). Anima mucho más que 2.6.
FORMATO batch_input.json:
  [ { "n":"01", "image_url":"https://…", "prompt":"…", "duration":5|10,
      "negative_prompt":"(opcional)", "cfg_scale":0.5 (opcional) } ]
Muestra tabla de aprobación y pide "OK" antes de gastar (regla H de control de gasto).

### fal — KEYFRAME: batch_keyframes_fal.mjs
USO:  node batch_keyframes_fal.mjs [keyframes_input.json] [out_dir]   (default out_dir = assets/)
- sin refs → fal-ai/nano-banana (texto→imagen)
- con refs → fal-ai/nano-banana/edit (image_urls de referencia, para consistencia de personajes)
- 9:16, png. precio aprox $0.039/img.
FORMATO keyframes_input.json:
  [ { "n":"01", "prompt":"…", "refs":["https://…"] (opcional), "out":"kf_01.png" (opcional) } ]

### fal — SUBIR IMAGEN LOCAL: upload_asset.mjs
USO:  node upload_asset.mjs <ruta_local>   → imprime la URL de fal storage (CDN).
Necesario porque nano-banana (ambos proveedores) NO acepta base64.
