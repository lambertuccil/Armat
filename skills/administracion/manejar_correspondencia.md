# Skill: manejar_correspondencia

## Identidad
- **Agente**: Administración
- **Nombre**: Manejo de Correspondencia
- **Versión**: 1.0

## Objetivo
Administrar la correspondencia entrante y saliente de la empresa, incluyendo oficios, contratos y notificaciones.

## Entradas
- **tipo** (requerido): Entrante, saliente
- **remitente** (requerido): Quien envía o recibe
- **asunto** (requerido): Tema del documento
- **urgencia** (requerido): Alta, media, baja
- **documento** (requerido): Archivo o contenido

## Proceso
1. Registrar correspondencia entrante
2. Clasificar por asunto y urgencia
3. Derivar al responsable
4. Registrar respuestas
5. Archivar documentos
6. Dar seguimiento a pendientes
7. Generar reporte de correspondencia

## Salida
Registro de correspondencia con:
- Folio de recibido/enviado
- Fecha
- Asunto
- Responsable
- Estatus

## Checklist
- [ ] Correspondencia registrada
- [ ] Clasificada correctamente
- [ ] Derivada al responsable
- [ ] Respuesta registrada
- [ ] Archivada

## Ejemplo
```markdown
# CORRESPONDENCIA - 4 JULIO 2026

## Entrante
| Folio | De | Asunto | Estatus |
|-------|-----|--------|---------|
| E-2026-145 | Hacienda | Revisión fiscal | Pendiente |
| E-2026-146 | Cliente | Reclamación | En revisión |

## Saliente
| Folio | Para | Asunto | Estatus |
|-------|------|--------|---------|
| S-2026-089 | Proveedor | Cotización | Enviado |
```
