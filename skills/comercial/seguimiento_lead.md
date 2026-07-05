# Skill: seguimiento_lead

## Identidad
- **Nombre**: seguimiento_lead
- **Agente**: Comercial
- **Categoría**: CRM
- **Complejidad**: Baja

## Objetivo
Generar mensaje de seguimiento personalizado para un lead que no respondió.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| cliente | string | Sí | Nombre del cliente |
| dias | number | Sí | Días desde última interacción |
| motivo | string | No | Motivo de la consulta original |

## Proceso
1. Evaluar días de espera
2. Seleccionar tono apropiado
3. Generar mensaje personalizado
4. Incluir CTA claro
5. Formatear para el canal (email/WhatsApp)

## Salida
Mensaje de seguimiento con:
- Saludo personalizado
- Referencia a consulta anterior
- Oferta de ayuda
- CTA claro

## Checklist
- [ ] Tono apropiado
- [ ] Personalizado
- [ ] CTA claro
- [ ] No es invasivo
- [ ] Profesional

## Ejemplo
```
Input: seguimiento_lead("Carlos", 5, "consulta por 1 dorm")

Output:
Hola Carlos, ¿cómo estás?

Te escribo para hacer seguimiento de tu consulta sobre el departamento de 1 dormitorio en ENTANYQ.

Si todavía estás interesado, me encantaría poder ayudarte con más información.

¿Tenés 10 minutos para que te cuente?

Saludos,
ARMAT | 299 508 9366
```