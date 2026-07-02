# Control de obra

Cuando la obra empieza, IngePresupuestos pasa de *elaborar* el presupuesto a **acompañarte durante la ejecución**. El módulo de **Control de Obra** vive detrás del botón **«Control de Obra»** de la barra superior (junto a Cronogramas) y reúne, en cinco pestañas, el trabajo del día a día del residente.

![Valorización de avance de obra](../img/control-obra-valorizacion.jpeg)

<div class="grid cards" markdown>

-   :material-clipboard-list: **[Requerimientos](requerimientos.md)**

    Los pedidos de la obra por categoría, con Términos de Referencia redactados por IA.

-   :material-warehouse: **[Almacén (kárdex)](almacen.md)**

    Materiales: pedido, ingresado, consumido, stock y por llegar.

-   :material-notebook-edit: **[Cuaderno de obra](cuaderno.md)**

    Los asientos diarios: metrado ejecutado, mano de obra e insumos.

-   :material-progress-check: **[Valorizaciones](valorizaciones.md)**

    El avance por partida: Base, Anterior, Actual, Acumulado y Saldo.

-   :material-chart-bell-curve-cumulative: **[Curva S real](curva-s.md)**

    Programado vs. reprogramado vs. real.

</div>

## Cómo se conecta con tu presupuesto

El Control de Obra **solo lee** tu presupuesto y su análisis de costos; **nunca los modifica**. El presupuesto aprobado queda como **base contractual** y todo el avance se compara contra él.

El flujo natural es:

1. Registras el avance del día en el **[Cuaderno de obra](cuaderno.md)**.
2. Ese avance se **acumula solo** hacia las **[Valorizaciones](valorizaciones.md)**.
3. Los pedidos salen de los **[Requerimientos](requerimientos.md)** y su llegada/consumo se controla en el **[Almacén](almacen.md)**.
4. La **[Curva S real](curva-s.md)** te muestra si vas adelantado o atrasado.

!!! tip "Un reporte por pestaña"
    Cada pestaña genera su propio reporte (PDF, Excel, Word u ODT según corresponda) con el botón **📄 Reporte**. No pasan por el Centro de Reportes: se generan directo desde la vista.

!!! note "Se activa con la obra en marcha"
    El Control de Obra tiene sentido cuando el presupuesto ya está **congelado** (estado *Ejecutado*), porque ese presupuesto es la base contractual del avance. Puedes abrirlo antes, pero verás un aviso recordándotelo.
