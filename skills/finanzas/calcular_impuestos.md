# Skill: calcular_impuestos

## Identidad
- **Agente**: Finanzas
- **Nombre**: Cálculo de Impuestos
- **Versión**: 1.0

## Objetivo
Calcular obligaciones fiscales de proyectos inmobiliarios incluyendo ISR, IVA, predial e impuestos de adquisición.

## Entradas
- **tipo_operacion** (requerido): Venta, arrendamiento, desarrollo
- **monto_transaccion** (requerido): Valor de la operación
- **ubicacion** (requerido): Estado y municipio
- **tipo_persona** (requerido): Física o moral
- **regimen_fiscal** (opcional): Régimen especial aplicable

## Proceso
1. Identificar impuestos aplicables
2. Calcular ISR por enajenación
3. Calcular IVA si aplica
4. Determinar impuesto predial proporcional
5. Calcular impuesto de adquisición
6. Verificar beneficios fiscales
7. Generar desglose de obligaciones

## Salida
Desglose de impuestos con:
- ISR a cargo
- IVA trasladado
- Impuesto predial
- Impuesto adquisición
- Total obligación fiscal

## Checklist
- [ ] Operación clasificada
- [ ] Impuestos identificados
- [ ] Cálculos realizados
- [ ] Beneficios verificados
- [ ] Desglose generado

## Ejemplo
```markdown
# CÁLCULO DE IMPUESTOS - VENTA ENTANYQ

## Operación
- Venta de departamento: $1,800,000
- Tipo: Enajenación de bienes inmuebles

## Impuestos Calculados
| Impuesto | Base | Tasa | Monto |
|----------|------|------|-------|
| ISR | $1,800,000 | 25% | $450,000 |
| IVA | $1,800,000 | 16% | $288,000 |
| Predial (proporcional) | $1,800,000 | 0.1% | $1,800 |

## Total Obligación
$739,800
```
