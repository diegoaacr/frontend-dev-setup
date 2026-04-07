# ⚙️ Standard Decisions

Este documento define las decisiones oficiales del entorno de desarrollo.

Su objetivo es:

* Evitar ambigüedad en herramientas
* Asegurar consistencia entre desarrolladores
* Reducir problemas de configuración
* Estandarizar el onboarding técnico

---

# 🧠 Principio clave

> Todos los desarrolladores deben trabajar con el mismo stack base.

No se recomienda modificar estas decisiones sin un motivo justificado.

---

# 🖥️ Sistema operativo

## Windows

* Uso recomendado: **WSL (Windows Subsystem for Linux)**
* Alternativa: PowerShell (solo si es necesario)

## macOS

* Uso estándar: entorno nativo con zsh

---

# 💻 Shell

* macOS → `zsh`
* Windows (WSL) → `bash` o `zsh`
* Windows (nativo) → PowerShell (opcional)

👉 Se priorizan shells tipo Unix para compatibilidad con tooling moderno.

---

# 🧬 Node.js

* Instalación mediante **version manager**

  * Recomendado: `fnm`
  * Alternativa: `nvm`

* Uso exclusivo de versiones **LTS**

* ❌ No instalar Node manualmente desde web oficial

---

# 📦 Package Manager

## Manager principal

* **pnpm**

## Gestión de versiones

* **Corepack**

---

## Reglas

* Todos los proyectos deben usar `pnpm`
* La versión del package manager debe estar definida en `package.json`

Ejemplo:

```json
{
  "packageManager": "pnpm@9.x"
}
```

---

# 🔐 Git

## Autenticación

* Uso obligatorio de **SSH**

## Configuración base

* `user.name`
* `user.email`

## Commit signing

* Recomendado: **SSH signing**

---

# 🧑‍💻 Editor

## Editor estándar

* **VSCode**

## Reglas

* Uso de configuración compartida (`.vscode`)
* Uso de extensiones recomendadas
* Uso de Settings Sync entre dispositivos

---

# 🌐 Navegador

* Recomendado: **Chrome o Edge**

## Uso

* DevTools para debugging
* Performance analysis
* Network inspection

---

# 🧪 Entorno reproducible (opcional)

## Dev Containers

* Uso recomendado en equipos
* No obligatorio para proyectos simples

---

# 🔒 Seguridad

* Uso de SSH keys seguras
* Activación de 2FA en servicios
* No exponer credenciales en repositorios

---

# 🚫 Herramientas no recomendadas

Para mantener consistencia:

* ❌ Instalar Node manualmente
* ❌ Usar múltiples package managers en un mismo proyecto
* ❌ Usar autenticación HTTPS en Git
* ❌ Configuraciones personales no documentadas

---

# 📌 Notas importantes

* Este documento define el estándar del entorno
* No es una guía paso a paso (eso está en otros módulos)
* Las decisiones aquí deben respetarse en todos los setups

---

# 🎯 Objetivo final

Un entorno donde:

* todos los desarrolladores trabajan igual
* no hay conflictos de versiones
* el onboarding es rápido
* el entorno es predecible

---

# 🚀 Resultado

Un estándar base sólido para desarrollo frontend profesional.
