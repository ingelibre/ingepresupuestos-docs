# Bases .sqlite

IngePresupuestos lee directamente bases **`.sqlite`** de otros programas de presupuestos, trayendo el proyecto, la biblioteca de costos y los índices INEI.

## Pasos

1. En IngePresupuestos: **Importar** y elige el origen de la base `.sqlite`.
2. Selecciona el archivo **`.sqlite`**.
3. Si la base contiene varios presupuestos, elige el que quieres importar.
4. Confirma. El proyecto se crea con sus partidas, ACU e insumos.

!!! info "Si tu programa guarda otro formato"
    Algunos programas guardan además archivos en formatos internos que no se pueden leer. Usa siempre la base **`.sqlite`**, o exporta a **Excel** e impórtalo como Excel.

## Qué se importa

- Las **partidas** con su jerarquía, unidad y metrado.
- El **análisis de costos unitarios** de cada partida.
- Los **insumos**, reutilizando el mismo recurso del catálogo cuando coinciden (aunque cambie el código).
- Los **índices unificados (INEI)** asociados a los insumos, útiles para la fórmula polinómica.

!!! tip "El pie de presupuesto"
    Igual que con los demás importadores, los rubros del pie (gastos generales, utilidad, etc.) entran **desactivados**. Actívalos según tu proyecto.
