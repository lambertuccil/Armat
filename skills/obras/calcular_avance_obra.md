# Skill: calcular_avance_obra

## Identidad
- **Agente**: Obras
- **Nombre**: Cálculo de Avance de Obra
- **Versión**: 1.0

## Objetivo
Calcular el porcentaje de avance físico y financiero de un proyecto de construcción, comparando lo ejecutado contra lo programado.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **fecha_corte** (requerido): Fecha de medición
- **presupuesto_total** (requerido): Presupuesto total autorizado
- **avance_fisico_parcial** (requerido): Porcentaje de avance físico
- **inversion_acumulada** (requerido): Inversión financiera acumulada
- **programa_original** (opcional): Cronograma base

## Proceso
1. Calcular avance físico: (trabajo ejecutado / trabajo total) × 100
2. Calcular avance financiero: (inversión acumulada / presupuesto total) × 100
3. Comparar avance físico vs financiero
4. Calcular desviación del programa
5. Identificar retrasos o adelantos
6. Generar indicadores de desempeño

## Salida
Reporte de avance con:
- Porcentaje físico y financiero
- Desviación del programa
- Valor Ganado (Earned Value)
- Proyección de conclusión

## Checklist
- [ ] Datos de entrada completos
- [ ] Cálculos verificados
- [ ] Desviación calculada
- [ ] Indicadores generados
- [ ] Proyección realizada

## Ejemplo
```markdown
# REPORTE DE AVANCE - ENTANYQ
**Fecha**: 4 de julio, 2026

## Avance Físico
- Programado: 75%
- Ejecutado: 68%
- Desviación: -7%

## Avance Financiero
- Presupuesto: $15,000,000
- Inversión: $10,500,000
- Avance financiero: 70%

## Análisis
- Físico atrasado vs financiero
- Posible sobrecosto en actividades críticas
- Recomendación: revisar programa de trabajo
```
