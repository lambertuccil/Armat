# Skill: generar_informe_legal

## Identidad
- **Agente**: Legal
- **Nombre**: Generación de Informe Legal
- **Versión**: 1.0

## Objetivo
Generar informes legales consolidados para directivos sobre estatus de asuntos jurídicos, riesgos y obligaciones.

## Entradas
- **tipo_informe** (requerido): Periódico, por proyecto, por asunto
- **periodo** (requerido): Semanal, mensual
- **datos_asuntos** (requerido): Información de asuntos legales activos
- **directivos** (requerido): Destinatarios del informe

## Proceso
1. Consolidar información de asuntos legales
2. Clasificar por tipo y prioridad
3. Evaluar riesgos y exposición
4. Calcular costos acumulados
5. Identificar acciones pendientes
6. Generar resumen ejecutivo
7. Recomendar estrategias

## Salida
Informe legal ejecutivo con:
- Resumen ejecutivo
- Asuntos por tipo
- Análisis de riesgo
- Costos acumulados
- Acciones recomendadas

## Checklist
- [ ] Datos consolidados
- [ ] Clasificación realizada
- [ ] Riesgos evaluados
- [ ] Costos calculados
- [ ] Informe formateado

## Ejemplo
```markdown
# INFORME LEGAL - JUNIO 2026

## Resumen Ejecutivo
- 3 litigios activos
- 5 contratos en revisión
- 2 permisos pendientes

## Por Tipo
| Tipo | Cantidad | Riesgo |
|------|----------|--------|
| Litigios | 3 | Alto |
| Contratos | 5 | Medio |
| Permisos | 2 | Bajo |

## Riesgos Principales
1. Litigio laboral: exposición de $500K
2. Permiso ambiental: retraso de 2 meses

## Acciones
1. Priorizar resolución litigio laboral
2. Gestionar permiso ambiental
```
