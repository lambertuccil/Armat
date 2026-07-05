# Skill: controlar_presupuesto

## Identidad
- **Agente**: Obras
- **Nombre**: Control Presupuestario
- **Versión**: 1.0

## Objetivo
Monitorear y controlar el presupuesto de obra, detectando variaciones, anticipando sobrecostos y proponiendo acciones correctivas.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **presupuesto_original** (requerido): Presupuesto aprobado
- **gasto_real_acumulado** (requerido): Gasto ejecutado hasta la fecha
- **avance_fisico** (requerido): Porcentaje de avance físico
- **compromisos_pendientes** (opcional): Órdenes de compra comprometidas

## Proceso
1. Comparar presupuesto vs gasto real
2. Calcular valor ganado (Earned Value)
3. Determinar variaciones por partida
4. Identificar sobrecostos o ahorros
5. Proyectar gasto al cierre
6. Generar alertas tempranas
7. Recomendar acciones correctivas

## Salida
Dashboard de control con:
- Estado del presupuesto
- Variaciones por concepto
- Valor ganado y desempeño
- Proyección de cierre
- Acciones correctivas

## Checklist
- [ ] Presupuesto base registrado
- [ ] Gastos capturados
- [ ] Variaciones calculadas
- [ ] Valor ganado determinado
- [ ] Proyección realizada
- [ ] Alertas generadas

## Ejemplo
```markdown
# CONTROL PRESUPUESTARIO - ENTANYQ
**Fecha**: 4 de julio, 2026

## Estado General
- Presupuesto: $15,000,000
- Ejecutado: $10,500,000 (70%)
- Avance físico: 68%
- Variación: +2% sobrecosto

## Variaciones por Concepto
| Concepto | Presupuesto | Real | Var% |
|----------|-----------|------|------|
| Estructura | $4.5M | $4.2M | -6.7% |
| Instalaciones | $3.0M | $3.3M | +10% |

## Alertas
- Instalaciones sobre presupuesto
- Revisar costos de materiales

## Acciones
1. Negociar precios con proveedores de instalaciones
2. Revisar especificaciones para reducir costos
```
