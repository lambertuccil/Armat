# Skill: predecir_demanda

## Identidad
- **Agente**: Data
- **Nombre**: Predicción de Demanda
- **Versión**: 1.0

## Objetivo
Predecir la demanda futura de unidades inmobiliarias para planificación estratégica.

## Entradas
- **datos_historicos** (requerido): Ventas pasadas
- **tendencias_mercado** (requerido): Condiciones del mercado
- **factores_externos** (requerido): Economía, competencia
- **horizonte** (requerido): Meses a predecir

## Proceso
1. Recopilar datos históricos
2. Identificar patrones
3. Seleccionar modelo
4. Entrenar modelo
5. Generar predicciones
6. Validar precisión
7. Presentar resultados

## Salida
Predicciones con:
- Demanda esperada
- Rango de confianza
- Factores influyentes
- Recomendaciones

## Checklist
- [ ] Datos recopilados
- [ ] Patrones identificados
- [ ] Modelo entrenado
- [ ] Predicciones generadas
- [ ] Validación realizada

## Ejemplo
```markdown
# PREDICCIÓN DEMANDA - Q4 2026

## Modelo: Regresión múltiple
## Precisión: 89%

## Predicciones
| Mes | Unidades | Ingresos |
|-----|----------|----------|
| Oct | 8 | $11.2M |
| Nov | 6 | $8.4M |
| Dic | 4 | $5.6M |

## Total Q4: $25.2M

## Recomendación
- Mantener inventario 2 hab
- Incrementar marketing digital
```
