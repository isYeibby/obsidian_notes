## 1. Comprueba si ya tienes una clave SSH

Abre una terminal y ejecuta:

```
ls ~/.ssh
```

Si estás en Windows PowerShell:

```
Get-ChildItem ~/.ssh
```

Busca archivos como:

```
id_ed25519
id_ed25519.pub
```

Si ya existen, **no necesitas crear otra clave necesariamente**. Puedes comprobarla primero.

---

## 2. Crea una clave SSH

Recomiendo **Ed25519**.

```
ssh-keygen -t ed25519 -C "tu-correo@example.com"
```

Te preguntará:

```
Enter file in which to save the key:
```

Pulsa **Enter** para aceptar la ubicación predeterminada.

Después:

```
Enter passphrase:
```

Pon una contraseña para proteger la clave.

Te creará dos archivos:

```
~/.ssh/id_ed25519
~/.ssh/id_ed25519.pub
```

⚠️ **Nunca compartas** **`id_ed25519`**.

El archivo que puedes compartir es:

```
id_ed25519.pub
```

---

## 3. Inicia ssh-agent

### Linux / macOS

```
eval "$(ssh-agent -s)"
```

Después:

```
ssh-add ~/.ssh/id_ed25519
```

### Windows PowerShell

Primero:

```
Get-Service ssh-agent | Set-Service -StartupType Automatic
Start-Service ssh-agent
```

Luego:

```
ssh-add $env:USERPROFILE\.ssh\id_ed25519
```

---

## 4. Copia tu clave pública

### Linux/macOS

```
cat ~/.ssh/id_ed25519.pub
```

### Windows PowerShell

```
Get-Content ~/.ssh/id_ed25519.pub
```

Verás algo parecido a:

```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIxxxxxxxxxxxxxxxxxxxxxxxx tu-correo@example.com
```

Copia **toda la línea**.

---

## 5. Añádela a GitHub

Entra a GitHub y ve a:

**Settings → SSH and GPG keys → New SSH key**

Pon, por ejemplo:

```
Title:
PC Windows
```

En **Key**, pega la línea completa:

```
ssh-ed25519 AAAAC3...
```

Guarda la clave.

Si tienes varias computadoras, **cada computadora debería tener su propia clave SSH**:

```
PC       → clave SSH A
Laptop   → clave SSH B
Mac      → clave SSH C
```

No copies la clave privada de una computadora a otra.

---

## 6. Prueba la conexión

En la terminal:

```
ssh -T git@github.com
```

La primera vez probablemente aparecerá algo como:

```
The authenticity of host 'github.com' can't be established.
Are you sure you want to continue connecting?
```

Escribe:

```
yes
```

Si todo está correcto, GitHub responderá aproximadamente:

```
Hi TU_USUARIO! You've successfully authenticated...
```

🎉 Ya tienes SSH funcionando.

---
