# Skill: coordinar_logistica

## Identidad
- **Agente**: Administración
- **Nombre**: Coordinación Logística
- **Versión**: 1.0

## Objetivo
Coordinar la logística de materiales, equipos y personal entre oficina central y sitios de construcción.

## Entradas
- **proyecto** (requerido): Nombre del proyecto
- **recurso** (requerido): Material, equipo o personal
- **cantidad** (requerido): Cantidad requerida
- **fecha_requerida** (requerido): Fecha de entrega
- **ubicacion_origen** (requerido): Origen del recurso

## Proceso
1. Identificar necesidad del recurso
2. Verificar disponibilidad
3. Coordinar transporte
4. Programar entrega en sitio
5. Confirmar recepción
6. Documentar movimientos
7. Actualizar inventario

## Salida
Orden de movimiento con:
- Descripción del recurso
- Origen y destino
- Fecha programada
- Costo de transporte
- Responsable de recepción

## Checklist
- [ ] Necesidad identificada
- [ ] Disponibilidad verificada
- [ ] Transporte coordinado
- [ ] Entrega programada
- [ ] Recepción confirmada

## Ejemplo
```markdown
# MOVIMIENTO #2026-045

## Recurso
- Material: 200 blocks standard
- Origen: Almacén central
- Destino: Obra ENTANYQ, Nivel 3

## Logística
- Transporte: Camión plataformas
- Fecha: 5 julio 2026, 8:00 hrs
- Costo: $2,500

## Responsables
- Origen: Almacén - Juan Pérez
- Destino: Obra - Carlos Méndez
```
