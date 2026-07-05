# Skill: disenar_estructura_brochure

## Identidad
- **Nombre**: disenar_estructura_brochure
- **Agente**: Marketing
- **Categoría**: Diseño
- **Complejidad**: Media

## Objetivo
Diseñar la estructura y layout de un brochure antes de implementarlo en código.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| propiedad | string | Sí | Propiedad a presentar |
| paginas | number | No | Cantidad de páginas (default: 4) |
| objetivo | string | No | Objetivo (vender, informar) |

## Proceso
1. Definir cantidad de páginas
2. Diseñar wireframe de cada página
3. Definir jerarquía de información
4. Seleccionar tipo de contenido por página
5. Definir flujo de lectura
6. Documentar estructura

## Salida
Documentación de estructura con:
- Wireframe por página
- Contenido de cada página
- Jerarquía de información
- Flujo de lectura

## Checklist
- [ ] Páginas definidas
- [ ] Wireframe claro
- [ ] Jerarquía establecida
- [ ] Flujo lógico
- [ ] Contenido completo

## Ejemplo
```
Input: disenar_estructura_brochure("ENTANYQ", 4)

Output:
# Estructura Brochure ENTANYQ

## Página 1: Portada
- Render fachada (fondo)
- Logo ARMAT
- Título: ENTANYQ
- Dato clave: Desde USD 60.000

## Página 2: Unidades
- Renders interiores (2 columnas)
- 1 dormitorio: specs + precio
- Monoambiente: specs + precio
- Cocheras

## Página 3: Estado de Obra
- Fotos reales (grandes)
- Avance: 50%
- Próximos pasos

## Página 4: Contacto
- Datos de contacto
- Ubicación
- CTA
```