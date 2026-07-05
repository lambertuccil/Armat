# Skill: seguir_pedido

## Identidad
- **Agente**: Proveedores
- **Nombre**: Seguimiento de Pedidos
- **Versión**: 1.0

## Objetivo
Dar seguimiento a órdenes de compra emitidas, asegurando entrega oportuna y conformidad.

## Entradas
- **orden_compra** (requerido): Número de orden
- **proveedor** (requerido): Proveedor
- **fecha_entrega** (requerido): Fecha comprometida
- **material** (requerido): Material a recibir

## Proceso
1. Verificar orden de compra
2. Confirmar preparación
3. Coordinar logística
4. Supervisar entrega
5. Verificar conformidad
6. Liberar pago

## Salida
Reporte de seguimiento con:
- Estado del pedido
- Fecha de entrega
- Conformidad
- Observaciones

## Checklist
- [ ] Orden verificada
- [ ] Preparación confirmada
- [ ] Logística coordinada
- [ ] Entrega supervisada
- [ ] Conformidad verificada

## Ejemplo
```markdown
# SEGUIMIENTO - OC-2026-045

## Material: 200 blocks
## Proveedor: Block Norte
## Entrega: 5 julio 2026

## Estado
- Preparación: ✓
- Transporte: En curso
- Llegada esperada: 10:00 hrs

## Verificación
- Cantidad: Pendiente
- Calidad: Pendiente
```
