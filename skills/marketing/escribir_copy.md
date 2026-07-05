# Skill: escribir_copy

## Identidad
- **Nombre**: escribir_copy
- **Agente**: Marketing
- **Categoría**: Contenido
- **Complejidad**: Baja

## Objetivo
Escribir copy profesional y persuasivo para piezas de marketing.

## Entradas
| Parámetro | Tipo | Requerido | Descripción |
|-----------|------|-----------|-------------|
| plataforma | string | Sí | Instagram, email, web, etc. |
| tema | string | Sí | Tema del copy |
| tono | string | No | Tono (premium, cercano, urgente) |
| largo | string | No | Largo (corto, medio, largo) |

## Proceso
1. Definir plataforma y audiencia
2. Seleccionar tono
3. Escribir hook inicial
4. Desarrollar contenido
5. Agregar CTA
6. Revisar y pulir

## Salida
Copy formateado para la plataforma con:
- Hook atractivo
- Contenido relevante
- CTA claro
- Extensión adecuada

## Checklist
- [ ] Tono correcto
- [ ] Extensión adecuada
- [ ] CTA incluido
- [ ] Sin errores
- [ ] Adecuado para plataforma

## Ejemplo
```
Input: escribir_copy("instagram", "departamento 1 dormitorio", "premium")

Output:
# Copy Instagram — 1 Dormitorio (Premium)

## Opción 1 (Corto)
✨ Viví como merecés

Departamento de 1 dormitorio en ENTANYQ.
45,5 m² | USD 85.000 | Centenario

📞 299 508 9366

## Opción 2 (Medio)
🏠 Departamento de 1 dormitorio

Diseño moderno y funcional.
45,5 m² de pura comodidad.

Balcón privado. Cocheras disponibles.

📍 Centenario, Neuquén
💰 Desde USD 85.000

#ARMAT #ENTANYQ #Centenario
```