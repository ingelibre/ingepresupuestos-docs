# Fórmula polinómica

La **fórmula polinómica** permite reajustar el monto de la obra ante la variación de precios, según el D.S. 011-79-VC. IngePresupuestos la **deriva automáticamente** de tu presupuesto.

![Fórmula polinómica con sus monomios](img/formula.jpeg)

!!! warning "Solo en obras por contrata"
    La fórmula polinómica reajusta lo que se le valoriza a un contratista. En proyectos con modalidad **Administración directa** no corresponde: el programa lo avisa y no la calcula, ni aplica reajuste a las valorizaciones.

## Cómo se genera

A partir del análisis de costos, IngePresupuestos agrupa los insumos por **índice unificado (INEI)** y calcula la incidencia de cada uno sobre el **subtotal del presupuesto** — costo directo más gastos generales y utilidad, que es la base que fija la norma.

- Cada índice que llega al **5%** se convierte en un monomio propio.
- Los que no llegan se suman al monomio **afín** —el de más peso de su mismo tipo—, porque un monomio por debajo del 5% no es válido.
- **Gastos generales y utilidad** forman siempre un monomio propio, con símbolo **GU**.
- Si ningún índice alcanza el mínimo, la fórmula se arma con los monomios clásicos por tipo: mano de obra (J), materiales (M) y equipo (E).

Los coeficientes se expresan **al milésimo** (tres decimales) y suman 1.000.

El símbolo de cada monomio sale de lo que representa: **J** el jornal, **E** el equipo, **GU** los gastos generales y la utilidad, y para los materiales la inicial del índice que lo encabeza —**C** de cemento, **A** de acero, **T** de tubería.

## Ver y editar la composición

Al seleccionar un monomio, la tarjeta **Composición** lista los índices unificados que lo forman, con su monto y su incidencia. La columna **Monomio** permite mover un índice a otro: los coeficientes se recalculan solos y la fórmula sigue sumando 1.000.

Cuando un monomio agrupa varios índices, su índice de precio es el **promedio ponderado de sus tres componentes de mayor peso**, como fija el artículo 2. El monomio puede agrupar la incidencia de más índices —descartarlos perdería costo directo—, pero solo esos tres forman el índice.

El cuadro de composición sale también en los reportes PDF y Excel.

## Varias fórmulas en una obra

Una obra puede tener hasta **cuatro fórmulas** polinómicas (ocho si el contrato incluye obras de diversa naturaleza), subdividiendo el presupuesto en tantas partes como fórmulas. En IngePresupuestos esa subdivisión son los **subpresupuestos**: en «Fórmulas…» se crea cada fórmula y se marcan los subpresupuestos que cubre. Si no se marca ninguno, la fórmula cubre toda la obra.

Cada fórmula calcula sobre su parte del presupuesto y reajusta las valorizaciones de esa parte con su propio coeficiente K.

## Validaciones del D.S. 011-79-VC

- La **suma de los coeficientes** es igual a **1.000**.
- Cada **incidencia** es **mayor o igual a 5%** (0.050).
- Como **máximo 8 monomios** por fórmula.
- El índice de un monomio agrupado promedia **hasta tres** índices unificados.
- Hasta **4 fórmulas** por obra (8 con obras de diversa naturaleza).

## Reajuste de las valorizaciones

El coeficiente **K = Σ k·(Ir/Io)** se calcula con los índices del mes en que se paga la valorización frente a los del presupuesto base. El reajuste de la valorización es **R = V·(K−1)** y aparece en Control de Obra junto al monto del período.

Cuando no se puede reajustar, el programa dice por qué: la modalidad de la obra, que no haya fórmula guardada, que falten índices del mes, o que el período cruce el cambio de base del INEI.

## Índices unificados: dos bases

En enero de 2026 el INEI cambió el régimen (**RJ 016-2026-INEI**):

| | hasta noviembre 2025 | desde diciembre 2025 |
|---|---|---|
| Base | Julio 1992 = 100 | **Diciembre 2025 = 100** |
| Áreas geográficas | 6 | **13** |
| Índices | 68 | **77** (códigos 01 a 95) |

Las dos bases **conviven** en el programa y no se mezclan: un presupuesto anterior a diciembre de 2025 se reajusta con la serie vieja y uno posterior con la nueva. El selector **Base** de la vista de índices cambia entre ellas.

Es importante porque **30 códigos cambiaron de significado**: el 21 era «Cemento Portland Tipo I» y ahora es «Cemento Portland e hidráulico», que absorbió los tipos II y V. Si el presupuesto base y el mes de reajuste caen en bases distintas, el programa no calcula K y lo explica: hace falta el factor de empalme oficial.

El catálogo se **edita**: puedes dar de alta índices, renombrarlos y darlos de baja. Al importar el archivo oficial del INEI, los índices que aún no estén se dan de alta solos.

## El diccionario del INEI

El **Diccionario de Elementos de la Construcción válido para elaborar Fórmulas Polinómicas** es el Anexo 2 de la RJ 016-2026-INEI: 1930 elementos con el índice unificado que les corresponde. Viene incluido en el programa.

El botón **Diccionario** de la vista de índices muestra cuántos insumos están sin clasificar y propone un índice para cada uno, primero según el diccionario oficial y después por parecido con los insumos de tu propia biblioteca. La tabla indica la fuente de cada propuesta.

Las propuestas **no se aplican solas**: se revisan y se marcan. Las que tienen otro índice casi igual de parecido salen en ámbar y desmarcadas, porque asignar mal un índice mueve costo de un monomio a otro. El diccionario propio se puede exportar e importar como archivo JSON.
