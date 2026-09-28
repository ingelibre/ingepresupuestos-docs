# Archivos .prs y Excel (presupuesto + ACU)

IngePresupuestos abre presupuestos guardados como base **`.prs`** (Access) y también los que llegan como dos archivos **Excel**: el presupuesto y el análisis de costos unitarios (ACU).

## Desde Excel (presupuesto + ACU)

Muchos programas de presupuestos exportan dos archivos: el **presupuesto** y el **ACU**. IngePresupuestos los lee juntos.

1. En tu programa de origen, exporta a Excel el **presupuesto** y el **ACU** de la obra.
2. En IngePresupuestos: **Importar**, elige el origen del archivo y el formato **Excel**.
3. Selecciona el archivo de **presupuesto** y el de **ACU**.
4. Confirma. El proyecto se crea con sus partidas, su jerarquía, los ACU y los insumos.

!!! success "Qué se importa correctamente"
    - La **jerarquía** completa (componentes, títulos, subpartidas y partidas).
    - El **análisis de costos unitarios** de cada partida, sin insumos duplicados.
    - Los **insumos** consolidados, reutilizando el mismo recurso del catálogo (un solo «peón», un solo cemento, etc.).
    - El **monto total**, idéntico al del archivo original.

## Sobre los códigos de partida

Algunos programas numeran cada partida de varias formas (numérico, letra, número romano o un **código propio** de la entidad), e incluso saltan correlativos. Por eso sus códigos a veces se ven como `101.A`, `503.A3` o `500. A`.

Esos códigos son un **estilo de numeración**, no una jerarquía. Al importar, IngePresupuestos **renumera limpio** (01, 01.01, 01.01.01…) según la estructura real de títulos, para que el árbol del presupuesto quede bien anidado. El total y los análisis no cambian.

## Verificar después de importar

Te recomendamos revisar:

1. Que el **monto total** coincida con el del archivo original (debería ser idéntico salvo centavos por redondeo).
2. Que cada partida muestre su **ACU** con la mano de obra, materiales, equipo y, si corresponde, las **herramientas manuales (%MO)**.
3. Que la **jerarquía** (títulos y subpartidas) se vea correcta en el árbol.

!!! note "¿El monto cambia al pulsar «Recalcular»?"
    Si tras importar todo cuadra pero al **recalcular** el total varía, suele deberse a que en el ACU original faltaba algún insumo de porcentaje (como las herramientas manuales). Asegúrate de exportar el ACU **completo**. Con la versión actual de IngePresupuestos esto ya se importa correctamente.

## Desde una base `.prs`

Si tienes el archivo `.prs` (una base de datos Access):

1. **Importar**, elige el origen del archivo y el formato **Base nativa (.prs)**.
2. Selecciona el archivo.
3. Confirma.

!!! info "En Linux"
    Para leer bases Access, IngePresupuestos usa `mdbtools` (`sudo apt install mdbtools`). En Windows usa el controlador gratuito Access Database Engine.

---

¿Tienes una copia de seguridad `.bak`? [Ver la guía de copias de seguridad :octicons-arrow-right-24:](s10.md)
