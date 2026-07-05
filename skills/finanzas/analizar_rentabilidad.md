# Skill: analizar_rentabilidad

## Identidad
- **Agente**: Finanzas
- **Nombre**: Análisis de Rentabilidad
- **Versión**: 1.0

## Objetivo
Evaluar la rentabilidad de un proyecto inmobiliario o de construcción, calculando indicadores como ROI, VAN, TIR y período de recuperación.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **inversion_total** (requerido): Inversión inicial
- **ingresos_proyectados** (requerido): Ingresos por ventas o arrendamiento
- **costos_totales** (requerido): Costos de construcción y operación
- **tasa_descuento** (opcional): Tasa para calcular VAN (default: 12%)
- **horizonte_evaluacion** (requerido): Años de evaluación

## Proceso
1. Registrar inversión inicial
2. Proyectar ingresos por año
3. Proyectar costos por año
4. Calcular flujos netos
5. Calcular VAN (Valor Actual Neto)
6. Calcular TIR (Tasa Interna de Retorno)
7. Calcular período de recuperación
8. Comparar con benchmark del sector

## Salida
Análisis de rentabilidad con:
- VAN y TIR calculados
- Período de recuperación
- ROI proyectado
- Comparativa con benchmark
- Recomendación de viabilidad

## Checklist
- [ ] Inversión inicial registrada
- [ ] Ingresos proyectados
- [ ] Costos estimados
- [ ] Flujos calculados
- [ ] VAN determinado
- [ ] TIR calculada
- [ ] Período de recuperación
- [ ] Recomendación generada

## Ejemplo
```markdown
# ANÁLISIS DE RENTABILIDAD - ENTANYQ

## Datos del Proyecto
- Inversión: $15,000,000
- Horizonte: 3 años
- Tasa descuento: 12%

## Resultados
| Indicador | Valor | Benchmark |
|-----------|-------|-----------|
| VAN | $4,200,000 | >$0 ✓ |
| TIR | 28% | >15% ✓ |
| ROI | 45% | >20% ✓ |
| Payback | 2.1 años | <3 años ✓ |

## Recomendación
Proyecto VIABLE. Supera todos los indicadores de benchmark.
```
