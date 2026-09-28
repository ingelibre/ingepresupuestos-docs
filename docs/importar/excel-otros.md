# Importar desde Excel, IFC y `.db`

Además de los formatos nativos, IngePresupuestos importa precios de insumos desde Excel, cantidades desde modelos BIM y proyectos desde su propia base de datos.

## Excel (`.xlsx`)

!!! warning "No hay una importación genérica de presupuestos desde Excel"
    IngePresupuestos lee el Excel **de reporte** (presupuesto + ACU) que exportan los programas de presupuestos (ver [Archivos .prs y Excel](powercost.md)). Un presupuesto armado a mano en Excel, o una hoja con otro formato —por ejemplo un tarifario oficial—, **no se reconoce** como presupuesto: el programa responde «El archivo no contiene partidas reconocibles».

### Lo que sí puedes importar desde tu Excel: tus precios de insumos

Si tienes una lista de precios propia (materiales, mano de obra, equipos, o un tarifario oficial de tu país), cárgala en el **Catálogo de Insumos**:

1. **Catálogos → Catálogo de Insumos → Exportar ▾ → A Excel (.xlsx)**. Así obtienes una plantilla con las columnas correctas.
2. Copia tus datos en esa plantilla, respetando la **primera fila** como cabecera.
3. **Catálogos → Catálogo de Insumos → Importar ▾ → Desde Excel (.xlsx)**.

| Columna | ¿Obligatoria? | Contenido |
|---|---|---|
| **Descripción** | Sí | Nombre del insumo |
| **Tipo** | Sí | `MO` (mano de obra), `MAT` (material), `EQ` (equipo) o `SC` (subcontrato/servicio) |
| Código | No | Si ya existe, el insumo se **actualiza**; si falta, se genera uno |
| Unidad | No | `hh`, `m3`, `kg`, `und`… |
| Precio | No | Acepta `1234.56` y `1.234,56` |
| Índice INEI | No | Solo para la fórmula polinómica (Perú) |

!!! tip "La columna Tipo es la que más filas descarta"
    Una fila sin **Descripción** o con un **Tipo** distinto de `MO`, `MAT`, `EQ` o `SC` se salta. Al terminar, el programa dice cuántas filas creó, cuántas actualizó y cuántas descartó.

!!! note "Moneda"
    El catálogo de insumos usa la **moneda** elegida en **Configuración → País**. Cambiarla solo cambia el símbolo y los separadores: los importes no se convierten.

## BIM — modelos IFC (`.ifc`)

Puedes importar cantidades desde un modelo **IFC** (de Revit, ArchiCAD, Tekla, etc.) para generar partidas a partir de los elementos del modelo.

1. **Importar → IFC**.
2. Selecciona el archivo `.ifc`.
3. Revisa los elementos y cantidades detectados y confirma.

## Base de datos de IngePresupuestos (`.db`)

Para **mover un proyecto entre computadoras** o compartirlo con un colega que también use IngePresupuestos:

=== "Exportar"

    1. Abre el proyecto.
    2. **Exportar → Base de datos (`.db`)**.
    3. Guarda el archivo y compártelo.

=== "Importar"

    1. **Importar → IngePresupuestos (`.db`)**.
    2. Selecciona el archivo `.db`.
    3. Elige el proyecto a importar y confirma.

La exportación `.db` conserva **todo**: partidas, ACU, insumos, metrados, cronograma, fórmula polinómica y pie de presupuesto.

!!! tip "Atajo: abrir un `.db` directamente"
    Con un proyecto abierto, también puedes ir a **Archivo → Abrir → Desde archivo (`.db`)**: eliges el archivo, IngePresupuestos lo agrega al programa y lo abre en una pestaña. Si el `.db` contiene varios proyectos, te deja elegir cuál.
