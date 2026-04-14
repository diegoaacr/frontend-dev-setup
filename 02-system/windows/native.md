# 🪟 Windows Setup (Native)

Este módulo describe el uso de Windows en entorno nativo (sin WSL).

---

# 🎯 Objetivo

Permitir trabajar en desarrollo frontend directamente en Windows usando PowerShell.

---

# ⚠️ Contexto

👉 Esta opción es alternativa.

El entorno recomendado es:

* WSL → ver `wsl.md`

---

# 🧠 Cuándo usar este entorno

Usa Windows nativo si:

* No puedes instalar WSL (restricciones de empresa)
* Ya tienes un entorno funcional configurado
* Necesitas trabajar directamente con herramientas de Windows

---

# ⚙️ Preparación

## 1. Actualizar sistema

Asegúrate de tener Windows actualizado.

---

## 2. Usar Windows Terminal

Instala y usa:

* Windows Terminal
* PowerShell

---

## 3. Verificar entorno limpio

Evita configuraciones previas conflictivas:

* múltiples versiones de Node
* instalaciones manuales antiguas
* PATH desordenado

---

# ⚠️ Limitaciones

Trabajar en entorno nativo puede generar:

* incompatibilidades con scripts Unix
* problemas con dependencias
* diferencias respecto a entornos de producción

---

# 📌 Reglas

* No mezclar con WSL en el mismo proyecto
* Mantener una sola configuración de herramientas
* Evitar instalaciones duplicadas

---

# ✅ Resultado esperado

* Terminal lista para uso (PowerShell)
* Sistema preparado para instalar herramientas

---

# ➡️ Siguiente paso

Continúa con:

👉 `03-shell`
