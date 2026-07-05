# MCP Integrations — ConstructoraAI

## Integraciones Disponibles

### 1. Gmail (Google Mail)
- **Propósito**: Enviar y recibir emails
- **Uso**: Comunicación con clientes, proveedores, equipo
- **Agentes**: Todos

#### Configuración
```json
{
  "gmail": {
    "type": "remote",
    "url": "https://mcp.gmail.com/mcp"
  }
}
```

#### Uso por Agente
- **Comercial**: Enviar propuestas, seguimiento
- **Marketing**: Campañas de email
- **Legal**: Contratos, notificaciones
- **Postventa**: Confirmaciones, encuestas

---

### 2. Google Drive
- **Propósito**: Almacenamiento y gestión de documentos
- **Uso**: Contratos, presupuestos, reportes, fotos
- **Agentes**: Todos

#### Configuración
```json
{
  "gdrive": {
    "type": "remote",
    "url": "https://mcp.gdrive.com/mcp"
  }
}
```

#### Uso por Agente
- **Obras**: Fotos de avance, bitácoras
- **Legal**: Contratos firmados
- **Finanzas**: Estados financieros
- **Marketing**: Materiales, renders

---

### 3. WhatsApp Business
- **Propósito**: Comunicación con clientes
- **Uso**: Seguimiento, notificaciones, soporte
- **Agentes**: Comercial, Clientes, Postventa

#### Configuración
```json
{
  "whatsapp": {
    "type": "remote",
    "url": "https://mcp.whatsapp.com/mcp"
  }
}
```

#### Uso por Agente
- **Comercial**: Seguimiento de leads
- **Clientes**: Notificaciones
- **Postventa**: Soporte post-venta

---

### 4. Calendario Google
- **Propósito**: Gestión de eventos y reuniones
- **Uso**: Visitas, juntas, mantenimientos
- **Agentes**: Todos

#### Configuración
```json
{
  "gcalendar": {
    "type": "remote",
    "url": "https://mcp.gcalendar.com/mcp"
  }
}
```

#### Uso por Agente
- **Comercial**: Visitas a clientes
- **Obras**: Juntas de proyecto
- **Postventa**: Mantenimientos
- **RRHH**: Reuniones, entrevistas

---

### 5. Google Sheets
- **Propósito**: Hojas de cálculo colaborativas
- **Uso**: Presupuestos, inventarios, reportes
- **Agentes**: Finanzas, Presupuestos, Compras

#### Configuración
```json
{
  "gsheets": {
    "type": "remote",
    "url": "https://mcp.gsheets.com/mcp"
  }
}
```

#### Uso por Agente
- **Finanzas**: Estados financieros
- **Presupuestos**: Control de costos
- **Compras**: Inventarios
- **Data**: Análisis de datos

---

### 6. Slack
- **Propósito**: Comunicación interna del equipo
- **Uso**: Notificaciones, coordinación
- **Agentes**: Todos

#### Configuración
```json
{
  "slack": {
    "type": "remote",
    "url": "https://mcp.slack.com/mcp"
  }
}
```

#### Uso por Agente
- **Todos**: Notificaciones de status
- **Obras**: Alertas de avance
- **Compras**: Aprobaciones
- **Calidad**: No conformidades

---

## Instalación

1. Agregar configuración en `opencode.json` bajo `mcp`
2. Autenticar cada servicio
3. Configurar permisos por agente
4. Probar integraciones

## Notas
- Todas las integraciones son remotas (cloud)
- Requieren autenticación OAuth
- Los datos se almacenan en la nube de cada servicio
- Respetar políticas de privacidad de datos
