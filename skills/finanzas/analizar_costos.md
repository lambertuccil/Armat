# Skill: analizar_costos

## Identidad
- **Agente**: Finanzas
- **Nombre**: Análisis de Costos
- **Versión**: 1.0

## Objetivo
Desglosar y analizar costos de construcción por concepto, identifying áreas de optimización y sobrecostos.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **presupuesto** (requerido): Presupuesto aprobado
- **costos_reales** (requerido): Costos ejecutados
- **avance** (requerido): Porcentaje de avance

## Proceso
1. Desglosar costos por categoría
2. Comparar presupuesto vs real
3. Calcular variaciones por concepto
4. Identificar sobrecostos significativos
5. Analizar causas de variaciones
6. Recomendar acciones de control
7. Generar reporte ejecutivo

## Salida
Análisis de costos con:
- Desglose por categoría
- Tabla de variaciones
- Sobrecostos identificados
- Acciones correctivas

## Checklist
- [ ] Costos desglosados
- [ ] Variaciones calculadas
- [ ] Sobrecostos identificados
- [ ] Causas analizadas
- [ ] Acciones definidas

## Ejemplo
```markdown
# ANÁLISIS DE COSTOS - ENTANYQ

## Resumen
- Presupuesto: $15,000,000
- Real: $15,800,000
- Variación: +5.3%

## Por Categoría
| Categoría | Presupuesto | Real | Var% |
|-----------|-----------|------|------|
| Materiales | $7.5M | $8.0M | +6.7% |
| Mano de obra | $4.5M | $4.3M | -4.4% |
| Equipos | $1.5M | $1.8M | +20% |
| Indirectos | $1.5M | $1.7M | +13.3% |

## Sobrecostos
1. Equipos: +$300K (equipo no contemplado)
2. Indirectos: +$200K (costos administrativos)

## Acciones
1. Renegociar contratos de renta de equipo
2. Optimizar gastos administrativos
```
