# Skill: seleccionar_renders

## Identidad
- **Nombre**: seleccionar_renders
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Baja

## Objetivo
Seleccionar los renders y fotos más adecuados para una pieza de marketing.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| pieza | string | Sí | Tipo de pieza (brochure, flyer, etc.) |
| objetivo | string | Sí | Objetivo (vender, informar, etc.) |
| propiedad | string | No | Propiedad específica |

## Proceso
1. Analizar objetivo de la pieza
2. Revisar renders disponibles
3. Seleccionar por relevancia
4. Verificar calidad
5. Preparar para uso

## Salida
Lista de renders seleccionados con:
- Archivo
- Descripción
- Uso recomendado
- Alternativas

## Checklist
- [ ] Renders relevantes
- [ ] Calidad adecuada
- [ ] Variedad (exterior, interior)
- [ ] Alternativas incluidas

## Ejemplo
```
Input: seleccionar_renders("brochure", "vender", "ENTANYQ")

Output:
# Renders Seleccionados — ENTANYQ

## Para Portada
- AM.jpeg — Fachada frontal (impacto)

## Para Interiores
- AM (3).jpeg — 1 dormitorio living
- AM (6).jpeg — Monoambiente

## Para Baño
- AM (8).jpeg — Baño con mosaico

## Para Estado (fotos reales)
- materialmarketing/PHOTO-*.jpg
```