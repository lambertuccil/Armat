# Skill: crear_email_marketing

## Identidad
- **Nombre**: crear_email_marketing
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Media

## Objetivo
Crear un email de marketing profesional y responsive para clientes.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| tipo | string | Sí | Tipo (bienvenida, seguimiento, promoción) |
| cliente | string | No | Nombre del cliente |
| contenido | string | No | Contenido específico |

## Proceso
1. Definir tipo de email
2. Seleccionar template
3. Personalizar contenido
4. Aplicar estilos ARMAT
5. Asegurar responsive
6. Revisar calidad

## Salida
Email HTML con:
- Header con logo ARMAT
- Contenido personalizado
- CTA claro
- Footer con contacto
- Responsive

## Checklist
- [ ] Ancho máximo 600px
- [ ] Responsive
- [ ] Logo ARMAT
- [ ] CTA incluido
- [ ] Contacto visible
- [ ] Tono profesional

## Ejemplo
```
Input: crear_email_marketing("bienvenida", "María")

Output:
# Email Bienvenida — María

**Asunto**: ¡Bienvenido a ARMAT!

**Contenido**:
- Saludo personalizado
- Presentación de proyectos
- CTA: Ver propiedades
- Footer: Contacto

**HTML**: Template responsive con paleta ARMAT
```