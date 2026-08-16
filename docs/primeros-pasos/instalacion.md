# Instalación

IngePresupuestos funciona en **Windows** y **Linux** con la misma aplicación y los mismos archivos de proyecto. No necesita internet para trabajar ni instalar Office o MS Project.

Descarga siempre la última versión desde **[ingepresupuestos.com](https://ingepresupuestos.com/#descargar)**.

## Windows

=== "Instalador .exe"

    1. Descarga el instalador **`.exe`**.
    2. Haz doble clic y sigue el asistente.
    3. Si aparece la pantalla azul **«Windows protegió tu PC»**, haz clic en **Más información → Ejecutar de todas formas**.

        !!! note "¿Por qué sale ese aviso?"
            Es la advertencia normal de SmartScreen para programas que todavía no llevan firma digital. IngePresupuestos es seguro; el aviso desaparecerá cuando el programa esté firmado.

    4. Al terminar, busca **IngePresupuestos** en el menú Inicio y ábrelo.

=== "Microsoft Store"

    1. Abre la ficha de **[IngePresupuestos en la Microsoft Store](https://apps.microsoft.com/detail/9PN8FKLP4RH5)**.
    2. Pulsa **Obtener**.

    Instalado así no aparece el aviso de SmartScreen, y las actualizaciones
    las gestiona la propia Store.

## Linux

=== "AppImage (recomendado)"

    1. Descarga el archivo **`.AppImage`**.
    2. Dale permisos de ejecución:

        ```bash
        chmod +x IngePresupuestos-*.AppImage
        ```

    3. Haz doble clic (o ejecútalo desde la terminal). No requiere instalación.

=== "Flatpak"

    Instala con un comando (o desde el enlace de un clic de la web):

    ```bash
    flatpak install --from https://downloads.ingepresupuestos.com/flatpak/ingepresupuestos.flatpakref
    ```

    Es la edición completa —incluye la exportación a ODT y ODS usando el
    LibreOffice de tu sistema— y se actualiza sola con el resto de tus
    aplicaciones Flatpak.

## Actualizaciones

Cuando haya una versión nueva, el programa te avisa automáticamente al abrirlo, con un resumen de las novedades y un botón para descargarla. También puedes revisarlo manualmente en **Configuración → Acerca de → Buscar actualizaciones**.

Si lo instalaste desde la **Microsoft Store** o como **Flatpak**, no verás ese aviso: en esos dos canales las actualizaciones llegan solas.

## Tus datos

Tu información vive en tu PC, en un archivo **SQLite estándar** (`presupuestos.db`). El programa hace **copias de seguridad automáticas** cada día. Puedes abrir ese archivo con cualquier herramienta SQLite si lo necesitas — no es un formato propietario.

---

**Siguiente paso:** [Tu primer proyecto :octicons-arrow-right-24:](primer-proyecto.md){ .md-button .md-button--primary }
