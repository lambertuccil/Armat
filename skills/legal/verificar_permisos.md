# Skill: verificar_permisos

## Identidad
- **Agente**: Legal
- **Nombre**: Verificación de Permisos
- **Versión**: 1.0

## Objetivo
Verificar el estatus de permisos de construcción, licencias y trámites municipales/estatales para proyectos inmobiliarios.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **ubicacion** (requerido): Municipio y estado
- **tipo_proyecto** (requerido): Residencial, comercial, mixto
- **etapa** (requerido): Preoperaciones, construcción, entrega

## Proceso
1. Identificar permisos requeridos por tipo y ubicación
2. Verificar estatus de cada permiso
3. Detectar permisos pendientes o vencidos
4. Calcular plazos de renovación
5. Identificar riesgos de paro de obra
6. Generar checklist de permisos
7. Recomendar acciones

## Salida
Reporte de permisos con:
- Lista de permisos requeridos
- Estatus de cada uno
- Fechas de vencimiento
- Permisos pendientes
- Acciones recomendadas

## Checklist
- [ ] Permisos identificados
- [ ] Estatus verificado
- [ ] Plazos calculados
- [ ] Riesgos determinados
- [ ] Reporte generado

## Ejemplo
```markdown
# VERIFICACIÓN DE PERMISOS - ENTANYQ
**Municipio**: Benito Juárez, CDMX

## Permisos Requeridos
| Permiso | Estatus | Vence |
|---------|---------|-------|
| Licencia construcción | ✅ Vigente | Dic 2026 |
| Uso de suelo | ✅ Vigente | — |
| Impacto ambiental | ⚠️ Pendiente | — |
| Conexión agua | ✅ Aprobada | — |

## Acciones
1. Gestionar impacto ambiental (2 semanas)
2. Renovar licencia antes de dic 2026
```
