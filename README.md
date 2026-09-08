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
  perdidas, win rate) y embudo de conversión por nº o por €.
- **Reports**: funnel por BDM (o todo el equipo), número e importe por
  etapa, top 5 de propuestas abiertas por AOV, alertas de propuestas sin
  avanzar y detalle desplegable con acceso a cada ficha. Incluye impresión/PDF.
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

El informe usa toda la cartera del BDM seleccionado, con un selector propio
independiente de los filtros del dashboard. El funnel muestra la distribución
actual, incluyendo ganadas, perdidas y sin clasificar; no calcula conversiones
históricas. El ranking prioriza las cinco propuestas abiertas de mayor AOV
positivo, incluidas las ofertas enviadas.

Las alertas incluyen propuestas abiertas con al menos 30 días sin cambiar de
etapa. El umbral puede cambiarse a 14, 60 o 90 días. Se utiliza la última
transición registrada, compatible con el histórico anterior; las nuevas
transiciones guardan también origen y destino de forma estructurada. Las notas
y cambios de importe no reinician el contador. Sin transiciones, se estima
la antigüedad desde la inclusión o el alta y se etiqueta como estimada. Las
fechas ausentes, inválidas, futuras o los históricos inconsistentes se muestran
como antigüedad sin determinar. Las alertas indican permanencia en etapa,
no ausencia de actividad comercial.

Puedes editar las propuestas abriendo su ficha desde el nombre del cliente.
**Descargar informe editable** genera una copia HTML autónoma: ábrela en el
navegador, pulsa sobre el contenido para editarlo y usa **Guardar copia editada**
para descargar tus cambios. Incluye todo el detalle por etapa. Esta edición es
una copia del informe: no modifica el CRM ni recalcula totales.
**Descargar CSV para Excel** exporta las propuestas del BDM seleccionado,
con importes numéricos, antigüedad, origen de la fecha y alertas. Ambas descargas
funcionan localmente, sin dependencias ni conexión. Se mantiene **Imprimir / PDF**.

El informe solo utiliza los datos reales que se carguen en la aplicación;
no incluye datos ficticios ni de demostración.

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
