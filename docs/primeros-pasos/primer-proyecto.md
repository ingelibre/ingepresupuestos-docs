# Tu primer proyecto

Desde el **[panel principal](panel-principal.md)** puedes crear un proyecto nuevo, abrir uno existente o importar desde otro programa. Aquí vamos a crear uno desde cero.

## Crear un proyecto desde cero

1. Haz clic en **Nuevo proyecto**.
2. Completa los datos generales:

    | Campo | Para qué sirve |
    |-------|----------------|
    | **Nombre** | El nombre de la obra. |
    | **Cliente / Entidad** | A quién pertenece el proyecto. |
    | **Ubicación** | Distrito, provincia y departamento (con autocompletado por UBIGEO). |
    | **Costo al** | La fecha de referencia de los precios. |
    | **Plazo** | Duración de la obra en días. |
    | **Modalidad** | Contrata o Administración directa. |
    | **Moneda** | Soles por defecto. |

3. *(Opcional)* Pulsa el botón de **ubicación en el mapa** para fijar el punto exacto de la obra. Esto captura las coordenadas en **UTM WGS84** y la altitud, que luego mejoran la memoria descriptiva y las especificaciones generadas con IA.

4. Pulsa **Crear**. El proyecto se abre listo para empezar a cargar partidas.

!!! tip "¿Ya tienes el presupuesto en otro programa?"
    No empieces de cero. Usa **[Importar](../importar/index.md)** para traerlo desde archivos `.prs`, `.sqlite`, `.bak`, Excel o una base `.db`.

## La vista del proyecto

Dentro de un proyecto verás, en la parte superior, las pestañas de trabajo:

- **Partidas** — la estructura del presupuesto (componentes, títulos y partidas).
- **ACU** — el análisis de costos unitarios de la partida seleccionada.
- **Insumos** — todos los recursos del proyecto, consolidados.
- **Metrados** — la planilla de metrados (incluido acero por diámetro).
- **Especificaciones** — la descripción técnica de cada partida.
- **Resumen** — la distribución del costo y los totales en vivo.
- **Memoria** — la memoria descriptiva del proyecto.

![Análisis de costos unitarios](../img/acu.jpeg)

## Agregar una partida

1. En la pestaña **Partidas**, usa los botones de la barra de herramientas para agregar un **título** o una **partida**.
2. Escribe la descripción, la unidad y el metrado.
3. Selecciona la partida y, en el panel **ACU**, agrega los insumos (mano de obra, materiales, equipo). El **precio unitario se calcula solo** a partir del análisis.

!!! note "Numeración automática"
    No te preocupes por los códigos: IngePresupuestos numera las partidas automáticamente (01, 01.01, 01.01.01…) según cómo las organices. Puedes reordenarlas arrastrándolas y la numeración se ajusta sola.

---

**Siguiente paso:** [Importar desde otros programas :octicons-arrow-right-24:](../importar/index.md){ .md-button .md-button--primary }
