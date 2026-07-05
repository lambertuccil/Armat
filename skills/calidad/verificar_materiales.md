# Skill: verificar_materiales

## Identidad
- **Agente**: Calidad
- **Nombre**: Verificación de Materiales
- **Versión**: 1.0

## Objetivo
Verificar la calidad y especificaciones de materiales que llegan a sitio de construcción.

## Entradas
- **material** (requerido): Tipo de material
- **proveedor** (requerido): Quien suministra
- **lote** (requerido): Número de lote
- **cantidad** (requerido): Cantidad recibida
- **especificaciones** (requerido): Requisitos técnicos

## Proceso
1. Recibir material en sitio
2. Verificar cantidad contra pedido
3. Revisar documentación (certificados, lotes)
4. Inspeccionar visualmente
5. Realizar pruebas si aplica
6. Aprobar o rechazar
7. Documentar resultado

## Salida
Acta de recepción con:
- Material recibido
- Cantidad verificada
- Estado del material
- Aprobación o rechazo
- Observaciones

## Checklist
- [ ] Cantidad verificada
- [ ] Documentación revisada
- [ ] Inspección visual realizada
- [ ] Pruebas aplicadas
- [ ] Decisión registrada

## Ejemplo
```markdown
# ACTA DE RECEPCIÓN - CEMENTO

## Material
- Tipo: Cemento CPC 30R
- Proveedor: Cemex
- Lote: 2026-07-001
- Cantidad: 50 sacos

## Verificación
- Cantidad: ✓ 50 sacos
- Peso unitario: ✓ 50 kg
- Estado: ✓ Seco, sin humedad
- Certificado: ✓ Adjunto

## Decisión: APROBADO
```
