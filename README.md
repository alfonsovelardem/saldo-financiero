# saldo-financiero
Algoritmo para calcular un saldo financiero en base a una lista de transacciones financieras, donde cada transacción tiene un identificador, un monto y un tipo (ingreso o egreso).

### Descripcion del algoritmo

### Analisis de Complejidad

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

### Caso 1

### Caso 2


### Archivos del Pseudocodigo

    *`saldo_final.pseudocode`
    