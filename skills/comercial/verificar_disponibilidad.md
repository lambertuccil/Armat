# Skill: verificar_disponibilidad

## Identidad
- **Nombre**: verificar_disponibilidad
- **Agente**: Comercial
- **Categoría**: Ventas
- **Complejidad**: Baja

## Objetivo
Consultar y reportar la disponibilidad actual de unidades en ARMAT.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| unidad | string | No | Tipo de unidad específica (opcional) |

## Proceso
1. Consultar estado de unidades
2. Identificar disponibles vs vendidas
3. Formatear reporte
4. Incluir estadísticas

## Salida
Reporte de disponibilidad con:
- Unidades disponibles
- Unidades vendidas
- Porcentaje de venta
- Detalle por tipo

## Checklist
- [ ] Datos actualizados
- [ ] Unidades listadas
- [ ] Porcentaje calculado
- [ ] Formato claro

## Ejemplo
```
Input: verificar_disponibilidad()

Output:
# Disponibilidad ENTANYQ

**Estado general**: 50% vendido

| Unidad | Estado | Precio |
|--------|--------|--------|
| 1 Dormitorio | Disponible | USD 85.000 |
| Monoambiente | Disponible | USD 60.000 |
| Cochera Cubierta | Disponible | USD 10.000 |

**Resumen**: 2 unidades disponibles de 4 totales.
```