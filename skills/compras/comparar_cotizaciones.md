# Skill: comparar_cotizaciones

## Identidad
- **Agente**: Compras
- **Nombre**: Comparación de Cotizaciones
- **Versión**: 1.0

## Objetivo
Comparar cotizaciones de diferentes proveedores para seleccionar la opción más conveniente.

## Entradas
- **cotizaciones** (requerido): Lista de cotizaciones recibidas
- **criterios** (requerido): Precio, calidad, entrega, garantía
- **presupuesto** (requerido): Límite de inversión

## Proceso
1. Recopilar todas las cotizaciones
2. Estandarizar comparables
3. Evaluar precio unitario
4. Verificar condiciones de entrega
5. Revisar garantías y terms
6. Calificar proveedores
7. Recomendar opción óptima

## Salida
Análisis comparativo con:
- Tabla comparativa
- Proveedor recomendado
- Justificación
- Ahorro estimado

## Checklist
- [ ] Cotizaciones recopiladas
- [ ] Comparativa realizada
- [ ] Proveedor seleccionado
- [ ] Justificación documentada

## Ejemplo
```markdown
# COMPARATIVA - TUBERÍA PVC 4"

| Proveedor | Precio Unitario | Total | Entrega | Garantía |
|-----------|----------------|-------|---------|----------|
| Ferretería | $85 | $17,000 | 5 días | 1 año |
| Distribuidora | $78 | $15,600 | 7 días | 6 meses |
| Norte | $82 | $16,400 | 3 días | 1 año |

## Recomendación
**Distribuidora Técnica** - Mejor precio, entrega aceptable.
Ahorro: $1,400 vs Ferretería
```
