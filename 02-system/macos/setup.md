# 🍎 macOS Setup

Este módulo prepara macOS como entorno base para desarrollo frontend.

---

# 🎯 Objetivo

Dejar el sistema listo para instalar herramientas de desarrollo sin conflictos.

---

# ⚙️ Preparación

## 1. Actualizar sistema

Asegúrate de tener macOS actualizado desde:

* System Settings → General → Software Update

---

## 2. Instalar herramientas base

Ejecuta en Terminal:

```bash id="j6n8p2"
xcode-select --install
```

Esto instala:

* herramientas de línea de comandos
* compiladores necesarios

---

## 3. Verificar shell

macOS usa `zsh` por defecto.

Verifica:

```bash id="v3kq9a"
echo $SHELL
```

Debe mostrar algo como:

```bash id="3e2w9p"
/bin/zsh
```

---

## 4. Revisar entorno limpio

Evita configuraciones previas conflictivas:

* múltiples versiones de Node
* instalaciones manuales antiguas
* configuraciones no documentadas

---

# 🔍 Verificación

Comprueba que el sistema está listo:

```bash id="xk3j8s"
xcode-select -p
```

Debe devolver una ruta válida.

---

# ⚠️ Problemas comunes

## Herramientas no instaladas

* Ejecutar nuevamente: `xcode-select --install`

---

## Permisos

* Aceptar prompts del sistema al instalar herramientas

---

# ✅ Resultado esperado

* Sistema actualizado
* Herramientas base instaladas
* Terminal lista para uso

---

# ➡️ Siguiente paso

Continúa con:

👉 `03-shell`
