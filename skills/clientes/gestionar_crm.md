# Skill: gestionar_crm

## Identidad
- **Agente**: Clientes
- **Nombre**: Gestión de CRM
- **Versión**: 1.0

## Objetivo
Administrar el sistema CRM, manteniendo información actualizada y generando reportes de pipeline.

## Entradas
- **accion** (requerido): Agregar, actualizar, consultar, reportar
- **filtro** (requerido): Por vendedor, etapa, proyecto, período
- **datos** (requerido): Información del cliente o movimiento

## Proceso
1. Capturar nuevos leads
2. Actualizar información de contacto
3. Registrar interacciones
4. Mover entre etapas del funnel
5. Generar reportes de pipeline
6. Analizar métricas de conversión
7. Identificar oportunidades

## Salida
Dashboard de CRM con:
- Leads por etapa
- Tasa de conversión
- Pipeline por vendedor
- Proyección de ventas

## Checklist
- [ ] Leads registrados
- [ ] Información actualizada
- [ ] Interacciones capturadas
- [ ] Reportes generados

## Ejemplo
```markdown
# PIPELINE - JULIO 2026

## Por Etapa
| Etapa | Leads | Valor |
|-------|-------|-------|
| Prospecto | 45 | $63M |
| Interesado | 28 | $39M |
| Negociación | 12 | $17M |
| Cierre | 5 | $7M |

## Conversión
- Prospecto → Interesado: 62%
- Interesado → Negociación: 43%
- Negociación → Cierre: 42%
```
