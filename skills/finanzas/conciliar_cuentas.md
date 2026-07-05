# Skill: conciliar_cuentas

## Identidad
- **Agente**: Finanzas
- **Nombre**: Conciliación de Cuentas
- **Versión**: 1.0

## Objetivo
Realizar conciliaciones bancarias y contables para verificar consistencia de movimientos y saldos.

## Entradas
- **cuenta_bancaria** (requerido): Número de cuenta
- **periodo** (requerido): Mes a conciliar
- **saldo_contable** (requerido): Saldo según libros
- **saldo_bancario** (requerido): Saldo según banco
- **movimientos_banco** (requerido): Estado de cuenta

## Proceso
1. Obtener saldos iniciales
2. Comparar movimientos banco vs contabilidad
3. Identificar diferencias
4. Clasificar diferencias (pendientes, errores)
5. Ajustar partidas contables
6. Calcular saldo conciliado
7. Generar reporte de conciliación

## Salida
Reporte de conciliación con:
- Saldos comparativos
- Diferencias encontradas
- Ajustes realizados
- Saldo conciliado

## Checklist
- [ ] Saldos obtenidos
- [ ] Movimientos comparados
- [ ] Diferencias identificadas
- [ ] Ajustes realizados
- [ ] Saldo conciliado

## Ejemplo
```markdown
# CONCILIACIÓN BANCARIA - JUNIO 2026
**Cuenta**: 123456789

## Saldos
- Contable: $2,500,000
- Bancario: $2,350,000
- Diferencia: $150,000

## Diferencias
| Concepto | Monto | Tipo |
|----------|-------|------|
| Cheque 1234 | $50,000 | Pendiente |
| Depósito | $100,000 | Error |

## Ajustes
1. Registrar cheque 1234
2. Corregir depósito

## Saldo Conciliado
$2,500,000 ✓
```
