# Skill: programar_mantenimiento

## Identidad
- **Agente**: Postventa
- **Nombre**: Programación de Mantenimiento
- **Versión**: 1.0

## Objetivo
Programar y realizar visitas de mantenimiento preventivo a departamentos entregados.

## Entradas
- **departamento** (requerido): Unidad a mantener
- **meses_post_entrega** (requerido): Tiempo desde entrega
- **tipo_mantenimiento** (requerido): Preventivo, correctivo

## Proceso
1. Verificar elegibilidad
2. Coordinar visita
3. Realizar revisiones
4. Documentar hallazgos
5. Ejecutar mantenimiento
6. Recomendar mejoras

## Salida
Reporte de mantenimiento con:
- Revisiones realizadas
- Hallazgos
- Acciones ejecutadas
- Recomendaciones

## Checklist
- [ ] Visita coordinada
- [ ] Revisiones ejecutadas
- [ ] Hallazgos documentados
- [ ] Mantenimiento realizado
- [ ] Recomendaciones entregadas

## Ejemplo
```markdown
# MANTENIMIENTO - DEPTO 301
## Meses post-entrega: 3

## Revisiones
- Hidráulica: ✓ OK
- Eléctrica: ✓ OK
- Acabados: ⚠️ Grieta menor
- Carpintería: ✓ OK

## Acciones
- Monitorear grieta
- Próxima revisión: 6 meses

## Costo: $0
```
