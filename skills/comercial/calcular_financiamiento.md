# Skill: calcular_financiamiento

## Identidad
- **Nombre**: calcular_financiamiento
- **Agente**: Comercial
- **Categoría**: Ventas/Finanzas
- **Complejidad**: Baja

## Objetivo
Calcular opciones de financiamiento para una propiedad, mostrando seña, cuotas y total.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| unidad | string | Sí | Tipo de unidad |
| cuotas | number | No | Cantidad de cuotas (default: 12) |

## Proceso
1. Obtener precio de la unidad
2. Calcular seña (50% del precio)
3. Calcular cuota mensual
4. Calcular total financiado
5. Calcular diferencia vs contado

## Salida
Opciones de financiamiento:
- Precio contado
- Seña
- Cuotas
- Total financiado
- Diferencia

## Checklist
- [ ] Precio correcto
- [ ] Seña calculada (50%)
- [ ] Cuotas correctas
- [ ] Total verificado
- [ ] Diferencia incluida

## Ejemplo
```
Input: calcular_financiamiento("1 dorm", 12)

Output:
Financiamiento — 1 Dormitorio

• Precio contado: USD 85.000
• Seña (50%): USD 45.000
• 12 cuotas: USD 3.750
• Total financiado: USD 90.000
• Diferencia: +USD 5.000 (6%)
```