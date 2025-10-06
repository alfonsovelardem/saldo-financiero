# saldo-financiero
Algoritmo para calcular un saldo financiero en base a una lista de transacciones financieras, donde cada transacción tiene un identificador, un monto y un tipo (ingreso o egreso).

### Descripcion del algoritmo

El algoritmo está diseñado para procesar una lista de transacciones y calcular el saldo final.

1.  **Inicialización y Validación:**
    * El proceso inicia el **`saldo_actual`** en **0**.
    * Se realiza una validación inicial para asegurar que la clave `"datos"` exista y no esté vacía. Si no hay datos, se retorna el saldo inicial que es 0.

2.  **Iteración :**
    * Se utiliza un único bucle para recorrer todas las transacciones.
    * Dentro del bucle, se comprueba que cada transacción contenga los campos (`monto` y `tipo`). Las transacciones mal formadas son ignoradas para evitar errores.

3.  **Lógica de Acumulación:**
    * Si el `tipo` es **`"ingreso"`**, el `monto` se **suma** al saldo.
    * Si el `tipo` es **`"egreso"`**, el `monto` se **resta** del saldo.

4.  **Resultado Final:**
    * El valor acumulado en `saldo_actual` se retorna como el saldo final.

### Analisis de Complejidad

| Aspecto | Complejidad | Justificación |
| :--- | :--- | :--- |
| **Tiempo ($T$)** | **$O(N)$ (Lineal)** | El algoritmo debe visitar cada una de las $N$ transacciones. El tiempo de ejecución crece de forma directamente proporcional al número de transacciones. Esta es la eficiencia maxima posible para el problema. |
| **Espacio ($S$)** | **$O(1)$ (Constante)** | El espacio de memoria auxiliar es constante, limitado solo a almacenar el `saldo_actual` y variables temporales. No depende del número de transacciones ($N$). |

## Casos de prueba.

### Caso 1: Transacciones Mixtas

Este caso valida que la suma de ingresos y la resta de egresos funcionen correctamente.

Entrada:

json
{
    "datos": [
        {"id": 1, "monto": 100, "tipo": "ingreso"},
        {"id": 2, "monto": 50, "tipo": "egreso"},
        {"id": 3, "monto": 200, "tipo": "ingreso"}
    ]
}

Saldo Final Esperado: **$250** ( 0 + 100 - 50 + 200$)
### Caso 2: Lista Vacía

Sin datos

Entrada:
json
{
    "datos": []
}

Saldo Final Esperado: **$0** (Retorna el saldo inicial por validación de lista vacía)

### Archivos del Pseudocodigo

    *`saldo_final.pseudocode`
    