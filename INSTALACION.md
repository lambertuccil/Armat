# Guía de Instalación — ARMAT en otra PC

## Requisitos Mínimos

| Componente | Mínimo | Recomendado |
|------------|--------|-------------|
| **Sistema** | Windows 10 / macOS 12 / Ubuntu 20 | Windows 11 / macOS 14 / Ubuntu 22 |
| **RAM** | 8 GB | 16 GB |
| **Disco** | 5 GB libres | 10 GB libres |
| **Internet** | Sí (obligatorio para IA) | Conexión estable |

---

## Paso 1: Instalar OpenCode

OpenCode es la plataforma donde corren los agentes.

### Windows (PowerShell)
```powershell
winget install opencode
```

### macOS / Linux
```bash
curl -fsSL https://opencode.ai/install | bash
```

**Verificar instalación:**
```bash
opencode --version
```

---

## Paso 2: Clonar el Repositorio

```bash
git clone https://github.com/lambertuccil/Armat.git
cd Armat
```

Si no tenés Git instalado:
- **Windows**: `winget install Git.Git`
- **macOS**: `xcode-select --install`
- **Ubuntu**: `sudo apt install git`

---

## Paso 3: Configurar la API Key de IA

El sistema necesita un modelo de IA. La opción recomendada es **MiMo V2.5 Free** (gratuita).

### Opción A: MiMo V2.5 Free (Recomendada — GRATIS)

1. Crear cuenta en [OpenRouter](https://openrouter.ai)
2. Ir a **Keys** → **Create Key**
3. Copiar la key

### Opción B: Claude Sonnet 4 (De pago — API de Anthropic)

1. Crear cuenta en [console.anthropic.com](https://console.anthropic.com)
2. Ir a **API Keys** → **Create Key**
3. Copiar la key

### Configurar en OpenCode

```bash
opencode config
```

O crear el archivo manualmente en `~/.config/opencode/opencode.json`:

```json
{
  "provider": {
    "openrouter": {
      "apiKey": "TU-AQUI-VA-LA-KEY"
    }
  },
  "model": {
    "default": "mimo-v2.5-free"
  }
}
```

---

## Paso 4: Instalar MCP Servers (Opcional — Mejora la funcionalidad)

Los MCP servers son servidores que amplían las capacidades del sistema.

### Engram (Memoria persistente)

```bash
# Descargar engram desde GitHub
# https://github.com/engram-ai/engram
# Seguir instrucciones del README del repo
```

### DuckDB (Análisis financiero)

```bash
# Windows
winget install duckdb

# macOS
brew install duckdb

# Ubuntu
sudo apt install duckdb
```

### Context7 (Documentación de librerías)

Context7 es un servicio remoto, no necesita instalación local. Se configura en OpenCode automáticamente.

### Nucleus (Gobierno y seguridad)

```bash
# Descargar desde GitHub
# https://github.com/nucleus-ai/nucleus
# Seguir instrucciones del README del repo
```

---

## Paso 5: Configurar Integraciones (Opcional)

Las integraciones conectan el sistema con servicios externos.

### Google Drive / Gmail / Calendar

1. Ir a [Google Cloud Console](https://console.cloud.google.com)
2. Crear un proyecto nuevo
3. Habilitar las APIs: Gmail, Drive, Calendar
4. Crear credenciales OAuth 2.0
5. Descargar `credentials.json`
6. Copiar a `integrations/gmail/credentials.json`

### WhatsApp Business API

1. Ir a [Meta for Developers](https://developers.facebook.com)
2. Crear una app con WhatsApp Business API
3. Obtener token y Phone ID
4. Copiar a `.env`:

```
WHATSAPP_PHONE_ID=tu-phone-id
WHATSAPP_TOKEN=tu-token
```

---

## Paso 6: Verificar que Todo Funciona

```bash
# Abrir OpenCode en el directorio del proyecto
cd Armat
opencode
```

### Probar un agente

Escribí en el chat de OpenCode:

```
CEO: ¿Cuánto sale el departamento de 1 dormitorio?
```

El sistema debería:
1. Activar el agente CEO
2. Delegar al agente Comercial
3. Responder con la cotización

---

## Estructura de Archivos Importante

```
C:\IA\Armat\
├── agents/          ← Los 17 agentes (NO modificar salvo que sepas)
├── skills/          ← Las 98 habilidades (NO modificar)
├── base-conocimiento/ ← Datos de construcción y legislación
├── plantillas/      ← Contratos, emails, marketing
├── config/          ← Configuración del sistema
├── proyectos/       ← Proyectos específicos (ENTANYQ, etc.)
├── integrations/    ← Credenciales de servicios externos
├── GUIA-COMPLETA-ARMAT.html  ← Guía visual del sistema
└── .env.example     ← Template de variables de entorno
```

---

## Archivos que NO se suben a Git (por seguridad)

Estos archivos quedan solo en tu PC:

- `.env` (credenciales)
- `integrations/*/credentials.json` (credenciales Google)
- `config/local.json` (configuración local)
- `config/secrets.json` (secretos)
- `*.key`, `*.pem`, `*.cert` (certificados)

---

## Solución de Problemas

### "No se encuentra opencode"
→ Verificá que esté en el PATH: `opencode --version`

### "API key inválida"
→ Verificá la key en el dashboard del proveedor (OpenRouter o Anthropic)

### "Agente no responde"
→ Verificá que tengas conexión a internet y que la API key sea válida

### "No encuentra archivos del proyecto"
→ Asegurate de estar en el directorio correcto: `cd Armat`

### "Error de MCP server"
→ Los MCP servers son opcionales. El sistema funciona sin ellos, pero con menos funcionalidades.

---

## Resumen Rápido

```bash
# 1. Instalar OpenCode
winget install opencode          # Windows
curl -fsSL https://opencode.ai/install | bash  # macOS/Linux

# 2. Clonar repositorio
git clone https://github.com/lambertuccil/Armat.git
cd Armat

# 3. Configurar API key (elegir una)
opencode config                  # Seguir instrucciones

# 4. ¡Listo!
opencode
```

**Tiempo estimado de instalación**: 10-15 minutos

---

*Guía creada para ARMAT — Desarrolladora Inmobiliaria*
*Julio 2026*
