# Skill: controlar_inventario

## Identidad
- **Agente**: Administración
- **Nombre**: Control de Inventario
- **Versión**: 1.0

## Objetivo
Mantener inventario actualizado de materiales, herramientas y equipos en almacén y sitios de construcción.

## Entradas
- **accion** (requerido): Entrada, salida, ajuste, inventario físico
- **articulo** (requerido): Descripción del artículo
- **cantidad** (requerido): Cantidad a registrar
- **ubicacion** (requerido): Almacén o sitio de obra
- **referencia** (opcional): Orden de compra o folio

## Proceso
1. Registrar movimientos de entrada
2. Registrar movimientos de salida
3. Actualizar existencias
4. Realizar inventarios físicos
5. Ajustar diferencias
6. Generar reportes de stock
7. Alertar mínimos y máximos

## Salida
Reporte de inventario con:
- Existencias por artículo
- Valor del inventario
- Movimientos del período
- Artículos bajo mínimo

## Checklist
- [ ] Movimientos registrados
- [ ] Existencias actualizadas
- [ ] Inventario físico realizado
- [ ] Diferencias ajustadas
- [ ] Reporte generado

## Ejemplo
```markdown
# INVENTARIO - ALMACÉN CENTRAL

## Existencias
| Artículo | Mín | Actual | Máx | Estado |
|----------|-----|--------|-----|--------|
| Blocks | 1,000 | 2,500 | 5,000 | OK |
| Cemento | 50 | 30 | 100 | Bajo |
| Arena | 20 | 25 | 50 | OK |

## Movimientos Junio
- Entradas: 45
- Salidas: 38
- Ajustes: 2

## Alertas
- Cemento por debajo del mínimo
```
