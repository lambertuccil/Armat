# ARMAT — Guía Completa del Sistema

## Sistema de Agentes Inteligentes para Desarrolladora Inmobiliaria

---

## Tabla de Contenidos

1. [Resumen del Sistema](#resumen-del-sistema)
2. [Estructura del Proyecto](#estructura-del-proyecto)
3. [Agentes por Departamento](#agentes-por-departamento)
4. [Skills Disponibles](#skills-disponibles)
5. [Workflows Automatizados](#workflows-automatizados)
6. [Base de Conocimiento Legal](#base-de-conocimiento-legal)
7. [Plantillas y Contratos](#plantillas-y-contratos)
8. [Integraciones](#integraciones)
9. [Materiales de Marketing](#materiales-de-marketing)
10. [Configuración](#configuración)
11. [Cómo Usar el Sistema](#cómo-usar-el-sistema)
12. [Próximos Pasos](#próximos-pasos)

---

## Resumen del Sistema

| Componente | Cantidad |
|------------|----------|
| **Agentes** | 17 |
| **Skills** | 98 |
| **Workflows** | 4 |
| **Plantillas** | 10+ |
| **Documentos de Marketing** | 3 (brochure, flyer, folleto) |
| **Base de Conocimiento Legal** | 2 documentos |
| **Integraciones** | 4 (WhatsApp, Gmail, Drive, Calendar) |

### Arquitectura

```
CEO (Orquestador)
├── Comercial (Ventas)
├── Marketing (Comunicación)
├── Obras (Construcción)
├── Finanzas (Gestión Financiera)
├── Legal (Asesoría Jurídica)
├── Administración (Trámites)
├── Calidad (Control)
├── Clientes (Postventa)
├── Compras (Adquisiciones)
├── IA (Tecnología)
├── Presupuestos (Costos)
├── RRHH (Personal)
├── IT (Sistemas)
├── Postventa (Garantías)
├── Proveedores (Relación)
└── Data (Analítica)
```

---

## Estructura del Proyecto

```
Armat/
├── README.md                      # Documentación principal
├── GUIA-COMPLETA.md               # Esta guía
├── .env.example                   # Variables de entorno
├── .gitignore                     # Exclusiones de git
│
├── agents/                        # 17 agentes especializados
│   ├── administracion/
│   ├── calidad/
│   ├── ceo/
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
│   └── rrhh/
│
├── skills/                        # 98 skills organizados
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
├── base-conocimiento/             # Base de conocimiento
│   ├── construccion/
│   ├── legislacion/
│   │   └── neuquen/
│   │       ├── arancel-cajn.md
│   │       └── leyes-provinciales-clave.md
│   ├── marketing/
│   └── ventas/
│
├── plantillas/                    # Plantillas reutilizables
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
├── workflows/                     # Workflows automatizados
│
├── config/                        # Configuración del sistema
│   ├── agentes.json
│   ├── alertas.json
│   ├── integraciones.json
│   ├── permisos.json
│   └── mcp-config.json
│
├── integrations/                  # Integraciones externas
│   ├── calendar/
│   ├── gmail/
│   ├── google-drive/
│   └── whatsapp/
│
├── marketing/                     # Materiales de marketing
│   ├── brochures/
│   │   ├── brochure-entanyq-v2.html
│   │   └── brochure-entanyq-v2-enviar.html
│   ├── flyers/
│   │   ├── flyer-entanyq-v2.html
│   │   └── flyer-entanyq.html
│   ├── folletos/
│   │   ├── folleto-entanyq-v2.html
│   │   └── folleto-entanyq.html
│   └── GUIA-COMPLETA-ARMAT.html
│
├── Documentacion/                 # Documentación estratégica
│   ├── 01_Analisis_Mercado_ENTANYQ.md
│   ├── 02_Estrategia_Ventas_ENTANYQ.md
│   ├── 03_Proyecciones_Financieras_ENTANYQ.md
│   └── 04_Observaciones_y_Mejoras.md
│
├── brand/                         # Identidad visual
├── img/                           # Recursos visuales
│   └── render/                    # 18 renders
├── documentos_entregados/         # Documentos originales
└── memory/                        # Memoria persistente
```

---

## Agentes por Departamento

### 1. CEO — Director General
**Función**: Orquesta todas las operaciones, toma decisiones estratégicas y coordina entre departamentos.

**Responsabilidades**:
- Recibir y analizar peticiones del usuario
- Determinar complejidad: simple (ejecuto inline) vs compleja (delego)
- Seleccionar el agente correcto para cada tarea
- Supervisar calidad de entregables
- Sintetizar resultados

---

### 2. Comercial — Ventas y Negociación
**Función**: Gestiona todo el proceso de venta, desde la captación de leads hasta el cierre.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `calcular_financiamiento` | Calcula opciones de pago y cuotas |
| `calcular_roi` | Retorno de inversión para el comprador |
| `comparar_unidades` | Compara departamentos disponibles |
| `cotizar_propiedad` | Genera cotización de unidad |
| `generar_propuesta_venta` | Crea propuesta comercial personalizada |
| `responder_objecion` | Responde dudas del cliente |
| `seguimiento_lead` | Programa seguimiento de prospectos |
| `verificar_disponibilidad` | Consulta unidades disponibles |

---

### 3. Marketing — Comunicación y Marca
**Función**: Crea contenido, gestiona redes y materiales de marketing.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `crear_brochure` | Genera brochures de proyectos |
| `crear_contenido_redes` | Crea contenido para Instagram/Facebook |
| `crear_email_marketing` | Diseña campañas de email |
| `crear_flyer_instagram` | Genera flyers para redes sociales |
| `disenar_estructura_brochure` | Planifica estructura de materiales |
| `escribir_copy` | Redacta textos de venta |
| `escribir_email` | Redacta emails comerciales |
| `generar_hashtags` | Crea hashtags relevantes |
| `optimizar_contenido` | Mejora contenido existente |
| `seleccionar_renders` | Elige mejores imágenes para materiales |

---

### 4. Obras — Construcción
**Función**: Supervisa la construcción, controla avance de obra y gestiona proveedores.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `calcular_avance_obra` | Calcula porcentaje de avance |
| `controlar_calidad` | Verifica calidad de constructiva |
| `generar_bitacora` | Crea reporte diario de obra |
| `gestionar_proveedores` | Administra relación con proveedores |
| `planificar_entregas` | Programa entregas de materiales |
| `supervisar_obras` | Supervisa trabajos en sitio |

---

### 5. Finanzas — Gestión Financiera
**Función**: Controla finanzas, presupuestos, flujo de caja e inversiones.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `analizar_rentabilidad` | Calcula ROI y rentabilidad |
| `calcular_impuestos` | Estima impuestos |
| `controlar_caja` | Monitorea flujo de caja |
| `generar_reporte_financiero` | Crea reportes financieros |
| `gestionar_pagos` | Administra pagos a proveedores |
| `presupuestar_obra` | Elabora presupuestos de construcción |

---

### 6. Legal — Asesoría Jurídica
**Función**: Asesora en temas legales, contratos, regulaciones y permisos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `asesorar_legalmente` | Brinda asesoramiento legal |
| `calcular_honorarios` | Calcula honorarios profesionales |
| `generar_contrato` | Crea contratos |
| `revisar_documentacion` | Verifica documentación legal |
| `verificar_permisos` | Gestiona permisos y habilitaciones |

---

### 7. Administración — Gestión Administrativa
**Función**: Gestiona trámites administrativos, habilitaciones y documentación.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `gestionar_habilitaciones` | Tramita habilitaciones |
| `organizar_documentacion` | Organiza documentos |
| `seguir_tramites` | Da seguimiento a trámites |

---

### 8. Calidad — Control
**Función**: Supervisa la calidad constructiva y de terminaciones.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `auditar_calidad` | Realiza auditorías de calidad |
| `controlar_materiales` | Verifica calidad de materiales |
| `generar_informe_calidad` | Crea informes de calidad |
| `supervisar_terminaciones` | Revisa terminaciones |

---

### 9. Clientes — Postventa
**Función**: Gestiona la relación con clientes, postventa y reclamos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `atender_cliente` | Atiende consultas de clientes |
| `gestionar_reclamos` | Administra reclamos |
| `realizar_seguimiento` | Da seguimiento postventa |
| `responder_cliente` | Responde consultas |

---

### 10. Compras — Adquisiciones
**Función**: Gestiona compras de materiales y negociación con proveedores.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `calcular_materiales` | Estima materiales necesarios |
| `comparar_precios` | Compara precios de proveedores |
| `gestionar_compras` | Administra proceso de compra |
| `negociar_proveedores` | Negocia condiciones |

---

### 11. IA / Tecnología — Soporte Tecnológico
**Función**: Gestiona herramientas de IA, automatización y sistemas.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `automatizar_tareas` | Automatiza procesos |
| `configurar_herramientas` | Configura herramientas IA |
| `integrar_sistemas` | Integra diferentes sistemas |

---

### 12. Presupuestos — Estimación de Costos
**Función**: Elabora presupuestos de obras y estimación de costos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `elaborar_presupuesto` | Crea presupuestos detallados |
| `estimar_costos` | Estima costos de construcción |
| `hacer_presupuesto` | Genera presupuestos |

---

### 13. RRHH — Gestión de Personal
**Función**: Gestiona personal, contrataciones y capacitación.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `capacitar_personal` | Organiza capacitaciones |
| `contratar_personal` | Gestiona contrataciones |
| `gestionar_nomina` | Administra nómina |

---

### 14. IT / Sistemas — Soporte Informático
**Función**: Gestiona infraestructura tecnológica, redes y sistemas.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `configurar_redes` | Configura redes |
| `mantener_sistemas` | Mantiene sistemas |
| `soporte_tecnico` | Brinda soporte técnico |

---

### 15. Postventa — Garantías
**Función**: Gestiona servicio postventa, garantías y mantenimiento.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `gestionar_garantias` | Administra garantías |
| `programar_mantenimiento` | Programa mantenimiento |
| `responder_postventa` | Responde consultas postventa |

---

### 16. Proveedores — Relación
**Función**: Gestiona relación con proveedores, contratos y pagos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `administrar_proveedores` | Administra proveedores |
| `evaluar_proveedores` | Evalúa desempeño |
| `negociar_contratos` | Negocia contratos |

---

### 17. Data / Analítica — Análisis de Datos
**Función**: Gestiona datos, reportes y analítica de negocio.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `analizar_datos` | Analiza datos de negocio |
| `generar_dashboards` | Crea dashboards |
| `generar_reportes` | Genera reportes |
| `predecir_tendencias` | Predice tendencias |

---

## Base de Conocimiento Legal

### Legislación de Neuquén

| Documento | Contenido |
|-----------|-----------|
| `leyes-provinciales-clave.md` | Leyes provinciales relevantes para construcciones |
| `arancel-cajn.md` | Arancel del Colegio de Abogados de Neuquén |

### Leyes Relevantes

- **Ley 1920**: Código Procesal Civil y Comercial
- **Ley 6.839**: Mediación Obligatoria
- **Ley 3.017**: Arbitraje
- **Ley 5.853**: Código del Trabajo Provincial
- **Ley 5.908**: Riesgos del Trabajo
- **Ley 17.565**: Código Civil y Comercial de la Nación

---

## Plantillas y Contratos

### Contratos

| Plantilla | Uso |
|-----------|-----|
| `compraventa-inmueble.md` | Contrato de compra de departamentos |
| `convenio-confidencialidad.md` | NDA para proveedores |
| `comision-venta.md` | Comisiones para corredores |

### Branding

| Plantilla | Uso |
|-----------|-----|
| `guia-voz-marca.md` | Tono y voz de comunicación |
| `manual-marca.md` | Manual de identidad |
| `paleta-colores.md` | Sistema de colores |
| `tipografia.md` | Guía tipográfica |

### Marketing

| Plantilla | Uso |
|-----------|-----|
| `post-instagram-legal.md` | Estructura para posts |
| `newsletter-mensual.md` | Formato newsletter |
| `articulo-blog.md` | Artículos de blog |

---

## Integraciones

| Integración | Estado | Agentes que la usan |
|-------------|--------|---------------------|
| **WhatsApp** | Pendiente | CEO, Comercial, Clientes, Marketing |
| **Gmail** | Pendiente | CEO, Comercial, Marketing, Clientes |
| **Google Drive** | Pendiente | Legal, Administración, Obras |
| **Google Calendar** | Pendiente | CEO, Comercial, Obras |

### Configurar Integraciones

Ver `integrations/` para guías detalladas de cada integración.

---

## Materiales de Marketing

### Brochure ENTANYQ

| Archivo | Tipo |
|---------|------|
| `brochure-entanyq-v2.html` | Editable (rutas relativas) |
| `brochure-entanyq-v2-enviar.html` | Autocontenido (base64) |

### Flyer ENTANYQ

| Archivo | Tipo |
|---------|------|
| `flyer-entanyq-v2.html` | Editable |
| `flyer-entanyq.html` | Versión anterior |

### Folleto ENTANYQ

| Archivo | Tipo |
|---------|------|
| `folleto-entanyq-v2.html` | Editable |
| `folleto-entanyq.html` | Versión anterior |

### Guía Visual

| Archivo | Descripción |
|---------|-------------|
| `GUIA-COMPLETA-ARMAT.html` | Guía visual del sistema |

---

## Configuración

### Archivos de Configuración

| Archivo | Descripción |
|---------|-------------|
| `agentes.json` | Configuración de los 17 agentes |
| `alertas.json` | Sistema de alertas escalonadas |
| `integraciones.json` | Integraciones disponibles |
| `permisos.json` | Perfiles de acceso |
| `mcp-config.json` | Configuración MCP |

### Variables de Entorno

Ver `.env.example` para las variables necesarias.

---

## Cómo Usar el Sistema

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
5. Envía a dirección
```

### Ejemplo 3: Crear contenido para Instagram

```
Usuario: "Haceme un post para Instagram mostrando el avance de obra"

CEO → Marketing:
1. Selecciona mejores fotos
2. Escribe copy atractivo
3. Genera hashtags relevantes
4. Sugiere horario de publicación
```

### Ejemplo 4: Análisis de rentabilidad

```
Usuario: "Analizá la rentabilidad del proyecto ENTANYQ"

CEO → Data:
1. Recopila datos de ventas
2. Calcula ROI proyectado
3. Genera dashboard
4. Presenta hallazgos
```

---

## Próximos Pasos

### Corto Plazo (1-2 semanas)
- [x] Agregar testimonios de compradores al brochure
- [x] Incluir planos de unidades
- [x] Agregar marcas de materiales
- [x] Agregar datos legales
- [ ] Configurar acceso a Google Drive

### Mediano Plazo (1-2 meses)
- [ ] Integrar con Instagram Business API
- [ ] Configurar CRM para gestión de leads
- [ ] Crear dashboard de métricas
- [ ] Automatizar envío de reportes

### Largo Plazo (3-6 meses)
- [ ] Integrar con sistemas contables
- [ ] Configurar chatbot para WhatsApp
- [ ] Crear app móvil para clientes
- [ ] Implementar IA predictiva de ventas

---

## Contacto

**ARMAT — Desarrolladora Inmobiliaria**
- Teléfono: 299 508-9366 / 299 580-6377
- Instagram: @ARMAT.DESARROLLOS

---

*Documento generado automáticamente por el sistema de agentes ARMAT*
*Última actualización: Julio 2026*
