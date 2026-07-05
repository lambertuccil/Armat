# Skill: generar_hashtags

## Identidad
- **Nombre**: generar_hashtags
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Baja

## Objetivo
Generar hashtags relevantes y efectivos para publicaciones de redes sociales.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| tema | string | Sí | Tema de la publicación |
| plataforma | string | Sí | Instagram, Facebook, etc. |
| cantidad | number | No | Cantidad de hashtags (default: 10) |

## Proceso
1. Identificar palabras clave del tema
2. Buscar hashtags trending
3. Seleccionar hashtags relevantes
4. Mezclar populares y nicho
5. Verificar cantidad
6. Formatear salida

## Salida
Lista de hashtags con:
- Hashtags principales (populares)
- Hashtags de nicho (específicos)
- Hashtags de ubicación
- Hashtags de marca

## Checklist
- [ ] Relevantes al tema
- [ ] Mix populares/nicho
- [ ] Ubicación incluida
- [ ] Marca incluida
- [ ] Cantidad adecuada

## Ejemplo
```
Input: generar_hashtags("departamento 1 dormitorio", "instagram", 10)

Output:
# Hashtags Instagram

## Principales
#departamentos #inmuebles #inversion

## Nicho
#1dormitorio #departamentonuevo #vendodepartamento

## Ubicación
#centenario #neuquen #patagonia

## Marca
#armat #entanyq

## Total: 10 hashtags
```