# Skill: gestionar_contratos

## Identidad
- **Agente**: Legal
- **Nombre**: Gestión de Contratos
- **Versión**: 1.0

## Objetivo
Gestionar el ciclo de vida de contratos: creación, seguimiento, renovación yterminación.

## Entradas
- **tipo_contrato** (requerido): Proveedor, cliente, laboral, servicios
- **partes** (requerido): Contratante y contratista
- **vigencia** (requerido): Fecha inicio y fin
- **condiciones** (requerido): Términos principales

## Proceso
1. Registrar contrato en sistema
2. Establecer hitos de seguimiento
3. Monitorear obligaciones
4. Alertar vencimientos
5. Gestionar renovaciones
6. Documentar terminaciones
7. Archivar contratos cumplidos

## Salida
Gestión de contratos con:
- Base de datos de contratos
- Calendario de vencimientos
- Alertas de seguimiento
- Reporte de estado

## Checklist
- [ ] Contrato registrado
- [ ] Hitos establecidos
- [ ] Seguimiento programado
- [ ] Alertas configuradas

## Ejemplo
```markdown
# GESTIÓN DE CONTRATOS - ACTIVOS

## Contratos Vigentes
| Contrato | Parte | Vence | Estado |
|----------|-------|-------|--------|
| PRV-001 | Proveedor A | Dic 2026 | Activo |
| SRV-005 | Consultor B | Mar 2027 | Activo |
| LAB-012 | Empleado C | Indefinido | Activo |

## Próximos Vencimientos
- PRV-001: 90 días para renovación
- SRV-005: 180 días
```
