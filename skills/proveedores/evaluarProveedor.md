# Skill: evaluarProveedor

## Identidad
- **Agente**: Proveedores
- **Nombre**: Evaluación de Proveedor
- **Versión**: 1.0

## Objetivo
Evaluar el desempeño de proveedores para mantener una base de datos de proveedores confiables.

## Entradas
- **proveedor** (requerido): Proveedor a evaluar
- **criterios** (requerido): Calidad, precio, tiempo, servicio
- **periodo** (requerido): Período de evaluación

## Proceso
1. Recopilar datos de desempeño
2. Calificar cada criterio
3. Calcular promedio ponderado
4. Generar clasificación
5. Actualizar historial
6. Tomar decisiones

## Salida
Reporte de evaluación con:
- Calificación por criterio
- Calificación global
- Clasificación (A, B, C, D)
- Recomendaciones

## Checklist
- [ ] Datos recopilados
- [ ] Criterios calificados
- [ ] Promedio calculado
- [ ] Clasificación asignada
- [ ] Historial actualizado

## Ejemplo
```markdown
# EVALUACIÓN - CONCRETO DEL NORTE

## Criterios
| Criterio | Peso | Calificación |
|----------|------|--------------|
| Calidad | 30% | 9/10 |
| Precio | 25% | 7/10 |
| Tiempo | 25% | 8/10 |
| Servicio | 20% | 8/10 |

## Global: 8.1/10
## Clasificación: A (Estratégico)

## Recomendación: Mantener relación
```
