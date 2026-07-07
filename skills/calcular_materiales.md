# Skill calcular_materiales
Cómputo de materiales para construcción — recibe plano (imagen, PDF, CAD o medidas manuales) y genera lista completa de materiales con cantidades, costos y rendimientos.

## Trigger
- "calcula materiales"
- "computo de materiales"
- "cuánto material necesito"
- "lista de materiales"
- "presupuesto de materiales"
- "material takeoff"

## Objetivo
Recibir un plano o medidas de una unidad constructiva y generar un cómputo detallado de materiales con:
1. Lista por rubro (estructura, mampostería, instalaciones, acabados)
2. Cantidades exactas con rendimientos aplicados
3. Costos estimados (USD y ARS, Neuquén)
4. Resumen ejecutivo con totales
5. Alertas de faltantes y recomendaciones

## Entradas

### Formato A: Plano imagen (JPEG, PNG)
1. Analizar visualmente el plano
2. Extraer medidas visibles
3. Confirmar medidas con el usuario
4. Calcular materiales

### Formato B: Plano PDF
1. Leer el documento
2. Extraer medidas del contenido
3. Confirmar medidas con el usuario
4. Calcular materiales

### Formato C: Plano CAD/DWG
1. Leer archivo si es posible
2. Extraer layer de medidas
3. Confirmar medidas con el usuario
4. Calcular materiales

### Formato D: Medidas manuales
1. Recibir medidas en formato libre
2. Organizar por ambiente
3. Calcular materiales

## Datos Necesarios

Para cada ambiente, necesito:

```
AMBIENTE: [nombre]
- Largo: X.XX m
- Ancho: X.XX m
- Alto: X.XX m (default: 2.60m)
- Paredes: [cuántas paredes da a exterior]
- Ventanas: [cantidad y tamaño aproximado]
- Puertas: [cantidad]
- Piso: [tipo: porcelanato/cerámica]
```

Si el usuario no provee el alto, usar 2.60m (estándar Neuquén).

## Proceso

### Paso 1: Organizar Datos
```
Por cada ambiente:
  - Calcular superficie (largo × ancho)
  - Calcular perímetro (2 × (largo + ancho))
  - Calcular superficie de paredes (perímetro × alto)
  - Restar huecos (ventanas: 1.5m² c/u, puertas: 1.8m² c/u)
  - Calcular superficie de piso
  - Calcular superficie de techo
```

### Paso 2: Aplicar Rendimientos
Usar tabla de rendimientos en `base-conocimiento/construccion/materiales-rendimientos.md`

```
Para cada material:
  cantidad_base × rendimiento × (1 + desperdicio%)
```

### Paso 3: Calcular por Rubros

**Estructura:**
- Hormigón = superficie × espesor losa
- Acero = superficie × rendimiento kg/m²
- Encofrado = superficie × rendimiento

**Mampostería:**
- Ladrillos/bloques = superficie paredes × rendimiento/m²
- Mortero = superficie × rendimiento

**Instalaciones:**
- Cableado = superficie × rendimiento m/m²
- Tuberías = superficie × rendimiento m/m²
- Accesorios = cantidad ambientes × factor

**Acabados:**
- Piso = superficie × (1 + desperdicio)
- Revestimiento muros = superficie paredes × rendimiento
- Pintura = (superficie paredes + techo) × rendimiento
- Carpintería = cantidad ambientes × factor

### Paso 4: Costos
Aplicar precios de referencia Neuquén (materiales-rendimientos.md).

### Paso 5: Generar Reporte

## Salida — Formato del Reporte

```markdown
# CÓMPUTO DE MATERIALES — ENTANYQ
**Fecha**: [fecha]
**Unidad**: [1 Dormitorio / Monoambiente]
**Superficie total**: [XX.XX] m²

---

## RESUMEN EJECUTIVO

| Rubro | Subtotal (USD) | Subtotal (ARS) |
|-------|----------------|----------------|
| Estructura | $X.XXX | $X.XXX.XXX |
| Mampostería | $X.XXX | $X.XXX.XXX |
| Instalaciones | $X.XXX | $X.XXX.XXX |
| Acabados | $X.XXX | $X.XXX.XXX |
| **TOTAL** | **$XX.XXX** | **$XX.XXX.XXX** |

**Costo por m²**: $XXX USD/m²
**Margen sugerido**: XX% → **Precio de venta**: $XX.XXX USD

---

## DETALLE POR RUBRO

### 1. ESTRUCTURA

| Material | Unidad | Cantidad | Precio Unit. | Subtotal |
|----------|--------|----------|--------------|----------|
| Hormigón f'c=210 | m³ | X.XX | $XX | $X.XXX |
| Acero varillas | kg | XXX | $X.XX | $X.XXX |
| ... | | | | |
| **Subtotal Estructura** | | | | **$X.XXX** |

### 2. MAMPOSTERÍA
[ mismo formato ]

### 3. INSTALACIONES
[ mismo formato ]

### 4. ACABADOS
[ mismo formato ]

---

## DETALLE POR AMBIENTE

### [Nombre del Ambiente] — [XX.XX] m²
- Piso: [material] — [XX.XX] m²
- Paredes: [XX.XX] m²
- Techo: [XX.XX] m²

---

## ALERTAS Y RECOMENDACIONES

- ⚠️ [Faltante o exceso detectado]
- 💡 [Recomendación de ahorro]
- 📋 [Material a cotizar con proveedor]

---

## NOTAS
- Precios de referencia Neuquén — Julio 2025
- Incluye 5-10% de desperdicio según material
- No incluye mano de obra
- No incluye permisos ni honorarios profesionales
```

## Checklist
- [ ] ¿Se recibieron todas las medidas?
- [ ] ¿Los ambientes están correctamente dimensionados?
- [ ] ¿Se aplicaron rendimientos correctos?
- [ ] ¿Se incluyó desperdicio?
- [ ] ¿Los precios son actuales?
- [ ] ¿El resumen cuadra con el detalle?
- [ ] ¿Se generaron alertas si corresponde?

## Archivos Relacionados
- `base-conocimiento/construccion/materiales-rendimientos.md` — tabla de rendimientos y precios
- `base-conocimiento/construccion/construccion.md` — etapas de obra
- `skills/hacer_presupuesto.md` — para generar presupuesto completo
- `skills/analizar_rentabilidad.md` — para analizar ROI

## Ejemplo de Invocación

```
armat-obras calcular_materiales

Plano del departamento 1 dormitorio:
- Dormitorio: 3.20m × 3.00m
- Living/Comedor: 4.50m × 3.50m
- Cocina: 3.00m × 2.50m
- Baño: 2.20m × 1.80m
- Alto paredes: 2.60m
- 2 ventanas en living (1.50m × 1.20m cada una)
- 1 puerta de entrada
- 3 puertas internas
```
