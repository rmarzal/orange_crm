# Orange CRM · Pipeline Comercial

Prototipo funcional para el seguimiento del pipeline comercial: sustituye el Excel
por un formulario de entrada controlado, un embudo de conversión y un tablero
Kanban, con filtros y visualización.

## Uso

Abre `index.html` en el navegador (Chrome, Edge o Firefox actualizados). Es una
página **autocontenida** (sin dependencias externas): los datos y toda la lógica
viajan dentro del propio HTML. Los cambios se guardan en el navegador
(`localStorage`).

También se puede publicar con **GitHub Pages** (Settings → Pages → Deploy from
branch → `main` / root) y acceder desde la URL que genere.

## Funcionalidades

- **Formulario de alta** con desplegables controlados (evita el desorden de valores libres).
- **Embudo de conversión** por nº de oportunidades o por valor (€).
- **Tablero Kanban** con arrastrar y soltar entre etapas (cambia el estado y lo registra en el histórico).
- **Filtros** por territorio, KAM, BDM, sector, tipología, estado, **semestre (H1/H2 automático)** y **rango de fechas de apertura**.
- **Ficha de edición** con histórico de cambios por oportunidad.
- **Importar Excel** (`.xlsx`) para actualizar los datos — reemplaza los registros anteriores.
- **Exportar CSV**.

## Reglas de negocio incluidas

- **Normalización de caracteres**: acentos, mayúsculas y espacios no diferencian valores (`Rubén` = `Ruben` = `RUBEN` → forma única).
- **Semestre automático** derivado de la fecha de apertura (ene–jun → H1, jul–dic → H2).
- **Precio por defecto**: toda oportunidad en *Perdida / KO* sin importe recibe **40.000 €** automáticamente.
- **Motivo de KO** obligatorio al mover una oportunidad a la columna de perdidas.

## Estado

Prototipo para validación con el equipo comercial. El siguiente paso es la
aplicación a medida con backend y base de datos compartida (los datos aquí viven
solo en el navegador de cada usuario).
