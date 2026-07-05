# Skill: calcular_roi

## Identidad
- **Nombre**: calcular_roi
- **Agente**: Comercial
- **Categoría**: Ventas/Finanzas
- **Complejidad**: Media

## Objetivo
Calcular retorno de inversión estimado para una propiedad de ARMAT.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| unidad | string | Sí | Tipo de unidad |
| meses | number | No | Plazo estimado de inversión (default: 24) |
| valorizacion | number | No | % valorización anual estimada |

## Proceso
1. Obtener precio de la unidad
2. Estimar valorización según zona
3. Calcular valor futuro
4. Calcular ganancia neta
5. Calcular ROI porcentual

## Salida
Análisis de ROI con:
- Precio actual
- Valor estimado futuro
- Ganancia neta
- ROI porcentual
- Comparativa con otros instrumentos

## Checklist
- [ ] Precio correcto
- [ ] Valorización realista
- [ ] Cálculos verificados
- [ ] Comparativa incluida

## Ejemplo
```
Input: calcular_roi("mono", 24, 15)

Output:
# ROI Estimado — Monoambiente

• Precio actual: USD 60.000
• Valorización: 15% anual (2 años)
• Valor futuro: USD 79.350
• Ganancia neta: USD 19.350
• **ROI: 32.3%** (16.1% anual)

Comparativa:
- Plazo fijo: ~8% anual
- Cedear: ~12% anual
- **Inmueble: ~16% anual**
```