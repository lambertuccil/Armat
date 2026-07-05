# Skill: optimizar_contenido

## Identidad
- **Nombre**: optimizar_contenido
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Baja

## Objetivo
Optimizar contenido existente para diferentes plataformas y formatos.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| contenido | string | Sí | Contenido a optimizar |
| plataforma_origen | string | Sí | Plataforma original |
| plataforma_destino | string | Sí | Plataforma destino |

## Proceso
1. Analizar contenido original
2. Identificar restricciones de destino
3. Adaptar formato
4. Ajustar extensión
5. Modificar CTA si es necesario
6. Revisar calidad

## Salida
Contenido optimizado para la plataforma destino con:
- Formato adecuado
- Extensión correcta
- CTA apropiado
- Sin pérdida de mensaje

## Checklist
- [ ] Formato correcto
- [ ] Extensión adecuada
- [ ] CTA adaptado
- [ ] Mensaje intacto
- [ ] Calidad mantenida

## Ejemplo
```
Input: optimizar_contenido("Post largo Instagram", "instagram", "whatsapp")

Output:
# Optimización: Instagram → WhatsApp

**Original**: Post largo con múltiples párrafos
**Optimizado**: Mensaje conciso (máx 750px)

**Cambios**:
- Reducir texto 60%
- Eliminar hashtags
- Agregar formato de lista
- CTA más directo
```