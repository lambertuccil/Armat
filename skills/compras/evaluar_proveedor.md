# Skill: evaluar_proveedor

## Identidad
- **Agente**: Compras
- **Nombre**: Evaluación de Proveedor
- **Versión**: 1.0

## Objetivo
Evaluar el desempeño de proveedores basado en calidad, precio, tiempo de entrega y servicio.

## Entradas
- **proveedor** (requerido): Nombre del proveedor
- **proyecto** (requerido): Proyecto en que participó
- **criterios** (requerido): Calidad, precio, tiempo, servicio
- **evidencia** (requerido): Datos objetivos de desempeño

## Proceso
1. Recopilar datos de desempeño
2. Calificar cada criterio
3. Calificar ponderación
4. Generar calificación global
5. Actualizar historial del proveedor
6. Identificar áreas de mejora
7. Tomar decisiones de continuidad

## Salida
Evaluación de proveedor con:
- Calificación por criterio
- Calificación global
- Fortalezas y debilidades
- Recomendación

## Checklist
- [ ] Datos recopilados
- [ ] Calificaciones asignadas
- [ ] Calificación global calculada
- [ ] Recomendación documentada

## Ejemplo
```markdown
# EVALUACIÓN - DISTRIBUIDORA TÉCNICA

## Calificaciones
| Criterio | Peso | Calificación |
|----------|------|--------------|
| Calidad | 30% | 9/10 |
| Precio | 25% | 8/10 |
| Tiempo | 25% | 7/10 |
| Servicio | 20% | 8/10 |

## Global: 8.1/10

## Recomendación
Mantener como proveedor estratégico.
```
