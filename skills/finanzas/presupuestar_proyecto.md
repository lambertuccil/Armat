# Skill: presupuestar_proyecto

## Identidad
- **Agente**: Finanzas
- **Nombre**: Presupuestación de Proyecto
- **Versión**: 1.0

## Objetivo
Crear presupuestos detallados para proyectos de construcción, desglosando costos por concepto, partida y período.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **superficie** (requerido): Metros cuadrados a construir
- **tipo_vivienda** (requerido): Habitacional, comercial, mixto
- **nivel_acabado** (requerido): Básico, medio, alto, premium
- **ubicacion** (requerido): Zona geográfica
- **especificaciones** (opcional): Detalles técnicos adicionales

## Proceso
1. Definir conceptos de costo ( mano de obra, materiales, indirectos)
2. Estimar costos por m² según tipo y acabado
3. Desglosar por partida (estructura, acabados, instalaciones)
4. Agregar costos indirectos ( supervisión, seguridad, administración)
5. Incluir utilidad del contractor
6. Agregar contingency (5-10%)
7. Generar presupuesto detallado

## Salida
Presupuesto estructurado con:
- Resumen por concepto
- Desglose por partida
- Costo por m²
- Cronograma de pagos
- Contingency

## Checklist
- [ ] Conceptos definidos
- [ ] Costos por m² estimados
- [ ] Partidas desglosadas
- [ ] Indirectos incluidos
- [ ] Contingency agregado
- [ ] Presupuesto formateado

## Ejemplo
```markdown
# PRESUPUESTO - DEPARTAMENTO TIPO ENTANYQ

## Resumen
- Superficie: 120 m²
- Costo total: $1,800,000
- Costo/m²: $15,000

## Desglose por Concepto
| Concepto | Monto | % |
|----------|-------|---|
| Mano de obra | $540,000 | 30% |
| Materiales | $900,000 | 50% |
| Indirectos | $270,000 | 15% |
| Contingency | $90,000 | 5% |

## Por Partida
| Partida | Costo |
|---------|-------|
| Estructura | $360,000 |
| Mampostería | $180,000 |
| Instalaciones | $450,000 |
| Acabados | $540,000 |
| Carpintería | $270,000 |
```
