# ✍️ Commit Signing

Este módulo cubre la firma de commits usando SSH.

---

# 🎯 Objetivo

Firmar commits para verificar su autoría y aumentar la confianza en el historial del repositorio.

---

# 🧠 Recomendación

Usar **SSH signing** como método recomendado.

Es una opción más simple de mantener que GPG para la mayoría de entornos modernos.

---

# ⚙️ Configuración

Configura Git para usar firma con SSH:

```bash id="b5h2zq"
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

---

# 🌐 Añadir clave al proveedor

En plataformas como GitHub, añade tu clave pública también como **Signing Key**.

👉 No basta con tenerla solo como clave de autenticación SSH.

---

# 🔍 Verificación

Haz un commit de prueba y revisa que aparezca como firmado en tu proveedor remoto.

---

# 📌 Reglas

* Usar la misma clave SSH del entorno actual
* Mantener la configuración simple
* Documentar cualquier excepción

---

# ⚠️ Qué evitar

* mezclar múltiples métodos de firma sin necesidad
* activar signing sin verificar que funciona
* asumir que autenticación SSH y signing son exactamente lo mismo

---

# ✅ Resultado esperado

* Git configurado para firmar commits
* Commits verificados correctamente en el proveedor remoto

---

# ➡️ Siguiente paso

Continúa con:

👉 `05-node`
