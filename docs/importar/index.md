# Importar tus presupuestos

Una de las mayores ventajas de IngePresupuestos es que **lee directamente los archivos que ya tienes** — no tienes que volver a digitar el presupuesto ni pasar todo por Excel a mano.

## Formatos soportados

| Formato | Notas |
|---------|-------|
| `.prs` (Access) | Base nativa: presupuesto, ACU, insumos y metrados. |
| `.sqlite` | Proyecto, biblioteca de costos e índices INEI. |
| `.bak` / `.bkf` / `.S2K` | Copias de seguridad de SQL Server, a través de IngeConverter (incluido gratis). |
| `.xlsx` | Presupuesto + ACU exportados a Excel desde cualquier programa. |
| `.ifc` | Modelos BIM de Revit, ArchiCAD o Tekla. |
| `.db` | Bases de IngePresupuestos, para mover proyectos entre PCs. |

## Cómo importar

1. En el panel principal, haz clic en **Importar**.
2. Elige el **origen** y el **formato** del archivo.
3. Selecciona el archivo (o los archivos: algunos formatos usan uno para el presupuesto y otro para el ACU).
4. Revisa el resumen y confirma. El proyecto aparece en tu lista, listo para editar.

!!! tip "El pie de presupuesto"
    Al importar, los rubros del pie (gastos generales, utilidad, supervisión, etc.) se cargan **desactivados**. Actívalos según los necesite tu proyecto desde la pestaña **Pie de presupuesto**.

## Guías por formato

<div class="grid cards" markdown>

-   :material-file-excel: **Archivos .prs y Excel**

    ---

    Importa la base `.prs` o el presupuesto y el ACU exportados a Excel.

    [:octicons-arrow-right-24: Ver guía](powercost.md)

-   :material-database-arrow-down: **Copias de seguridad .bak**

    ---

    Convierte tus copias `.bak`, `.bkf` o `.S2K` con IngeConverter.

    [:octicons-arrow-right-24: Ver guía](s10.md)

-   :material-database: **Bases .sqlite**

    ---

    Abre bases `.sqlite` de otros programas.

    [:octicons-arrow-right-24: Ver guía](delphin.md)

</div>
