# Guía de Instalación Completa — ARMAT

**Sistema Operativo creado por Lambertucci Leandro**

---

## Resumen de lo que necesitás instalar

| # | Componente | Obligatorio | Tamaño |
|---|-----------|-------------|--------|
| 1 | Git | Sí | ~50 MB |
| 2 | Node.js (v20+) | Sí | ~100 MB |
| 3 | OpenCode CLI | Sí | ~200 MB |
| 4 | Repositorio ARMAT | Sí | ~50 MB |
| 5 | API Key de IA (OpenRouter) | Sí | Gratis |
| 6 | Engram (memoria persistente) | Recomendado | ~30 MB |
| 7 | Skills globales (52 packs) | Recomendado | ~200 MB |
| 8 | Nucleus MCP | Opcional | ~50 MB |
| 9 | DuckDB MCP | Opcional | ~20 MB |

---

## Paso 1: Instalar Git

### Windows
```powershell
winget install Git.Git
```
Cerrar y abrir PowerShell después de instalar.

### macOS
```bash
xcode-select --install
```

### Linux (Ubuntu/Debian)
```bash
sudo apt update && sudo apt install git -y
```

### Verificar
```bash
git --version
```
Debe mostrar algo como `git version 2.x.x`

---

## Paso 2: Instalar Node.js

OpenCode necesita Node.js v20 o superior.

### Windows
```powershell
winget install OpenJS.NodeJS.LTS
```

### macOS
```bash
brew install node
```

### Linux
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install nodejs -y
```

### Verificar
```bash
node --version   # Debe mostrar v20.x.x o superior
npm --version    # Debe mostrar 10.x.x o superior
```

---

## Paso 3: Instalar OpenCode CLI

### Windows / macOS / Linux
```bash
npm install -g @anthropic-ai/opencode
```

### Verificar
```bash
opencode --version
```

### Si no funciona el comando global
```bash
npx @anthropic-ai/opencode --version
```

---

## Paso 4: Clonar el Repositorio ARMAT

```bash
# Elegí dónde querés tener el proyecto
cd C:\IA                          # Windows
# cd ~/Projects                  # macOS/Linux

git clone https://github.com/lambertuccil/Armat.git
cd Armat
```

### Verificar estructura
```bash
dir                                 # Windows
# ls                               # macOS/Linux
```

Deberías ver:
```
agents/          (17 carpetas de agentes)
skills/          (98 skills)
base-conocimiento/
plantillas/
config/
integrations/
brand/
workflows/
proyectos/
GUIA-COMPLETA-ARMAT.html
README.md
INSTALACION.md
```

---

## Paso 5: Configurar la API Key de IA

### Opción A: OpenRouter (Recomendada — GRATIS con MiMo V2.5)

1. Ir a **https://openrouter.ai**
2. Crear cuenta (gratis)
3. Ir a **Keys** → **Create Key**
4. Copiar la key (empieza con `sk-or-...`)

### Opción B: Anthropic (De pago)

1. Ir a **https://console.anthropic.com**
2. Crear cuenta
3. Ir a **API Keys** → **Create Key**
4. Copiar la key (empieza con `sk-ant-...`)

### Configurar en OpenCode

```bash
opencode config
```

O crear manualmente el archivo `~/.config/opencode/opencode.json`:

```json
{
  "provider": {
    "openrouter": {
      "apiKey": "sk-or-VACÍO-AQUÍ-TU-KEY"
    }
  },
  "model": {
    "default": "mimo-v2.5-free"
  }
}
```

**Nota**: En Windows la ruta es `C:\Users\TU-USUARIO\.config\opencode\opencode.json`

---

## Paso 6: Instalar Engram (Memoria Persistente)

Engram permite que el sistema recuerde entre sesiones.

### Opción A: Descargar binario (recomendado)

1. Ir a **https://github.com/engram-ai/engram/releases**
2. Descargar la versión para tu sistema:
   - Windows: `engram-windows-x64.exe`
   - macOS: `engram-macos-arm64` o `engram-macos-x64`
   - Linux: `engram-linux-x64`
3. Crear carpeta y mover el ejecutable:

```bash
# Windows
mkdir C:\Users\TU-USUARIO\Egram
move engam.exe C:\Users\TU-USUARIO\Egram\engram.exe

# macOS/Linux
mkdir -p ~/Egram
mv engram ~/Egram/engram
chmod +x ~/Egram/engram
```

### Opción B: Compilar desde fuente

```bash
git clone https://github.com/engram-ai/engram.git
cd engram
cargo build --release
# El binario queda en target/release/engram
```

### Verificar
```bash
C:\Users\TU-USUARIO\Egram\engram.exe --version    # Windows
~/Egram/engram --version                          # macOS/Linux
```

### Configurar en OpenCode

En `opencode.json`, sección `mcp`:
```json
{
  "mcp": {
    "engram": {
      "command": ["C:\\Users\\TU-USUARIO\\Egram\\engram.exe", "mcp", "--tools=agent"],
      "type": "local"
    }
  }
}
```

---

## Paso 7: Instalar Skills Globales (Recomendado)

Los skills son las habilidades que los agentes usan. En esta PC hay 52 packs instalados.

### Skills que vienen con el repo ARMAT

Ya están en `C:\IA\Armat\skills\` — no necesitan instalación adicional.

### Skills globales de OpenCode (mejoran la experiencia)

Los skills globales van en `~/.config/opencode/skills/`. En esta PC hay:

**Pack principal:**
- `superpowers` — Framework base de skills (brainstorming, TDD, debugging, etc.)

**Skills de código:**
- `react-19`, `nextjs-15`, `angular-core`, `angular-architecture`, `angular-forms`, `angular-performance`
- `typescript`, `tailwind-4`, `zod-4`, `zustand-5`
- `spring-boot-3`, `java-21`, `hexagonal-architecture-layers-java`
- `django-drf`, `electron`, `go-testing`, `pytest`, `playwright`, `react-native`

**Skills de producto:**
- `gstack` — Suite completa de desarrollo (review, QA, ship, deploy, etc.)
- `claude-para-legal` — 22 categorías de derecho (inmobiliario, fiscal, laboral, etc.)
- `claude-seo` — 24 skills de SEO técnico, contenido, schemas, etc.
- `servicios-financieros` — Análisis financiero
- `skills-de-marketing` — Estrategia de marketing
- `skills-redes-sociales` — Marketing en redes sociales
- `frontend-design` — Diseño UI
- `cognitive-doc-design` — Documentación

**Skills de operaciones:**
- `sdd-*` (10 skills) — Spec-Driven Development
- `conventional-commit`, `release-please`, `pre-commit`
- `branch-pr`, `chained-pr`, `github-pr`, `work-unit-commits`
- `skill-creator`, `skill-improver`, `skill-registry`

### Cómo instalarlos

```bash
# Clonar el pack superpowers (necesario para casi todo)
cd ~/.config/opencode/skills
git clone https://github.com/opencode-ai/superpowers.git

# Los demás se instalan igual — clonar en la carpeta de skills
# Revisar cada repo para instrucciones específicas
```

**Nota**: Los skills no son estrictamente obligatorios. El sistema ARMAT funciona sin ellos, pero con menos funcionalidades auxiliares.

---

## Paso 8: Instalar Nucleus MCP (Opcional)

Nucleus provee herramientas de gobierno, seguridad y orquestación multi-agente.

### Instalar
```bash
npm install -g nucleus-mcp
```

### Configurar en OpenCode

En `opencode.json`:
```json
{
  "mcp": {
    "nucleus": {
      "type": "local",
      "command": ["nucleus-mcp"],
      "enabled": true,
      "environment": {
        "NUCLEUS_BRAIN_PATH": ".brain"
      }
    }
  }
}
```

---

## Paso 9: Instalar DuckDB MCP (Opcional)

DuckDB permite análisis financiero con SQL.

### Instalar
```bash
pip install mcp-server-duckdb
# O con uvx (viene con uv)
uvx mcp-server-duckdb --help
```

### Configurar en OpenCode

En `opencode.json`:
```json
{
  "mcp": {
    "duckdb": {
      "type": "local",
      "command": ["uvx", "mcp-server-duckdb", "--db-path", ":memory:"],
      "enabled": true
    }
  }
}
```

---

## Paso 10: Configurar Variables de Entorno (Opcional)

Si querés integraciones con Google, WhatsApp, etc.:

```bash
cd C:\IA\Armat
copy .env.example .env     # Windows
# cp .env.example .env     # macOS/Linux
```

Editar `.env` con tus credenciales. Ver `integrations/` para documentación de cada servicio.

---

## Paso 11: Verificar que Todo Funciona

```bash
cd C:\IA\Armat
opencode
```

### Probar el sistema

Escribí en el chat de OpenCode:

```
¿Cuánto sale el departamento de 1 dormitorio?
```

El sistema debe:
1. Activar el agente CEO
2. Delegar al agente Comercial
3. Responder con la cotización

### Probar memoria (si instalaste Engram)

```
¿De qué hablamos la última vez?
```

Si Engram funciona, el sistema recordará conversaciones anteriores.

---

## Archivos de Configuración Importantes

| Archivo | Ubicación | Qué hace |
|---------|-----------|----------|
| `opencode.json` | `~/.config/opencode/` | Config principal de OpenCode |
| `AGENTS.md` | `C:\IA\Armat\` | Define agentes MCP del proyecto |
| `.env` | `C:\IA\Armat\` | Credenciales (NO subir a git) |
| `agents/` | `C:\IA\Armat\agents\` | Instrucciones de los 17 agentes |
| `skills/` | `C:\IA\Armat\skills\` | 98 skills del sistema |
| `config/` | `C:\IA\Armat\config\` | Configuración del sistema |

---

## Estructura del `opencode.json` Completo

```json
{
  "agent": {
    "armat-ceo": { ... },
    "armat-comercial": { ... },
    "armat-marketing": { ... },
    "armat-obras": { ... },
    "armat-finanzas": { ... },
    "armat-legal": { ... },
    "armat-administracion": { ... },
    "armat-calidad": { ... },
    "armat-clientes": { ... },
    "armat-compras": { ... },
    "armat-ia": { ... },
    "armat-presupuestos": { ... }
  },
  "mcp": {
    "engram": { ... },
    "nucleus": { ... },
    "duckdb": { ... },
    "context7": { ... }
  }
}
```

**Nota**: El `opencode.json` completo con los 17 agentes está en `C:\Users\Lean\.config\opencode\opencode.json`. Copiarlo a la nueva PC.

---

## Archivos que NO se Suben a Git (Seguridad)

- `.env` — Credenciales
- `integrations/*/credentials.json` — Credenciales Google
- `config/local.json` — Configuración local
- `config/secrets.json` — Secretos
- `*.key`, `*.pem`, `*.cert` — Certificados
- `.brain/` — Datos de memoria local

---

## Troubleshooting

### "opencode no se encuentra"
→ Verificar que esté en el PATH: `npm list -g @anthropic-ai/opencode`
→ Si no está: `npm install -g @anthropic-ai/opencode`

### "API key inválida"
→ Verificar la key en el dashboard del proveedor
→ OpenRouter: https://openrouter.ai/keys
→ Anthropic: https://console.anthropic.com/settings/keys

### "Agente no responde"
→ Verificar conexión a internet
→ Verificar que la API key sea válida
→ Probar con `opencode --verbose` para ver logs

### "Engram no funciona"
→ Verificar que el path en `opencode.json` sea correcto
→ Verificar que `engram.exe` esté en la ruta indicada
→ Probar directamente: `C:\Users\TU-USUARIO\Egram\engram.exe --version`

### "Skills no aparecen"
→ Verificar que estén en `~/.config/opencode/skills/`
→ Verificar que cada skill tenga un `SKILL.md`

### "No encuentra archivos del proyecto"
→ Asegurate de estar en el directorio correcto: `cd C:\IA\Armat`

---

## Instalación Express (Copiar de una PC a otra)

Si ya tenés todo funcionando en una PC y querés clonar en otra:

### En la PC origen
```bash
# Comprimir todo menos .git y archivos sensibles
cd C:\IA
tar -czf armat-backup.tar.gz --exclude='.git' --exclude='*.env' --exclude='.brain' Armat
```

### En la PC destino
```bash
# Copiar el backup (USB, red, etc.)
# Luego descomprimir
tar -xzf armat-backup.tar.gz

# Copiar opencode.json
copy C:\Users\Lean\.config\opencode\opencode.json C:\Users\TU-USUARIO\.config\opencode\

# Copiar engram
copy C:\Users\Lean\Egram\engram.exe C:\Users\TU-USUARIO\Egram\

# Instalar OpenCode si no está
npm install -g @anthropic-ai/opencode
```

---

## Resumen de Comandos (Copia y pega)

```bash
# 1. Git
winget install Git.Git

# 2. Node.js
winget install OpenJS.NodeJS.LTS

# 3. OpenCode
npm install -g @anthropic-ai/opencode

# 4. Clonar ARMAT
git clone https://github.com/lambertuccil/Armat.git
cd Armat

# 5. API Key
opencode config

# 6. Engram
mkdir C:\Users\TU-USUARIO\Egram
# Descargar engram.exe desde GitHub y moverlo ahí

# 7. ¡Listo!
opencode
```

**Tiempo estimado**: 15-20 minutos (sin skills globales) / 30-40 minutos (con todo)

---

## Checklist de Verificación

- [ ] `git --version` funciona
- [ ] `node --version` muestra v20+
- [ ] `opencode --version` funciona
- [ ] `C:\IA\Armat\` existe y tiene la estructura correcta
- [ ] API key configurada en `opencode.json`
- [ ] `opencode` abre sin errores
- [ ] Escribir "hola" genera respuesta del sistema
- [ ] Engram responde (opcional): `C:\Users\TU-USUARIO\Egram\engram.exe --version`

---

*Sistema Operativo ARMAT creado por Lambertucci Leandro*
*Guía de instalación — Julio 2026*
