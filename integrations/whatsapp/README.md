# WhatsApp MCP - Integración para Estudio Jurídico

## Descripción

Integración MCP para enviar y recibir mensajes de WhatsApp. Permite a los agentes comunicarse con clientes y contactos del estudio jurídico.

**Agentes que la utilizan:** ceo, agente-admision, agente-cobranzas

---

## ⚠️ Consideraciones Éticas y Legales

**IMPORTANTE:** Antes de habilitar esta integración, considerar:

1. **Protección de datos personales:** La Ley 25.326 de Protección de Datos Personales (Argentina) requiere consentimiento para comunicaciones
2. **Información sensible:** NUNCA enviar por WhatsApp:
   - Detalles de expedientes
   - Documentos judiciales
   - Información de contraparte
   - Datos bancarios o financieros
3. **Registro de comunicaciones:** Todas las interacciones quedan registradas
4. **Horarios de contacto:** Respetar horarios laborales (8-20hs en Argentina)
5. **Consentimiento:** Obtener autorización del cliente para recibir mensajes

**Política del estudio:** Usar WhatsApp solo para:
- Confirmación de turnos
- Recordatorios de audiencias (sin detalles)
- Estados generales de expedientes ("en trámite", "pendiente")
- Comunicaciones administrativas

---

## Requisitos previos

- Node.js 18+ instalado
- Cuenta de WhatsApp Business o WhatsApp Business API
- Número de teléfono verificado

---

## Opción 1: WhatsApp Business API (Recomendada para estudios)

### Configurar Meta Business Suite

1. Ir a [Meta for Developers](https://developers.facebook.com/)
2. Crear una cuenta de desarrollador
3. Ir a **My Apps** → **Create App**
4. Seleccionar tipo: **Business**
5. Nombre: `Juridico WhatsApp`
6. Ir a **WhatsApp** → **API Setup**
7. Copiar el **Phone Number ID** y **Temporary Access Token**

### Obtener credenciales permanentes

1. En **WhatsApp** → **API Setup**
2. Click en **Generate access token**
3. El token expira en 24 horas
4. Para token permanente, configurar OAuth:
   - Crear app de Facebook
   - Solicitar permisos de WhatsApp
   - Usar System User Token

### Limitaciones

- Costo por mensaje (aprox. $0.05-0.10 USD por mensaje en Argentina)
- Límite de 1000 mensajes/mes para cuentas nuevas
- Requiere verificación de Meta para volúmenes altos

---

## Opción 2: Twilio WhatsApp API (Alternativa)

### Configurar Twilio

1. Crear cuenta en [Twilio](https://www.twilio.com/)
2. Activar WhatsApp Sandbox (para pruebas)
3. Obtener **Account SID** y **Auth Token**
4. Configurar número de WhatsApp remitente

### Ventajas de Twilio

- Más fácil de configurar
- Sandbox para pruebas
- Soporte técnico en español
- Pricing más predecible

### Desventajas

- Costo adicional por mensaje
- Dependencia de servicio externo
- Latencia adicional

---

## Opción 3: WhatsApp Web (No recomendada para producción)

**NO recomendada** para estudios jurídicos por:
- Viola términos de servicio de WhatsApp
- Riesgo de bloqueo permanente del número
- No cumple con normativa de protección de datos
- Sin soporte oficial

---

## Paso 1: Elegir proveedor

Para un estudio jurídico en Neuquén, recomendamos:
- **Producción:** Meta WhatsApp Business API
- **Pruebas:** Twilio WhatsApp Sandbox

---

## Paso 2: Obtener credenciales

### Para Meta WhatsApp Business API

```json
{
  "env": {
    "WHATSAPP_PHONE_ID": "1234567890",
    "WHATSAPP_TOKEN": "tu-access-token-permanente"
  }
}
```

### Para Twilio (alternativa)

```json
{
  "env": {
    "WHATSAPP_PHONE_ID": "+5492991234567",
    "WHATSAPP_TOKEN": "tu-auth-token-twilio"
  }
}
```

---

## Paso 3: Configurar el archivo config.json

```json
{
  "env": {
    "WHATSAPP_PHONE_ID": "1234567890",
    "WHATSAPP_TOKEN": "tu-access-token"
  },
  "habilitada": true,
  "notas": "Configurado para Meta WhatsApp Business API"
}
```

---

## Paso 4: Configurar plantillas de mensajes

### Plantilla de confirmación de turno

```
Estudio Jurídico [Nombre]
Turno confirmado para el [FECHA] a las [HORA]
Lugar: [DIRECCIÓN]
Por favor, traer DNI y documentación del caso.
```

### Plantilla de recordatorio de audiencia

```
Estudio Jurídico [Nombre]
Recordatorio: Audiencia programada para [FECHA]
Hora: [HORA]
Lugar: [TRIBUNAL]
No olvide traer su documentación.
```

### Plantilla de estado de expediente

```
Estudio Jurídico [Nombre]
Estado del expediente [NÚMERO]:
[ESTADO GENERAL - sin detalles sensibles]
Para más información, comunicarse al [TELÉFONO].
```

---

## Paso 5: Probar la conexión

1. En Twilio: usar el sandbox para enviar mensajes de prueba
2. En Meta: usar el número de prueba proporcionado
3. Verificar recepción del mensaje

### Prueba con opencode

1. Habilitar la integración
2. Reiniciar opencode
3. Preguntar: "Envía un mensaje de prueba al número +5492991234567"

---

## Seguridad

- **NUNCA** enviar información sensible por WhatsApp
- **NUNCA** commitear tokens de acceso
- Usar números dedicados para el estudio
- Configurar mensajes de respuesta automática fuera de horario
- Mantener registro de todas las comunicaciones
- Revisar logs periódicamente

---

## Solución de problemas

### Error "invalid_token"
- El token de acceso expiró
- Generar nuevo token en Meta Business Suite o Twilio

### Error "phone_number_not_verified"
- El número no está verificado en WhatsApp Business
- Completar proceso de verificación

### Error "rate_limit_exceeded"
- Demasiados mensajes en poco tiempo
- Implementar rate limiting en los agentes

---

## Normativa aplicable

- **Ley 25.326** - Protección de Datos Personales
- **Ley 26.994** - Código Civil y Comercial (arts. 1525-1536 sobre comunicaciones)
- **Resolución 17/2018** - Defensa del Consumidor (comunicaciones comerciales)
- **RGPD** (si hay clientes europeos)

---

## Referencias

- [WhatsApp Business API Documentation](https://developers.facebook.com/docs/whatsapp)
- [Twilio WhatsApp Documentation](https://www.twilio.com/docs/whatsapp)
- [Ley 25.326 - Protección de Datos Personales](https://www.argentina.gob.ar/normativa/nacional/25326)
