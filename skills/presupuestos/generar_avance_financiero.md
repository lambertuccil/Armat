# Skill: generar_avance_financiero

## Identidad
- **Agente**: Presupuestos
- **Nombre**: Avance Financiero
- **Versión**: 1.0

## Objetivo
Generar reportes de avance financiero de obra comparando ejecución contra presupuesto.

## Entradas
- **proyecto** (requerido): Nombre del proyecto
- **periodo** (requerido): Semanal, quincenal, mensual
- **datos_bitacora** (requerido): Avance de obra
- **datos_financieros** (requerido): Pagos realizados

## Proceso
1. Consolidar avance físico
2. Consolidar avance financiero
3. Comparar ambos avances
4. Calcular valor ganado
5. Identificar desviaciones
6. Proyectar terminación
7. Generar reporte ejecutivo

## Salida
Reporte de avance financiero con:
- Avance físico
- Avance financiero
- Valor ganado
- Proyección

## Checklist
- [ ] Avance físico consolidado
- [ ] Avance financiero consolidado
- [ ] Comparativa realizada
- [ ] Proyección generada

## Ejemplo
```markdown
# AVANCE FINANCIERO - ENTANYQ JUNIO 2026

## Físico
- Programado: 75%
- Real: 68%
- Desviación: -7%

## Financiero
- Presupuesto: $15M
- Ejecutado: $10.5M
- Avance: 70%

## Valor Ganado
- EV: $10.2M
- AC: $10.5M
- SV: -$300K (sobrecosto)
```
