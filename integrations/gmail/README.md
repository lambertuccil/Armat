# Gmail MCP - Integración para Estudio Jurídico

## Descripción

Integración MCP para acceder al correo electrónico del estudio jurídico a través de Gmail. Permite a los agentes leer, buscar y gestionar emails de forma automatizada.

**Agentes que la utilizan:** ceo, agente-admision, agente-cobranzas

---

## Requisitos previos

- Node.js 18+ instalado
- Cuenta de Google Workspace (o Gmail personal)
- Acceso a Google Cloud Console

---

## Paso 1: Crear proyecto en Google Cloud Console

1. Ir a [Google Cloud Console](https://console.cloud.google.com/)
2. Click en el selector de proyectos (barra superior) → **Nuevo proyecto**
3. Nombre: `juridico-mcp-gmail`
4. Click en **Crear**
5. Seleccionar el proyecto recién creado

---

## Paso 2: Habilitar Gmail API

1. En el menú lateral, ir a **APIs y servicios** → **Library**
2. Buscar "Gmail API"
3. Click en **Gmail API** → **Habilitar**

---

## Paso 3: Configurar pantalla de consentimiento OAuth

1. Ir a **APIs y servicios** → **Pantalla de consentimiento OAuth**
2. Seleccionar tipo de usuario: **Externo** (si no tienes dominio de Google Workspace)
3. Completar información de la app:
   - Nombre de la aplicación: `Juridico MCP Gmail`
   - Email de soporte: tu email
   - Email de notificaciones: tu email
4. Click en **Guardar y continuar**
5. En **Alcances**, agregar:
   - `https://www.googleapis.com/auth/gmail.readonly`
   - `https://www.googleapis.com/auth/gmail.send`
   - `https://www.googleapis.com/auth/gmail.modify`
6. Click en **Guardar y continuar**
7. En **Usuarios de prueba**, agregar tu email de Google
8. Click en **Guardar**

---

## Paso 4: Generar credenciales OAuth

1. Ir a **APIs y servicios** → **Credenciales**
2. Click en **+ Crear credenciales** → **ID de cliente de OAuth**
3. Tipo de aplicación: **Aplicación de escritorio**
4. Nombre: `Juridico MCP Gmail`
5. Click en **Crear**
6. Copiar el **ID de cliente** y el **Secreto del cliente**
7. Descargar el archivo JSON (opcional, pero útil)

---

## Paso 5: Obtener Refresh Token

### Usando la herramienta de Google (recomendado)

```bash
# Instalar la herramienta
npm install -g google-auth-library

# Crear script temporal para obtener el token
node -e "
const { google } = require('google-auth-library');
const readline = require('readline');

const oauth2Client = new google.auth.OAuth2(
  'TU_CLIENT_ID',
  'TU_CLIENT_SECRET',
  'http://localhost:3000/oauth2callback'
);

const authUrl = oauth2Client.generateAuthUrl({
  access_type: 'offline',
  scope: [
    'https://www.googleapis.com/auth/gmail.readonly',
    'https://www.googleapis.com/auth/gmail.send',
    'https://www.googleapis.com/auth/gmail.modify'
  ]
});

console.log('Abre esta URL en tu navegador:');
console.log(authUrl);

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question('Pega el código de autorización aquí: ', async (code) => {
  const { tokens } = await oauth2Client.getToken(code);
  console.log('Refresh Token:', tokens.refresh_token);
  rl.close();
});
"
```

### Método alternativo (cURL)

1. Abrir esta URL en el navegador (reemplazar `TU_CLIENT_ID`):

```
https://accounts.google.com/o/oauth2/auth?client_id=TU_CLIENT_ID&redirect_uri=http://localhost:3000&response_type=code&scope=https://www.googleapis.com/auth/gmail.readonly&access_type=offline
```

2. Autorizar la aplicación
3. Copiar el `code` de la URL de redireccionamiento
4. Intercambiar el código por tokens:

```bash
curl -X POST https://oauth2.googleapis.com/token \
  -d "client_id=TU_CLIENT_ID" \
  -d "client_secret=TU_CLIENT_SECRET" \
  -d "code=TU_CODIGO" \
  -d "redirect_uri=http://localhost:3000" \
  -d "grant_type=authorization_code"
```

---

## Paso 6: Configurar el archivo config.json

Editar `config.json` con las credenciales obtenidas:

```json
{
  "env": {
    "GMAIL_CLIENT_ID": "123456789-abc.apps.googleusercontent.com",
    "GMAIL_CLIENT_SECRET": "GOCSPX-tu-secreto",
    "GMAIL_REFRESH_TOKEN": "1//0tu-refresh-token"
  },
  "habilitada": true
}
```

---

## Paso 7: Probar la conexión

```bash
# Desde la raíz del proyecto
cd integrations/gmail

# Probar el servidor MCP
npx -y @modelcontextprotocol/server-gmail
```

Si no hay errores, la integración está funcionando.

### Prueba rápida con opencode

1. Habilitar la integración en `config.json`: `"habilitada": true`
2. Reiniciar opencode
3. Preguntar al agente: "¿Cuántos emails nuevos tengo?"

---

## Seguridad

- **NUNCA** commitear credenciales al repositorio
- Los archivos `.env` y `credentials.json` están en `.gitignore`
- Usar variables de entorno en producción
- Rotar credenciales periódicamente
- Revisar permisos de la cuenta de servicio

---

## Solución de problemas

### Error "invalid_grand"
- El refresh token expiró o fue revocado
- Repetir el Paso 5 para obtener un nuevo token

### Error "access_not_configured"
- La Gmail API no está habilitada
- Verificar en Google Cloud Console → APIs y servicios

### Error "deleted_client"
- El proyecto de Google Cloud fue eliminado
- Crear un nuevo proyecto y repetir todo el proceso

---

## Referencias

- [Gmail API Documentation](https://developers.google.com/gmail/api)
- [OAuth 2.0 for Desktop Apps](https://developers.google.com/identity/protocols/oauth2/native-app)
- [MCP Server Gmail](https://github.com/modelcontextprotocol/servers)
