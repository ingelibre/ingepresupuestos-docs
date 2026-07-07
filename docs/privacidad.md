# Política de privacidad

**Última actualización:** 15 de junio de 2026

Esta política explica qué información trata **IngePresupuestos** (la "aplicación") y cómo se maneja. Resumen en una línea: **tus presupuestos y datos se guardan en tu propia computadora; la aplicación no tiene publicidad, no te rastrea y no vende tus datos.**

## Responsable

IngePresupuestos es desarrollado por **Ing. Marco Sumari** (Perú).

- Web: [https://ingepresupuestos.com](https://ingepresupuestos.com)
- Contacto: a través del formulario de [ingepresupuestos.com](https://ingepresupuestos.com) o WhatsApp **+51 998 839 090**.

## Qué datos trata la aplicación

### Datos que tú creas (se quedan en tu equipo)
Tus proyectos, partidas, análisis de costos, precios, metrados, cronogramas, reportes y configuración se guardan **localmente** en tu computadora, en la carpeta de datos del usuario:

- **Windows:** `%APPDATA%\ingepresupuestos\` (o el contenedor de la app si la instalaste desde la Microsoft Store).
- **Linux:** `~/.local/share/ingepresupuestos/`
- **macOS:** `~/Library/Application Support/ingepresupuestos/`

**Esta información no se envía a nuestros servidores.** No tenemos acceso a tus presupuestos.

### Identificador del equipo
La aplicación calcula un **identificador de máquina**: un valor derivado (con una función hash de un solo sentido) de las direcciones MAC de tus adaptadores de red. Se calcula y se guarda **localmente**; no se transmite ni revela tu identidad o ubicación.

## Conexiones a internet

La aplicación funciona **sin conexión** para lo esencial. Solo se conecta a internet en estos casos, y solo lo necesario:

| Función | A dónde se conecta | Qué se envía |
|---------|--------------------|--------------|
| **Asistente de IA (Tuxia)** — *opcional* | Al proveedor que tú elijas y configures con **tu propia clave**: Anthropic, Groq, OpenAI, Google (Gemini), OpenRouter, o un modelo local (Ollama). | El texto de tu consulta y el contexto de la partida/proyecto que envías a ese proveedor. Solo cuando usas la función. |
| **Buscar actualizaciones** | `downloads.ingepresupuestos.com` | Una petición para leer la última versión publicada. *(Desactivado en la versión de la Microsoft Store: ahí las actualizaciones las gestiona la Store.)* |
| **Índices de inflación (INEI)** | `inei.gob.pe` (datos públicos) | Una petición para descargar índices oficiales. |
| **Mapa de ubicación** — *opcional* | Servidores de mapas (OpenStreetMap / Esri) | Las coordenadas del área que visualizas, para descargar los mosaicos del mapa. |

Si usas el **asistente de IA**, tus consultas se procesan según las políticas de privacidad del proveedor que **tú** configures. Revisa la política de ese proveedor. Si prefieres no enviar nada a terceros, puedes usar un modelo **local (Ollama)** o simplemente no usar las funciones de IA.

## Lo que NO hacemos

- **No** mostramos publicidad.
- **No** usamos analítica, telemetría ni rastreadores.
- **No** vendemos ni compartimos tus datos con terceros para marketing.
- **No** recopilamos tus proyectos, contactos, ubicación ni hábitos de uso.

## Si nos contactas

Si nos escribes por el formulario de la web o por WhatsApp, recibimos los datos que tú nos proporciones (nombre, correo, mensaje) únicamente para responderte. No se usan para otra cosa.

## Distribución por tiendas

Si descargaste la aplicación desde la **Microsoft Store**, la propia tienda puede recopilar datos de instalación y diagnóstico según la [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/privacystatement). Eso es independiente de la aplicación.

## Seguridad

Como tus datos viven en tu equipo, su seguridad depende principalmente de tu propio dispositivo. La aplicación crea **respaldos automáticos** locales de tu base de datos para ayudarte a recuperar tu información.

## Menores de edad

IngePresupuestos es una herramienta profesional de ingeniería y no está dirigida a menores de edad.

## Tus derechos sobre tus datos

Como toda tu información se almacena localmente, tú tienes control total: puedes **exportarla** (a `.db`, Excel, PDF, etc.) o **eliminarla** borrando la base de datos de la carpeta de datos del usuario. No conservamos copias en nuestros servidores.

## Cambios a esta política

Podemos actualizar esta política. Publicaremos la versión vigente en esta página con su fecha de "Última actualización".

## Contacto

¿Dudas sobre privacidad? Escríbenos desde [ingepresupuestos.com](https://ingepresupuestos.com) o por WhatsApp **+51 998 839 090**.
