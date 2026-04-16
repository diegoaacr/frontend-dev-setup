# 🐧 Shell en WSL

Cuando se usa WSL, el shell de trabajo será `bash` o `zsh` dentro del entorno Linux.

---

# 🎯 Objetivo

Tener una terminal consistente y compatible con herramientas modernas de desarrollo.

---

# 📍 Archivo de configuración

La configuración del shell vive dentro del entorno Linux.

Archivos comunes:

```bash id="iqx3y3"
~/.bashrc
~/.zshrc
```

---

# ⚙️ Configuración base

Incluye únicamente lo necesario:

* alias básicos
* variables de entorno necesarias
* configuración mínima del prompt

👉 Mantén la configuración simple y cercana a la de macOS siempre que sea posible.

---

# ✅ Recomendaciones

* Trabaja siempre dentro del entorno Linux
* Usa una sola configuración principal por shell
* Mantén alias y comportamiento consistentes con otros entornos

---

# ⚠️ Qué evitar

* mezclar configuración de Windows y WSL
* trabajar en rutas de Windows para proyectos activos
* duplicar lógica entre varios archivos de shell

---

# 🧠 Nota

WSL es el entorno recomendado en Windows porque ofrece una experiencia más cercana a Linux y menor fricción con tooling moderno.

---

# ➡️ Siguiente paso

Continúa con:

👉 `windows/powershell.md`
