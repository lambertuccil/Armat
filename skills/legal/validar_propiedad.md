# Skill: validar_propiedad

## Identidad
- **Agente**: Legal
- **Nombre**: Validación de Propiedad
- **Versión**: 1.0

## Objetivo
Validar la situación legal de un inmueble antes de adquisición, verificando propiedad, gravámenes, y libertad de cargo.

## Entradas
- **direccion** (requerido): Dirección del inmueble
- **propietario_actual** (requerido): Nombre del propietario actual
- **folio_real** (opcional): Número de folio real
- **tipo_operacion** (requerido): Compraventa, adjudicación, donación

## Proceso
1. Solicitar certificado de libertad de gravamen
2. Verificar registro de propiedad
3. Buscar juicios pendientes
4. Verificar avalúo catastral
5. Confirmar estatus de impuestos
6. Validar identidad del propietario
7. Generar reporte de titulación

## Salida
Reporte de validación con:
- Estatus de propiedad
- Gravámenes encontrados
- Juicios pendientes
- Impuestos al corriente
- Recomendación

## Checklist
- [ ] Dirección verificada
- [ ] Propietario identificado
- [ ] Gravámenes consultados
- [ ] Juicios verificados
- [ ] Impuestos revisados
- [ ] Reporte generado

## Ejemplo
```markdown
# VALIDACIÓN DE PROPIEDAD - DEPTO 301 ENTANYQ

## Inmueble
- Dirección: Av. Insurgentes Sur 1234, Depto 301
- Propietario: Desarrolladora ARMAT S.A. de C.V.

## Resultados
| Concepto | Estatus |
|----------|---------|
| Libertad de gravamen | ✅ Libre |
| Juicios pendientes | ✅ Ninguno |
| Impuestos predial | ✅ Al corriente |
| Avalúo catastral | $1,800,000 |

## Recomendación
Propiedad apta para transacción.
```
