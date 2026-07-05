# Skill: cotizar_propiedad

## Identidad
- **Nombre**: cotizar_propiedad
- **Agente**: Comercial
- **Categoría**: Ventas
- **Complejidad**: Baja

## Objetivo
Generar una cotización precisa y profesional para una propiedad específica de ARMAT.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| unidad | string | Sí | Tipo de unidad (1 dorm, monoambiente, etc.) |
| cliente | string | No | Nombre del cliente |
| formato | string | No | Formato de salida (simple, completo) |

## Proceso
1. Validar unidad contra tabla oficial
2. Obtener precio y características
3. Calcular USD/m²
4. Determinar opciones de pago
5. Generar cotización en formato solicitado

## Salida
Cotización formateada con:
- Tipo de unidad
- Superficie (m²)
- Precio contado
- USD/m²
- Opciones de financiamiento
- Disclaimer

## Checklist
- [ ] Unidad existe en tabla oficial
- [ ] Precio correcto
- [ ] USD/m² calculado correctamente
- [ ] Opciones de pago incluidas
- [ ] Disclaimer presente

## Ejemplo
```
Input: cotizar_propiedad("1 dorm", "Juan Pérez")

Output:
Cotización para Juan Pérez — 1 Dormitorio ENTANYQ

• Superficie: 45,5 m²
• Precio: USD 85.000
• USD/m²: USD 1.868
• Contado: USD 85.000
• Financiado: Seña USD 45.000 + 12 cuotas USD 3.750

Disclaimer: Renders ilustrativos.
```