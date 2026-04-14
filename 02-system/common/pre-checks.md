# 🧪 Pre-checks del sistema

Antes de comenzar la configuración del entorno, es importante validar el estado actual de la máquina.

Este paso ayuda a evitar conflictos y problemas durante la instalación.

---

# 🎯 Objetivo

Asegurar que el sistema está en condiciones adecuadas antes de instalar herramientas de desarrollo.

---

# 🔍 Qué revisar

## 1. Instalaciones previas

Verifica si ya tienes instaladas herramientas como:

* Node.js
* Git
* Package managers (npm, yarn, pnpm)

👉 Si existen, identifica cómo fueron instaladas.

---

## 2. Versiones activas

Comprueba versiones actuales:

```bash id="cq3k5z"
node -v
npm -v
git --version
```

👉 Esto te permite detectar configuraciones previas que puedan interferir.

---

## 3. PATH del sistema

Asegúrate de que no haya rutas duplicadas o conflictivas.

Problemas comunes:

* múltiples instalaciones de Node
* herramientas instaladas en rutas no estándar

---

## 4. Tipo de máquina

Identifica si estás en:

* máquina nueva → entorno limpio
* máquina reutilizada → posible conflicto de configuraciones

---

# ⚠️ Recomendaciones

* Evita mezclar múltiples formas de instalar una misma herramienta
* No combines instaladores manuales con version managers
* Mantén el entorno lo más limpio posible

---

# ✅ Resultado esperado

Al finalizar este paso:

* conoces el estado actual del sistema
* sabes si hay posibles conflictos
* estás listo para continuar con la configuración

---

# ➡️ Siguiente paso

Continúa con:

* Windows → `windows/overview.md`
* macOS → `macos/setup.md`
