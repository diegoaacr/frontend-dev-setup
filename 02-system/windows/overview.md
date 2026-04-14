# 🪟 Windows Setup – Overview

En Windows existen dos formas de trabajar en desarrollo frontend:

* WSL (Windows Subsystem for Linux)
* Entorno nativo (PowerShell)

---

# 🎯 Decisión recomendada

👉 **Usar WSL como entorno principal de desarrollo**

---

# 🧠 ¿Por qué WSL?

WSL permite trabajar en un entorno Linux dentro de Windows.

Ventajas:

* Mejor compatibilidad con herramientas modernas (Node, pnpm, bundlers)
* Menos problemas con dependencias y scripts
* Entorno más cercano a producción

---

# ⚠️ Alternativa: entorno nativo

También es posible trabajar directamente en Windows usando:

* PowerShell
* Windows Terminal

👉 Esta opción es válida, pero puede presentar más fricción en proyectos modernos.

---

# 🧩 ¿Qué opción elegir?

## Usa WSL si:

* Estás empezando desde cero
* Quieres evitar problemas de compatibilidad
* Buscas un entorno más estable

## Usa entorno nativo si:

* Tienes restricciones (empresa, permisos, etc.)
* Ya tienes un entorno configurado y funcional

---

# 📌 Reglas

* No mezclar entornos (WSL y nativo en el mismo proyecto)
* Elegir una opción y mantenerla
* Priorizar consistencia sobre preferencia personal

---

# ➡️ Siguiente paso

* WSL → `wsl.md`
* Nativo → `native.md`
