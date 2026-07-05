# Skill: generar_orden_compra

## Identidad
- **Agente**: Compras
- **Nombre**: Generación de Orden de Compra
- **Versión**: 1.0

## Objetivo
Generar órdenes de compra formales para adquisición de materiales y servicios aprobados.

## Entradas
- **proveedor** (requerido): Proveedor seleccionado
- **materiales** (requerido): Lista de artículos a comprar
- **condiciones** (requerido): Precio, entrega, pago
- **proyecto** (requerido): Proyecto al que aplica
- **aprobacion** (requerido): Autorización de compra

## Proceso
1. Verificar aprobación de compra
2. Elaborar orden de compra
3. Detallar artículos y cantidades
4. Especificar condiciones
5. Enviar a proveedor
6. Confirmar recepción
7. Dar seguimiento a entrega

## Salida
Orden de compra con:
- Número de orden
- Proveedor
- Artículos detallados
- Condiciones comerciales
- Fecha de entrega

## Checklist
- [ ] Aprobación verificada
- [ ] Orden elaborada
- [ ] Proveedor notificado
- [ ] Confirmación recibida
- [ ] Seguimiento programado

## Ejemplo
```markdown
# ORDEN DE COMPRA #OC-2026-045

## Proveedor
Distribuidora Técnica S.A. de C.V.

## Artículos
| Descripción | Cant | Precio | Total |
|-------------|------|--------|-------|
| Tubería PVC 4" | 200 m | $78 | $15,600 |

## Condiciones
- Total: $15,600
- Entrega: 12 julio 2026
- Pago: 30 días
- Proyecto: ENTANYQ
```
