# Skill: predecir_tendencias

## Identidad
- **Agente**: IA
- **Nombre**: Predicción de Tendencias
- **Versión**: 1.0

## Objetivo
Utilizar modelos predictivos para anticipar tendencias de ventas, costos y demanda.

## Entradas
- **datos_historicos** (requerido): Datos del pasado
- **variable_objetivo** (requerido): Qué predecir
- **horizonte** (requerido): Período a predecir
- **factores_externos** (opcional): Variables externas

## Proceso
1. Recopilar datos históricos
2. Limpiar y preparar datos
3. Seleccionar modelo predictivo
4. Entrenar modelo
5. Validar precisión
6. Generar predicciones
7. Presentar resultados

## Salida
Predicciones con:
- Valores esperados
- Rango de confianza
- Factores influyentes
- Recomendaciones

## Checklist
- [ ] Datos históricos recopilados
- [ ] Modelo seleccionado
- [ ] Modelo entrenado
- [ ] Predicciones generadas
- [ ] Resultados presentados

## Ejemplo
```markdown
# PREDICCIÓN VENTAS - Q4 2026

## Modelo
- Algoritmo: Regresión múltiple
- Precisión: 89%

## Predicciones
| Mes | Unidades | Ingresos |
|-----|----------|----------|
| Oct | 8 | $11.2M |
| Nov | 6 | $8.4M |
| Dic | 4 | $5.6M |

## Total Q4: $25.2M
```
