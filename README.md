# ConstructoraAI — Sistema Operativo para Inmobiliaria

Sistema completo de agentes IA para la gestión integral de una desarrolladora inmobiliaria. Diseñado para competir con asistentes profesionales a nivel empresarial.

![Estado](https://img.shields.io/badge/estado-activo-green)
![Versión](https://img.shields.io/badge/versión-1.0.0-blue)
![Agentes](https://img.shields.io/badge/agentes-17-brightgreen)
![Skills](https://img.shields.io/badge/skills-98-blue)

---

## Visión General

```
┌─────────────────────────────────────────────────────────────────┐
│                     CEO (Director General)                       │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │ 1. Recibe y clasifica el pedido                         │    │
│  │ 2. Verifica si es simple o compleja                     │    │
│  │ 3. Delega al agente o agentes correspondientes          │    │
│  │ 4. Coordina trabajo paralelo cuando es necesario        │    │
│  └─────────────────────────────────────────────────────────┘    │
└───────┬───────┬───────┬───────┬───────┬───────┬────────────────┘
        │       │       │       │       │       │
        ▼       ▼       ▼       ▼       ▼       ▼
┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐
│Comer-│ │Mktg. │ │Obras │ │Finan.│ │Legal │ │Admin.│
│cial  │ │      │ │      │ │      │ │      │ │      │
└──┬───┘ └──┬───┘ └──┬───┘ └──┬───┘ └──┬───┘ └──┬───┘
   │        │        │        │        │        │
   └────────┴────────┴────────┘        │        │
                         │              │        │
                         ▼              │        │
               ┌─────────────────┐      │        │
               │  RESULTADO      │      │        │
               │  PARCIAL        │──────┘        │
               └─────────────────┘               │
                         │                       │
                         ▼                       │
               ┌─────────────────┐               │
               │  CALIDAD        │───────────────┘
               │  (Revisión)     │
               └─────────────────┘
                         │
                         ▼
               ┌─────────────────┐
               │  ENTREGA AL     │
               │  USUARIO        │
               └─────────────────┘
```

---

## Estructura del Proyecto

```
C:\IA\Armat\
├── README.md                      # Este archivo
├── GUIA-COMPLETA-ARMAT.html       # Guía visual del sistema (12 páginas)
├── GUIA-COMPLETA.md               # Guía completa del sistema
├── .env.example                   # Variables de entorno
├── .gitignore                     # Exclusiones de git
│
├── agents/                        # 17 agentes especializados (COMPARTIDO)
│   ├── administracion/            # Gestión administrativa
│   ├── calidad/                   # Control de calidad
│   ├── ceo/                       # Director ejecutivo
│   ├── clientes/                  # Atención al cliente
│   ├── comercial/                 # Ventas
│   ├── compras/                   # Adquisiciones
│   ├── data/                      # Analítica
│   ├── finanzas/                  # Finanzas
│   ├── ia/                        # Tecnología
│   ├── it/                        # Sistemas
│   ├── legal/                     # Jurídico
│   ├── marketing/                 # Comunicación
│   ├── obras/                     # Construcción
│   ├── postventa/                 # Garantías
│   ├── presupuestos/              # Costos
│   ├── proveedores/               # Relación
│   └── rrhh/                      # Personal
│
├── skills/                        # 98 skills organizados (COMPARTIDO)
│   ├── administracion/
│   ├── calidad/
│   ├── clientes/
│   ├── comercial/
│   ├── compras/
│   ├── data/
│   ├── finanzas/
│   ├── ia/
│   ├── it/
│   ├── legal/
│   ├── marketing/
│   ├── obras/
│   ├── postventa/
│   ├── presupuestos/
│   ├── proveedores/
│   ├── rrhh/
│   └── shared/
│
├── base-conocimiento/             # Base de conocimiento (COMPARTIDO)
│   ├── construccion/
│   │   └── materiales-rendimientos.md  # Tabla de materiales Neuquén
│   ├── legislacion/
│   │   └── neuquen/
│   │       ├── arancel-cajn.md
│   │       └── leyes-provinciales-clave.md
│   ├── marketing/
│   └── ventas/
│
├── plantillas/                    # Plantillas reutilizables (COMPARTIDO)
│   ├── branding/
│   │   ├── guia-voz-marca.md
│   │   ├── manual-marca.md
│   │   ├── paleta-colores.md
│   │   └── tipografia.md
│   ├── contratos/
│   │   ├── compraventa-inmueble.md
│   │   ├── convenio-confidencialidad.md
│   │   └── comision-venta.md
│   ├── emails/
│   ├── marketing/
│   │   ├── articulo-blog.md
│   │   ├── newsletter-mensual.md
│   │   └── post-instagram-legal.md
│   ├── presupuestos/
│   ├── propuestas/
│   └── publicaciones/
│
├── workflows/                     # Workflows automatizados (COMPARTIDO)
│
├── config/                        # Configuración del sistema (COMPARTIDO)
│   ├── agentes.json
│   ├── alertas.json
│   ├── integraciones.json
│   ├── permisos.json
│   └── mcp-config.json
│
├── integrations/                  # Integraciones externas (COMPARTIDO)
│   ├── calendar/
│   ├── gmail/
│   ├── google-drive/
│   └── whatsapp/
│
├── brand/                         # Identidad visual ARMAT (COMPARTIDO)
│
├── proyectos/                     # PROYECTOS DE DESARROLLO
│   ├── entanyq/                   # Proyecto ENTANYQ (Centenario)
│   │   ├── marketing/             # Materiales de marketing
│   │   │   ├── brochures/
│   │   │   ├── flyers/
│   │   │   └── folletos/
│   │   ├── documentacion/         # Documentación estratégica
│   │   │   ├── 01_Analisis_Mercado.md
│   │   │   ├── 02_Estrategia_Ventas.md
│   │   │   ├── 03_Proyecciones_Financieras.md
│   │   │   └── 04_Observaciones_y_Mejoras.md
│   │   ├── img/                   # Renders, fotos, videos
│   │   │   ├── render/
│   │   │   └── Video/
│   │   └── documentos/            # Documentos originales
│   │
│   ├── [proyecto-2]/              # Próximo proyecto
│   └── [proyecto-3]/              # Futuro proyecto
│
└── memory/                        # Memoria persistente
```

---

## Agentes

### CEO (Director Ejecutivo)
- **Rol**: Orquestador principal
- **Responsabilidades**: Analizar peticiones, delegar, supervisar, aprobar
- **Archivo**: `agents/ceo/`

### Comercial (Ventas)
- **Rol**: Generar propuestas y cerrar deals
- **Responsabilidades**: Cotizaciones, propuestas, seguimiento, negociación
- **Skills**: 8 (cotizar, propuesta, comparar, financiamiento, etc.)

### Marketing (Contenido)
- **Rol**: Crear material de marketing profesional
- **Responsabilidades**: Brochures, flyers, emails, redes sociales
- **Skills**: 10 (brochure, flyer, email, copy, hashtags, etc.)

### Obras (Construcción)
- **Rol**: Supervisar la construcción
- **Responsabilidades**: Avance de obra, calidad, proveedores, entregas
- **Skills**: 8 (avance, calidad, bitácora, proveedores, etc.)

### Finanzas (Gestión)
- **Rol**: Controlar finanzas del proyecto
- **Responsabilidades**: Presupuestos, flujo de caja, rentabilidad
- **Skills**: 10 (rentabilidad, impuestos, caja, reportes, etc.)

### Legal (Jurídico)
- **Rol**: Asesorar en temas legales
- **Responsabilidades**: Contratos, permisos, regulaciones
- **Skills**: 5 (asesoramiento, honorarios, contratos, etc.)

### Administración (Trámites)
- **Rol**: Gestionar trámites administrativos
- **Responsabilidades**: Habilitaciones, documentación, seguimiento
- **Skills**: 3 (habilitaciones, documentación, trámites)

### Calidad (Control)
- **Rol**: Supervisar calidad constructiva
- **Responsabilidades**: Auditorías, materiales, informes
- **Skills**: 4 (auditoría, materiales, informes, terminaciones)

### Clientes (Postventa)
- **Rol**: Atender a compradores
- **Responsabilidades**: Consultas, reclamos, seguimiento
- **Skills**: 4 (atención, reclamos, seguimiento, respuesta)

### Compras (Adquisiciones)
- **Rol**: Gestionar compras
- **Responsabilidades**: Materiales, precios, negociación
- **Skills**: 4 (materiales, precios, compras, negociación)

### IA (Tecnología)
- **Rol**: Soporte tecnológico
- **Responsabilidades**: Automatización, herramientas, integración
- **Skills**: 3 (automatización, configuración, integración)

### Presupuestos (Costos)
- **Rol**: Elaborar presupuestos
- **Responsabilidades**: Estimación de costos, detalle de materiales
- **Skills**: 3 (presupuesto, costos, elaboración)

### RRHH (Personal)
- **Rol**: Gestionar personal
- **Responsabilidades**: Contrataciones, capacitación, nómina
- **Skills**: 3 (capacitación, contratación, nómina)

### IT (Sistemas)
- **Rol**: Soporte informático
- **Responsabilidades**: Redes, sistemas, soporte
- **Skills**: 3 (redes, mantenimiento, soporte)

### Postventa (Garantías)
- **Rol**: Gestión postventa
- **Responsabilidades**: Garantías, mantenimiento, consultas
- **Skills**: 3 (garantías, mantenimiento, respuesta)

### Proveedores (Relación)
- **Rol**: Gestión de proveedores
- **Responsabilidades**: Administración, evaluación, negociación
- **Skills**: 3 (administración, evaluación, negociación)

### Data (Analítica)
- **Rol**: Análisis de datos
- **Responsabilidades**: Dashboards, reportes, tendencias
- **Skills**: 4 (datos, dashboards, reportes, tendencias)

---

## Skills (98 total)

| Departamento | Cantidad | Ejemplos |
|--------------|----------|----------|
| **Comercial** | 8 | cotizar, propuesta, comparar, financiamiento |
| **Marketing** | 10 | brochure, flyer, email, copy, hashtags |
| **Obras** | 8 | avance, calidad, bitácora, proveedores |
| **Finanzas** | 10 | rentabilidad, impuestos, caja, reportes |
| **Legal** | 5 | asesoramiento, honorarios, contratos |
| **Administración** | 3 | habilitaciones, documentación, trámites |
| **Calidad** | 4 | auditoría, materiales, informes |
| **Clientes** | 4 | atención, reclamos, seguimiento |
| **Compras** | 4 | materiales, precios, negociación |
| **IA** | 3 | automatización, configuración |
| **Presupuestos** | 3 | presupuesto, costos |
| **RRHH** | 3 | capacitación, contratación |
| **IT** | 3 | redes, mantenimiento |
| **Postventa** | 3 | garantías, mantenimiento |
| **Proveedores** | 3 | administración, evaluación |
| **Data** | 4 | datos, dashboards, reportes |

---

## Workflows Automatizados

| Workflow | Descripción |
|----------|-------------|
| **Onboarding Cliente** | Proceso de alta de nuevo comprador |
| **Control de Obra** | Seguimiento diario de avance |
| **Compra de Materiales** | Adquisición y entrega |
| **Pipeline de Ventas** | Seguimiento de leads |

---

## Base de Conocimiento Legal

### Legislación de Neuquén

- **Ley 1920**: Código Procesal Civil y Comercial
- **Ley 6.839**: Mediación Obligatoria
- **Ley 3.017**: Arbitraje
- **Ley 5.853**: Código del Trabajo Provincial
- **Ley 5.908**: Riesgos del Trabajo
- **Ley 17.565**: Código Civil y Comercial de la Nación

### Plantillas de Contratos

- **Compraventa**: Para departamentos ENTANYQ
- **Confidencialidad**: NDA para proveedores
- **Comisión**: Para corredores inmobiliarios

---

## Integraciones

| Integración | Estado | Agentes |
|-------------|--------|---------|
| **WhatsApp** | Pendiente | CEO, Comercial, Clientes, Marketing |
| **Gmail** | Pendiente | CEO, Comercial, Marketing, Clientes |
| **Google Drive** | Pendiente | Legal, Administración, Obras |
| **Google Calendar** | Pendiente | CEO, Comercial, Obras |

---

## Materiales de Marketing

### Proyecto ENTANYQ — Centenario, Neuquén

| Material | Archivo | Tipo |
|----------|---------|------|
| **Brochure** | `proyectos/entanyq/marketing/brochures/brochure-entanyq-v2.html` | Editable |
| **Brochure (enviar)** | `proyectos/entanyq/marketing/brochures/brochure-entanyq-v2-enviar.html` | Autocontenido |
| **Flyer** | `proyectos/entanyq/marketing/flyers/flyer-entanyq-v2.html` | Editable |
| **Folleto** | `proyectos/entanyq/marketing/folletos/folleto-entanyq-v2.html` | Editable |
| **Guía Visual** | `GUIA-COMPLETA-ARMAT.html` | Guía del sistema |

### Datos del Proyecto ENTANYQ

- **Tipo**: Departamentos nuevos
- **Ubicación**: Centenario, Neuquén
- **Unidades**: 1 Dormitorio (USD 85.000), Monoambiente (USD 60.000)
- **Cocheras**: Desde USD 7.500
- **Estado**: 50% vendido (8 unidades disponibles)

### Cómo Crear Materiales para un Nuevo Proyecto

1. Crear carpeta: `proyectos/[nombre-proyecto]/`
2. Copiar estructura de ENTANYQ como template
3. Actualizar datos del proyecto (precios, ubicación, renders)
4. Los agentes de marketing generarán materiales automáticamente

---

## Documentación Estratégica

### Proyecto ENTANYQ

| Documento | Contenido |
|-----------|-----------|
| **01_Analisis_Mercado** | Demografía, competencia, público objetivo |
| **02_Estrategia_Ventas** | Pipeline, fuentes de leads, métricas |
| **03_Proyecciones_Financieras** | Costos, ingresos, rentabilidad, ROI |
| **04_Observaciones_y_Mejoras** | Análisis de materiales, mejoras priorizadas |

**Ubicación**: `proyectos/entanyq/documentacion/`

### Para Nuevo Proyecto

1. Crear carpeta: `proyectos/[nombre-proyecto]/documentacion/`
2. Usar plantillas de documentación existentes
3. Adaptar análisis de mercado a nueva ubicación
4. Calcular proyecciones financieras propias

---

## Instalación en Otra PC

**Necesitás**: Git + OpenCode + API Key de IA (gratuita con MiMo V2.5 Free)

```bash
# 1. Instalar OpenCode
winget install opencode                    # Windows
curl -fsSL https://opencode.ai/install | bash  # macOS/Linux

# 2. Clonar repositorio
git clone https://github.com/lambertuccil/Armat.git
cd Armat

# 3. Configurar API key
opencode config                            # Seguir instrucciones

# 4. ¡Listo!
opencode
```

**Tiempo estimado**: 10-15 minutos

📖 **Guía completa paso a paso**: [INSTALACION.md](INSTALACION.md)
📖 **Guía visual del sistema**: [GUIA-COMPLETA-ARMAT.html](GUIA-COMPLETA-ARMAT.html)

---

## Cómo Usar

### Ejemplo 1: Cotizar un departamento

```
Usuario: "¿Cuánto sale el departamento de 1 dormitorio?"

CEO → Comercial:
1. Verifica disponibilidad
2. Calcula precio
3. Genera cotización
4. Presenta opciones de pago
```

### Ejemplo 2: Reporte de avance de obra

```
Usuario: "¿Cómo va la obra?"

CEO → Obras:
1. Recopila bitácora diaria
2. Calcula porcentaje de avance
3. Verifica calidad
4. Genera reporte ejecutivo
```

### Ejemplo 3: Crear contenido para Instagram

```
Usuario: "Haceme un post para Instagram"

CEO → Marketing:
1. Selecciona mejores fotos
2. Escribe copy atractivo
3. Genera hashtags relevantes
4. Sugiere horario de publicación
```

---

## Contacto

**ARMAT — Desarrolladora Inmobiliaria**
- Teléfono: 299 508-9366 / 299 580-6377
- Instagram: @ARMAT.DESARROLLOS

---

*Documento generado automáticamente por el sistema de agentes ARMAT*
*Última actualización: Julio 2026*
