# 🖥️ Frontend Dev Environment Setup (2026)

Configuración profesional del entorno de desarrollo para **frontend moderno**.
Diseñado para equipos, onboarding técnico y setups reproducibles.

Compatible con:

* Windows (WSL recomendado)
* macOS

---

# 🎯 Objetivo

Estandarizar el entorno base de desarrollo para:

* Onboarding de desarrolladores
* Formación técnica
* Equipos frontend
* Setups personales profesionales

Este repositorio define cómo preparar una máquina **desde cero** de forma limpia, consistente y sin conflictos.

---

# 🧠 Filosofía

Este entorno está diseñado bajo los siguientes principios:

* Opinionated → decisiones claras, no múltiples opciones
* Minimalista → solo lo necesario para trabajar correctamente
* Reproducible → mismo entorno en cualquier máquina
* Profesional → alineado con prácticas reales de industria
* Independiente del proyecto → no depende de frameworks ni apps

---

# ⚙️ Decisiones estándar del entorno

Este repositorio define las siguientes decisiones:

* Node.js → gestionado con version manager (fnm recomendado)
* Package Manager → pnpm
* Gestión de package manager → Corepack
* Git → autenticación mediante SSH (obligatorio)
* Commit signing → recomendado (SSH)
* Editor → VSCode
* Navegador → Chrome / Edge
* Windows → WSL como entorno recomendado

---

# 🚀 Quick Start (15–20 min)

Si ya tienes experiencia, sigue este flujo:

1. System Setup → `02-system`
2. Shell → `03-shell`
3. Git básico → `04-git/basic`
4. Node.js → `05-node`
5. Corepack → `06-package-manager/corepack.md`
6. pnpm → `06-package-manager/pnpm.md`
7. VSCode → `07-editor-vscode`
8. Verificación → `11-verification`

---

# 📦 Archivos de configuración incluidos

Este repositorio incluye algunos archivos de configuración para mantener una experiencia consistente entre desarrolladores y sistemas operativos.

* `.editorconfig` → mantiene reglas básicas de formato (indentación, espacios, etc.)
* `.prettierrc` → define formato automático del código
* `.gitignore` → evita subir archivos innecesarios al repositorio
* `.vscode/settings.json` → configuración recomendada del editor
* `.vscode/extensions.json` → extensiones sugeridas para VSCode
* `scripts/` → scripts de verificación del entorno

👉 Estos archivos **no necesitan ser modificados al comenzar**.
Su objetivo es estandarizar el entorno y evitar diferencias entre máquinas.

---

# 📚 Estructura del repositorio

## 00 – Introducción

* Contexto del entorno
* Objetivos
* Definition of Done
* Requisitos previos

---

## 01 – Standard Decisions

Documento clave del repositorio:

* Stack definido
* Reglas del entorno
* Herramientas oficiales
* Qué es obligatorio vs opcional

---

## 02 – System Setup

### Windows

* WSL (recomendado)
* Alternativa: PowerShell nativo

### macOS

* Configuración base del sistema
* PATH
* Permisos

### Common

* Variables de entorno
* Configuración global

---

## 03 – Shell

### Windows

* WSL (bash/zsh)
* PowerShell (opcional)

### macOS

* zsh como shell estándar

### Common

* Alias básicos
* Prompt limpio

---

## 04 – Git (Base mínima)

Solo lo necesario para comenzar:

* Instalación
* Configuración básica
* SSH Keys
* Commit signing (recomendado)

📌 Git avanzado → repositorio dedicado

---

## 05 – Node.js

* Instalación mediante version manager (fnm / nvm)
* Uso de versiones LTS
* Verificación del entorno

---

## 06 – Package Manager

### Corepack

* Qué es
* Por qué usarlo
* Activación

### pnpm

* Instalación
* Configuración base
* Uso recomendado

---

## 07 – Editor (VSCode)

### Base

* Instalación
* settings.json
* Extensiones esenciales

### Profiles & Sync

* Perfiles de trabajo
* Sincronización entre dispositivos

### Remote Development

* WSL
* Dev Containers (introducción)

---

## 08 – Browser & DevTools

* Chrome / Edge
* Configuración básica
* Debugging y performance

---

## 09 – Seguridad

### Base

* SSH
* 2FA
* Buenas prácticas

### Corporate

* Proxy
* Certificados
* Registry privado

---

## 10 – Opcional (Nivel Pro)

* Dev Containers
* WSL (profundización)

---

## 11 – Verificación & Troubleshooting

Validación final del entorno:

```bash
git --version
ssh -T git@github.com
node -v
corepack --version
pnpm -v
code -v
```

---

# ✅ Definition of Done

El entorno está listo cuando:

* Git funciona mediante SSH
* Node LTS está correctamente instalado
* Corepack está habilitado
* pnpm funciona sin errores
* VSCode abre desde terminal
* DevTools está operativo

---

# 🚫 Qué NO cubre este repositorio

Este repo NO incluye:

* Arquitectura frontend
* Bundlers (Vite, RSBuild, etc.)
* Frameworks (React, etc.)
* Testing
* CI/CD
* Dockerización de aplicaciones
* Estrategias avanzadas de Git

👉 Todo esto se cubrirá en repositorios especializados.

---

# 🧩 Repositorios relacionados (futuro)

Este repositorio forma parte de una arquitectura mayor:

* Frontend Engineering Standards
* Git Advanced Workflow
* React + Tailwind + Architecture
* Testing & Quality
* CI/CD & DevOps Frontend

---

# 💡 Nota final

Este repositorio no busca enseñar herramientas.

Busca asegurar que todos los desarrolladores parten de una base:

* limpia
* consistente
* profesional

---

# 🚀 Estado del proyecto

En construcción — evolucionando hacia un estándar profesional de entorno frontend.
