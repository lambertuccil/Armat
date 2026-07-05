# Skill: verificar_calidad

## Identidad
- **Agente**: Obras
- **Nombre**: Verificación de Calidad
- **Versión**: 1.0

## Objetivo
Realizar inspecciones de calidad en obra, verificando cumplimiento de especificaciones técnicas, normativas y estándares de calidad.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **area_inspeccion** (requerido): Zona o elemento a inspeccionar
- **especificaciones** (requerido): Requisitos técnicos a verificar
- **resultados_previos** (opcional): Inspecciones anteriores

## Proceso
1. Identificar área o elemento a inspeccionar
2. Revisar especificaciones técnicas (NOMs, planos)
3. Realizar verificación visual y dimensional
4. Documentar conformidades y no conformidades
5. Clasificar hallazgos por severidad
6. Generar recomendaciones de corrección
7. Registrar evidencia fotográfica

## Salida
Reporte de inspección con:
- Estado de cumplimiento
- Lista de hallazgos
- Clasificación de severidad
- Acciones correctivas recomendadas

## Checklist
- [ ] Área inspeccionada identificada
- [ ] Especificaciones revisadas
- [ ] Verificación dimensional realizada
- [ ] Hallazgos documentados
- [ ] Severidad clasificada
- [ ] Recomendaciones generadas

## Ejemplo
```markdown
# INSPECCIÓN DE CALIDAD - ENTANYQ
**Fecha**: 4 de julio, 2026
**Área**: Muros departamentos 301-304

## Conforme
- Altura de muros: 2.70m ✓
- Verticalidad: dentro de tolerancia ✓
- Acabado: aceptable ✓

## No Conforme
- Grietas menores en muro 302 (severidad: baja)
- Falta impermeabilización en junta (severidad: media)

## Acciones Correctivas
1. Reparar grietas con mortero especial
2. Aplicar sellador en juntas
```
