# Shotlist — Glucora / "Mi Esposo Es Diabético" V4
# Historia: esposa testimonia cómo su esposo diabético mejoró con Glucora (berberina+canela+cromo gotas)
# Audio: voz narradora femenina (esposa) · duración: 80s · vertical 9:16
# Modelo de imagen: Nano Banana vía fal (batch_keyframes_fal.mjs)
# Modelo de video: Kling 3.0 v3 Pro vía fal (batch_kling3.mjs)
# Estética: 3D Pixar style, warm cinematic lighting
# Regla anti-lipsync: personajes en plano medio gesticulando; NO primer plano de boca.
# ANCLA DE ESTILO: "3D Pixar style character, warm cinematic lighting"
# ACENTO DE COLOR: Dorado-ámbar cálido (golden hour exterior) + interiores de ámbar naranja

═══════════════════════════════════════════════════════════
DATOS TÉCNICOS DEL LOTE
═══════════════════════════════════════════════════════════
- Total tomas: 11
- Distribución duración:
  · 4 tomas con duration "5"  (≤5.5s) → 4 × 5s × $0.112 = $2.24
  · 7 tomas con duration "10" (>5.5s) → 7 × 10s × $0.112 = $7.84
- Costo videos (fal Kling 3.0 Pro): $10.08
- Costo imágenes (fal nano-banana ~$0.04/img): 11 × $0.04 = $0.44
- COSTO TOTAL ESTIMADO: ~$10.52 USD

═══════════════════════════════════════════════════════════
NOTA SOBRE NANO BANANA (fal)
═══════════════════════════════════════════════════════════
fal nano-banana responde mejor a prompts CONCRETOS y FÍSICOS:
- "3D Pixar style" va al INICIO de cada prompt.
- Describir CARA, EXPRESIÓN, OBJETO específicamente.
- El packaging GLUCORA es real — tomas 10 y 11 requieren packaging real subido vía upload_asset.mjs.

═══════════════════════════════════════════════════════════
GUION TRANSCRITO COMPLETO
═══════════════════════════════════════════════════════════
[s01–08]  "Mi esposo es diabético. Se me queda dormido en la silla. Va cuatro veces al baño de noche
           y yo me despierto."
[s09–16]  "Le compré berberina en gotas. Sin avisarle, la puse junto a sus pastillas."
[s17–24]  "Esto es lo que pasó en sesenta días. Ni preguntó qué era. Se puso las gotas y siguió
           con su mañana."
[s25–32]  "Así empezó todo. Yo solo conté los días. Día catorce: conté sus idas al baño esa noche.
           Dos. No cuatro. Dos. Él no lo notó. Yo sí. Yo siempre noto."
[s33–40]  "Día treinta: me dijo algo que no me decía hace años. Anoche dormí bien. Se midió,
           sacudió el glucómetro."
[s41–48]  "Día sesenta: nos medimos juntos. Yo ciento cinco. Él ciento treinta. Me miró,
           miró las gotas, me agarró la mano. No dijo nada. No hacía falta."
[s49–51]  "Ya no se levanta de noche. Ya no se queda dormido en la silla."
[s52–53]  "Ya no le cuento las idas al baño."
[s54–56]  "Recuperé a mi esposo y dejé de contar."
[s57–64]  "Si alguien que amas tiene diabetes y tú también cuentas, hazlo. No esperes seis años."
[s65–72]  "Glucora berberina. La fórmula líquida que frena al hígado de producir azúcar sin control.
           Lo que seis años de pastillas no pudieron. Sesenta días de gotas."
[s73–80]  "Sí, más de diez ingredientes. Dos gotas al día. La diabetes le roba noches.
           Devuélveselas. Consíguela abajo."

═══════════════════════════════════════════════════════════
TOMA 01 · HOOK — ESPOSO DORMIDO EN SILLÓN · duration "10" · s01–08 (8.03s)
═══════════════════════════════════════════════════════════
GUION: "Mi esposo es diabético. Se me queda dormido en la silla. Va cuatro veces al baño de noche y yo me despierto."
ROL: STORY
LO QUE SE VE: Sala de estar cálida y oscura. El esposo (hombre hispano de mediana edad, cabello canoso, barba corta, camisa azul) duerme en un sillón tipo reclinable de cuadros escoceses. La esposa (mujer hispana ~38 años, cabello negro rizado recogido, sudadera gris) está de pie a su lado, una mano en su hombro, mirándolo preocupada. Lámpara de mesa iluminando la escena. Fotos familiares en la pared. Crucifijo en la pared.

kf_prompt:
"3D Pixar style character, warm cinematic lighting, soft amber home tones. A tired Hispanic middle-aged man with gray-streaked hair and short beard, wearing a blue t-shirt and dark jeans, slumped asleep in a plaid armchair in a cozy living room — his mouth slightly open, one arm hanging limp over the armrest. A worried Hispanic woman in her late 30s with dark curly hair in a bun, wearing a gray hoodie and jogger pants, stands beside him placing a gentle hand on his shoulder, looking at him with concern. Warm lamp light from a side table. Family photos on the wall. Vertical 9:16."

anim_prompt:
"The woman gently shakes the man's shoulder; he stirs slightly without fully waking. Her free hand presses to her chest in worry. Camera: slow push-in toward her concerned face from a medium wide shot. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.03s → recortar ~1.9s del final en editor)

═══════════════════════════════════════════════════════════
TOMA 02 · HISTORIA — ESPOSA DESCUBRE LA BERBERINA · duration "10" · s08–16 (8.0s)
═══════════════════════════════════════════════════════════
GUION: "Le compré berberina en gotas. Sin avisarle, la puse junto a sus pastillas."
ROL: STORY
LO QUE SE VE: Habitación de mañana. Esposa de pie junto a mesita de noche con glucómetro, vaso de agua, pastillas Metformin y un frasquito gotero ámbar (berberina). La sostiene con las dos manos, ojos muy abiertos de sorpresa y determinación.

kf_prompt:
"3D Pixar style character, warm cinematic lighting, soft amber bedroom tones. A worried Hispanic woman in her late 30s with dark curly hair loosely tied up, wearing a gray hoodie, stands beside a wooden nightstand inside a bright morning bedroom. On the nightstand: a glucose meter, a glass of water, a bottle of Metformin pills, and a small amber glass dropper bottle labeled 'Berberina en gotas'. She holds the dropper bottle in both hands, staring at it with wide surprised eyes, mouth slightly open. Warm morning sunlight from a window. Vertical 9:16."

anim_prompt:
"The woman picks up the amber dropper bottle from the nightstand and turns it slowly in her hands, examining the label with wide curious eyes. Her other hand stays resting on the nightstand surface. Camera: slow push-in toward the bottle held in her hands. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s → recortar ~2.0s del final en editor)

═══════════════════════════════════════════════════════════
TOMA 03 · HISTORIA — ESPOSO TOMA LAS GOTAS SIN SABER · duration "10" · s16–24 (7.8s)
═══════════════════════════════════════════════════════════
GUION: "Esto es lo que pasó en sesenta días. Ni preguntó qué era. Se puso las gotas y siguió con su mañana."
ROL: STORY
LO QUE SE VE: Habitación de mañana. Esposa discretamente coloca el frasquito junto a la Metformin. Esposo en pijama azul oscuro sentado en la cama descubre el frasco, se lo pone sin preguntar, y se levanta de la cama. Esposa lo observa desde el fondo sonriendo.

kf_prompt:
"3D Pixar style character, warm cinematic lighting, soft amber bedroom tones. A Hispanic woman in her late 30s with dark curly hair loosely tied, wearing a gray hoodie, leans forward over a wooden nightstand placing a small amber glass dropper bottle next to a bottle of Metformin pills and a glucose meter. She wears a mischievous half-smile. Her husband — a tired Hispanic middle-aged man in navy blue pajamas — sits on the bed edge in the background, unaware, looking down. Morning sunlight fills the room. Vertical 9:16."

anim_prompt:
"The woman quietly sets the dropper bottle next to the Metformin pills on the nightstand, then steps back with a small triumphant nod. In the background the husband sits up from bed and reaches for the bottle, examining it curiously. Camera: slow pan from the nightstand to the husband discovering the bottle. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (7.8s → recortar ~2.2s del final en editor)

═══════════════════════════════════════════════════════════
TOMA 04 · AGITAR — NOCHE, ESPOSA CONTANDO VIAJES AL BAÑO · duration "10" · s24–32 (8.0s)
═══════════════════════════════════════════════════════════
GUION: "Así empezó todo. Yo solo conté los días. Día catorce: conté sus idas al baño esa noche. Dos. No cuatro. Dos. Él no lo notó. Yo sí. Yo siempre noto."
ROL: EMOTION
LO QUE SE VE: Habitación oscura a las 2:00 AM. Esposa acostada despierta con los ojos muy abiertos, ansiosa. Esposo duerme profundamente a su lado. Reloj digital rojo marcando 2:00 AM. Ella levanta dos dedos contando en silencio.

kf_prompt:
"3D Pixar style character, dark cinematic lighting, deep blue-navy bedroom night tones. A Hispanic woman in her late 30s with short dark hair, wearing a dark t-shirt, lies in bed awake at 2:00 AM — her eyes wide open, anxious, staring at the ceiling. Beside her, a Hispanic middle-aged man with gray-streaked hair and beard sleeps deeply. A red digital clock on the nightstand reads 2:00 AM. The room is lit only by the clock's red glow. She holds up two fingers counting silently. Vertical 9:16."

anim_prompt:
"The woman in bed raises two fingers slowly, then three, counting bathroom trips in her mind while her husband sleeps undisturbed beside her. Her expression shifts from worried to quietly hopeful. Camera: slow push-in toward her face lit by the red clock glow. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s → recortar ~2.0s del final en editor)

═══════════════════════════════════════════════════════════
TOMA 05 · TRANSFORMACIÓN — DÍA 30, EL GLUCÓMETRO DICE 95 · duration "10" · s32–40 (8.0s)
═══════════════════════════════════════════════════════════
GUION: "Día treinta: me dijo algo que no me decía hace años. Anoche dormí bien. Se midió, sacudió el glucómetro."
ROL: STORY
LO QUE SE VE: Mañana brillante en el dormitorio. El esposo sentado en la cama sostiene el glucómetro que marca 95 mg/dL, levanta el brazo en señal de triunfo. La esposa, acostada de lado, lo mira con ojos de asombro y alegría.

kf_prompt:
"3D Pixar style character, warm bright morning lighting, golden sunlight through curtains. A Hispanic middle-aged man with gray-streaked hair and short beard, wearing a light blue t-shirt, sits upright on the edge of a bed holding a glucose meter up in one hand — the screen shows '95 mg/dL'. His other arm is raised in a fist pump of surprise and joy. His Hispanic wife, dark hair in a bun, lies on her side in bed watching him with amazed sleepy eyes. Wooden headboard behind them. Vertical 9:16."

anim_prompt:
"The husband raises the glucose meter triumphantly showing the '95' reading, while his wife props herself up on one elbow to look at it with wide delighted eyes. He points at the number with excitement. Camera: slow push-in from medium shot toward the glucose meter display. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s → recortar ~2.0s del final en editor)

═══════════════════════════════════════════════════════════
TOMA 06 · TRANSFORMACIÓN — DÍA 60, MANOS ENTRELAZADAS · duration "5" · s40–48 (8.0s)
═══════════════════════════════════════════════════════════
NOTA: Esta toma dura 8.0s pero tiene dos momentos distintos visualmente. Se puede partir en 2 clips
de 4s cada uno — VER NOTA PARA EL EDITOR abajo. Si se deja en una sola toma, generar a "10".

GUION: "Día sesenta: nos medimos juntos. Yo ciento cinco. Él ciento treinta. Me miró, miró las gotas, me agarró la mano. No dijo nada. No hacía falta."
ROL: STORY / EMOTION
LO QUE SE VE: Cama iluminada. Pareja tomada de las manos. Plano detalle de las manos entrelazadas de ambos sobre la cama — ella con anillo de bodas. Luz cálida bañando la escena.

kf_prompt:
"3D Pixar style character, warm golden morning lighting. A Hispanic couple sits together on a bed: the wife — dark hair in a bun, wearing a gray t-shirt — and the husband — gray-streaked hair and beard, blue t-shirt. They sit facing each other, hands intertwined resting on the bed between them. Both look at each other with tender emotional smiles. Soft golden sunlight fills the room from a window behind them. Wooden headboard. Vertical 9:16."

anim_prompt:
"The husband gently squeezes the wife's hands with both of his; she squeezes back and tilts her head toward him with a warm smile. Their clasped hands rest on the bed surface. Camera: slow push-in to a medium close shot of their joined hands bathed in golden light. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s — generar 10s, recortar ~2.0s del final en editor)
⚠ EDITOR: Esta toma fue marcada duration "5" en el JSON porque la escena central de las manos
   dura ~3s antes del siguiente corte. Si se separa en 2 tomas, usar clip 48–50 por separado.

═══════════════════════════════════════════════════════════
TOMA 07 · TRANSFORMACIÓN — SPLIT-SCREEN 3 ESCENAS FELICES · duration "5" · s48–51 (2.94s)
═══════════════════════════════════════════════════════════
GUION: "Ya no se levanta de noche. Ya no se queda dormido en la silla."
ROL: EMOTION
LO QUE SE VE: Pantalla dividida verticalmente en 3 paneles superpuestos. ARRIBA: pareja durmiendo feliz con crucifijo en la pared. CENTRO: pareja desayunando con café, frutas, jugos. ABAJO: pareja caminando de la mano en parque dorado al atardecer.

kf_prompt:
"3D Pixar style scene, warm golden cinematic lighting, split into three stacked horizontal panels. TOP panel: the Hispanic couple (gray-haired husband in blue t-shirt, dark-haired wife in gray t-shirt) sleep peacefully together in bed under white covers with a small cross on the wall above. MIDDLE panel: the same couple sits happily at a bright breakfast table with fruit, coffee cups, pastries, and orange juice — family photos on the wall behind them. BOTTOM panel: the couple walks hand in hand down a golden sunlit park path surrounded by autumn trees and green grass, seen from behind at distance. Vertical 9:16."

anim_prompt:
"A gentle slow pan upward from the bottom walking panel to the middle breakfast panel to the top sleeping panel, showing life returning to normal. Each panel subtly animates: couple walks in bottom, husband laughs in middle, couple breathes peacefully in top. Camera: slow upward pan across all three panels. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" (2.94s real → FREEZE last frame ~2.0s en editor. Imperceptible en corte seco.)

═══════════════════════════════════════════════════════════
TOMA 08 · CTA EMOCIONAL — ESPOSA PRESENTA EL FRASCO · duration "5" · s51–56 (5.0s)
═══════════════════════════════════════════════════════════
GUION: "Ya no le cuento las idas al baño. Recuperé a mi esposo y dejé de contar."
ROL: STORY
LO QUE SE VE: Exterior porch/jardín, luz dorada de atardecer. Esposa de frente a cámara extendiendo el frasco gotero ámbar con ambas manos. Esposo en el fondo corriendo energético en el jardín. Ella tiene expresión decidida y esperanzadora.

kf_prompt:
"3D Pixar style character, warm golden sunset lighting, outdoor front porch setting. A Hispanic woman in her late 30s with dark curly hair in a loose bun, wearing a gray hoodie, stands on a porch facing the camera. She holds up an amber glass dropper bottle with both hands toward the viewer, eyes wide and earnest, slight hopeful smile. In the blurred background: her husband jogs energetically on the garden path. Green garden and warm sunset light behind her. Vertical 9:16."

anim_prompt:
"The woman extends the dropper bottle forward toward the camera with both hands in a presenting gesture, then with one hand points at the bottle label while her other hand gestures open-palmed toward the viewer. Camera: slow push-in toward the bottle held toward camera. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" (5.0s → encaja exacto, freeze frame de 0.1s si necesario)

═══════════════════════════════════════════════════════════
TOMA 09 · MECANISMO — INFOGRAFÍA PASTILLAS vs GOTAS · duration "10" · s56–64 (8.0s)
═══════════════════════════════════════════════════════════
GUION: "Si alguien que amas tiene diabetes y tú también cuentas, hazlo. No esperes seis años. Glucora berberina. La fórmula líquida que frena al hígado de producir azúcar sin control."
ROL: CONCEPT / SCIENCE
LO QUE SE VE: Pantalla infográfica: pirámide de pastillas con X roja a la izquierda, flecha dorada → frasco gotero Glucora con cara animada. En la parte inferior: hígado 3D animado con mecanismo de válvula dorada. Super-texto "6 años". El frasco tiene la etiqueta real de GLUCORA / Sugar Control.

kf_prompt:
"3D Pixar style infographic scene, warm amber medical lighting. LEFT half: a towering pile of colorful pharmaceutical pills and tablets stacked into a pyramid shape on a white surface, with a large red X overlaid. RIGHT half: an amber glass dropper bottle with a cartoon face (friendly wide eyes, slight smile, small arms) glowing with warm amber-gold light. A golden arrow points from the pill pyramid to the bottle. BOTTOM: a stylized 3D anatomical liver with a golden gear/valve mechanism on it. The scene communicates '6 years of pills vs. this drop solution'. Vertical 9:16."

anim_prompt:
"A golden liquid drop falls from the dropper tip in slow motion and lands on the liver below, which then glows with warm golden light as the gear on it begins to turn smoothly. The pill pyramid on the left slightly crumbles. Camera: slow push-in toward the dropper bottle and its falling drop. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s → recortar ~2.0s del final en editor)
⚠ PACKAGING: El frasco en esta toma muestra la etiqueta real GLUCORA. El editor mete el packaging
   real vía nano-banana/edit con imagen real de referencia. kf_ref_urls debe actualizarse con la
   URL del packaging real subido a fal storage.

═══════════════════════════════════════════════════════════
TOMA 10 · PRODUCTO HÉROE — GLUCORA CON INGREDIENTES · duration "10" · s64–72 (8.0s)
═══════════════════════════════════════════════════════════
GUION: "Lo que seis años de pastillas no pudieron. Sesenta días de gotas. Sí, más de diez ingredientes."
ROL: CONCEPT
LO QUE SE VE: Frasco GLUCORA personaje animado (cara feliz, brazos blancos levantados) en primer plano. Ingredientes orbitando: canela, bayas rojas, cúrcuma, hojas verdes. Glucómetros verdes 105 y 130 en esquina superior. Badge "60 días de gotas". Parque dorado y silueta pareja de fondo.

kf_prompt:
"3D Pixar style product hero scene, warm golden outdoor lighting, park pathway background with couple silhouette walking in golden hour. CENTER: a large amber glass dropper bottle character — the GLUCORA Sugar Control bottle (Berberine, Ceylon Cinnamon, Chromium, Liquid Drops, by Glucora Labs) — with an expressive cartoon face (friendly wide eyes, confident smile) and small white-gloved hands raised in a welcoming gesture. Around the bottle: floating ingredient icons — cinnamon sticks, red berries, turmeric root, green leaves. TOP RIGHT corner: two green glucose meters showing readings 105 and 130 mg/dL. '60 días de gotas' badge visible. Vertical 9:16."

anim_prompt:
"The Glucora bottle character raises its small white-gloved hands wider in a triumphant welcoming pose while the ingredient icons orbit slowly around it at a steady distance. The two glucose meters in the corner gently pulse with green light. Camera: slow push-in toward the bottle's face. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s → recortar ~2.0s del final en editor)
⚠ PACKAGING: Toma con frasco real GLUCORA. Subir imagen real a fal storage y pasar como
   kf_ref_urls antes de generar. Usar nano-banana/edit con referencia.

═══════════════════════════════════════════════════════════
TOMA 11 · CTA — GLUCORA EN PARQUE, DEVUÉLVESELAS · duration "10" · s72–80 (8.0s)
═══════════════════════════════════════════════════════════
GUION: "Dos gotas al día. La diabetes le roba noches. Devuélveselas. Consíguela abajo."
ROL: CONCEPT / CTA
LO QUE SE VE: Frasco GLUCORA personaje animado avanza hacia cámara sobre pavimento del parque. Ingredientes en el suelo a sus pies. Glucómetros 103 y 110 mg/dL (mejorando). Pareja caminando en el fondo hacia el sol. Espacio inferior para texto CTA.

kf_prompt:
"3D Pixar style product hero scene, radiant golden sunset outdoor lighting, park pathway receding into the background with a couple silhouette. CENTER FOREGROUND: a large amber glass dropper bottle character — the GLUCORA Sugar Control bottle (Berberine, Ceylon Cinnamon, Chromium, Liquid Drops, by Glucora Labs) — with a determined expressive cartoon face and small arms extended outward. Ingredients — cinnamon sticks, red cranberries, turmeric, green mint leaves — scattered on the ground around the bottle's base. TOP RIGHT: two green glucose meters showing 103 and 110 mg/dL. Warm gold and amber light radiates outward from behind the bottle. Vertical 9:16."

anim_prompt:
"The Glucora bottle character steps forward one determined step toward the camera while the scattered ingredients on the ground glow with golden sparks. The glucose meters pulse dropping slightly lower, showing improvement. Camera: slow push-in toward the bottle advancing toward the viewer. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (8.0s → recortar ~2.0s del final en editor)
⚠ PACKAGING: Misma toma de producto real. Misma imagen de referencia que toma 10.
   Espacio en la parte inferior para overlay: "CONSÍGUELA ABAJO" + flecha + link.

═══════════════════════════════════════════════════════════
NOTAS PARA EL EDITOR (cuando montes el video)
═══════════════════════════════════════════════════════════

FREEZE FRAMES (tomas generadas más largas que el tramo real):
- Toma 01 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 02 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 03 → clip 10s, tramo real 7.8s → RECORTAR ~2.2s del final.
- Toma 04 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 05 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 06 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 07 → clip 5s, tramo real 2.94s → FREEZE last frame ~2.0s. Imperceptible.
- Toma 08 → clip 5s, tramo real 5.0s → encaja exacto (freeze 0.1s si necesario).
- Toma 09 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 10 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.
- Toma 11 → clip 10s, tramo real 8.0s → RECORTAR ~2.0s del final.

PACKAGING REAL — TOMAS QUE LO NECESITAN:
- Toma 09 (s56–64): frasco GLUCORA Sugar Control / Glucora Labs. Subir imagen real a fal storage.
  Usar batch_keyframes_fal.mjs con kf_ref_urls:[<URL del frasco>] para generar con referencia.
- Toma 10 (s64–72): mismo frasco. Reusar la misma URL de referencia.
- Toma 11 (s72–80): mismo frasco. Reusar la misma URL de referencia.
PLAN B si la etiqueta sale distorsionada en nano-banana/edit: generar el frasco sin cara
(solo objeto) y componer la cara encima en editor.

OVERLAYS QUE VA EL EDITOR:
- Toma 09: badge "6 AÑOS" + ícono X pastillas → flecha → frasco.
- Toma 10: badge "60 DÍAS DE GOTAS" + glucómetros verdes 105/130.
- Toma 11: "CONSÍGUELA ABAJO" + flecha + link en zona inferior. Dejar espacio libre en keyframe.

ORDEN DE PRODUCCIÓN RECOMENDADO:
1. Subir imagen real del frasco GLUCORA a fal storage con upload_asset.mjs.
2. Generar keyframe ancla de los personajes (toma 01) → reusar esposo y esposa en tomas 02-06.
3. Generar keyframes de producto (tomas 09, 10, 11) con kf_ref_urls del frasco real.
4. Generar las tomas restantes (07, 08).
5. Aprobar los 11 keyframes antes de lanzar batch_kling3.mjs.
6. ffmpeg recorta cada clip a su timecode exacto y concatena. Voz va aparte en editor.
