# Teoría de la decisión

Se combina con la teoría de la probabilidad para la toma de decisiones óptimas en situaciones donde se involucra la incertidumbre. Decidir implica elegir, para luego actuar. Los elementos de la desición son:

- Estados: Situaciones en la que se encuentra un elemento. Puede ser incierto.
- Acciones u opciones: alternativas ante la elección
- Resultado o rendimiento: evaluación de las consecuencias al elegir (ganancias o perdidas).

    ||Estado 1|Estado 2|Estado n|
    |--|--|--|--|
    |Acción 1|Resultado_11|Resultado_12|Resultado_1n|
    |Acción 1|Resultado_21|Resultado_22|Resultado_2n|
    |Acción n|Resultado_n1|Resultado_n2|Resultado_nn|

## Ejemplo 1 de la teoría de la decisión

Un fabricante planea introducir un nuevo télefono móvil. Puede elegir entre 4 procesos de producción $A, B, C, B$, que van desde una modificación relativamente pequeña de las instalaciones existentes, hasta una gran ampliación de la planta. La decisión sobre el curso de acción debe tomarse en un momento en el que no se conoce la demanda posible del producto. Por comodidad, decimos que esta demanda potencial puede ser "baja", "moderada" o "alta". También se suponen que el fabricante puede calcular para cada proceso de producción el beneficio durante la vida de la inversión correspondiente a cada uno de los niveles de demanda. La tabla muestra estos niveles de beneficio (en dólares) para cada combinación "proceso de producción - nivel de demanda". Averigüe si hay alguna acción inadmisible.

Acción vs Estado de la naturaleza

|Proceso de producción|Demanda baja|Demanda moderada|Demanda alta|
|--|--|--|--|
|A|70000|120000|200000|
|B|80000|120000|180000|
|C|100000|125000|160000|
|D|100000|120000|150000|

*Respuesta/:* $C$ domina a $D$, por lo tanto $D$ es inadmisible.

## Estrategias o métodos para la toma de decisiones

### Criterio Maximin

Selecciona la acción que tiene el mayor dentro de los rendimientos mínimos (se maximiza el rendimiento mínimo)

|Proceso de producción|Demanda baja|Demanda moderada|Demanda alta|
|--|--|--|--|
|A|70000|120000|200000|
|B|80000|120000|180000|
|C|100000|125000|160000|

*Respuesta/:* El criterio Maximin selecciona el proceso de producción $C$, bajo la demanda baja.

|Proceso de producción|Rendimientos mínimos|
|--|--|
|A|70000|
|B|80000|
|C|100000|

|Proceso de producción|Mejor resultado|
|--|--|
|C|100000|

#### Ejemplo 2

Un inversor quiere elegir entre invertir $10,000 durante un año a un tipo de interés garantizado del 12% e invertir la misma cantidad durante ese periodo en una cartera de acciones ordinarias. Si elegie el tipo de interés fijo, tendrá con seguridad un rendimiento de $1,200. Si elige la cartera de acciones, el rendimiento dependerá del comportamiento del mercado durante el año. Si el mercado está boyante, se espera un beneficio de $2,500; si el mercado se mantiene estable, el beneficio esperado es de $500; y si está deprimido, se espera una pérdida de $1,000. Elabore la tabla de rendimientos de este inversor y halle la elección de la acción mediante el criterio Maximin.

|Opción de inversión|Estado boyante|Estado Estable|Estado deprimido|Rendimiento|
|--|--|--|--|--|
|Interés fijo|1200|1200|1200|1200|
|Cartera de acciones|2500|500|-1000|-100|

*Respuesta/:* La elección es de un interés fijo de $1200 cuando este en un estado deprimido.  

### Criterio Minimax

También llamado criterio de la pérdida de oportunidades minimax. Los pasos a seguir son:

1. Se resta cada rendimiento de la tabla, del rendimiento mayor de su columna. Esto produce la tabla de pérdida de oportunidades.
2. Se halla en cada fila la máxima pérdida
3. Se elige la acción que tiene el mínimo de esas pérdidas máximas.

|Proceso de producción|Demanda baja|Demanda moderada|Demanda alta|
|--|--|--|--|
|A|70000|120000|200000|
|B|80000|120000|180000|
|C|100000|125000|160000|

1. Tabla de perdida de oportunidades

- Demanda baja: $100000 - 70000$
- Demanda Moderada: $125000 - 120000$
- Demanda baja: $200000 - 160000$

|Proceso de producción|Demanda baja|Demanda moderada|Demanda alta|
|--|--|--|--|
|A|30000|5000|0|
|B|20000|5000|0|
|C|0|0|40000|

2. Se halla en cada fila la máxima pérdida.

|Acción|Máx pérdida|
|--|--|
|A|30000|
|B|20000|
|C|40000|

3. Se elige la acción que tiene el mínimo de esas pérdidas máximas.

|Acción|Mínimo pérdida|
|--|--|
|B|20000|

### Ejemplo 3

Considere el ejercicio ejemplo 2, en el que el inversor está considerando tres alternativas -un certificado de depósito, un fondo de acciones de bajo riesgo y un fondo de acciones de alto riesgo- para hacer una inversión de $20,000. Considera tres estados de la naturaleza posibles:

- $s_1$: mercado de valores fuerte
- $s_2$: mercado de valores moderado
- $s_3$: mercado de valores débil

La tabla de rendimiento (en dólares) es la siguiente:

|Alternativas de inversión posibles|s1|s2|s3|
|--|--|--|--|
|Certificado de déposito|1200|1200|1200|
|Fondo de acciones bajo riesgo|4300|1200|-600|
|Fondo de acciones de alto riesgo|6600|800|-1500|

- ¿Que acción se selecciona mediante el criterio maximin?

    |Alternativas de inversión posibles|s3|
    |--|--|
    |Certificado de déposito|1200|
    |Fondo de acciones bajo riesgo|-600|
    |Fondo de acciones de alto riesgo|-1500|

    |Alternativas de inversión posibles|s3|
    |--|--|
    |Certificado de déposito|1200|

    *Respuesta/:* El certificado de déposito es el mejor resultado en el peor escenario.

- ¿Que acción se selecciona mediante el criterio de oportunidades minimax?

    |Alternativas de inversión posibles|s1|s2|s3|
    |--|--|--|--|
    |Certificado de déposito|5400|0|0|
    |Fondo de acciones bajo riesgo|2300|0|600|
    |Fondo de acciones de alto riesgo|0|400|(menos)300|

    |Acción|Máx pérdida|
    |--|--|
    |Certificado de déposito|5400|
    |Fondo de acciones bajo riesgo|2300|
    |Fondo de acciones de alto riesgo|400|

    |Acción|Mínimo pérdida|
    |--|--|
    |Fondo de acciones de alto riesgo|400|

    *Respuesta/:* El Fondo de acciones de alto riesgo el mejor resultado en el mejor escenario.
