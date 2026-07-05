# Skill: controlar_costos

## Identidad
- **Agente**: Presupuestos
- **Nombre**: Control de Costos
- **Versión**: 1.0

## Objetivo
Monitorear y controlar costos reales vs presupuestados, identificando variaciones y acciones correctivas.

## Entradas
- **proyecto** (requerido): Nombre del proyecto
- **presupuesto** (requerido): Presupuesto aprobado
- **costos_reales** (requerido): Costos ejecutados
- **avance** (requerido): Porcentaje de avance

## Proceso
1. Capturar costos reales por partida
2. Comparar con presupuesto
3. Calcular variaciones
4. Identificar sobrecostos
5. Analizar causas
6. Recomendar acciones
7. Generar reportes

## Salida
Reporte de control con:
- Variaciones por partida
- Sobrecostos identificados
- Acciones correctivas
- Proyección de cierre

## Checklist
- [ ] Costos capturados
- [ ] Variaciones calculadas
- [ ] Sobrecostos identificados
- [ ] Causas analizadas
- [ ] Reporte generado

## Ejemplo
```markdown
# CONTROL DE COSTOS - ENTANYQ

## Variaciones
| Partida | Presupuesto | Real | Var% |
|---------|-----------|------|------|
| Estructura | $3.6M | $3.4M | -5.6% |
| Instalaciones | $4.5M | $5.1M | +13.3% |
| Acabados | $5.4M | $5.4M | 0% |

## Alerta: Instalaciones +$600K
Causa: Cambios en especificaciones
Acción: Renegociar alcance
```
