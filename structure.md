# 📁 Estructura del repositorio

```bash
frontend-dev-setup/
│
├─ README.md                          # Portada: propósito, alcance, quick start
├─ LICENSE                            # MIT (u otra licencia)
├─ .gitignore                         # Node, logs, OS, editor, etc.
├─ .editorconfig                      # Estilo consistente entre editores
├─ .prettierrc                        # Formato base (MD, JSON, etc.)
│
├─ .vscode/
│  ├─ extensions.json                 # Extensiones recomendadas
│  └─ settings.json                   # Configuración base del editor
│
├─ scripts/
│  ├─ check-env.sh                    # Verificación entorno (macOS / WSL)
│  └─ check-env.ps1                   # Verificación entorno (Windows)
│
├─ 00-introduction/
│  └─ readme.md                       # Contexto, objetivos, definition of done
│
├─ 01-standard-decisions/
│  └─ readme.md                       # Stack definido, reglas y decisiones del entorno
│
├─ 02-system/
│  ├─ windows/
│  │  ├─ wsl.md                       # Instalación y uso de WSL (recomendado)
│  │  └─ native.md                    # Alternativa: PowerShell nativo
│  │
│  ├─ macos/
│  │  └─ setup.md                     # Configuración base del sistema
│  │
│  └─ common/
│     └─ config.md                    # Variables de entorno, PATH, ajustes globales
│
├─ 03-shell/
│  ├─ windows/
│  │  ├─ wsl-shell.md                 # Bash/Zsh en WSL
│  │  └─ powershell.md                # Configuración PowerShell (opcional)
│  │
│  ├─ macos/
│  │  └─ zsh.md                       # Shell estándar macOS
│  │
│  └─ common/
│     ├─ alias.md                     # Alias recomendados
│     └─ prompt.md                    # Prompt limpio y minimalista
│
├─ 04-git/
│  └─ basic/
│     ├─ installation.md              # Instalación Git
│     ├─ config.md                    # user.name, user.email, defaults
│     ├─ ssh.md                       # Configuración SSH
│     └─ signing.md                   # Commit signing (recomendado)
│
├─ 05-node/
│  ├─ windows.md                      # Instalación con fnm/nvm en Windows
│  ├─ macos.md                        # Instalación con fnm/nvm en macOS
│  └─ verification.md                 # Validación Node LTS
│
├─ 06-package-manager/
│  ├─ corepack.md                     # Gestión de versiones de package managers
│  ├─ pnpm.md                         # Instalación y uso de pnpm
│  └─ troubleshooting.md              # Problemas comunes (registry, proxy, PATH)
│
├─ 07-editor-vscode/
│  ├─ base/
│  │  ├─ installation.md              # Instalación VSCode
│  │  ├─ settings.md                  # Configuración base
│  │  └─ extensions.md                # Extensiones esenciales
│  │
│  ├─ profiles-sync.md                # Profiles + Settings Sync
│  └─ remote-dev.md                   # WSL y Dev Containers (intro)
│
├─ 08-browser/
│  ├─ browser.md                      # Chrome / Edge setup
│  └─ devtools.md                     # Configuración DevTools
│
├─ 09-security/
│  ├─ base.md                         # SSH, 2FA, buenas prácticas
│  └─ corporate.md                    # Proxy, certificados, registry privado
│
├─ 10-optional/
│  ├─ devcontainers.md                # Entornos reproducibles (VSCode)
│  └─ wsl-advanced.md                 # Uso avanzado de WSL
│
├─ 11-verification/
│  └─ checklist.md                    # Validación final del entorno
│
└─ ROADMAP.md                         # Evolución futura del repo
```

---

# 🧠 Cómo leer esta estructura

El repositorio está organizado en capas:

### 1. Base conceptual

* `00-introduction`
* `01-standard-decisions`

👉 Define el **por qué y el estándar**

---

### 2. Setup del entorno

* `02-system`
* `03-shell`
* `04-git`
* `05-node`
* `06-package-manager`

👉 Define el **cómo instalar todo correctamente**

---

### 3. Herramientas de desarrollo

* `07-editor-vscode`
* `08-browser`

👉 Define el **entorno de trabajo diario**

---

### 4. Seguridad y contexto real

* `09-security`

👉 Pensado para entornos profesionales

---

### 5. Nivel avanzado (opcional)

* `10-optional`

👉 No obligatorio, pero recomendado en equipos modernos

---

### 6. Validación final

* `11-verification`

👉 Garantiza que todo funciona correctamente

---

# 🎯 Principios de organización

* Separación clara por sistema operativo (Windows / macOS)
* Configuración común centralizada (`common`)
* Cada herramienta tiene su propio módulo
* Evitar archivos gigantes → todo modular
* Preparado para escalar sin romper estructura

---

# 🚀 Escalabilidad futura

Este repositorio está diseñado para convivir con otros:

* frontend-architecture
* git-advanced
* react-standards
* testing-quality
* ci-cd-devops

👉 Cada uno con responsabilidad independiente

---

# 💡 Nota

Este repo NO busca cubrir todo el ecosistema frontend.

Busca asegurar una base sólida, consistente y profesional desde la cual construir cualquier proyecto.
