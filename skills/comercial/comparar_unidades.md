# Skill: comparar_unidades

## Identidad
- **Nombre**: comparar_unidades
- **Agente**: Comercial
- **Categoría**: Ventas
- **Complejidad**: Baja

## Objetivo
Generar una comparativa entre dos o más unidades de ARMAT para ayudar al cliente a decidir.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| unidades | array | Sí | Lista de unidades a comparar |
| criterio | string | No | Criterio de comparación (precio, espacio, inversión) |

## Proceso
1. Obtener datos de cada unidad
2. Calcular métricas comparativas
3. Generar tabla de comparación
4. Incluir análisis y recomendación
5. Formatear salida

## Salida
Tabla comparativa con:
- Características de cada unidad
- Precios y USD/m²
- Análisis comparativo
- Recomendación

## Checklist
- [ ] Todas las unidades son válidas
- [ ] Datos correctos
- [ ] USD/m² calculado
- [ ] Análisis incluido
- [ ] Recomendación clara

## Ejemplo
```
Input: comparar_unidades(["mono", "1 dorm"])

Output:
# Comparativa ENTANYQ

| Característica | Monoambiente | 1 Dormitorio |
|----------------|--------------|--------------|
| Superficie | 34,5 m² | 45,5 m² |
| Precio | USD 60.000 | USD 85.000 |
| USD/m² | 1.739 | 1.868 |
| Cuota | 2.900 | 3.750 |

Análisis:
- Mono: mejor para inversión (menor costo)
- 1 Dorm: mejor para vivir (más espacio)
```