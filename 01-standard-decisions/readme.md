# ⚙️ Standard Decisions

Este documento define las decisiones oficiales del entorno de desarrollo.

Su objetivo es:

* Asegurar consistencia entre desarrolladores
* Evitar conflictos de configuración
* Estandarizar el onboarding técnico

---

# 🧠 Principio

> Todos los desarrolladores trabajan con el mismo stack base.

Estas decisiones deben respetarse en todos los entornos.

---

# 🖥️ Sistema operativo

* **Windows → WSL (recomendado)**
* **macOS → entorno nativo**

---

# 💻 Shell

* macOS → `zsh`
* Windows (WSL) → `bash` o `zsh`
* Windows (nativo) → PowerShell (solo si es necesario)

---

# 🧬 Node.js

* Instalación mediante **version manager**

  * Recomendado: `fnm`
  * Alternativa: `nvm`

* Uso exclusivo de versiones **LTS**

* ❌ No instalar Node manualmente

---

# 📦 Package Manager

* Manager principal → **pnpm**
* Gestión de versiones → **Corepack**

## Reglas

* Todos los proyectos usan `pnpm`
* La versión debe definirse en `package.json`

```json
{
  "packageManager": "pnpm@9.x"
}
```

---

# 🔐 Git

* Autenticación → **SSH (obligatorio)**
* Configuración base → `user.name`, `user.email`
* Commit signing → recomendado (SSH)

---

# 🧑‍💻 Editor

* Editor estándar → **VSCode**

## Reglas

* Uso de configuración compartida (`.vscode`)
* Uso de extensiones recomendadas
* Uso de Settings Sync

---

# 🌐 Navegador

* Estándar → **Chrome o Edge**

Uso:

* DevTools
* Performance
* Network

---

# 🧪 Entorno reproducible

* Dev Containers → recomendado en equipos
* No obligatorio para proyectos simples

---

# 🔒 Seguridad

* Uso de SSH keys seguras
* Activación de 2FA
* No exponer credenciales

---

# 🚫 Restricciones

Para mantener consistencia:

* ❌ Instalar Node manualmente
* ❌ Usar múltiples package managers
* ❌ Usar HTTPS en Git
* ❌ Configuraciones no documentadas

---

# 🎯 Resultado esperado

Un entorno donde:

* todos los desarrolladores trabajan igual
* no hay conflictos de versiones
* el entorno es predecible
* el onboarding es rápido
