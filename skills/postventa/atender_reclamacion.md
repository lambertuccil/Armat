# Skill: atender_reclamacion

## Identidad
- **Agente**: Postventa
- **Nombre**: Atención de Reclamaciones
- **Versión**: 1.0

## Objetivo
Atender y resolver reclamaciones de clientes post-venta de manera oportuna y efectiva.

## Entradas
- **cliente** (requerido): Datos del cliente
- **problema** (requerido): Descripción del problema
- **departamento** (requerido): Unidad afectada
- **urgencia** (requerido): Alta, media, baja

## Proceso
1. Registrar reclamación
2. Verificar garantía
3. Coordinar visita técnica
4. Diagnosticar
5. Reparar
6. Confirmar satisfacción

## Salida
Reporte de reclamación con:
- Diagnóstico
- Solución aplicada
- Costo (si aplica)
- Estado de satisfacción

## Checklist
- [ ] Reclamación registrada
- [ ] Garantía verificada
- [ ] Visita coordinada
- [ ] Solución ejecutada
- [ ] Cliente satisfecho

## Ejemplo
```markdown
# RECLAMACIÓN #2026-023

## Cliente: Juan Pérez, Depto 301
## Problema: Fuga en baño
## Garantía: Vigente (hidráulica)

## Diagnóstico
- Conexión floja en lavabo

## Solución
- Reemplazo de joined
- Costo: $0 (garantía)
- Tiempo: 2 horas

## Estado: RESUELTO
## Satisfacción: 9/10
```
