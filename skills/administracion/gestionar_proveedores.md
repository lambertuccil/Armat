# Skill: gestionar_proveedores

## Identidad
- **Agente**: Administración
- **Nombre**: Gestión de Proveedores
- **Versión**: 1.0

## Objetivo
Administrar la base de datos de proveedores, evaluar desempeño y mantener relaciones comerciales favorables.

## Entradas
- **accion** (requerido): Registrar, evaluar, actualizar, eliminar
- **proveedor** (requerido): Datos del proveedor
- **categoria** (requerido): Materiales, servicios, equipos
- **calificacion** (opcional): Puntuación de desempeño

## Proceso
1. Registrar proveedor con datos completos
2. Clasificar por categoría y especialidad
3. Evaluar desempeño en proyectos anteriores
4. Mantener historial de transacciones
5. Generar reportes de evaluación
6. Identificar proveedores estratégicos
7. Negociar condiciones preferentes

## Salida
Ficha de proveedor con:
- Datos generales
- Categoría y especialidad
- Calificación de desempeño
- Historial de transacciones
- Condiciones comerciales

## Checklist
- [ ] Datos completos
- [ ] Categoría asignada
- [ ] Calificación realizada
- [ ] Historial actualizado
- [ ] Condiciones documentadas

## Ejemplo
```markdown
# PROVEEDOR: Concreto del Norte S.A.

## Datos
- RFC: CDN850101ABC
- Contacto: Ing. Roberto Méndez
- Tel: (55) 1234-5678

## Categoría
- Materiales → Concreto premezclado

## Calificación
- Calidad: 9/10
- Puntualidad: 8/10
- Precio: 7/10
- **Global: 8/10**

## Condiciones
- Pago: 30 días
- Minimo: 10 m³
- Descuento: 5% por volumen
```
