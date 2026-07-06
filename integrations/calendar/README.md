# Google Calendar MCP - Integración para Estudio Jurídico

## Descripción

Integración MCP para gestionar el calendario del estudio jurídico. Permite a los agentes crear, modificar y consultar eventos relacionados con audiencias, plazos procesales y citas con clientes.

**Agentes que la utilizan:** agente-agenda

---

## Requisitos previos

- Node.js 18+ instalado
- Cuenta de Google Workspace (o Gmail personal)
- Acceso a Google Cloud Console
- Proyecto de Google Cloud ya creado

---

## Paso 1: Habilitar Google Calendar API

1. Ir a [Google Cloud Console](https://console.cloud.google.com/)
2. Seleccionar el proyecto del estudio
3. Ir a **APIs y servicios** → **Library**
4. Buscar "Google Calendar API"
5. Click en **Google Calendar API** → **Habilitar**

---

## Paso 2: Configurar alcances de Calendar

En la pantalla de consentimiento OAuth, agregar estos alcances:

- `https://www.googleapis.com/auth/calendar`
- `https://www.googleapis.com/auth/calendar.events`
- `https://www.googleapis.com/auth/calendar.readonly`

Si reutilizas credenciales existentes, agregar estos alcances a la lista.

---

## Paso 3: Obtener Refresh Token

Usa el mismo método que en Gmail (ver `integrations/gmail/README.md`), pero con los alcances de Calendar:

```javascript
const scopes = [
  'https://www.googleapis.com/auth/calendar',
  'https://www.googleapis.com/auth/calendar.events',
  'https://www.googleapis.com/auth/calendar.readonly'
];
```

---

## Paso 4: Configurar Calendar ID

### Para un calendario específico del estudio

1. Abrir Google Calendar
2. Ir a **Configuración** (⚙️) → **Calendarios**
3. Seleccionar el calendario del estudio
4. Copiar el **Calendar ID** (formato: `abc123@group.calendar.google.com`)

### Para usar el calendario principal

Usar `primary` como Calendar ID (usará el calendario predeterminado de la cuenta).

### Recomendación: Crear calendario dedicado

Crear un calendario específico para el estudio:

1. En Google Calendar, click en **+** junto a "Otros calendarios"
2. **Crear nuevo calendario**
3. Nombre: `Estudio Jurídico - Audiencias y Plazos`
4. Descripción: `Calendario para gestión de audiencias, plazos procesales y citas del estudio`
5. Copiar el Calendar ID

---

## Paso 5: Configurar el archivo config.json

```json
{
  "env": {
    "GOOGLE_CLIENT_ID": "123456789-abc.apps.googleusercontent.com",
    "GOOGLE_CLIENT_SECRET": "GOCSPX-tu-secreto",
    "GOOGLE_REFRESH_TOKEN": "1//0tu-refresh-token",
    "CALENDAR_ID": "abc123@group.calendar.google.com"
  },
  "habilitada": true
}
```

---

## Paso 6: Probar la conexión

```bash
# Probar el servidor MCP
npx -y @modelcontextprotocol/server-google-calendar
```

### Prueba rápida con opencode

1. Habilitar la integración
2. Reiniciar opencode
3. Preguntar: "¿Qué eventos hay mañana en el calendario del estudio?"

---

## Gestión de plazos procesales

### Tipos de plazos a registrar

| Tipo de plazo | Ejemplo | Antelación |
|---------------|---------|------------|
| Contestación de demanda | 15 días hábiles | 3 días antes |
| Apelación | 5 días hábiles | 1 día antes |
| Período de prueba | 30 días | 7 días antes |
| Sentencia (estimada) | Variable | 1 día antes |
| Audiencia de conciliación | Fecha fija | 1 día antes |

### Evento de plazo procesal

```
Título: [EXPEDIENTE] Plazo vence - [DESCRIPCIÓN]
Fecha: [FECHA LÍMITE]
Hora: 09:00
Descripción:
- Expediente: [NÚMERO]
- Carátula: [CAUSA]
- Plazo: [DÍAS] días hábiles
- Vence: [FECHA]
- Acción requerida: [ACCIÓN]
```

### Evento de audiencia

```
Título: [AUDIENCIA] [TIPO] - [EXPEDIENTE]
Fecha: [FECHA]
Hora: [HORA]
Descripción:
- Tipo: [AUDIENCIA/CONCILIACIÓN/JUICIO]
- Expediente: [NÚMERO]
- Carátula: [CAUSA]
- Juzgado: [JUZGADO]
- Juez: [NOMBRE]
- Lugar: [DIRECCIÓN]
- Documentación: [LISTA]
```

---

## Uso por agente-agenda

El agente-agenda puede:

### Consultar
- Ver eventos del día/semana/mes
- Buscar audiencias por expediente
- Verificar disponibilidad horaria
- Listar plazos próximos a vencer

### Crear
- Agendar audiencias
- Programar recordatorios
- Bloquear horarios para reuniones
- Crear eventos recurrentes (reuniones de equipo)

### Modificar
- Reagendar audiencias
- Actualizar información de eventos
- Agregar notas a eventos existentes
- Cancelar eventos

### Alertas
- Plazos que vencen en 3 días
- Audiencias de mañana
- Plazos vencidos sin acción

---

## Configuración de recordatorios

### Para audiencias
- 1 día antes: Recordatorio al abogado responsable
- 2 horas antes: Alerta final

### Para plazos procesales
- 5 días antes: Primer recordatorio
- 3 días antes: Segundo recordatorio
- 1 día antes: Alerta urgente

---

## Seguridad

- **NUNCA** incluir detalles sensibles en títulos de eventos
- Usar códigos de expediente, no nombres de clientes
- Configurar permisos de calendario (solo lectura para algunos usuarios)
- Mantener respaldo de eventos importantes
- Revisar permisos de compartición periódicamente

---

## Solución de problemas

### Error "calendarNotFound"
- Verificar que el `CALENDAR_ID` sea correcto
- La cuenta debe tener acceso al calendario

### Error "insufficientPermissions"
- Los alcances de Calendar no están configurados
- Repetir el Paso 2

### Error "timeZoneInvalid"
- Configurar la zona horaria en Google Calendar
- Usar `America/Argentina/Buenos_Aires` para Neuquén

---

## Zona horaria

Para Neuquén, Argentina, configurar:
- Zona horaria: `America/Argentina/Buenos_Aires` (UTC-3)
- No aplica horario de verano (Argentina no cambia más)

---

## Referencias

- [Google Calendar API Documentation](https://developers.google.com/calendar/api)
- [Calendario Argentinado](https://www.argentina.gob.ar/interior/feriados-nacionales-2024)
- [MCP Server Google Calendar](https://github.com/modelcontextprotocol/servers)
