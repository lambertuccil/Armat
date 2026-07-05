# Skill: escribir_email

## Identidad
- **Nombre**: escribir_email
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Baja

## Objetivo
Escribir emails profesionales para diferentes propósitos (marketing, seguimiento, transaccional).

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| tipo | string | Sí | marketing, seguimiento, transaccional |
| asunto | string | Sí | Asunto del email |
| contenido | string | Sí | Contenido principal |
| cta | string | No | Llamado a la acción |

## Proceso
1. Definir tipo y objetivo
2. Estructurar contenido
3. Escribir asunto atractivo
4. Desarrollar cuerpo del email
5. Agregar CTA
6. Incluir footer

## Salida
Email completo con:
- Asunto
- Cuerpo estructurado
- CTA
- Footer con contacto

## Checklist
- [ ] Asunto atractivo
- [ ] Contenido claro
- [ ] CTA incluido
- [ ] Footer presente
- [ ] Tono adecuado

## Ejemplo
```
Input: escribir_email("seguimiento", "Tu consulta ENTANYQ", "Gracias por tu interés...")

Output:
**Asunto**: Tu consulta sobre ENTANYQ

Hola,

Gracias por tu interés en nuestros departamentos.

¿Tenés alguna consulta que pueda resolver?

¿Querés que te llamemos?

Saludos,
ARMAT
299 508 9366
```