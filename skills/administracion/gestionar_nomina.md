# Skill: gestionar_nomina

## Identidad
- **Agente**: Administración
- **Nombre**: Gestión de Nómina
- **Versión**: 1.0

## Objetivo
Administrar la nómina del personal de planta y de obra, incluyendo cálculos de nómina, prestaciones y obligaciones.

## Entradas
- **tipo_personal** (requerido): Planta, obra, temporal
- **periodo** (requerido): Quincenal, mensual
- **datos_empleado** (requerido): Salario, horas, deducciones
- **prestaciones** (opcional): Seguro, aguinaldo, vacaciones

## Proceso
1. Capturar días trabajados
2. Calcular salario bruto
3. Aplicar deducciones (ISR, IMSS)
4. Calcular prestaciones proporcionales
5. Generar recibo de nómina
6. Realizar pagos
7. Declarar ante autoridades

## Salida
Recibo de nómina con:
- Salario bruto
- Deducciones
- Percepciones netas
- Desglose de impuestos

## Checklist
- [ ] Datos capturados
- [ ] Cálculos realizados
- [ ] Deducciones aplicadas
- [ ] Recibo generado
- [ ] Pago ejecutado

## Ejemplo
```markdown
# NÓMINA - QUINCENA 1-15 JULIO 2026

## Empleado: Ing. Carlos Méndez
- Salario mensual: $35,000
- Quincena: $17,500

## Deducciones
- ISR: $2,100
- IMSS: $525
- Total: $2,625

## Neto a pagar: $14,875
```
