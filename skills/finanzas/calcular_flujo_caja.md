# Skill: calcular_flujo_caja

## Identidad
- **Agente**: Finanzas
- **Nombre**: Cálculo de Flujo de Caja
- **Versión**: 1.0

## Objetivo
Proyectar y analizar el flujo de efectivo de un proyecto o empresa inmobiliaria, identificando períodos de déficit o superávit.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **periodo** (requerido): Meses a proyectar
- **ingresos_esperados** (requerido): Ventas, pagos de clientes
- **egresos_estimados** (requerido): Costos, gastos, inversiones
- **saldo_inicial** (requerido): Efectivo disponible al inicio

## Proceso
1. Registrar saldo inicial
2. Proyectar ingresos por período
3. Proyectar egresos por período
4. Calcular flujo neto mensual
5. Calcular flujo acumulado
6. Identificar déficits o superávits
7. Recomendar líneas de crédito si es necesario

## Salida
Proyección de flujo de caja con:
- Flujo mensual detallado
- Flujo acumulado
- Períodos críticos
- Recomendaciones de financiamiento

## Checklist
- [ ] Saldo inicial registrado
- [ ] Ingresos proyectados
- [ ] Egresos estimados
- [ ] Flujos calculados
- [ ] Períodos críticos identificados
- [ ] Recomendaciones generadas

## Ejemplo
```markdown
# FLUJO DE CAJA - ENTANYQ 2026

## Proyección Mensual
| Mes | Ingresos | Egresos | Flujo Neto | Acumulado |
|-----|----------|---------|------------|-----------|
| Ene | $800K | $600K | $200K | $200K |
| Feb | $500K | $700K | -$200K | $0 |
| Mar | $1,200K | $800K | $400K | $400K |
| Abr | $600K | $900K | -$300K | $100K |

## Períodos Críticos
- Febrero: déficit de $200K
- Abril: déficit de $300K

## Recomendaciones
1. Disponer línea de crédito por $500K
2. Negociar pagos a proveedores a 60 días
```
