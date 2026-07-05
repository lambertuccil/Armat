# Skill: calcular_nomina

## Identidad
- **Agente**: RRHH
- **Nombre**: Cálculo de Nómina
- **Versión**: 1.0

## Objetivo
Calcular nómina quincenal o mensual incluyendo percepciones, deducciones y neto a pagar.

## Entradas
- **empleado** (requerido): Nombre y puesto
- **sueldo_base** (requerido): Salario mensual
- **dias_trabajados** (requerido): Días del período
- **percepciones** (opcional): Bonos, comisiones
- **deducciones** (opcional): Préstamos, faltas

## Proceso
1. Calcular sueldo proporcional
2. Sumar percepciones
3. Calcular ISR
4. Calcular IMSS
5. Calcular AFORE
6. Restar deducciones
7. Generar recibo

## Salida
Recibo de nómina con:
- Percepciones detalladas
- Deducciones detalladas
- Neto a pagar
- Desglose de impuestos

## Checklist
- [ ] Datos del empleado verificados
- [ ] Sueldo calculado
- [ ] Percepciones sumadas
- [ ] ISR calculado
- [ ] IMSS calculado
- [ ] Neto determinado

## Ejemplo
```markdown
# RECIBO #2026-145

## Empleado: Ing. Carlos Méndez
## Período: 1-15 julio 2026

## Percepciones
- Sueldo: $17,500
- Bono: $2,000
- **Total: $19,500**

## Deducciones
- ISR: $2,800
- IMSS: $650
- AFORE: $585
- **Total: $4,035**

## **NETO: $15,465**
```
