# ConstructoraAI — Sistema Operativo para Inmobiliaria

Sistema completo de agentes IA para la gestión integral de una desarrolladora inmobiliaria. Diseñado para competir con asistentes profesionales a nivel empresarial.

## Visión General

```
CEO (Orquestador)
    │
    ├── Comercial (Ventas)
    │   ├── cotizar_propiedad
    │   ├── generar_propuesta_venta
    │   ├── comparar_unidades
    │   ├── calcular_financiamiento
    │   ├── seguimiento_lead
    │   ├── responder_objecion
    │   ├── verificar_disponibilidad
    │   └── calcular_roi
    │
    ├── Marketing (Contenido)
    │   ├── crear_brochure
    │   ├── crear_flyer_instagram
    │   ├── crear_email_marketing
    │   ├── escribir_copy
    │   ├── optimizar_contenido
    │   ├── seleccionar_renders
    │   ├── crear_contenido_redes
    │   ├── disenar_estructura_brochure
    │   ├── escribir_email
    │   └── generar_hashtags
    │
    ├── Obras (Fase 2)
    ├── Finanzas (Fase 2)
    ├── Legal (Fase 2)
    └── ... (10 agentes más en roadmap)
```

## Estructura del Proyecto

```
C:\IA\Armat\
├── README.md                    # Este archivo
├── agents/                      # Agentes especializados
│   ├── ceo/                     # Director ejecutivo (6 archivos)
│   ├── comercial/               # Ventas (6 archivos)
│   ├── marketing/               # Contenido (6 archivos)
│   ├── obras/                   # Construcción (6 archivos)
│   ├── finanzas/                # Finanzas (6 archivos)
│   ├── legal/                   # Jurídico (6 archivos)
│   └── ...                      # 9 agentes más
│
├── skills/                      # Skills documentados
│   ├── comercial/               # 8 skills de ventas
│   ├── marketing/               # 10 skills de contenido
│   ├── obras/                   # 8 skills de construcción
│   ├── finanzas/                # 10 skills de finanzas
│   ├── legal/                   # 8 skills legales
│   └── shared/                  # Skills compartidos
│
├── knowledge/                   # Base de conocimiento
│   ├── ventas/                  # Ventas inmobiliarias
│   ├── marketing/               # Marketing inmobiliario
│   └── construccion/            # Construcción
│
├── templates/                   # Plantillas profesionales
│   ├── propuestas/              # Propuestas de venta
│   ├── presupuestos/            # Presupuestos de obra
│   ├── publicaciones/           # Redes sociales
│   └── emails/                  # Email marketing
│
├── brand/                       # Manual de branding
│   ├── identidad_visual.md      # Guía de identidad
│   └── paleta_colores.md        # Paleta oficial
│
├── config/                      # Configuraciones
├── memory/                      # Memoria persistente
├── img/                         # Recursos visuales
├── brochure-entanyq.html        # Brochure existente
└── brochure-styles.css          # Estilos existentes
```

## Agentes

### Fase 1 — Completada ✅

#### CEO (Director Ejecutivo)
- **Rol**: Orquestador principal
- **Responsabilidades**: Analizar peticiones, delegar, supervisar, aprobar
- **Archivo**: `agents/ceo/`
- **Skills**: Delegación, toma de decisiones, reportes

#### Comercial (Ventas)
- **Rol**: Generar propuestas y cerrar deals
- **Responsabilidades**: Cotizaciones, propuestas, seguimiento, negociación
- **Archivo**: `agents/comercial/`
- **Skills**: 8 (cotizar, propuesta, comparar, financiamiento, etc.)

#### Marketing (Contenido)
- **Rol**: Crear material de marketing profesional
- **Responsabilidades**: Brochures, flyers, emails, redes sociales
- **Archivo**: `agents/marketing/`
- **Skills**: 10 (brochure, flyer, email, copy, renders, etc.)

### Fase 2 — Completada ✅

#### Obras (Construcción)
- **Rol**: Supervisión y control de construcción
- **Responsabilidades**: Bitácora, avance, calidad, presupuesto
- **Archivo**: `agents/obras/`
- **Skills**: 8 (bitácora, avance, calidad, reporte, presupuesto, programa, etc.)

#### Finanzas
- **Rol**: Análisis y control financiero
- **Responsabilidades**: Estados financieros, flujo de caja, impuestos, proyecciones
- **Archivo**: `agents/finanzas/`
- **Skills**: 10 (estados financieros, flujo caja, rentabilidad, presupuesto, etc.)

#### Legal
- **Rol**: Asesoría jurídica y compliance
- **Responsabilidades**: Contratos, permisos, cumplimiento, litigios
- **Archivo**: `agents/legal/`
- **Skills**: 8 (contratos, permisos, normativa, litigios, etc.)

### Fase 3 — Completada ✅

#### Administración
- **Rol**: Gestión administrativa y logística
- **Responsabilidades**: Contratos de proveedores, coordinación, trámites
- **Archivo**: `agents/administracion/`
- **Skills**: 8 (proveedores, logística, contratos, inventario, nómina, oficina, correspondencia, reuniones)

#### Calidad
- **Rol**: Control de calidad y estándares
- **Responsabilidades**: Inspecciones, verificación, certificaciones
- **Archivo**: `agents/calidad/`
- **Skills**: 8 (inspección, materiales, informe, auditoría, etc.)

#### Clientes
- **Rol**: Gestión de relaciones con clientes
- **Responsabilidades**: CRM, seguimiento, satisfacción
- **Archivo**: `agents/clientes/`
- **Skills**: 8 (leads, seguimiento, satisfacción, CRM, etc.)

#### Compras
- **Rol**: Adquisiciones y proveedores
- **Responsabilidades**: Licitaciones, negociación, contratación
- **Archivo**: `agents/compras/`
- **Skills**: 8 (cotizaciones, comparativas, órdenes, evaluación, etc.)

#### IA
- **Rol**: Inteligencia artificial y automatización
- **Responsabilidades**: Análisis de datos, automatización, optimización
- **Archivo**: `agents/ia/`
- **Skills**: 8 (análisis, automatización, predicción, optimización, etc.)

#### Presupuestos
- **Rol**: Control presupuestario de obras
- **Responsabilidades**: Presupuestos, costos, seguimiento financiero
- **Archivo**: `agents/presupuestos/`
- **Skills**: 8 (crear presupuesto, control costos, avance financiero, proyección, etc.)

### Fase 5 — Completada ✅

#### RRHH (Recursos Humanos)
- **Rol**: Gestión del capital humano
- **Responsabilidades**: Nómina, reclutamiento, capacitación, desempeño
- **Archivo**: `agents/rrhh/`
- **Skills**: 4 (reclutamiento, nómina, capacitación, evaluación)

#### IT (Tecnologías)
- **Rol**: Soporte y desarrollo tecnológico
- **Responsabilidades**: Soporte técnico, sistemas, seguridad, redes
- **Archivo**: `agents/it/`
- **Skills**: 4 (soporte, sistemas, seguridad, redes)

#### Postventa
- **Rol**: Servicio post-venta y garantías
- **Responsabilidades**: Garantías, mantenimiento, satisfacción
- **Archivo**: `agents/postventa/`
- **Skills**: 4 (reclamaciones, mantenimiento, garantías, satisfacción)

#### Proveedores
- **Rol**: Gestión de relación con proveedores
- **Responsabilidades**: Evaluación, negociación, pedidos
- **Archivo**: `agents/proveedores/`
- **Skills**: 4 (evaluación, búsqueda, negociación, seguimiento)

#### Data (Datos y Analítica)
- **Rol**: Análisis de datos y Business Intelligence
- **Responsabilidades**: Análisis, dashboards, predicciones, KPIs
- **Archivo**: `agents/data/`
- **Skills**: 4 (análisis ventas, dashboards, predicción, KPIs)

## Skills

### Fase 1 — Completada ✅

#### Comercial (8 skills)
1. `cotizar_propiedad` — Generar cotización precisa
2. `generar_propuesta_venta` — Propuesta completa
3. `comparar_unidades` — Comparativa entre unidades
4. `calcular_financiamiento` — Opciones de pago
5. `seguimiento_lead` — Mensajes de follow-up
6. `responder_objecion` — Manejo de objeciones
7. `verificar_disponibilidad` — Estado de unidades
8. `calcular_roi` — Retorno de inversión

#### Marketing (10 skills)
1. `crear_brochure` — Brochure HTML profesional
2. `crear_flyer_instagram` — Flyer para Instagram
3. `crear_email_marketing` — Emails profesionales
4. `escribir_copy` — Copy para publicaciones
5. `optimizar_contenido` — Adaptar a plataformas
6. `seleccionar_renders` — Elegir imágenes
7. `crear_contenido_redes` — Calendario de contenido
8. `disenar_estructura_brochure` — Wireframe
9. `escribir_email` — Emails transaccionales
10. `generar_hashtags` — Hashtags relevantes

### Fase 2 — Completada ✅

#### Obras (8 skills)
1. `registrar_bitacora_diaria` — Registro diario de actividades
2. `calcular_avance_obra` — Cálculo de avance físico/financiero
3. `verificar_calidad` — Inspecciones de calidad
4. `generar_reporte_avance` — Reportes ejecutivos de avance
5. `controlar_presupuesto` — Control presupuestario
6. `programar_actividades` — Programación de trabajo
7. `evaluar_proveedor` — Evaluación de proveedores
8. `gestionar_herramientas` — Control de herramientas

#### Finanzas (10 skills)
1. `generar_estado_financiero` — Estados financieros
2. `calcular_flujo_caja` — Flujo de efectivo
3. `analizar_rentabilidad` — ROI, VAN, TIR
4. `presupuestar_proyecto` — Presupuestos de construcción
5. `calcular_impuestos` — Obligaciones fiscales
6. `evaluar_inversion` — Evaluación de proyectos
7. `analizar_costos` — Análisis de costos
8. `proyectar_ventas` — Proyecciones de ingresos
9. `conciliar_cuentas` — Conciliación bancaria
10. `generar_reporte_ejecutivo` — Reportes para directivos

#### Legal (8 skills)
1. `redactar_contrato` — Borradores de contratos
2. `revisar_cumplimiento` — Verificación de obligaciones
3. `consultar_normativa` — Leyes y reglamentos
4. `verificar_permisos` — Permisos de construcción
5. `gestionar_litigios` — Seguimiento de demandas
6. `validar_propiedad` — Validación de inmuebles
7. `gestionar_contratos` — Ciclo de vida de contratos
8. `generar_informe_legal` — Informes ejecutivos legales

### Fase 3 — Completada ✅

#### Administración (8 skills)
1. `gestionar_proveedores` — Gestión de proveedores
2. `coordinar_logistica` — Coordinación logística
3. `elaborar_contratos` — Elaboración de contratos
4. `controlar_inventario` — Control de inventario
5. `gestionar_nomina` — Gestión de nómina
6. `organizar_oficina` — Organización de oficina
7. `manejar_correspondencia` — Manejo de correspondencia
8. `programar_reuniones` — Programación de reuniones

#### Calidad (8 skills)
1. `inspeccionar_obra` — Inspección de obra
2. `verificar_materiales` — Verificación de materiales
3. `generar_informe_calidad` — Informes de calidad
4. `auditar_proceso` — Auditoría de procesos

#### Clientes (8 skills)
1. `registrar_lead` — Registro de leads
2. `seguir_cliente` — Seguimiento de clientes
3. `calificar_satisfaccion` — Calificación de satisfacción
4. `gestionar_crm` — Gestión de CRM

#### Compras (8 skills)
1. `solicitar_cotizacion` — Solicitud de cotización
2. `comparar_cotizaciones` — Comparación de cotizaciones
3. `generar_orden_compra` — Generación de órdenes de compra
4. `evaluar_proveedor` — Evaluación de proveedores

#### IA (8 skills)
1. `analizar_datos` — Análisis de datos
2. `automatizar_tarea` — Automatización de tareas
3. `predecir_tendencias` — Predicción de tendencias
4. `optimizar_procesos` — Optimización de procesos

#### Presupuestos (8 skills)
1. `crear_presupuesto_obra` — Creación de presupuestos
2. `controlar_costos` — Control de costos
3. `generar_avance_financiero` — Avance financiero
4. `proyectar_cierre` — Proyección de cierre

## Base de Conocimiento

- **Ventas**: Técnicas, pipeline, mercado, perfil de clientes
- **Marketing**: Reglas de marca, formatos, métricas
- **Construcción**: Etapas, materiales, control de calidad

## Templates

- **Propuestas**: Propuesta de venta completa
- **Presupuestos**: Presupuesto de obra
- **Publicaciones**: Templates Instagram
- **Emails**: Templates de email marketing

## Branding

- **Paleta**: Negro #000 + Dorado #C9A96E + Blanco
- **Tipografía**: Playfair Display + DM Sans
- **Tono**: Premium, profesional, directo
- **Estilo**: Lujoso, espacio negativo, sin superposiciones

## Configuración OpenCode

Los agentes están registrados en `opencode.json`:
- `armat-ceo` — CEO Agent
- `armat-comercial` — Comercial Agent
- `armat-marketing` — Marketing Agent
- `armat-obras` — Obras Agent
- `armat-finanzas` — Finanzas Agent
- `armat-legal` — Legal Agent
- `armat-administracion` — Administración Agent
- `armat-calidad` — Calidad Agent
- `armat-clientes` — Clientes Agent
- `armat-compras` — Compras Agent
- `armat-ia` — IA Agent
- `armat-presupuestos` — Presupuestos Agent

## Roadmap

### Fase 1 (Completada) ✅
- [x] CEO configurado
- [x] Comercial configurado
- [x] Marketing configurado
- [x] 18 skills documentados
- [x] Knowledge base
- [x] Templates
- [x] Branding

### Fase 2 (Completada) ✅
- [x] Obras configurado (8 skills)
- [x] Finanzas configurado (10 skills)
- [x] Legal configurado (8 skills)

### Fase 5 (Completada) ✅
- [x] RRHH configurado (4 skills)
- [x] IT configurado (4 skills)
- [x] Postventa configurado (4 skills)
- [x] Proveedores configurado (4 skills)
- [x] Data configurado (4 skills)
- [x] 98 skills totales

## Workflows

Flujos automatizados para procesos clave:

1. **Onboarding Cliente** — Desde lead hasta firma de contrato
2. **Control de Obra** — Bitácora, calidad, presupuesto diario
3. **Compra de Materiales** — Solicitud hasta recepción
4. **Pipeline de Ventas** — Prospecto hasta cierre

Ver `workflows/` para documentación completa.

## MCP Integraciones

Servicios externos conectados:

| Servicio | Estado | Uso |
|----------|--------|-----|
| Gmail | ✅ | Comunicación email |
| Google Drive | ✅ | Almacenamiento documentos |
| Google Calendar | ✅ | Eventos y reuniones |
| Google Sheets | ✅ | Hojas de cálculo |
| WhatsApp | 🔲 | Comunicación clientes |
| Slack | 🔲 | Comunicación interna |

Ver `config/mcp-integrations.md` para configuración.

## Uso

### desde OpenCode
```bash
# Llamar al CEO
opencode --agent armat-ceo "Creame una propuesta para un cliente"

# Llamar a Comercial directamente
opencode --agent armat-comercial "Cotizame el monoambiente"

# Llamar a Marketing directamente
opencode --agent armat-marketing "Creame un flyer para Instagram"
```

### Flujo de Trabajo
1. Usuario hace petición al CEO
2. CEO analiza y delega al agente correcto
3. Agente ejecuta con sus skills
4. CEO revisa y presenta resultado
5. Usuario aprueba o pide ajustes

## Mantenimiento

### Agregar nuevo agente
1. Crear carpeta en `agents/`
2. Crear 6 archivos (agent, instructions, rules, checklist, examples, memory)
3. Agregar skills en `skills/`
4. Registrar en `opencode.json`

### Agregar nueva skill
1. Crear archivo en `skills/<agente>/`
2. Documentar: identidad, objetivo, entradas, proceso, salida, checklist, ejemplo
3. Actualizar `agent.md` del agente correspondiente

---

**ARMAT Desarrolladora Inmobiliaria** — Centenario, Neuquén, Argentina