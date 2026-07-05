# Skill: registrar_lead

## Identidad
- **Agente**: Clientes
- **Nombre**: Registro de Leads
- **Versión**: 1.0

## Objetivo
Capturar y clasificar nuevos prospectos de clientes interesados en proyectos inmobiliarios.

## Entradas
- **nombre** (requerido): Nombre del prospecto
- **contacto** (requerido): Teléfono, email
- **fuente** (requerido): Referencia, redes, portal, visita
- **interes** (requerido): Proyecto, tipo de unidad
- **presupuesto** (opcional): Rango de inversión

## Proceso
1. Capturar datos de contacto
2. Identificar fuente del lead
3. Registrar interés específico
4. Clasificar por prioridad
5. Asignar vendedor
6. Programar seguimiento
7. Registrar en CRM

## Salida
Ficha de lead con:
- Datos personales
- Fuente del lead
- Interés registrado
- Prioridad asignada
- Vendedor asignado

## Checklist
- [ ] Datos capturados
- [ ] Fuente identificada
- [ ] Interés registrado
- [ ] Prioridad asignada
- [ ] CRM actualizado

## Ejemplo
```markdown
# LEAD #2026-089

## Datos
- Nombre: Juan Carlos Pérez
- Tel: (55) 9876-5432
- Email: jc@email.com

## Interés
- Proyecto: ENTANYQ
- Tipo: 2 habitaciones
- Presupuesto: $1.4M - $1.6M

## Seguimiento
- Fuente: Instagram
- Prioridad: Alta
- Vendedor: Ana García
- Próximo contacto: 5 julio
```
