# Skill: seguir_cliente

## Identidad
- **Agente**: Clientes
- **Nombre**: Seguimiento de Cliente
- **Versión**: 1.0

## Objetivo
Dar seguimiento oportuno a clientes en proceso de venta, manteniendo el interés y avanzando en el funnel.

## Entradas
- **cliente** (requerido): Nombre del cliente
- **etapa** (requerido): Prospecto, interesado, negociación, cierre
- **accion_anterior** (requerido): Última interacción
- **proximo_paso** (requerido): Acción a realizar

## Proceso
1. Revisar historial del cliente
2. Verificar último contacto
3. Preparar mensaje personalizado
4. Ejecutar seguimiento
5. Registrar interacción
6. Actualizar etapa del funnel
7. Programar próximo contacto

## Salida
Registro de seguimiento con:
- Fecha de contacto
- Mensaje enviado
- Respuesta del cliente
- Nueva etapa
- Próxima acción

## Checklist
- [ ] Historial revisado
- [ ] Contacto realizado
- [ ] Interacción registrada
- [ ] Etapa actualizada
- [ ] Próximo paso programado

## Ejemplo
```markdown
# SEGUIMIENTO - JUAN CARLOS PÉREZ

## 4 julio 2026
- Acción: Llamada telefónica
- Motivo: Enviar información departamento 2 hab
- Respuesta: Interesado, pide visita
- Etapa: Interesado → Visitado
- Próxima: Agendar visita sábado 6 julio
```
