# ARMAT — Guía Completa de Capacidades

## Sistema de Agentes Inteligentes para Desarrolladora Inmobiliaria

---

## Tabla de Contenidos

1. [Resumen del Sistema](#resumen-del-sistema)
2. [Agentes por Departamento](#agentes-por-departamento)
3. [Skills Disponibles](#skills-disponibles)
4. [Workflows Automatizados](#workflows-automatizados)
5. [Materiales de Marketing](#materiales-de-marketing)
6. [Cómo Usar el Sistema](#cómo-usar-el-sistema)
7. [Próximos Pasos](#próximos-pasos)

---

## Resumen del Sistema

| Componente | Cantidad |
|------------|----------|
| **Agentes** | 17 |
| **Skills** | 98 |
| **Workflows** | 4 |
| **Templates** | 4 |
| **Documentos de Marketing** | 3 (brochure, flyer, folleto) |

### Arquitectura

```
CEO (Orquestador)
├── Comercial
├── Marketing
├── Obras
├── Finanzas
├── Legal
├── Administración
├── Calidad
├── Clientes
├── Compras
├── IA
├── Presupuestos
├── RRHH
├── IT
├── Postventa
├── Proveedores
└── Data
```

---

## Agentes por Departamento

### 1. CEO — Director General
**Función**: Orquesta todas las operaciones, toma decisiones estratégicas y coordina entre departamentos.

**Skills**:
- Coordinar equipos
- Tomar decisiones estratégicas
- Comunicar visión
- Evaluar desempeño

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

### 4. Obras — Construcción y Supervisión
**Función**: Controla avance de obra, calidad constructiva y cumplimiento de plazos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `calcular_avance_obra` | Calcula porcentaje de avance |
| `controlar_presupuesto` | Monetiza gastos vs presupuesto |
| `generar_reporte_avance` | Crea informes de avance |
| `programar_actividades` | Planifica cronograma de obra |
| `registrar_bitacora_diaria` | Documenta actividad diaria |
| `verificar_calidad` | Inspecciona calidad constructiva |

---

### 5. Finanzas — Gestión Financiera
**Función**: Controla flujo de caja, costos, rentabilidad y reportes financieros.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `analizar_costos` | Descompone costos por rubro |
| `analizar_rentabilidad` | Calcula margen de ganancia |
| `calcular_flujo_caja` | Proyecta entradas y salidas |
| `calcular_impuestos` | Calcula obligaciones fiscales |
| `conciliar_cuentas` | Verifica movimientos bancarios |
| `evaluar_inversion` | Analiza viabilidad de proyecto |
| `generar_estado_financiero` | Crea estados contables |
| `generar_reporte_ejecutivo` | Informe para dirección |
| `presupuestar_proyecto` | Crea presupuesto de obra |
| `proyectar_ventas` | Estima ventas futuras |

---

### 6. Legal — Asesoramiento Jurídico
**Función**: Gestiona contratos, permisos, cumplimiento normativo y aspectos legales.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `consultar_normativa` | Busca leyes y regulaciones |
| `generar_informe_legal` | Crea informes jurídicos |
| `gestionar_contratos` | Administra contratos vigentes |
| `gestionar_litigios` | Maneja conflictos legales |
| `redactar_contrato` | Elabora contratos nuevos |
| `revisar_cumplimiento` | Verifica cumplimiento normativo |
| `validar_propiedad` | Verifica documentación de inmueble |
| `verificar_permisos` | Consulta permisos de construcción |

---

### 7. Administración — Gestión Operativa
**Función**: Administra recursos, proveedores, contratos y operaciones diarias.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `controlar_inventario` | Gestiona stock de materiales |
| `coordinar_logistica` | Organiza transporte y entrega |
| `elaborar_contratos` | Redacta contratos con proveedores |
| `gestionar_nomina` | Administra pagos a empleados |
| `gestionar_proveedores` | Evalúa y administra proveedores |
| `manejar_correspondencia` | Procesa documentos y emails |
| `organizar_oficina` | Gestiona recursos de oficina |
| `programar_reuniones` | Organiza reuniones y agendas |

---

### 8. Calidad — Control de Calidad
**Función**: Asegura estándares de calidad en construcción y procesos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `auditar_proceso` | Realiza auditorías de calidad |
| `generar_informe_calidad` | Crea informes de inspección |
| `inspeccionar_obra` | Visita técnica a obra |
| `verificar_materiales` | Controla calidad de materiales |

---

### 9. Clientes — Atención al Cliente
**Función**: Gestiona relación con clientes, satisfaction y soporte post-venta.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `calificar_satisfaccion` | Mide satisfacción del cliente |
| `gestionar_crm` | Administra base de datos de clientes |
| `registrar_lead` | Captura nuevos prospectos |
| `seguir_cliente` | Realiza seguimiento post-venta |

---

### 10. Compras — Adquisiciones
**Función**: Gestiona compras de materiales, cotizaciones y relación con proveedores.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `comparar_cotizaciones` | Evalúa opciones de precio |
| `evaluar_proveedor` | Califica proveedores |
| `generar_orden_compra` | Emite órdenes de compra |
| `solicitar_cotizacion` | Pide precios a proveedores |

---

### 11. IA — Inteligencia Artificial
**Función**: Aplica análisis de datos, automatización y optimización de procesos.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `analizar_datos` | Procesa datos del negocio |
| `automatizar_tarea` | Crea flujos automatizados |
| `optimizar_procesos` | Mejora eficiencia operativa |
| `predecir_tendencias` | Anticipa comportamientos del mercado |

---

### 12. Presupuestos — Control de Costos
**Función**: Crea y controla presupuestos de obra y operaciones.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `controlar_costos` | Monetiza gastos reales vs plan |
| `crear_presupuesto_obra` | Elabora presupuesto detallado |
| `generar_avance_financiero` | Reporta avance económico |
| `proyectar_cierre` | Estima cierre financiero |

---

### 13. RRHH — Recursos Humanos
**Función**: Gestiona personal, selección, capacitación y evaluación.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `calcular_nomina` | Calcula sueldos y cargas |
| `evaluar_desempeno` | Realiza evaluaciones de personal |
| `programar_capacitacion` | Organiza cursos y entrenamientos |
| `reclutar_personal` | Busca y selecciona candidatos |

---

### 14. IT — Tecnología
**Función**: Gestiona infraestructura tecnológica, seguridad y soporte.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `administrar_sistemas` | Gestiona servidores y aplicaciones |
| `configurar_red` | Administra infraestructura de red |
| `gestionar_seguridad` | Protege datos y sistemas |
| `soporte_tecnico` | Resuelve problemas técnicos |

---

### 15. Postventa — Servicio Post-Venta
**Función**: Atiende reclamos, garantías y mantenimiento.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `atender_reclamacion` | Gestiona quejas de clientes |
| `emitir_garantia` | Emite documentos de garantía |
| `medir_satisfaccion` | Evalúa experiencia del cliente |
| `programar_mantenimiento` | Agenda mantenimientos |

---

### 16. Proveedores — Gestión de Proveedores
**Función**: Evalúa, negocia y administra relación con proveedores.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `buscar_proveedor` | Localiza nuevos proveedores |
| `evaluarProveedor` | Califica proveedores existentes |
| `negociar_contrato` | Negocia condiciones comerciales |
| `seguir_pedido` | Rastrea estado de pedidos |

---

### 17. Data — Análisis de Datos
**Función**: Genera reportes, dashboards y análisis de datos del negocio.

**Skills**:
| Skill | Descripción |
|-------|-------------|
| `analizar_ventas` | Analiza performance de ventas |
| `generar_dashboard` | Crea paneles de control |
| `predecir_demanda` | Estima demanda futura |
| `reportar_kpis` | Reporta indicadores clave |

---

## Workflows Automatizados

### 1. Onboarding de Cliente
**Trigger**: Nuevo lead registrado
**Pasos**:
1. Registrar datos del lead
2. Calificar interés y capacidad de compra
3. Asignar vendedor responsable
4. Enviar información del proyecto
5. Programar primera reunión
6. Seguimiento en 48 horas

---

### 2. Control de Obra
**Trigger**: Seguimiento semanal de obra
**Pasos**:
1. Registrar avance en bitácora
2. Verificar calidad constructiva
3. Controlar presupuesto
4. Generar reporte de avance
5. Actualizar cronograma
6. Notificar a dirección

---

### 3. Compra de Materiales
**Trigger**: Necesidad de material
**Pasos**:
1. Verificar stock actual
2. Solicitar cotizaciones a proveedores
3. Comparar opciones
4. Generar orden de compra
5. Seguir entrega
6. Verificar calidad al recibir

---

### 4. Pipeline de Ventas
**Trigger**: Nuevo lead en sistema
**Pasos**:
1. Capturar datos del lead
2. Calificar interés
3. Enviar información
4. Agendar visita
5. Realizar propuesta
6. Negociar
7. Cerrar venta
8. Post-venta

---

## Materiales de Marketing

### Brochure ENTANYQ
- **Formato**: HTML vertical (430px)
- **Contenido**: Hero, descripción, empresa, datos, galería, unidades, pago, ubicación
- **Versiones**: Original + V2 corporativo
- **Archivos**: `brochure-entanyq.html`, `brochure-entanyq-v2.html`

### Flyer ENTANYQ
- **Formato**: HTML vertical (430px)
- **Contenido**: Hero, precio, galería, datos, beneficios, pago, contacto
- **Versiones**: Original + V2 corporativo
- **Archivos**: `flyer-entanyq.html`, `flyer-entanyq-v2.html`

### Folleto ENTANYQ
- **Formato**: HTML horizontal plegable (990px)
- **Contenido**: Exterior (portada, central, trasero) + Interior (empresa, unidades, beneficios)
- **Versiones**: Original + V2 corporativo
- **Archivos**: `folleto-entanyq.html`, `folleto-entanyq-v2.html`

### Versiones para Envío
Todos los materiales tienen versiones autocontenidas con imágenes embebidas (base64):
- `brochure-entanyq-v2-enviar.html`
- `flyer-entanyq-v2-enviar.html`
- `folleto-entanyq-v2-enviar.html`

---

## Cómo Usar el Sistema

### Ejemplo 1: Generar propuesta de venta

```
Usuario: "Generá una propuesta de venta para un departamento de 1 dormitorio 
          al comprador Juan Pérez, con financiación en 12 cuotas"

Agente Comercial: 
1. Verifica disponibilidad
2. Calcula financiamiento
3. Genera propuesta personalizada
4. Reserva unidad
```

### Ejemplo 2: Reporte de avance de obra

```
Usuario: "Necesito un reporte de avance de obra de la semana"

Agente Obras:
1. Recopila bitácora diaria
2. Calcula porcentaje de avance
3. Verifica calidad
4. Genera reporte ejecutivo
5. Envía a dirección
```

### Ejemplo 3: Crear contenido para Instagram

```
Usuario: "Haceme un post para Instagram mostrando el avance de obra"

Agente Marketing:
1. Selecciona mejores fotos
2. Escribe copy atractivo
3. Genera hashtags relevantes
4. Sugiere horario de publicación
```

### Ejemplo 4: Análisis de rentabilidad

```
Usuario: "Analizá la rentabilidad del proyecto ENTANYQ"

Agente Data:
1. Recopila datos de ventas
2. Calcula ROI proyectado
3. Genera dashboard
4. Presenta hallazgos
```

---

## Próximos Pasos

### Corto Plazo (1-2 semanas)
- [ ] Agregar testimonios de compradores al brochure
- [ ] Incluir planos de unidades
- [ ] Agregar marcas de materiales
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

## Estructura del Proyecto

```
Armat/
├── agents/                    # 17 agentes especializados
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
├── skills/                    # 98 skills organizados
├── workflows/                 # 4 workflows automatizados
├── templates/                 # 4 templates reutilizables
├── brand/                     # Identidad visual
├── knowledge/                 # Base de conocimiento
├── config/                    # Configuración MCP
├── img/render/                # 18 renders
├── documentos_entregados/     # Documentos originales
├── brochure-entanyq-v2.html   # Brochure V2
├── flyer-entanyq-v2.html      # Flyer V2
├── folleto-entanyq-v2.html    # Folleto V2
└── README.md                  # Documentación principal
```

---

## Contacto

**ARMAT — Desarrolladora Inmobiliaria**
- Teléfono: 299 508-9366 / 299 580-6377
- Instagram: @ARMAT.DESARROLLOS

---

*Documento generado automáticamente por el sistema de agentes ARMAT*
*Última actualización: Julio 2026*
