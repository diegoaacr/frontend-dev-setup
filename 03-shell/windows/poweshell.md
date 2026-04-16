# 🪟 PowerShell

PowerShell es el shell nativo de Windows.

Este módulo cubre su uso como alternativa cuando no se utiliza WSL.

---

# 🎯 Objetivo

Tener un entorno funcional en PowerShell sin complejidad innecesaria.

---

# 📍 Archivo de configuración

El perfil de PowerShell se encuentra en:

```powershell
$PROFILE
```

Puedes abrirlo con:

```powershell
notepad $PROFILE
```

---

# ⚙️ Configuración base

Incluye únicamente lo necesario:

* alias básicos
* variables de entorno necesarias

👉 Mantén la configuración simple y fácil de mantener.

---

# ✅ Recomendaciones

* Usa Windows Terminal como interfaz
* Mantén consistencia con alias definidos en `common`
* Documenta cualquier personalización adicional

---

# ⚠️ Qué evitar

* configuraciones complejas desde el inicio
* instalar múltiples herramientas de personalización
* mezclar configuraciones con WSL

---

# 🧠 Nota

PowerShell es una opción válida, pero puede presentar diferencias respecto a entornos Unix.

Siempre que sea posible, se recomienda trabajar con WSL.

---

# ➡️ Siguiente paso

Continúa con:

👉 `04-git`
