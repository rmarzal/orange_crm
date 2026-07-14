# Refinamiento visual de la propuesta — Orange Business × Eiffage Energía

Fichero: `Orange_Business_x_Eiffage_-_Iniciativas_IA_v2.pptx` (18 → **19** diapositivas).

Se ha trabajado sobre la plantilla, colores (naranja de marca) y estructura originales.
El objetivo era el feedback recibido: **menos texto, letra más grande y más peso a la
ejecución de 3 iniciativas** (frente a la priorización de las 10 oportunidades).

## 1. Menos texto y letra más grande (recorte equilibrado)

| Slide | Antes | Ahora |
|------|-------|-------|
| **2. Contexto y necesidad** | Párrafos densos a 14pt | Idea clave + 3 frentes en bullets, cuerpo **16–18pt** |
| **3. Nuestro enfoque** | 4 descripciones largas a 14pt | 4 frases cortas a **16pt**, intro sintetizada |
| **4. Objetivo, alcance y método** | Lista de **8 pasos** a 12pt | **4 pasos** agrupados a 15pt; el último destaca *Foco y ejecución* |
| **5. Marco de priorización** | Bloques densos a 14pt | Frases con destacado en negrita a **15–16pt** |
| **7. Criterios de viabilidad** | 6 tarjetas a 10,5pt | Mismas 6 tarjetas, texto sintetizado a **12pt** |
| **17. Por qué Orange Business** | 4 columnas a 12pt | Columnas sintetizadas a **14pt** |

## 2. Más peso a la ejecución de las 3 iniciativas

- **Slide 8 (Plan de sesiones):** se han **resaltado en naranja** y enriquecido las dos
  filas de ejecución que pediste:
  - *6. Convergencia y cierre* → cierre de las 3 iniciativas, modelo de ejecución
    (autónomo / con apoyo / con partner), plan de acción y readout.
  - *4x sesiones flexibles* → deep-dive por iniciativa, sesión con referentes de negocio,
    readout a dirección y demo de contraste.
  Letra de la tabla subida de 10 a 11pt.
- **NUEVA slide 9 — «De la priorización a la ejecución»:** diapositiva dedicada, muy
  visual y con poco texto, que carga el peso en el *cómo llevar a cabo* las 3 iniciativas:
  - 3 tarjetas de **modelo de ejecución**: Autónomo · Con apoyo · Con partner.
  - Banda de **sesiones flexibles** orientadas a ejecutar.
  - Cierre: cada iniciativa sale con su caso de valor, modelo de ejecución y siguientes pasos.

## 3. Corrección de legibilidad detectada

En «Por qué Orange Business» el título *«Foco en el salto a operación»* estaba en
**blanco sobre fondo blanco** (invisible) y otro en gris de bajo contraste. Los 4 títulos
se han normalizado a **naranja de marca**.

## Notas

- Todo el texto se ha verificado con un medidor de ajuste (fuente métrica-compatible con
  Arial) para evitar desbordes: **0 desbordes** en las diapositivas editadas.
- No se pudo generar PDF/vista previa con LibreOffice en el entorno de trabajo (fallo del
  binario headless), por lo que la verificación fue programática + renders SVG propios.
- `build_v2.py` y `ppt_helpers.py` documentan exactamente los cambios aplicados (partiendo
  del `.pptx` original).
