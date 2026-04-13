# 🖥️ Frontend Dev Environment Setup (2026)

Configuración profesional del entorno de desarrollo para **frontend moderno**.
Pensado para onboarding técnico, equipos y setups reproducibles.

Compatible con:

* Windows
* macOS

---

# 🎯 Objetivo

Definir una base de entorno limpia, consistente y profesional para comenzar a desarrollar proyectos frontend desde cero.

Este repositorio está orientado a:

* Onboarding de desarrolladores
* Formación técnica
* Equipos frontend
* Setups personales profesionales

---

# ⚙️ Stack base definido

Este entorno está basado en decisiones estándar:

* Node.js con version manager
* pnpm como package manager principal
* Corepack para gestionar versiones del package manager
* Git con autenticación SSH
* VSCode como editor estándar
* Chrome / Edge para desarrollo y debugging
* WSL como opción recomendada en Windows

📌 Las decisiones completas del entorno están documentadas en `01-standard-decisions`.

---

# 🚀 Quick Start

Si ya tienes experiencia, sigue este flujo:

1. System Setup → `02-system`
2. Shell → `03-shell`
3. Git básico → `04-git`
4. Node.js → `05-nodejs`
5. Package Manager → `06-package-managers`
6. VSCode → `07-editor`
7. Browser & DevTools → `08-browser`
8. Verificación → `11-verification`

Para entender el contexto, alcance y definición de entorno listo, revisa `00-introduction` antes de comenzar.

---

# 📦 Archivos de configuración incluidos

Este repositorio incluye archivos de apoyo para mantener una experiencia consistente entre desarrolladores y sistemas operativos.

* `.editorconfig` → reglas básicas de formato
* `.prettierrc` → formato automático
* `.gitignore` → exclusión de archivos innecesarios
* `.vscode/settings.json` → configuración recomendada del editor
* `.vscode/extensions.json` → extensiones sugeridas
* `scripts/` → scripts de verificación del entorno

👉 Estos archivos no necesitan modificarse al comenzar.
Su objetivo es reducir diferencias entre máquinas y mantener una base compartida.

---

# 📚 Estructura del repositorio

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

# 🚫 Alcance del repositorio

Este repositorio cubre únicamente la **configuración base del entorno de desarrollo**.

No incluye:

* Arquitectura frontend
* Bundlers
* Frameworks
* Testing
* CI/CD
* Dockerización de aplicaciones
* Estrategias avanzadas de Git

👉 Estos temas se cubrirán en repositorios especializados.

---

# 🧩 Repositorios relacionados (futuro)

Este repositorio forma parte de una arquitectura mayor orientada a estándares de desarrollo frontend:

* Frontend Engineering Standards
* Git Advanced Workflow
* React + Tailwind + Architecture
* Testing & Quality
* CI/CD & DevOps Frontend

---

# 🚀 Estado del proyecto

En construcción — evolucionando hacia un estándar profesional de entorno frontend.
