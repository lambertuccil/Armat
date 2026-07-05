# Skill: emitir_garantia

## Identidad
- **Agente**: Postventa
- **Nombre**: Emisión de Garantías
- **Versión**: 1.0

## Objetivo
Emitir constancias de garantía para departamentos vendidos, especificando alcance y vigencia.

## Entradas
- **cliente** (requerido): Datos del cliente
- **departamento** (requerido): Unidad vendida
- **fecha_entrega** (requerido): Fecha de entrega
- **tipo_garantia** (requerido): Estructural, hidráulica, eléctrica

## Proceso
1. Verificar entrega
2. Definir alcance de garantía
3. Calcular vigencia
4. Emitir constancia
5. Entregar al cliente
6. Archivar

## Salida
Constancia de garantía con:
- Datos del cliente
- Unidad cubierta
- Alcance de cobertura
- Vigencia
- Condiciones

## Checklist
- [ ] Entrega verificada
- [ ] Alcance definido
- [ ] Vigencia calculada
- [ ] Constancia emitida
- [ ] Cliente notificado

## Ejemplo
```markdown
# CONSTANCIA DE GARANTÍA #GAR-2026-048

## Cliente: Juan Pérez López
## Departamento: 301, Edificio A, ENTANYQ
## Entrega: 15 marzo 2026

## Cobertura
- Estructural: 5 años (hasta 2031)
- Hidráulica: 2 años (hasta 2028)
- Eléctrica: 1 año (hasta 2027)
- Acabados: 6 meses (hasta sept 2026)

## Condiciones
- Uso adecuado del inmueble
- Mantenimiento preventivo
- No cubre daños por mal uso
```
