# 🧩 Alias básicos

Este módulo define alias simples para mejorar la productividad en terminal sin agregar complejidad innecesaria.

---

# 🎯 Objetivo

Tener una base mínima de alias útiles y fáciles de recordar.

---

# 📌 Criterios

Los alias de este repositorio deben ser:

* cortos
* claros
* fáciles de mantener
* opcionales, pero consistentes

👉 No deben reemplazar comandos importantes ni ocultar comportamientos complejos.

---

# ✅ Alias recomendados

```bash id="1lgkpi"
alias ll="ls -la"
alias la="ls -A"
alias ..="cd .."
alias ...="cd ../.."
alias gs="git status"
alias gl="git log --oneline --graph --decorate"
alias gc="git commit"
alias gp="git push"
```

---

# 🧠 Notas

* `ll` y `la` ayudan a navegar más rápido
* `..` y `...` simplifican movimiento entre carpetas
* `gs`, `gl`, `gc` y `gp` cubren operaciones frecuentes de Git

---

# ⚠️ Reglas

* No agregar alias innecesarios
* Evitar alias demasiado personales
* Mantener los mismos alias entre entornos siempre que sea posible

---

# ➡️ Siguiente paso

Continúa con:

👉 `common/prompt.md`
