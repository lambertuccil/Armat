# Skill: crear_contenido_redes

## Identidad
- **Nombre**: crear_contenido_redes
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Media

## Objetivo
Crear contenido completo para publicación en redes sociales (Instagram, Facebook).

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| plataforma | string | Sí | Instagram, Facebook, etc. |
| tema | string | Sí | Tema del contenido |
| cantidad | number | No | Cantidad de publicaciones (default: 1) |

## Proceso
1. Definir calendario de publicación
2. Crear concepto visual
3. Escribir copy para cada post
4. Seleccionar imágenes
5. Definir hashtags
6. Programar publicación

## Salida
Paquete de contenido con:
- Imágenes/diseños
- Copy para cada publicación
- Hashtags
- Horarios recomendados

## Checklist
- [ ] Calendario definido
- [ ] Concepto claro
- [ ] Copy atractivo
- [ ] Imágenes seleccionadas
- [ ] Hashtags relevantes
- [ ] Horarios óptimos

## Ejemplo
```
Input: crear_contenido_redes("instagram", "ENTANYQ", 3)

Output:
# Calendario Instagram — ENTANYQ

## Lunes
- Tema: Fachada del edificio
- Copy: "Diseñado para el futuro..."
- Hashtags: #ARMAT #ENTANYQ #Centenario

## Miércoles
- Tema: Interior 1 dormitorio
- Copy: "45,5 m² de pura comodidad..."
- Hashtags: #Departamentos #Neuquén

## Viernes
- Tema: Avance de obra
- Copy: "Obra al 50%..."
- Hashtags: #ObraGris #Construcción
```