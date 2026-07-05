# Skill: redactar_contrato

## Identidad
- **Agente**: Legal
- **Nombre**: Redacción de Contratos
- **Versión**: 1.0

## Objetivo
Redactar borradores de contratos inmobiliarios (compraventa, servicios, arrendamiento) siguiendo la legislación mexicana vigente.

## Entradas
- **tipo_contrato** (requerido): Compraventa, servicios, arrendamiento, laboral
- **partes** (requerido): Nombres y datos de las partes
- **objeto** (requerido): Descripción del objeto del contrato
- **condiciones** (requerido): Términos y condiciones específicas
- **monto** (opcional): Valor económico del contrato
- **duracion** (opcional): Vigencia del contrato

## Proceso
1. Identificar tipo de contrato y legislación aplicable
2. Definir cláusulas esenciales
3. Redactar objeto del contrato
4. Establecer obligaciones de cada parte
5. Definir condiciones de pago y entrega
6. Incluir cláusulas de resolución
7. Agregar disposiciones generales
8. Revisar conformidad legal

## Salida
Borrador de contrato con:
- Encabezado con datos de las partes
- Objeto del contrato
- Cláusulas numeradas
- Condiciones económicas
- Firma de las partes

## Checklist
- [ ] Tipo de contrato definido
- [ ] Partes identificadas
- [ ] Objeto descrito
- [ ] Cláusulas redactadas
- [ ] Condiciones establecidas
- [ ] Legislación verificada
- [ ] Borrador formateado

## Ejemplo
```markdown
# CONTRATO DE COMPRAVENTA DE INMUEBLE

**Contrato No.**: ARMAT-2026-001

**ENTRE**:
ARMAT Desarrolladora Inmobiliaria S.A. de C.V.
RFC: ARM260101XYZ
(Denominada "EL VENDEDOR")

**Y**:
Juan Pérez López
RFC: PEPL850101ABC
(Denominado "EL COMPRADOR")

## CLÁUSULAS

### PRIMERA - OBJETO
EL VENDEDOR se obliga a vender y EL COMPRADOR a comprar el inmueble descrito como Departamento 301, Edificio A, Proyecto ENTANYQ.

### SEGUNDA - PRECIO
El precio de venta es de $1,800,000.00 (Un Millón Ochocientos Mil Pesos 00/100 M.N.)

### TERCERA - FORMA DE PAGO
- Enganche: $180,000 (10%) al firmar
- 12 mensualidades de $135,000
- Crédito hipotecario: $450,000
```
