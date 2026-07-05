# Skill: registrar_bitacora_diaria

## Identidad
- **Agente**: Obras
- **Nombre**: Registro de Bitácora Diaria
- **Versión**: 1.0

## Objetivo
Generar entradas de bitácora diaria para proyectos de construcción, documentando actividades, personal, materiales, clima, novedades y observaciones del día.

## Entradas
- **nombre_proyecto** (requerido): Nombre del proyecto
- **fecha** (requerido): Fecha de la jornada
- **actividades_realizadas** (requerido): Lista de actividades ejecutadas
- **personal_en_sitio** (opcional): Número y tipo de personal
- **materiales_ingresados** (opcional): Materiales recibidos en sitio
- **condiciones_climaticas** (opcional): Estado del tiempo
- **novedades** (opcional): Incidentes, paradas, problemas
- **fotos** (opcional): Referencias fotográficas

## Proceso
1. Registrar fecha, proyecto y turno
2. Listar actividades por especialidad (albañilería, plomería, electricidad, etc.)
3. Documentar personal:数量, tipo, horas
4. Registrar materiales: tipo, cantidad, estado
5. Anotar condiciones climáticas
6. Documentar novedades y observaciones
7. Registrar pendientes para día siguiente

## Salida
Documento de bitácora estructurado en formato Markdown con:
- Encabezado del proyecto y fecha
- Secciones por categoría
- Firma de supervisión

## Checklist
- [ ] Fecha correcta
- [ ] Proyecto identificado
- [ ] Actividades documentadas
- [ ] Personal registrado
- [ ] Materiales anotados
- [ ] Clima registrado
- [ ] Novedades incluidas

## Ejemplo
```markdown
# BITÁCORA DIARIA - PROYECTO ENTANYQ
**Fecha**: 4 de julio, 2026
**Supervisor**: Ing. Carlos Méndez

## Actividades
- Avance en muros piso 3: 60%
- Instalación hidráulica departamento 301
- Colocación de contrapiso nivel 2

## Personal
- 8 albañiles
- 2 plomeros
- 1 electricista

## Materiales
- 15 m³ de concreto
- 200 blocks

## Clima
- Parcial nublado, 28°C

## Pendientes
- Terminar muros 301-304
- Revisar instalación eléctrica nivel 2
```
