# Skill: responder_objecion

## Identidad
- **Nombre**: responder_objecion
- **Agente**: Comercial
- **Categoría**: Ventas
- **Complejidad**: Media

## Objetivo
Generar respuesta profesional y persuasiva a objeciones comunes de clientes.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| objecion | string | Sí | Tipo de objeción (precio, ubicación, etc.) |
| cliente | string | No | Nombre del cliente |
| unidad | string | No | Unidad en consulta |

## Proceso
1. Identificar tipo de objeción
2. Seleccionar argumentos relevantes
3. Generar respuesta con datos
4. Incluir alternativas
5. Proponer próximo paso

## Salida
Respuesta estructurada con:
- Validación de la preocupación
- Argumentos con datos
- Alternativas
- Próximo paso

## Checklist
- [ ] Objeción identificada
- [ ] Argumentos con datos reales
- [ ] Tono respetuoso
- [ ] Alternativas incluidas
- [ ] CTA claro

## Ejemplo
```
Input: responder_objecion("precio", "1 dorm")

Output:
Entiendo tu preocupación por el precio.

Comparado con departamentos similares:
- Mercado zona: USD 2.000-2.200/m²
- ENTANYQ: USD 1.868/m²
- **Ahorro**: 7-15%

Además, con el crecimiento de Centenario (Vaca Muerta), puede valorizarse 15% en 2 años.

¿Te gustaría que te muestre el análisis financiero?
```