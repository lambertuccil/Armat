# Skill: programar_actividades

## Identidad
- **Agente**: Obras
- **Nombre**: Programación de Actividades
- **Versión**: 1.0

## Objetivo
Crear y optimizar programas de trabajo (cronogramas) para actividades de construcción, identificando secuencias críticas y recursos necesarios.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **alcance** (requerido): Actividades a programar
- **duracion_estimada** (requerido): Tiempo estimado por actividad
- **recursos_disponibles** (opcional): Personal y equipo disponible
- **dependencias** (opcional): Relaciones entre actividades

## Proceso
1. Descomponer trabajo en actividades (EDT)
2. Estimar duraciones por actividad
3. Identificar dependencias (predecesoras/sucesoras)
4. Determinar ruta crítica
5. Asignar recursos
6. Generar cronograma visual
7. Identificar holguras

## Salida
Programa de trabajo con:
- Cronograma visual (diagrama de Gantt simplificado)
- Ruta crítica identificada
- Asignación de recursos
- Hitos importantes
- Holguras disponibles

## Checklist
- [ ] Actividades descompuestas
- [ ] Duraciones estimadas
- [ ] Dependencias identificadas
- [ ] Ruta crítica calculada
- [ ] Recursos asignados
- [ ] Cronograma generado

## Ejemplo
```markdown
# PROGRAMA DE TRABAJO - NIVEL 3 ENTANYQ
**Duración**: 6 semanas

## Actividades
| Semana | 1 | 2 | 3 | 4 | 5 | 6 |
|--------|---|---|---|---|---|---|
| Muros | ████████ | ████ | | | | |
| Hidráulica | | ████████ | ████ | | | |
| Eléctrica | | | ████████ | ████ | | |
| Acabados | | | | ████████ | ████ | |

## Ruta Crítica
Muros → Hidráulica → Eléctrica → Acabados

## Recursos
- 8 albañiles (semanas 1-2)
- 3 plomeros (semanas 2-3)
- 2 electricistas (semanas 3-4)
```
