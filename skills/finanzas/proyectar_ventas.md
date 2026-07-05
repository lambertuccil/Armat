# Skill: proyectar_ventas

## Identidad
- **Agente**: Finanzas
- **Nombre**: Proyección de Ventas
- **Versión**: 1.0

## Objetivo
Proyectar ventas de un desarrollo inmobiliario por período, tipo de unidad y canal de venta.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **unidades_totales** (requerido): Total de unidades a vender
- **precio_promedio** (requerido): Precio por unidad
- **velocidad_venta** (requerido): Unidades esperadas por mes
- **mix_unidades** (opcional): Distribución por tipo

## Proceso
1. Definir tipos de unidades y precios
2. Estimar velocidad de ventas por canal
3. Proyectar ventas mensuales
4. Calcular flujo de ingresos
5. Identificar meses pico y valle
6. Estimar ingresos totales por período
7. Generar cronograma de cobros

## Salida
Proyección de ventas con:
- Cronograma de ventas mensuales
- Ingresos proyectados
- Distribución por tipo
- Flujo de caja esperado

## Checklist
- [ ] Unidades definidas
- [ ] Precios establecidos
- [ ] Velocidad estimada
- [ ] Proyección mensual generada
- [ ] Ingresos calculados

## Ejemplo
```markdown
# PROYECCIÓN DE VENTAS - ENTANYQ

## Unidades
- 1 habitación: 20 unidades a $950,000
- 2 habitación: 15 unidades a $1,400,000
- 3 habitación: 10 unidades a $1,800,000

## Proyección Mensual
| Mes | 1 Hab | 2 Hab | 3 Hab | Ingresos |
|-----|-------|-------|-------|----------|
| Jul | 3 | 2 | 1 | $4,750K |
| Ago | 4 | 3 | 2 | $7,150K |
| Sep | 3 | 2 | 1 | $4,750K |

## Total Esperado
- Ingresos: $38,000,000
- Plazo: 8 meses
```
