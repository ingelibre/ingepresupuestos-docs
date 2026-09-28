# Preguntas frecuentes

## ¿Funciona sin internet?

Sí, completamente offline. Tus datos viven en tu PC en un archivo SQLite estándar. Lo único que usa internet es el asistente Tuxia (y con **Ollama** puedes usar IA local sin conexión).

## ¿Necesito tener Office o MS Project instalado?

No. IngePresupuestos genera los **PDF, Excel y Word por sí solo**, sin Microsoft Office. El cronograma se exporta a un XML estándar que abre en programas gratuitos como **ProjectLibre**, **OpenProj** o **GanttProject**. Solo la exportación a **ODS / ODT** se apoya en LibreOffice, si lo tienes.

## ¿Puedo abrir mi base de datos con otro programa?

Sí. El archivo `presupuestos.db` es **SQLite puro** — ábrelo con DB Browser, DBeaver, Python o cualquier herramienta. No es formato propietario.

## ¿Puedo importar copias de seguridad `.bak`?

Sí, con **IngeConverter** (incluido gratis) conviertes copias `.bak`, `.bkf` y `.S2K`. También importas presupuestos exportados a Excel. Ver [Copias de seguridad .bak](importar/s10.md).

## Al importar, ¿por qué cambian los códigos de las partidas?

Porque muchos códigos de origen son un **estilo de numeración** (numérico, letra, código propio…), no una jerarquía. IngePresupuestos los renumera limpio (01, 01.01…) para que el árbol quede bien anidado. El total y los análisis no cambian. Ver [Archivos .prs y Excel](importar/powercost.md).

## ¿Cómo se instala en Windows?

Descarga el `.exe`, doble clic, sigue el asistente. Si sale «Windows protegió tu PC», haz clic en **Más información → Ejecutar de todas formas**.

## ¿Cómo se instala en Linux?

Descarga el `.AppImage`, dale permisos de ejecución (`chmod +x`) y haz doble clic. No requiere instalación.

## ¿Los reportes son gratis?

Sí, todos. Los **13 reportes**, en **todos** los formatos —PDF, Excel, Word, ODS, ODT y MS Project— y también los reportes de **Control de Obra**. IngePresupuestos es software libre bajo GPL-3.0: no hay funciones bloqueadas, período de prueba ni claves. Ver [Licencia](licencias.md).

## ¿Necesito una clave de API para la IA?

Para usar Tuxia con proveedores en la nube (Anthropic, OpenAI, Gemini, etc.) sí, usas tu propia clave. Pero puedes usar **Ollama** con un modelo local **gratis y offline**, sin ninguna clave.

## ¿Cómo recibo soporte?

Por **WhatsApp** ([+51 998 839 090](https://wa.me/51998839090)) y correo ([ing.sumari@gmail.com](mailto:ing.sumari@gmail.com)), o desde el formulario de contacto dentro de la app.
