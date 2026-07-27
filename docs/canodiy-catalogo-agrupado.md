# Canodiy.es — Catálogo agrupado por combinaciones afines

**Fuente:** https://canodiy.es/ (PrestaShop, tienda "Cano Do It Yourself")
**Fecha de extracción:** 27 de julio de 2026
**Cobertura:** 6.049 / 6.049 productos publicados (100 % del catálogo visible en `/42-productos`)
**Datos en bruto:** [`data/canodiy-catalogo.csv`](../data/canodiy-catalogo.csv) — familia, categoría, nombre, referencia, precio y URL de cada producto.

---

## 1. Resumen ejecutivo

Canodiy es un distribuidor de **material para marroquinería, tapicería y costura técnica** que vende
tanto a profesional como a DIY. El catálogo está fuertemente escorado: **2 de cada 3 referencias son hilo**,
y la variedad no viene del tipo de producto sino de la **combinación grosor × formato × color**.

| Familia afín | Refs. | % catálogo | Precio mediano | Rango |
|---|---:|---:|---:|---|
| Hilos | 3.866 | 63,9 % | 5,48 € | 1,74 – 230,00 € |
| Cremalleras y cursores | 525 | 8,7 % | 0,68 € | 0,08 – 15,46 € |
| Pasamanería y cintas | 387 | 6,4 % | 0,45 € | 0,17 – 6,03 € |
| Herramientas | 345 | 5,7 % | 4,17 € | 0,36 – 547,79 € |
| Tintes y químicos | 256 | 4,2 % | 5,22 € | 2,63 – 671,21 € |
| Agujas y leznas | 142 | 2,3 % | 4,94 € | 0,27 – 21,38 € |
| Embalaje y almacén | 117 | 1,9 % | 9,94 € | 0,44 – 85,86 € |
| Cordones | 104 | 1,7 % | 0,42 € | 0,29 – 416,24 € |
| Outlet / liquidación | 102 | 1,7 % | 1,29 € | 0,22 – 299,98 € |
| Fornituras | 87 | 1,4 % | 3,74 € | 0,17 – 121,97 € |
| Soportes y refuerzos | 45 | 0,7 % | 2,86 € | 0,72 – 7,65 € |
| Clavos, grapas y tachuelas | 31 | 0,5 % | 16,34 € | 3,15 – 20,00 € |
| Labores y costura | 13 | 0,2 % | 5,40 € | 0,19 – 19,11 € |
| EPI / protección | 13 | 0,2 % | 0,80 € | 0,02 – 77,83 € |
| Elásticos | 11 | 0,2 % | 0,41 € | 0,15 – 6,85 € |
| Adhesivos | 5 | 0,1 % | 15,25 € | 5,06 – 18,14 € |

Distribución de precios global: mín. 0,02 € · P25 2,29 € · **mediana 2,86 €** · P75 6,63 € · P95 19,27 € · máx. 671,21 €.
Es un catálogo de **ticket bajo y alta rotación**, con una cola larga de maquinaria y químicos profesionales.

---

## 2. Los tres ejes que generan el catálogo

Casi toda la profundidad del surtido se explica por tres dimensiones que se combinan entre sí.
Entender esto es lo que permite agrupar "tipos de producto" en vez de listar 6.049 SKUs.

| Eje | Se aplica a | Valores observados |
|---|---|---|
| **Grosor / calibre** | Hilos, cremalleras, cordones, agujas | Hilo: 10 · 11 · 15 · 20 · 30 · 40 · 60 · 70 · 80 · 120 — Cremallera: maya 3 · 5 · 8 |
| **Formato / longitud** | Hilos, cintas, cordones | Bobina (2.335 refs) vs. Cono (1.518 refs); 200–5.000 m |
| **Color** | Hilos, cremalleras, cintas, cordones, tintes | **370 códigos de color distintos** (`C/0000` … `C/3722`) |

> Un mismo "producto" (p. ej. *Hilo Gütermann Mara 70*) genera ~450 referencias sólo cruzando
> 2 formatos × ~200 colores. Es un catálogo de **matriz**, no de surtido.

---

## 3. Agrupaciones por afinidad

### 3.1 · HILOS — 3.866 refs (63,9 %) — el núcleo del negocio

Tres marcas/gamas cubren el 92 % de la familia. Todas comparten la misma lógica de
**grosor → formato → color**, así que son intercambiables en catálogo y sustitutivas en venta.

**a) Gütermann MARA** — poliéster para costura general y tapicería (1.041 refs)

| Grosor | Refs. | Formatos |
|---|---:|---|
| Mara 11 (extra grueso) | 122 | Bobina 110 m · Cono 1.130 m |
| Mara 30 | 463 | Bobina 300 m · Cono 1.200 m |
| Mara 70 | 449 | Bobina 700 m · Cono 2.800 m |
| Mara 120 (fino) | 405 | Bobina 1.000 m · Cono 5.000 m |

**b) Gütermann TERA** — poliéster de alta tenacidad, marroquinería y calzado (1.215 refs)

| Grosor | Refs. | Formatos |
|---|---:|---|
| Tera 10 | 117 | Cono 1.000 m |
| Tera 20 | 263 | Bobina 200 m · Bobina 600 m |
| Tera 30 | 218 | Bobina 300 m · Bobina 900 m |
| Tera 40 | 276 | Bobina 400 m · Bobina 1.200 m |
| Tera 60 | 187 | Bobina 600 m · Bobina 1.800 m |
| Tera 80 | 141 | Bobina 800 m · Bobina 2.400 m |

**c) SERAFIL (Amann)** — competidor directo de Tera, mismos usos (877 refs)
Serafil 10 (92) · 15 (18) · 20 (175) · 30 (183) · 40 (168) · 60 (128) · 80 (113)

**d) Hilos especiales** — donde no manda el color sino la aplicación (313 refs)

| Tipo | Refs. | Afinidad de uso |
|---|---:|---|
| Hilos de bordar (Isacord / Isamet 40) | 148 | Bordado a máquina; se vende en packs de 5/10/20/30/50 bobinas |
| Encerados | 41 | Costura a mano de cuero — afín a leznas, agujas curvas y cordón encerado |
| Poliamida | 38 | Alta resistencia / náutica |
| Overlock–remallar | 30 | Va siempre con agujas de remalladora |
| Packs Mara 120 / vaqueros | 14 | Producto de entrada, orientado a DIY |
| Hilo elástico | 11 | Frunce y confección |
| Técnicos | 7 | Kevlar / especiales |
| Yute | 1 | Decoración |

**Paleta de color (compartida por toda la familia):** marrones (899 apariciones) y azules (561)
dominan, seguidos de verdes (478), grises (341) y rojos (282). Es la paleta típica de
**tapicería + calzado + marroquinería**, no de moda.

---

### 3.2 · CREMALLERAS Y CURSORES — 525 refs (8,7 %)

Familia perfectamente matricial: **maya (calibre) × material × tipo de cierre**, más los cursores sueltos.

| | Plástico continua | Plástico cerrada | Plástico abierta | Metálica continua | Metálica cerrada | Metálica abierta |
|---|---:|---:|---:|---:|---:|---:|
| **Maya 3** | 45 | 1 | 1 | 1 | 3 | — |
| **Maya 5** | 108 | 149 | 4 | — | 17 | 4 |
| **Maya 8** | — | — | — | — | 17 | — |

- **Cursores sueltos:** 86 (maya 5) + 17 (maya 3) + 19 sin clasificar → **122 refs**.
  Son el complemento obligado de la cremallera continua: quien compra metros compra cursores.
- **Packs y kits:** 97 refs (Pack Cremalleras Maya 5 · Maya 3 · Pack para Bolsos).
  El *Pack para Bolsos* (20 refs, 6,65 € fijo) es el producto DIY mejor construido del catálogo:
  combina cremallera + cursor + color coordinado en un solo SKU.

**Lectura comercial:** maya 5 plástico es el 60 % de la familia; maya 8 sólo existe en metálica cerrada
(chaquetas y prendas gruesas).

---

### 3.3 · PASAMANERÍA, CINTAS Y CORDONES — 491 refs (8,1 %)

Dos subfamilias que el sitio separa pero que **compiten por el mismo carrito** (acabado y remate):

| Cintas (387) | Refs. | | Cordones (104) | Refs. |
|---|---:|---|---|---:|
| Cinta de raso | 101 | | Semiencerado 2 mm | 87 |
| Velcro (cintas de cierre) | 94 | | Cordón de algodón / macramé | 6 |
| Cinta faya | 58 | | Semiencerado 3 mm | 4 |
| Cola de ratón | 48 | | Cordón náutico | 4 |
| Cinta mochila | 36 | | Varios encerados | 3 |
| Cinta bies | 25 | | | |
| Otras cintas | 24 | | | |

Precio mediano 0,42–0,45 €: producto de **venta por metro/impulso**, ideal para bundles.
El cordón semiencerado 2 mm (87 refs de color) es afín directo al **hilo encerado** y a la
**marroquinería a mano**.

---

### 3.4 · TINTES, CERAS Y QUÍMICOS — 256 refs (4,2 %)

Es la familia que **el sitio ya agrupa por caso de uso**, no por producto — el modelo a replicar
en el resto del catálogo:

| Enfoque | Subcategorías | Refs. |
|---|---|---:|
| **Por soporte** | Cuero (48) · Cuero sintético (21) · Cuero regenerado (7) · Tejido (7) · Plástico (1) | 84 |
| **Por función** | Ceras de reparación (54) · Tintes cantos, con/sin brillo (43) · Tintes cuero (21) · Limpiadores (7) · Pintura (7) · Protectores (2) | 134 |
| **Por destino** | Tapicería hogar · Tapicería automóvil: cuero auto (8), tejido auto (1) · Prendas de piel (1) | 10 |
| **Empaquetado** | Kits de cuidado (3) · Pack tintes | 3 |
| **Sello verde** | CANO ECO-GREEN — tinte base agua | 13 |

Es también la familia de **mayor ticket** (mediana 5,22 €, máximo 671,21 €).

---

### 3.5 · HERRAMIENTAS Y AGUJAS — 487 refs (8,1 %)

Se compran juntas y por eso conviene tratarlas como un bloque "taller":

**Herramientas (345)**
Para lijar (63) · Pinceles (51) · Útiles (45) · Bolígrafos y marcadores (45) · Cuchillas y cutters (29) ·
Cepillos (25) · Remachadoras y maquinaria (16) · Tijeras (16) · Precisión (15) ·
Alicates y cortafríos (13) · Martillos (10) · Grapadoras (3) · Cardas de alambre (2)

**Agujas y leznas (142)** — el catálogo **ya las enlaza al hilo** ("PARA MARA 30", "PARA TERA 40"),
que es la afinidad más valiosa de toda la tienda:
Coser a máquina (61) · Coser a mano (28) · Leznas (28) · Máquina doméstica (15) · Máquina remallar (8)

El rango de precio es el más amplio del catálogo (0,36 € una aguja → 547,79 € maquinaria),
así que conviven **consumible** y **bien de equipo** bajo la misma etiqueta.

---

### 3.6 · FERRETERÍA DE MARROQUINERÍA — 163 refs (2,7 %)

Metal decorativo y de sujeción; se combinan entre sí en el mismo proyecto (bolso, cinturón, tapizado):

| Fornituras (87) | Refs. | | Clavos/grapas (31) | Refs. | | Soportes y refuerzos (45) | Refs. |
|---|---:|---|---|---:|---|---|---:|
| Hebillas | 38 | | Clavos | 16 | | Cintas adhesivas | 36 |
| Adornos | 20 | | Grapas | 7 | | Tiras de cuero por metros | 5 |
| Anillas | 10 | | Tachuelas | 6 | | Rellenos/refuerzos para asas | 3 |
| Broches y cierres | 4 | | | | | | |
| Cadenas | 4 | | | | | | |
| Adorno con clavo | 4 | | | | | | |

---

### 3.7 · CONSUMIBLE DE TALLER — 135 refs (2,2 %)

No es producto de creación sino de **operación del taller**. Alto ticket relativo (mediana 9,94 €):

Pistola y navetes (24) · Bolsas (16) · Precintos y film (15) · Guantes (13) · Gomas (12) ·
Carretes (10) · Recipientes (8) · Canastas y cubetas (8) · Pernitos (7) ·
Mascarillas y EPI (13) · Adhesivos, cianocrilato (5)

---

### 3.8 · OUTLET Y LIQUIDACIÓN — 102 refs (1,7 %)

Réplica reducida del catálogo principal con precio agresivo (mediana 1,29 €):
Fornituras y abalorios (39) · Tintes para cuero (34) · Hilos (24) · Pasamanerías (2) ·
Lotes de saldo (2) · Cremallera continua

---

## 4. Combinaciones afines transversales (agrupación por proyecto)

El árbol de la web está organizado **por tipo de material**. Cruzando las familias por caso de uso
aparecen seis conjuntos naturales de venta combinada, que es donde está el margen incremental:

### A · Kit marroquinería a mano (cuero)
`Hilo encerado` + `Cordón semiencerado 2–3 mm` + `Agujas curvas / tres filos` + `Leznas` +
`Tintes de cantos (con y sin brillo)` + `Ceras de reparación` + `Hebillas, anillas, broches` + `Cianocrilato`
→ **~350 refs**. Es el perfil de cliente artesano; hoy tiene que recorrer 6 menús distintos.

### B · Kit tapicería y restauración de sofá
`Mara 11 / 30` + `Agujas curvas` + `Clavos, grapas y tachuelas` + `Martillos` + `Grapadoras` +
`Cintas adhesivas` + `Tintes y ceras para cuero y tejido` + `Cuero regenerado`
→ **~700 refs**. La web ya lo intuye con la landing *"Restaura tu sofá"*.

### C · Kit confección de bolsos y mochilas
`Pack para Bolsos` + `Cremallera continua maya 5 + cursores` + `Cinta mochila` + `Cinta bies` +
`Rellenos y refuerzos para asas` + `Tiras de cuero por metros` + `Mosquetones/anillas` + `Mara 70`
→ **~400 refs**. La combinación mejor resuelta ya en producto (el *Pack para Bolsos* de 6,65 €).

### D · Kit costura técnica / industrial
`Tera` o `Serafil` (mismo grosor) + `Agujas de máquina 134/135` + `Hilo overlock` +
`Agujas de remalladora` + `Carretes` + `Tijeras profesionales`
→ **~2.400 refs**. Aquí la clave es el **selector grosor de hilo ↔ referencia de aguja**,
que el sitio ya modela en las categorías `PARA MARA xx` / `PARA TERA xx`.

### E · Kit bordado a máquina
`Isacord 40 / Isamet 40` + `Packs de 5/10/20/30/50 bobinas` + `Entretela de bordar` + `Agujas de bordar`
→ **~160 refs**. Es la única familia con packs por gama de color (Essential, Multicolor, Pastel, Metalizados, Fluor).

### F · Kit acabado y decoración
`Cinta de raso` + `Cinta faya` + `Cola de ratón` + `Velcro` + `Elásticos` + `Adornos` + `Cadenas`
→ **~500 refs**. Ticket unitario muy bajo (0,42 € mediana): sólo funciona en bundle o pedido mínimo.

---

## 5. Observaciones sobre la estructura del catálogo

1. **Concentración extrema.** El 64 % de las referencias son hilo y el 33 % son sólo tres gamas
   (Mara, Tera, Serafil). Cualquier análisis de surtido debe tratar el hilo como un eje aparte.
2. **370 códigos de color** conviven sin un diccionario común: el mismo `C/0000` (negro) se repite
   en Mara, Tera y Serafil. Es la clave natural para agrupar y para recomendar equivalencias entre gamas.
3. **Bobina vs. cono es una decisión de volumen, no de producto** (2.335 vs. 1.518 refs).
   Duplica el catálogo sin añadir variedad real — candidato claro a variante de producto.
4. **Las categorías "PARA MARA xx" / "PARA TERA xx" ya codifican la afinidad hilo↔aguja.**
   Es el mejor activo de datos del sitio y no está explotado fuera del menú.
5. **Categorías raíz con producto suelto.** 60 referencias cuelgan directamente de categorías padre
   (HILOS, HERRAMIENTAS, FORNITURAS, EMBALAJE…) sin subcategoría — ruido de mantenimiento.
6. **199 productos ya son packs o kits** (97 en cremalleras, 42 en hilos, 35 en tintes).
   La tienda ya está migrando hacia la venta combinada; las agrupaciones de la sección 4 son la
   extensión natural de ese movimiento.

---

## 6. Método

- Descubrimiento del árbol de categorías desde el megamenú de portada (`iqitmegamenu`): 197 nodos,
  18 familias de primer nivel.
- Recorrido paginado de `https://canodiy.es/42-productos` (253 páginas × 24 productos) parseando cada
  `article.product-miniature`: nombre, referencia, precio (`content` del microdato), categoría por
  defecto y URL canónica.
- Asignación de familia por el *slug* de categoría contenido en la URL del producto; los 13 productos
  colgados de la raíz se reclasificaron por nombre.
- Verificación de cobertura: el contador del propio PrestaShop declara 6.049 productos; se extrajeron
  6.049 (100 %).
- Precios en EUR con IVA tal y como los publica la tienda en la fecha de extracción.
