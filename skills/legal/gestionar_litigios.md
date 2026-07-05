# Skill: gestionar_litigios

## Identidad
- **Agente**: Legal
- **Nombre**: Gestión de Litigios
- **Versión**: 1.0

## Objetivo
Gestionar y dar seguimiento a litigios legales de la empresa, incluyendo demandas, amparos y controversias contractuales.

## Entradas
- **tipo_litigio** (requerido): Civil, laboral, administrativo, mercantil
- **partes** (requerido): Demandante y demandado
- **juzgado** (requerido): Autoridad jurisdiccional
- **fecha_inicio** (requerido): Inicio del litigio
- **cuantia** (opcional): Valor económico del litigio

## Proceso
1. Registrar datos del litigio
2. Identificar plazos procesales
3. Calcular probabilidades de éxito
4. Estimar costos legales
5. Generar timeline del proceso
6. Recomendar estrategia
7. Dar seguimiento a audiencias

## Salida
Reporte de litigio con:
- Ficha técnica del caso
- Timeline procesal
- Estimación de costos
- Probabilidades de éxito
- Estrategia recomendada

## Checklist
- [ ] Litigio registrado
- [ ] Plazos identificados
- [ ] Probabilidades estimadas
- [ ] Costos calculados
- [ ] Estrategia definida

## Ejemplo
```markdown
# LITIGIO - RECARGOS INDEBIDOS
**Tipo**: Administrativo
**Juzgado**: TFJFA
**Cuantia**: $150,000

## Ficha Técnica
- Demandante: ARMAT
- Demandado: SAT
- Inicio: Marzo 2026
- Audiencia: Septiembre 2026

## Probabilidad Éxito
- Alta (75%) - Jurisprudencia favorable

## Costos Estimados
- Abogado: $50,000
- Peritajes: $20,000
- Total: $70,000
```
