# Google Drive MCP - Integración para Estudio Jurídico

## Descripción

Integración MCP para acceder y gestionar documentos del estudio jurídico en Google Drive. Permite a los agentes buscar, subir, descargar y organizar expedientes y documentos legales.

**Agentes que la utilizan:** agente-legal, agente-admision

---

## Requisitos previos

- Node.js 18+ instalado
- Cuenta de Google Workspace (o Gmail personal)
- Acceso a Google Cloud Console
- Proyecto de Google Cloud ya creado (puede usar el mismo que Gmail)

---

## Paso 1: Habilitar Google Drive API

1. Ir a [Google Cloud Console](https://console.cloud.google.com/)
2. Seleccionar el proyecto del estudio (`juridico-mcp-gmail` o crear uno nuevo)
3. Ir a **APIs y servicios** → **Library**
4. Buscar "Google Drive API"
5. Click en **Google Drive API** → **Habilitar**

---

## Paso 2: Usar credenciales existentes o crear nuevas

Si ya configuraste Gmail MCP, puedes reutilizar las credenciales OAuth. Solo necesitas agregar el alcance de Drive.

### Si necesitas credenciales nuevas:

1. Ir a **APIs y servicios** → **Credenciales**
2. Click en **+ Crear credenciales** → **ID de cliente de OAuth**
3. Tipo: **Aplicación de escritorio**
4. Nombre: `Juridico MCP Drive`
5. Copiar ID y Secreto

---

## Paso 3: Configurar alcances de Drive

En la pantalla de consentimiento OAuth, agregar estos alcances:

- `https://www.googleapis.com/auth/drive.readonly`
- `https://www.googleapis.com/auth/drive.file`
- `https://www.googleapis.com/auth/drive.metadata.readonly`

Si reutilizas credenciales de Gmail, agregar estos alcances a la lista existente.

---

## Paso 4: Obtener Refresh Token

Usa el mismo método que en Gmail (ver `integrations/gmail/README.md`), pero con los alcances de Drive:

```javascript
const scopes = [
  'https://www.googleapis.com/auth/drive.readonly',
  'https://www.googleapis.com/auth/drive.file',
  'https://www.googleapis.com/auth/drive.metadata.readonly'
];
```

---

## Paso 5: Configurar carpeta raíz del estudio

### Crear estructura de carpetas en Google Drive

Recomendamos esta estructura para un estudio jurídico en Neuquén:

```
📁 Estudio Jurídico Neuquén (carpeta raíz)
├── 📁 01-Expedientes
│   ├── 📁 Penales
│   ├── 📁 Civiles
│   ├── 📁 Laborales
│   ├── 📁 Familia
│   └── 📁 Administrativos
├── 📁 02-Documentos
│   ├── 📁 Contratos
│   ├── 📁 Poderes
│   ├── 📁 Certificados
│   └── 📁 Plantillas
├── 📁 03-Correspondencia
│   ├── 📁 Entrante
│   └── 📁 Saliente
├── 📁 04-Facturacion
│   ├── 📁 Facturas
│   ├── 📁 Presupuestos
│   └── 📁 Comprobantes
├── 📁 05-Archivo
│   └── (expedientes cerrados)
└── 📁 06-Administracion
    ├── 📁 RRHH
    ├── 📁 Estudios
    └── 📁 Capacitacion
```

### Obtener el Folder ID

1. Abrir la carpeta raíz en Google Drive
2. El URL será: `https://drive.google.com/drive/folders/1ABC123def456...`
3. El `Folder ID` es: `1ABC123def456...`
4. Copiar ese ID para usar en la configuración

---

## Paso 6: Configurar el archivo config.json

```json
{
  "env": {
    "GOOGLE_CLIENT_ID": "123456789-abc.apps.googleusercontent.com",
    "GOOGLE_CLIENT_SECRET": "GOCSPX-tu-secreto",
    "GOOGLE_REFRESH_TOKEN": "1//0tu-refresh-token",
    "GOOGLE_FOLDER_ID": "1ABC123def456..."
  },
  "habilitada": true
}
```

---

## Paso 7: Probar la conexión

```bash
# Probar el servidor MCP
npx -y @modelcontextprotocol/server-google-drive
```

### Prueba rápida con opencode

1. Habilitar la integración
2. Reiniciar opencode
3. Preguntar: "¿Qué expedientes hay en la carpeta de Penales?"

---

## Uso por agentes

### agente-legal
- Buscar expedientes por cliente o número
- Descargar documentos para análisis
- Subir escritos y presentaciones
- Organizar documentación por materia

### agente-admision
- Crear carpetas para nuevos clientes
- Subir documentos de admisión
- Verificar documentación incompleta
- Gestionar plantillas de contratos

---

## Seguridad

- **NUNCA** compartir el Folder ID del estudio en repositorios públicos
- Usar permisos de solo lectura cuando sea posible
- Revisar periódicamente qué cuentas tienen acceso
- Mantener respaldo local de documentos críticos
- Configurar versionado en Google Drive para documentos importantes

---

## Solución de problemas

### Error "fileNotFound"
- Verificar que el `GOOGLE_FOLDER_ID` sea correcto
- La carpeta debe estar en la cuenta de Google vinculada

### Error "insufficientPermissions"
- Los alcances de Drive no están configurados
- Repetir el Paso 3

### Error "dailyLimitExceeded"
- Límite de API alcanzado
- Esperar 24 horas o solicitar aumento de cuota

---

## Referencias

- [Google Drive API Documentation](https://developers.google.com/drive/api)
- [Manage Google Drive Files](https://support.google.com/drive/answer/2424368)
- [MCP Server Google Drive](https://github.com/modelcontextprotocol/servers)
