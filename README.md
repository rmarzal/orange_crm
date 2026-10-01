# Orange CRM · Pipeline Comercial

Aplicación de seguimiento del pipeline comercial que sustituye el Excel del
equipo: dashboard con KPIs, embudo de conversión, tablero Kanban, control de
duplicados y limpieza de datos.

Es un **único archivo HTML autocontenido** (sin servidor, sin instalación, sin
dependencias externas): la lógica y el diseño viajan dentro del propio
fichero. **Este repositorio no contiene datos comerciales** — se distribuye
sin oportunidades cargadas (`RAW = []`) para poder mantenerlo en un repo
público; los datos reales se cargan aparte, en local, y nunca se suben aquí.

## Cómo se usa

1. Abre el HTML en **Google Chrome o Microsoft Edge** (no Firefox/Safari:
   usa la *File System Access API*).
2. Carga tus oportunidades con **«Actualizar desde Excel»** (pestaña
   Registros), o parte de una copia ya poblada.
3. (Opcional, trabajo en equipo) Pulsa **«Conectar carpeta compartida»** y
   elige una carpeta de SharePoint sincronizada con OneDrive. La app crea
   una subcarpeta `DB_CRM/` con `pipeline.json` y todo el equipo trabaja
   sobre los mismos datos, con bloqueo cooperativo (un editor a la vez) y
   detección de conflictos.

Sin conectar carpeta, cada cambio se guarda solo en el navegador de esa
persona (`localStorage`). No se publica con GitHub Pages ni ninguna URL
pública: es un fichero que se reparte y se abre en local.

## Funcionalidades

- **Embudo & Dashboard**: KPIs (abiertas, valor de pipeline, ganadas,
  perdidas, win rate) y embudo de conversión por nº o por €. La barra de
  filtros incluye, entre otros, un **filtro por Partner** (además de
  Territorio, BDM, KAM, Sector, Tipología y Estado).
- **Reports**: informe sencillo por BDM, número e importe por etapa y las
  cinco propuestas de mayor importe. La redacción analiza todas las métricas
  visibles del funnel y el texto y las propuestas se pueden
  editar o quitar del informe. Incluye descarga DOCX, guardado como PDF y
  **«Rellenar plantilla»** (genera un PowerPoint de seguimiento del BDM
  seleccionado a partir de la plantilla incrustada).
- **Tablero Kanban**: arrastrar y soltar entre etapas (queda en el
  histórico) y botón para duplicar una oportunidad.
- **Revisión**: clientes duplicados, oportunidades sin clasificar, casos
  marcados para revisar y papelera de eliminadas (recuperable).
- **Ficha de oportunidad**: edición completa de todos los campos, con
  histórico de cambios.
- **Registros**: tabla ordenable por columna, con buscador y exportación a
  CSV.
- **Ayuda**: guía de uso integrada en la propia app.

## Reglas de negocio

- Normalización de caracteres: acentos, mayúsculas y espacios no
  diferencian valores (`Rubén` = `Ruben` = `RUBEN`).
- Canonicalización de sector, tipología, KAM y cliente (variantes
  equivalentes se unifican).
- Semestre automático derivado de la fecha de apertura.
- Precio por defecto de 40.000 € para oportunidades *Perdida / KO* sin
  importe; motivo de KO obligatorio.
- Sub-estados como *Revisar caso* o *Stand by* se guardan como etiqueta
  aparte, no alteran el estado principal.

## Reports

El informe usa un único filtro de BDM. Muestra una distribución sencilla por
etapa con número e importe y las cinco propuestas de mayor importe. También redacta un análisis
de todas las métricas visibles (pipeline, cierres, win rate, reparto por etapa,
concentración y calidad del dato) con el contexto del BDM seleccionado; ese texto se puede editar directamente
en pantalla y se conserva mientras trabajas con ese BDM.

Las nuevas transiciones guardan origen y destino de forma estructurada. El
detalle de cada propuesta permite abrir su ficha para editarla.

Puedes editar las propuestas abriendo su ficha desde el nombre del cliente.
**Descargar Word** genera un documento DOCX editable con el
informe visible y sus cinco propuestas. **Descargar PDF** abre el diálogo de
impresión del navegador para guardarlo como PDF, conservando el estilo visual.
Ambas opciones funcionan localmente, sin dependencias ni conexión.

El informe solo utiliza los datos reales que se carguen en la aplicación;
no incluye datos ficticios ni de demostración.

## Rellenar plantilla (PowerPoint)

En **Reports**, el botón **«Rellenar plantilla»** genera un `.pptx` de
seguimiento para el **BDM seleccionado** en el desplegable, a partir de la
plantilla corporativa incrustada en la propia app (no requiere subir ni
seleccionar ningún archivo). Todo ocurre en local, sin librerías: solo se
reescribe el contenido de la diapositiva y se conserva intacto el resto del
diseño (imágenes, estilos, gráfico).

Qué rellena, con los datos del BDM:

- **Título**: «Seguimiento <BDM>».
- **Oportunidades ganadas**: estado `Ganada` (cliente e importe) y el
  **Total ganado**.
- **Ofertas presentadas**: estado `Oferta enviada` (cliente e importe) y el
  **Total presentado**.
- **Oportunidades en elaboración**: estado `En proceso` (cliente e importe) y
  el **Total en elaboración**. *(«Sin empezar» no se incluye.)*
- **Previsión de cierre**: **ganado + 80 % de lo presentado** (los dos
  sumandos del recuadro inferior).
- **% conseguido** (rombo/indicador) y el **gráfico de rosco**
  (Conseguido / Pendiente): calculados sobre un **objetivo de 0,6 M €**.
  El **YTD** muestra lo ganado en millones.

Los importes se toman del campo AOV de cada oportunidad. Cada columna lista
las de mayor importe; si hay más de las que caben, se añade una fila
«(+N más)» y los totales siguen reflejando **todas**.

## Vista de partner (Orange Business)

Permite enseñar el CRM a un partner **sin darle acceso total**: solo ve
**sus** oportunidades y **en solo lectura**.

- En **Registros**, **«Generar CRM de partner (OB)»** crea el **mismo
  ejecutable del CRM** (`index.html`) en una **carpeta nueva** que elijas,
  con los datos **únicamente del partner Orange Business** (campo *Partner*
  = `OB`, `Orange Business`, `OB - Orange Business`, …; el reconocimiento es
  insensible a mayúsculas, acentos y puntuación). Ese ejecutable es la misma
  app pero **de solo lectura**: no permite editar, crear, importar ni
  conectar carpetas, y no escribe nada en el navegador. El botón indica
  además cuántas oportunidades y con qué valor exacto de *Partner* ha
  encontrado (útil para confirmar la grafía real).
- **Se actualiza solo**: cuando el equipo tiene conectada la carpeta
  compartida, cada guardado regenera automáticamente ese ejecutable en una
  **carpeta nueva e independiente** `CRM_OB/index.html`, hermana de
  `DB_CRM` dentro de la raíz compartida. Basta con **compartir esa carpeta
  `CRM_OB`** (por ejemplo en SharePoint) con el partner: verá siempre la
  versión al día, aislada del resto de datos del equipo.

## Seguridad y robustez

- Todo el texto proveniente de datos se escapa antes de mostrarse
  (protección frente a inyección de HTML/script).
- Los datos se validan al cargar; un archivo dañado no rompe la
  aplicación y no se sobrescribe el archivo compartido.
- Copia de seguridad automática (`pipeline.backup.json`) en cada guardado
  a la carpeta compartida.

## Estado

Prototipo en uso por el equipo comercial. El siguiente paso, cuando haga
falta edición simultánea real y control de accesos, es una aplicación a
medida con backend (NestJS + PostgreSQL) — proyecto independiente.
