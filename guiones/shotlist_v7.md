# Shotlist — Glucora VSL v7 "El miedo que me hizo buscar otra salida"
# Audio: voz narradora femenina (1ª persona, testimonio real) · duración: 71s · vertical 9:16
# Modelo de imagen: Nano Banana (fal-ai/nano-banana) vía fal
# Modelo de video: Kling 3.0 v3 Pro image-to-video vía fal (batch_kling3.mjs)
# Estética: 3D Pixar-style animation, warm cinematic lighting, expressive characters with large eyes
# Regla anti-lipsync: TODO personaje tiene UNA ACCIÓN FÍSICA específica mientras "habla".
#                    El ojo va a la acción, no a la boca.

═══════════════════════════════════════════════════════════
DATOS TÉCNICOS DEL LOTE
═══════════════════════════════════════════════════════════
- Total tomas: 10
- Distribución duración:
  · 3 tomas con duration "5"  (≤5.5s) → 3 × $0.56 = $1.68
  · 7 tomas con duration "10" (>5.5s) → 7 × $1.12 = $7.84
- Costo videos: $9.52
- Costo imágenes: 10 × $0.039 = $0.39
- COSTO TOTAL: ~$9.91 USD por VSL completo

NOTA: precio fal nano-banana ≈ $0.039/img. Kling 3.0 v3 Pro en fal = $0.112/s sin audio.

═══════════════════════════════════════════════════════════
NOTA SOBRE NANO BANANA (fal)
═══════════════════════════════════════════════════════════
Nano banana responde mejor a prompts CONCRETOS y FÍSICOS:
- "3D Pixar-style" va al INICIO de cada prompt.
- Describir CARA, EXPRESIÓN, OBJETO y ENTORNO específicamente.
- Evitar adjetivos abstractos: "epic, premium, cinematic" se interpretan mal.
- Acción física descrita con verbos claros.

═══════════════════════════════════════════════════════════
ANCLA DE ESTILO (repetir en todos los kf_prompt)
═══════════════════════════════════════════════════════════
"3D Pixar-style animation, warm cinematic lighting"

ACENTO DE COLOR:
- MUNDO PROBLEMA: azul-gris oscuro (dormitorio nocturno, luz roja 3am) → angustia
- MUNDO SOLUCIÓN: dorado ámbar cálido (luz amanecer, gotas doradas, hígado brillante) → esperanza
- MUNDO FAMILIA: dorado suave exterior, naturaleza verde + luz sunset → amor/transformación

═══════════════════════════════════════════════════════════
PERSONAJE ANCLA: LA MADRE
═══════════════════════════════════════════════════════════
Mujer latina, aprox. 38 años, pelo largo rizado oscuro con reflejos castaños,
ojos expresivos grandes (estilo Pixar), cara ovalada, complexión media.
Ropas según escena: camisón azul oscuro floral (bedroom/problema),
sweater de punto beige-multicolor (cocina/descubrimiento),
top blanco casual (baño/transformación).

PERSONAJE SECUNDARIO: LA HIJA
Niña 8 años, pelo oscuro lacio, ojos grandes expresivos, top beige claro.

PERSONAJE SECUNDARIO: EL HIJO
Niño 10 años, polo verde, pelo corto castaño oscuro.

═══════════════════════════════════════════════════════════
GUION COMPLETO (transcrito de subtítulos quemados)
═══════════════════════════════════════════════════════════
[0-8s]   "No me da miedo la diabetes. No me da miedo la metformina.
          Me da miedo no estar para..."
[8-16s]  "Mi hija me peinó antes de [salir]. Me miró y me dijo: mami,
          ¿por qué tomas tantas pastillas? No supe qué decirle."
[16-24s] "Hay noches que me imagino la graduación de mi hija.
          Las flores, los aplausos. Y que yo no estoy ahí, que no llegué."
[24-32s] "Abro los ojos: tres a.m. Me despertó la necesidad del baño."
[32-40s] "Un día me cansé de tener miedo. Me cansé de tener [esto] para mi azúcar,
          para mis hijos."
[40-48s] "Vi un video sobre el hígado. La diabetes lo hace producir azúcar sin control.
          La metformina no [lo frena]. Por eso descubrí Glucora."
[48-56s] "Berberina líquida que cierra la [resistencia] y frena el descontrol de lo que
          cuatro años de pastillas [no hicieron]. Dos gotas al [día]."
[56-64s] "Hoy mi glucómetro marca ciento tres. Ya no despierto a las tres.
          Ya no tengo [miedo a la] diabetes. Y mi hija pregunta por las [pastillas]..."
[64-71s] "Glucora, diez ingredientes [que tu cuerpo] necesita. Ahí no [hay pastillas].
          Consíguela haciendo clic."

═══════════════════════════════════════════════════════════
TOMA 01 · HOOK — MIEDO REAL · duration "10" · 0s–8s (8.0s)
ROL: STORY
═══════════════════════════════════════════════════════════
GUION: "No me da miedo la diabetes. No me da miedo la metformina. Me da miedo no estar para..."
LO QUE SE VE: Mujer Latina en camisón en borde de cama. Dormitorio oscuro con lámpara de noche, glucómetro y pastillas en la mesita. Expresión de preocupación profunda, manos abiertas en gesto de resignación.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. A Latina woman in her late 30s with long dark curly hair sits on the edge of a rumpled bed in a dim bedroom. She wears a dark floral nightgown. Her expression is deeply worried — wide expressive eyes, furrowed brow, hands open in a gesture of resignation. On the wooden nightstand beside her: a glucometer, two orange prescription bottles, and a glass of water. Family photos hang on the wall in the background. A single lamp casts warm amber light against the dark room. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman sits on the edge of the bed, pressing her hands together on her lap and looking down with a heavy sigh. Her shoulders drop slowly in resignation. Camera: slow push-in toward her face. The lamp on the nightstand stays in the lower-right corner, grounding the scene. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (clip de 10s → usar completo, duración real 8s: recortar ~2s al final)

─────────────────────────────────────────────────────────
TOMA 02 · HISTORIA — HIJA EN EL BAÑO · duration "10" · 8s–16s (8.0s)
ROL: STORY
═══════════════════════════════════════════════════════════
GUION: "Mi hija me peinó antes de salir. Me miró y me dijo: mami, ¿por qué tomas tantas pastillas? No supe qué decirle."
LO QUE SE VE: Mamá sentada en el tocador del baño con espejo iluminado en arco. La hija de pie detrás peinándola con cepillo de madera. Ambas se ven reflejadas en el espejo. Bote METFORMIN naranja en el mármol. Luz dorada del espejo.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Same Latina woman with long dark curly hair, now sitting at a bright bathroom vanity with a large illuminated arch mirror. She wears a casual white T-shirt. Her young daughter (about 8 years old, dark straight hair, beige top) stands behind her reflected in the mirror, brushing the mother's hair with a wooden brush. Both mother and daughter are visible in the mirror reflection. On the marble counter: an orange prescription bottle labeled METFORMIN, a glass of water, a toothbrush holder. Warm golden backlight from the mirror frame. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The daughter gently brushes the mother's hair with slow strokes while smiling in the mirror. The mother watches her daughter's reflection with a mix of love and quiet sadness, eyes glistening. Camera: slow pan across the mirror surface, lingering on both faces. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (recortar ~2s al final en editor)

─────────────────────────────────────────────────────────
TOMA 03 · AGITAR — MIEDO A NO LLEGAR · duration "10" · 16s–24s (8.0s)
ROL: EMOTION
═══════════════════════════════════════════════════════════
GUION: "Hay noches que me imagino la graduación de mi hija. Las flores, los aplausos. Y que yo no estoy ahí, que no llegué."
LO QUE SE VE: Salón de graduación universitaria. Hija en toga azul navy en el escenario con diploma y flores. Padre y niño en butacas aplaudiendo. Confetti de colores cayendo. La mamá imagina la escena desde afuera, silla vacía en primer plano.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Wide shot of a university graduation ceremony hall. A young Latina woman in a navy blue graduation gown and cap stands on a wooden stage, holding a rolled diploma and a bouquet of lilies and roses. She has long dark curly hair and a bittersweet expression. In the audience: a handsome man in a tan suit clapping, and a young boy in a blue suit clapping excitedly beside him. An empty purple seat is visible in the foreground. Colorful confetti falls from above. Banners read 'CLASS OF 2024'. Warm golden celebratory light. Plano general. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The graduating daughter steps forward on the stage and extends one arm toward the audience with a hopeful smile. The father and son in the audience clap and lean forward with joy. Confetti drifts down slowly. The empty seat in the foreground stays visible. Camera: slow push-in from wide to medium, focusing on the empty seat and then the daughter on stage. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (recortar ~2s al final en editor)

─────────────────────────────────────────────────────────
TOMA 04 · AGITAR — 3AM INSOMNIO · duration "5" · 24s–31.5s (7.5s → PARTIR en 2)
ROL: EMOTION
═══════════════════════════════════════════════════════════
NOTA: Toma original dura 7.5s. Se parte en dos sub-tomas 04A y 04B.

### TOMA 04A · 3AM CAMA · duration "5" · 24s–28s (4s)
GUION: "Abro los ojos: tres a.m."
LO QUE SE VE: Mujer en cama oscura, ojos abiertos aterrados. Esposo dormido. Reloj rojo marcando 3:00 AM. Luz roja dramática en su cara.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Dark moody bedroom at night. The same Latina woman with long dark curly hair lies in bed, wide awake, eyes open with anxiety. Her husband sleeps beside her. On the nightstand: a red glowing digital clock reading 3:00 AM. The room is lit only by the red glow of the clock casting dramatic red light across her face. She clutches the blanket tightly with both hands. Plano medio cerrado. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman lies still, staring at the ceiling with frightened eyes. Her fingers tighten on the edge of the blanket. The red 3:00 AM clock glows steadily on the nightstand. Camera: very slow push-in toward her wide-open eyes. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" → freeze frame final ~1s en editor para cubrir los 4s exactos.

### TOMA 04B · 3AM LEVANTARSE · duration "5" · 28s–31.5s (3.5s)
GUION: "Me despertó la necesidad del baño."
LO QUE SE VE: Misma mujer ahora incorporándose en la cama, agarrando la cobija, expresión de urgencia y angustia, primer plano cerrado.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Same Latina woman with long dark curly hair sits upright in the dark bed, clutching the floral blanket against her chest with wide frightened eyes. Her husband is asleep behind her. The red digital clock casts red light on her face. She leans forward with an expression of urgent need and exhaustion. Close-up plano medio cerrado. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman sits up from the pillow with a startled expression, grips the blanket to her chest, and swings her legs toward the edge of the bed. Her face shows exhaustion and urgency. Camera: slow push-in to her face from slightly below. The red clock stays visible on the nightstand. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" → recortar a 3.5s en editor (usar primeros 3.5s del clip)

─────────────────────────────────────────────────────────
TOMA 05 · DECISIÓN — ME CANSÉ · duration "10" · 31.5s–39.5s (8.0s)
ROL: STORY
═══════════════════════════════════════════════════════════
GUION: "Un día me cansé de tener miedo. Me cansé de tener esto para mi azúcar, para mis hijos."
LO QUE SE VE: Mujer de pie en el dormitorio (pre-amanecer, luz azul suave por ventana). Camisón floral oscuro. Postura firme con puño cerrado, expresión de resolución furiosa pero esperanzada. Mesita con glucómetro y pastillas al fondo.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Same Latina woman with long dark curly hair stands barefoot on the bedroom floor rug. She wears a dark floral nightgown. Pre-dawn blue light comes through the curtained window. Her posture is firm and resolved — one fist raised at chest level, other hand extended outward, jaw set with fierce determination, eyebrows furrowed but hopeful. On the nightstand behind her: glucometer, orange pill bottles. Family photos on the wall. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman plants both feet firmly on the floor rug and raises one fist in front of her chest with a determined expression, as if making a personal vow. Her other hand gestures outward emphatically. Camera: slow push-in from waist up. The window behind her shows the first light of dawn beginning. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (recortar ~2s al final en editor)

─────────────────────────────────────────────────────────
TOMA 06 · MECANISMO — VIDEO DEL HÍGADO · duration "10" · 39.5s–47.5s (8.0s)
ROL: SCIENCE
═══════════════════════════════════════════════════════════
GUION: "Vi un video sobre el hígado. La diabetes lo hace producir azúcar sin control. La metformina no lo frena. Por eso descubrí Glucora."
LO QUE SE VE: Mamá en cocina soleada con sweater estampado, sosteniendo smartphone con diagrama del hígado en la pantalla (silueta azul del cuerpo humano con hígado naranja). Sus dos hijos comen cereal en la mesa del fondo. Luz solar matutina intensa.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. The same Latina woman with long dark curly hair stands in a bright sunny kitchen wearing a patterned knit sweater and jeans. She holds a smartphone in one hand with both eyes wide open in revelation. The phone screen shows a blue anatomical body diagram with the liver highlighted in glowing orange-red. In the kitchen background: a girl and a boy sit at a round wooden table eating cereal. Warm morning sunlight streams through a large window. Oak cabinets, coffee maker on counter. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman holds the phone up and taps the screen with her finger, eyes wide with a revelation. She glances back at her children at the table, then back to the phone with growing excitement. Camera: slow push-in toward the phone screen showing the liver diagram. The kitchen stays warm and grounded throughout. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (recortar ~2s al final en editor)

─────────────────────────────────────────────────────────
TOMA 07 · PRODUCTO — BERBERINA LÍQUIDA · duration "10" · 47.5s–55.5s (8.0s)
ROL: CONCEPT
═══════════════════════════════════════════════════════════
GUION: "Berberina líquida que cierra la resistencia y frena el descontrol de lo que cuatro años de pastillas no hicieron. Dos gotas al día."
LO QUE SE VE: Mujer en dormitorio con luz dorada. Sostiene frasco dropper marrón. Hígado brillante dorado flota encima. Montaña de pastillas en plato plateado a la izquierda. Segundo frasco dropper en pedestal dorado a la derecha.

⚠ ESTA TOMA MUESTRA EL PACKAGING REAL DE GLUCORA
kf_ref_urls: null (el editor debe insertar la imagen real del frasco Glucora vía nano-banana image-edit)
El frasco tiene: etiqueta con cara de caricatura, texto "BERBERINE CEYLON CINNAMON SUGAR CONTROL by GLUCORA LABS", dropper negro.

KEYFRAME PROMPT (nano-banana — REQUIERE IMAGEN REAL DEL FRASCO GLUCORA):
"3D Pixar-style animation, warm cinematic lighting. Same Latina woman in dark floral nightgown stands in a warmly lit bedroom. She holds a small dark brown glass dropper bottle with a cartoon face (from reference image — keep exact label) with both hands, presenting it proudly at chest height. Above the bottle, a glowing golden anatomical liver shape hovers with a warm pulse. On the left foreground of the wooden dresser: a large silver tray overflowing with colorful pills and capsules. On the right: a second identical brown dropper bottle on a small golden pedestal stand. Her expression is joyful and amazed. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman carefully holds the dropper bottle up at eye level and squeezes the dropper bulb, releasing a single golden drop that falls and causes the glowing liver icon above to pulse with warm light. She smiles with relief and awe. Camera: slow push-in toward the bottle and glowing liver. The pill tray on the left stays visible in foreground. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "10" (recortar ~2s al final en editor)

─────────────────────────────────────────────────────────
TOMA 08 · TRANSFORMACIÓN — DOS GOTAS · duration "5" · 55.5s–59s (3.5s)
ROL: STORY
═══════════════════════════════════════════════════════════
GUION: "Dos gotas al día."
LO QUE SE VE: Primer plano de la mujer tomando las gotas del dropper sobre la lengua. Expresión de satisfacción y alivio. Luz dorada ambiente.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Same Latina woman in dark floral nightgown stands in bedroom near the wooden dresser. She tilts a small dark brown glass dropper bottle over her open mouth, releasing a single golden drop onto her tongue. Her eyes are half-closed in satisfaction. The silver pill tray filled with colorful tablets sits on the dresser in the foreground. Warm amber golden-hour light fills the room. Plano medio cerrado. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The woman tilts the dropper bottle and releases one golden drop onto her tongue. She closes her eyes with a serene satisfied smile. The golden drop catches the warm amber light. Camera: slow push-in toward her face and the dropper. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" → freeze frame final ~1.5s en editor para cubrir los 3.5s exactos.

─────────────────────────────────────────────────────────
TOMA 09 · TRANSFORMACIÓN — GLUCÓMETRO 103 · duration "10" · 59s–63.5s (4.5s)
ROL: STORY
═══════════════════════════════════════════════════════════
GUION: "Hoy mi glucómetro marca ciento tres. Ya no despierto a las tres. Ya no tengo miedo a la diabetes. Y mi hija pregunta por las pastillas..."
LO QUE SE VE: Regreso al tocador del baño. Mamá y la hija en el espejo, ahora sonrientes. Glucómetro digital en el mármol marcando 103 en verde. Escena cálida, dorada, llena de paz.

KEYFRAME PROMPT (nano-banana):
"3D Pixar-style animation, warm cinematic lighting. Same Latina woman sits at the bathroom vanity mirror, now smiling warmly. Her daughter stands behind her reflected in the large illuminated arch mirror, touching her mother's cheek gently. Both are happy and glowing. On the marble counter: a digital glucometer showing the number 103 in bright green. The mirror frame glows with warm golden light. Both mother and daughter visible in reflection. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The daughter places one hand gently on the mother's shoulder and they both smile at each other in the mirror reflection. The glucometer on the counter clearly shows 103 in green. Camera: slow pan across the mirror capturing both smiling faces, ending on the glucometer. The counter stays fully visible. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" → el clip dura 4.5s: usar "5" y recortar los últimos 0.5s.

─────────────────────────────────────────────────────────
TOMA 10 · CTA — FAMILIA + PRODUCTO · duration "5" · 63.5s–71s (7.5s → PARTIR en 2)
ROL: CONCEPT + STORY
═══════════════════════════════════════════════════════════
NOTA: Toma original dura 7.5s. Se parte en dos sub-tomas 10A y 10B.

⚠ AMBAS SUB-TOMAS MUESTRAN EL PACKAGING REAL DE GLUCORA
kf_ref_urls: null (editor inserta frasco real vía nano-banana image-edit)

### TOMA 10A · PRODUCTO + FAMILIA · duration "5" · 63.5s–67s (3.5s)
GUION: "Glucora, diez ingredientes que tu cuerpo necesita."
LO QUE SE VE: Escena exterior golden hour. Mamá abraza a sus dos hijos. Frasco Glucora en primer plano izquierdo con carita animada. Ingredientes flotantes alrededor (canela, berberina, jengibre, hojas). Glucómetro 103 en el pasto.

KEYFRAME PROMPT (nano-banana — REQUIERE IMAGEN REAL DEL FRASCO GLUCORA):
"3D Pixar-style animation, warm cinematic lighting. Outdoor golden-hour park scene. A warm Latina mother with brown straight hair in a cream-colored knit sweater sits on the grass and hugs both her children tightly. Her daughter in a pink dress embraces her from the left. Her son in a green shirt leans in from the right. All three smile with pure joy. In the left foreground: the Glucora dropper bottle (from reference image — keep exact label and cartoon face). Floating around the family: cinnamon sticks, red berries, ginger root, green leaves, turmeric root. A glucometer in the grass shows 103. Warm burst of golden sunlight from behind. Plano general. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The mother squeezes both children in a warm hug. The daughter buries her face in her mother's shoulder. The son laughs with eyes closed. Golden light radiates outward. The dropper bottle in the left foreground catches the warm sunlight. Camera: slow push-in toward the family trio. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" → freeze frame final ~1.5s en editor para cubrir los 3.5s exactos.

### TOMA 10B · CTA FINAL · duration "5" · 67s–71s (4.0s)
GUION: "Consíguela haciendo clic."
LO QUE SE VE: Mamá y familia en exterior golden hora. Mamá extiende la mano hacia cámara con sonrisa invitadora. Frasco Glucora al costado. Flecha verde grande apuntando hacia arriba (gráfica del editor). Luz explosiva dorada.

KEYFRAME PROMPT (nano-banana — REQUIERE IMAGEN REAL DEL FRASCO GLUCORA):
"3D Pixar-style animation, warm cinematic lighting. Same outdoor golden-hour park scene. The Latina mother sits on the grass with children hugging her. She extends one open hand directly toward the camera with a warm inviting smile and bright hopeful eyes. Golden burst of warm light radiates from behind. The Glucora dropper bottle (from reference image) is visible in the left foreground. The overall scene glows with warm sunset gold. Plano medio. Vertical 9:16."

ANIM PROMPT (Kling 3.0):
"The mother extends her open hand toward the camera with a warm welcoming smile. Her children squeeze her from both sides. Golden light intensifies from behind, creating a warm halo effect. Camera: slow push-in toward the extended hand. negative_prompt: floating in void, spinning, orbiting, weightless, screensaver, empty background, static posing at camera, deformed hands, deformed face, extra fingers, text, watermark, logo, blurry, talking mouth closeup"

DURACIÓN: "5" → recortar a 4s en editor (últimos 1s del clip se descartan).

═══════════════════════════════════════════════════════════
ORDEN DE PRODUCCIÓN RECOMENDADO
═══════════════════════════════════════════════════════════
1. Generar primero los 3 KEYFRAMES ANCLA:
   - Toma 01 (Madre en cama, angustia) → base para tomas 04A, 04B, 05.
   - Toma 02 (Baño espejo, hija) → base para toma 09.
   - Toma 10A (Exterior familia) → base para toma 10B.
   Costo de los 3 anclas: ~$0.12.

2. APROBAR las 3 anclas antes de generar las otras 7.
3. Para tomas que reusan personaje ancla, usar nano-banana/edit con refs.
4. Tomas 07, 10A, 10B: insertar imagen real del frasco Glucora como ref.
5. Cuando los 10 keyframes estén aprobados, armar batch_input.json con URLs.
6. Lanzar batch_kling3.mjs. Tiempo total estimado: ~10-15 min.

═══════════════════════════════════════════════════════════
NOTAS PARA EL EDITOR
═══════════════════════════════════════════════════════════
FREEZE FRAME / RECORTES:
- Toma 04A: duration "5" generados → usar completos; freeze frame final ~1s (duración real 4s).
- Toma 04B: duration "5" generados → recortar a 3.5s (primeros 3.5s del clip).
- Toma 08: duration "5" generados → freeze frame final ~1.5s (duración real 3.5s).
- Toma 09: duration "5" generados → recortar últimos 0.5s.
- Toma 10A: duration "5" generados → freeze frame final ~1.5s (duración real 3.5s).
- Toma 10B: duration "5" generados → recortar últimos 1s.
- Tomas 01, 02, 03, 05, 06, 07: duration "10" generados → recortar ~2s al final.

PACKAGING REAL (tomas que lo requieren):
- Toma 07: frasco Glucora dropper marrón (cara caricatura, etiqueta BERBERINE CEYLON CINNAMON).
  → Subir foto real del frasco a fal storage → usar como ref en nano-banana/edit.
- Toma 10A: mismo frasco Glucora.
- Toma 10B: mismo frasco Glucora.

GRÁFICAS A AGREGAR EN EDITOR (NO se generan con IA):
- Toma 10B: flecha verde grande apuntando hacia arriba + texto "CONSÍGUELA HACIENDO CLIC" (igual que el original).

AUDIO:
- Voz narradora va aparte, completamente separada del video mudo.
- Música sugerida: tono emocional-dramático en tomas 01-05, sube en toma 06 (descubrimiento), explota en toma 10B (CTA).

DISCLAIMER SALUD:
- Este video menciona control de glucosa. Agregar disclaimer al final:
  "Estos resultados no son típicos. Consulte a su médico antes de cambiar su tratamiento."

═══════════════════════════════════════════════════════════
RESUMEN JSON PARA batch_kling3.mjs
═══════════════════════════════════════════════════════════
Archivo: keyframes_input_v7.json (n: 01–10, con los prompts de cada toma)
Clips esperados: 10 archivos en clips_v3/
Nomenclatura: 01.mp4 … 10.mp4
