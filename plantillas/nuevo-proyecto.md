# Template de Proyecto ARMAT

## Cómo Crear un Nuevo Proyecto

### Paso 1: Crear Estructura

```powershell
# Crear carpeta del proyecto
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]" -Force

# Crear subcarpetas
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/marketing/brochures" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/marketing/flyers" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/marketing/folletos" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/documentacion" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/img/render" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/img/Video" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/documentos" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/planos" -Force
New-Item -ItemType Directory -Path "proyectos/[nombre-proyecto]/datos" -Force
```

### Paso 2: Crear Archivos Base

Crear `proyectos/[nombre-proyecto]/datos/proyecto.json`:

```json
{
  "nombre": "[Nombre del Proyecto]",
  "ubicacion": "[Ciudad, Provincia]",
  "direccion": "[Dirección exacta]",
  "tipo": "[Departamentos / Casas / Lotes]",
  "estado": "[En planeación / En obra / Terminado]",
  "unidades": {
    "tipo_1": {
      "nombre": "[1 Dormitorio]",
      "precio_usd": 0,
      "superficie_m2": 0,
      "descripcion": ""
    }
  },
  "cocheras": {
    "disponibles": 0,
    "precio_desde_usd": 0
  },
  "contacto": {
    "telefono": "[Número]",
    "instagram": "@[Usuario]",
    "email": "[Email]"
  },
  "fechas": {
    "inicio": "[Fecha]",
    "entrega_estimada": "[Fecha]"
  }
}
```

### Paso 3: Documentación Estratégica

Crear en `proyectos/[nombre-proyecto]/documentacion/`:

1. `01_Analisis_Mercado.md` — Análisis de la zona, competencia, público objetivo
2. `02_Estrategia_Ventas.md` — Pipeline, fuentes de leads, métricas
3. `03_Proyecciones_Financieras.md` — Costos, ingresos, rentabilidad
4. `04_Observaciones_y_Mejoras.md` — Lista de mejoras y observaciones

### Paso 4: Materiales de Marketing

Usar los agentes de marketing para generar:

```
"Creame un brochure para el proyecto [Nombre]"
"Armame un flyer para [Nombre]"
"Haceme un folleto para [Nombre]"
```

### Paso 5: Cómputo de Materiales

Si tenés planos, usar el sistema de cómputo:

```
"Calcula materiales para [Nombre]"
```

---

## Estructura de Referencia

```
proyectos/[nombre-proyecto]/
├── datos/
│   └── proyecto.json          # Datos del proyecto
├── marketing/
│   ├── brochures/
│   │   ├── [nombre]-v1.html      # Editable
│   │   └── [nombre]-v1-enviar.html  # Autocontenido
│   ├── flyers/
│   │   └── [nombre]-v1.html
│   └── folletos/
│       └── [nombre]-v1.html
├── documentacion/
│   ├── 01_Analisis_Mercado.md
│   ├── 02_Estrategia_Ventas.md
│   ├── 03_Proyecciones_Financieras.md
│   └── 04_Observaciones_y_Mejoras.md
├── img/
│   ├── render/
│   └── Video/
├── documentos/
│   └── [documentos originales]
├── planos/
│   └── [planos del proyecto]
└── README.md
```

---

## Datos Mínimos para Empezar

Para cada nuevo proyecto, necesitás:

| Dato | Obligatorio | Ejemplo |
|------|-------------|---------|
| Nombre | ✅ | "Vista Verde" |
| Ubicación | ✅ | "Neuquén Capital" |
| Tipo | ✅ | "Departamentos" |
| Precio unitario | ✅ | "USD 95.000" |
| Superficie | ✅ | "52 m²" |
| Renders/Fotos | ✅ | Al menos 5 imágenes |
| Contacto | ✅ | Teléfono + Instagram |

---

## Checklist de Nuevo Proyecto

- [ ] Crear estructura de carpetas
- [ ] Completar `proyecto.json` con datos reales
- [ ] Agregar renders/fotos a `img/render/`
- [ ] Crear documentación estratégica
- [ ] Generar brochure con agente Marketing
- [ ] Generar flyer con agente Marketing
- [ ] Generar folleto con agente Marketing
- [ ] Calcular cómputo de materiales (si hay planos)
- [ ] Actualizar README del proyecto
- [ ] Probar materiales de marketing
