# Skill: crear_presupuesto_obra

## Identidad
- **Agente**: Presupuestos
- **Nombre**: Creación de Presupuesto de Obra
- **Versión**: 1.0

## Objetivo
Crear presupuestos detallados para proyectos de construcción, desglosando costos por partida.

## Entradas
- **proyecto** (requerido): Nombre del proyecto
- **superficie** (requerido): Metros cuadrados
- **tipo_obra** (requerido): Residencial, comercial
- **nivel_acabado** (requerido): Básico, medio, alto
- **especificaciones** (requerido): Detalles técnicos

## Proceso
1. Definir partidas de costo
2. Estimar cantidades por partida
3. Preciar unitariamente
4. Calcular costos directos
5. Agregar indirectos
6. Incluir utilidad y contingency
7. Generar presupuesto detallado

## Salida
Presupuesto con:
- Resumen por categorías
- Desglose por partida
- Costo total
- Costo por m²

## Checklist
- [ ] Partidas definidas
- [ ] Cantidades estimadas
- [ ] Precios asignados
- [ ] Costos calculados
- [ ] Presupuesto formateado

## Ejemplo
```markdown
# PRESUPUESTO - DEPARTAMENTO 120 m² ENTANYQ

## Resumen
| Categoría | Monto | % |
|-----------|-------|---|
| Estructura | $360,000 | 20% |
| Mampostería | $180,000 | 10% |
| Instalaciones | $450,000 | 25% |
| Acabados | $540,000 | 30% |
| Carpintería | $270,000 | 15% |

## Total: $1,800,000
## Costo/m²: $15,000
```
