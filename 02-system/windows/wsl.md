# 🐧 WSL Setup (Windows)

Este módulo configura WSL como entorno principal de desarrollo en Windows.

---

# 🎯 Objetivo

Tener un entorno Linux funcional dentro de Windows para desarrollo frontend.

---

# ⚙️ Instalación

## 1. Instalar WSL

Ejecuta en PowerShell como administrador:

```bash
wsl --install
```

Esto instalará:

* WSL
* Distribución Linux (Ubuntu por defecto)

---

## 2. Reiniciar el sistema

Después de la instalación, reinicia Windows.

---

## 3. Abrir WSL por primera vez

Abre:

* "Ubuntu" desde el menú inicio

Se te pedirá:

* crear usuario
* crear contraseña

---

## 4. Actualizar sistema Linux

Dentro de WSL ejecuta:

```bash
sudo apt update && sudo apt upgrade -y
```

---

# 📁 Ubicación de proyectos

👉 Trabaja dentro del sistema Linux:

```bash
/home/tu-usuario/
```

❌ Evita trabajar en rutas como:

```bash
/mnt/c/
```

---

# 🔍 Verificación

Comprueba que WSL funciona correctamente:

```bash
wsl -l -v
```

Debe mostrar:

* distribución instalada
* estado: Running
* versión: 2

---

# ⚠️ Problemas comunes

## WSL no inicia

* Reiniciar sistema
* Ejecutar PowerShell como administrador

---

## Permisos o errores de instalación

* Verificar que la virtualización está habilitada en BIOS
* Ejecutar actualización de Windows

---

# ✅ Resultado esperado

* WSL instalado
* Distribución Linux funcionando
* Terminal lista para usar

---

# ➡️ Siguiente paso

Continúa con:

👉 `03-shell`
