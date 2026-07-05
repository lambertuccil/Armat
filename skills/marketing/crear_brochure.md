# Skill: crear_brochure

## Identidad
- **Nombre**: crear_brochure
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Alta

## Objetivo
Crear un brochure HTML profesional y elegante para una propiedad de ARMAT.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| propiedad | string | Sí | Nombre de la propiedad |
| formato | string | No | Formato (whatsapp, print, ambos) |
| paginas | array | No | Páginas a incluir |

## Proceso
1. Recopilar información de la propiedad
2. Seleccionar renders/fotos
3. Definir estructura de páginas
4. Crear HTML con CSS inline
5. Aplicar reglas de marca
6. Optimizar para formato
7. Revisar calidad

## Salida
Archivo HTML single-file con:
- CSS inline (Google Fonts CDN)
- Páginas: Portada, Unidades, Estado, Contacto
- Paleta ARMAT
- Disclaimer incluido
- Responsive 750px

## Checklist
- [ ] Paleta correcta (negro + dorado)
- [ ] Tipografía correcta (Playfair + DM Sans)
- [ ] Disclaimer en renders
- [ ] USD/m² incluido
- [ ] Datos de contacto
- [ ] Responsive 750px
- [ ] Sin superposiciones
- [ ] Sin errores

## Ejemplo
```
Input: crear_brochure("ENTANYQ", "whatsapp")

Output:
Archivo: brochure-entanyq.html
- Portada con render fachada
- Unidades con renders interiores
- Estado con fotos reales
- Contacto
- CSS inline, 750px, disclaimer
```