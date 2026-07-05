# Skill: generar_estado_financiero

## Identidad
- **Agente**: Finanzas
- **Nombre**: Generación de Estados Financieros
- **Versión**: 1.0

## Objetivo
Generar estados financieros consolidados de la empresa o proyecto (balance general, estado de resultados, flujo de efectivo) a partir de datos contables.

## Entradas
- **tipo_estado** (requerido): Balance, resultados, flujo de efectivo
- **periodo** (requerido): Mes, trimestre, año
- **datos_contables** (requerido): Movimientos contables del período
- **tipo_empresa** (opcional): Inmobiliaria, constructora, mixta

## Proceso
1. Clasificar cuentas por tipo (activo, pasivo, capital)
2. Calcular totales por categoría
3. Generar balance general
4. Calcular utilidad neta (resultados)
5. Proyectar flujos de efectivo
6. Verificar ecuación contable
7. Formatear reporte ejecutivo

## Salida
Estados financieros con:
- Balance general
- Estado de resultados
- Flujo de efectivo
- Notas explicativas
- Indicadores financieros básicos

## Checklist
- [ ] Cuentas clasificadas
- [ ] Totales calculados
- [ ] Ecuación contable verificada
- [ ] Estados formateados
- [ ] Notas incluidas
- [ ] Indicadores calculados

## Ejemplo
```markdown
# ESTADO FINANCIERO - Q2 2026

## Balance General
| Concepto | Monto |
|----------|-------|
| **Activo** | |
| Efectivo | $2,500,000 |
| Cuentas por cobrar | $1,800,000 |
| Inventario | $8,000,000 |
| **Total Activo** | **$12,300,000** |
| **Pasivo** | |
| Proveedores | $3,200,000 |
| Créditos | $4,500,000 |
| **Total Pasivo** | **$7,700,000** |
| **Capital** | $4,600,000 |

## Estado de Resultados
| Concepto | Monto |
|----------|-------|
| Ingresos | $5,200,000 |
| Costos | $3,100,000 |
| Utilidad bruta | $2,100,000 |
| Gastos operativos | $800,000 |
| Utilidad neta | $1,300,000 |
```
