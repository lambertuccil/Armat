# Ejemplos Obras — ConstructoraAI

## Ejemplo 1: Reporte de Avance Semanal

### Input del Usuario:
"¿Cómo va la obra de ENTANYQ?"

### Análisis:
- **Tipo**: Consulta de avance
- **Proyecto**: ENTANYQ
- **Formato**: Reporte semanal

### Output:
```
# Reporte de Obra — ENTANYQ
**Fecha**: 04/07/2026
**Semana**: 24

## Resumen Ejecutivo
- Avance general: **50%**
- Estado: **Obra gris — Estructura y mampostería completas**

## Detalle por Etapa
| Etapa | Estado | % | Notas |
|-------|--------|---|-------|
| Estructura | ✅ Completa | 100% | Sin observaciones |
| Mampostería | ✅ Completa | 100% | Lista para instalaciones |
| Instalaciones | 🔄 Pendiente | 0% | Próxima etapa |
| Acabados | ⏳ Pendiente | 0% | Esperando instalaciones |

## Próximos Pasos (Semana 25)
1. Iniciar instalación de losa radiante
2. Coordinar proveedor de tuberías
3. Preparar cableado eléctrico

## Observaciones
- Estructura verificada, cumple especificaciones
- Mampostería sin fisuras, good quality
- Material almacenado correctamente

## Fotos
- [Foto 1]: Vista general del edificio
- [Foto 2]: Detalle de mampostería
```

---

## Ejemplo 2: Cálculo de Materiales

### Input del Usuario:
"¿Cuánto cable eléctrico necesito para el piso 1?"

### Análisis:
- **Tipo**: Cálculo de materiales
- **Proyecto**: ENTANYQ
- **Piso**: 1
- **Material**: Cable eléctrico

### Output:
```
# Cables Eléctricos — Piso 1 ENTANYQ

## Superficie
- 1 dormitorio: 45.5 m²
- Monoambiente: 34.5 m²
- **Total piso 1**: 80 m²

## Cálculo
```
Cable = m² × 3 (factor estimación)
Cable = 80 × 3 = 240 metros
```

## Desglose por Unidad

| Unidad | m² | Cable | Cable + 10% desperdicio |
|--------|-----|-------|-------------------------|
| 1 Dorm | 45.5 | 136.5 m | 150 m |
| Mono | 34.5 | 103.5 m | 115 m |
| **Total** | **80** | **240 m** | **265 m** |

## Costo Estimado
- Cable THW 2.5mm: USD 0.80/m
- **Total**: 265 m × USD 0.80 = **USD 212**

## Notas
- Incluir 10% de desperdicio
- Verificar tramos largos antes de comprar
- Coordinar con electricista para puntos específicos
```

---

## Ejemplo 3: Cronograma de Instalaciones

### Input del Usuario:
"Arma el cronograma de instalaciones para el piso 1"

### Análisis:
- **Tipo**: Cronograma
- **Proyecto**: ENTANYQ
- **Piso**: 1
- **Etapas**: Instalaciones

### Output:
```
# Cronograma Instalaciones — Piso 1 ENTANYQ

## Secuencia de Trabajo

### Semana 1: Preparación
- [ ] Revisión de planos eléctricos
- [ ] Marcação de puntos
- [ ] Compra de materiales

### Semana 2-3: Eléctrica
- [ ] Canalizaciones
- [ ] Tendido de cable
- [ ] Cajas de registro

### Semana 3-4: Gas
- [ ] Tuberías de gas
- [ ] Conexiones
- [ ] Prueba de hermeticidad

### Semana 4-5: Agua y Desagües
- [ ] Tuberías de agua fría
- [ ] Tuberías de agua caliente
- [ ] Desagües

### Semana 5-6: Calefacción
- [ ] Losa radiante
- [ ] Conexiones
- [ ] Prueba de sistema

## Duración Total: 6 semanas

## Dependencias
- Eléctrica → Antes de acabados
- Gas → Antes de pisos
- Agua → Antes de revestimientos
- Calefacción → Antes de piso final

## Recursos Necesarios
- Electricista: 2 personas
- Gasista: 1 persona
- Plomero: 1 persona
- Peón: 1 persona
```

---

## Ejemplo 4: Control de Calidad

### Input del Usuario:
"¿Cómo está la calidad de la mampostería?"

### Análisis:
- **Tipo**: Control de calidad
- **Elemento**: Mampostería
- **Formato**: Reporte de calidad

### Output:
```
# Control de Calidad — Mampostería ENTANYQ

## Verificación Realizada

### Paredes Exteriores
| Verificación | Estado | Observación |
|--------------|--------|-------------|
| Plomada | ✅ OK | Vertical correcta |
| Aplomo | ✅ OK | Sin desviaciones |
| Horizonte | ✅ OK | Nivel correcto |
| Juntas | ✅ OK | Uniformes |

### Paredes Internas
| Verificación | Estado | Observación |
|--------------|--------|-------------|
| Espesor | ✅ OK | 14cm (especificado) |
| Altura | ✅ OK | 2.60m |
| Puertas | ✅ OK | Umbrales correctos |
| Ventanas | ✅ OK | Marcos nivelados |

## Conclusión
- **Calidad**: Aprobada
- **Observaciones**: Ninguna significativa
- **Aprobado para**: Siguiente etapa (instalaciones)

## Recomendaciones
- Mantener estándares actuales
- Documentar fotos antes de cubrir
- Verificar após instalaciones
```

---

## Ejemplo 5: Problema Detectado

### Input del Usuario:
"Encontré una fisura en la pared del monoambiente"

### Análisis:
- **Tipo**: Problema de calidad
- **Ubicación**: Monoambiente
- **Gravedad**: Por determinar

### Output:
```
# Problema Detectado — Monoambiente ENTANYQ

## Descripción
- **Ubicación**: Pared norte del monoambiente
- **Tipo**: Fisura vertical
- **Tamaño**: ~30cm de largo
- **Gravedad**: Baja (superficial)

## Análisis
- **Causa probable**: Asentamiento normal de estructura
- **Riesgo**: Bajo (no estructural)
- **Solución**: Reparación con mortero de refuerzo

## Acción Propuesta
1. **Inmediata**: Marcar zona
2. **Corto plazo**: Reparar con mortero especial
3. **Seguimiento**: Verificar en 1 semana

## Documentación
- [Foto]: Fisura detectada
- [Foto]: Ubicación en plano
- [Medición]: Largo y profundidad

## Escalamiento
¿Querés que informe al CEO para programar la reparación?
```

---

## Ejemplo 6: Presupuesto de Etapa

### Input del Usuario:
"¿Cuánto va a costar la etapa de instalaciones del piso 1?"

### Análisis:
- **Tipo**: Presupuesto
- **Etapa**: Instalaciones
- **Alcance**: Piso 1

### Output:
```
# Presupuesto Instalaciones — Piso 1 ENTANYQ

## Desglose

### 1. Eléctrica
| Item | Cantidad | Costo | Total |
|------|----------|-------|-------|
| Cable THW 2.5mm | 265 m | USD 0.80/m | USD 212 |
| Tubería conduit | 100 m | USD 1.50/m | USD 150 |
| Cajas registro | 20 | USD 3 | USD 60 |
| Mano de obra | 80 m² | USD 8/m² | USD 640 |
| **Subtotal** | | | **USD 1,062** |

### 2. Gas
| Item | Cantidad | Costo | Total |
|------|----------|-------|-------|
| Tubería cobre | 40 m | USD 5/m | USD 200 |
| Conexiones | 15 | USD 8 | USD 120 |
| Mano de obra | — | — | USD 400 |
| **Subtotal** | | | **USD 720** |

### 3. Agua y Desagües
| Item | Cantidad | Costo | Total |
|------|----------|-------|-------|
| Tubería PVC | 50 m | USD 3/m | USD 150 |
| Conexiones | 25 | USD 5 | USD 125 |
| Mano de obra | — | — | USD 500 |
| **Subtotal** | | | **USD 775** |

### 4. Calefacción
| Item | Cantidad | Costo | Total |
|------|----------|-------|-------|
| Losa radiante | 80 m² | USD 15/m² | USD 1,200 |
| Mano de obra | — | — | USD 600 |
| **Subtotal** | | | **USD 1,800** |

## Total Instalaciones Piso 1: USD 4,357

## Notas
- Precios estimados sujetos a cotización final
- Incluir 10% imprevistos: USD 436
- **Presupuesto total con imprevistos**: USD 4,793
```