# Skill: generar_propuesta_venta

## Identidad
- **Nombre**: generar_propuesta_venta
- **Agente**: Comercial
- **Categoría**: Ventas
- **Complejidad**: Media

## Objetivo
Generar una propuesta de venta completa y profesional para un cliente potencial.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| unidad | string | Sí | Tipo de unidad |
| cliente | string | Sí | Nombre del cliente |
| email | string | No | Email del cliente |
| necesidades | string | No | Necesidades específicas |

## Proceso
1. Validar unidad y disponibilidad
2. Recopilar información del cliente
3. Generar propuesta con estructura completa
4. Incluir pricing, zona, beneficios
5. Agregar próximos pasos
6. Revisar calidad

## Salida
Propuesta completa en formato markdown con:
1. Encabezado con datos del cliente
2. Unidad seleccionada
3. Precio y opciones de pago
4. Beneficios de la zona
5. Próximos pasos
6. Contacto
7. Disclaimer

## Checklist
- [ ] Unidad verificada
- [ ] Precios correctos
- [ ] USD/m² incluido
- [ ] Estructura completa
- [ ] Disclaimer presente
- [ ] Datos de contacto

## Ejemplo
```
Input: generar_propuesta_venta("1 dorm", "María López")

Output:
# Propuesta de Venta — ENTANYQ

**Para**: María López
**Fecha**: 04/07/2026

## Unidad: 1 Dormitorio
- 45,5 m² cubiertos + 5,95 m² balcón
- Planta 2° contrafrente

## Precio
- Contado: USD 85.000 (USD 1.868/m²)
- Financiado: Seña 45K + 12 cuotas 3.750

## Beneficios
- Centenario: zona en crecimiento
- Acceso Ruta 22
- Cerca de comercios

## Próximos Pasos
1. Reserva: Señar USD 5.000
2. Firma: Contrato definitivo

ARMAT | 299 508 9366
```