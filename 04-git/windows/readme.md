# INSTALLATION AND CONFIGURATION GIT

## 1 - INSTALLATION GIT

- Ingresar al enlace oficial [GIT](https://git-scm.com/downloads)
- Luego de instalar , probaremos los siguientes comandos para verificar que lo tenemos

```cmd
    git --version
    ssh -V
```

## 2 - CONFIGURATION IDENTITY AND CONFIG GIT

- Ingresaremos al git bash y estableceremos ciertos comandos para aplicar configuraciones. 

```cmd
# Define el nombre del autor que GIT grabara en tus commits.

    git config --global user.name  "Tu Nombre"
```

```cmd
# Define el correo del autor que grabara en cada commit.

    git config --global user.email "tu-correo-github@ejemplo.com"
```

```cmd
# Define que al crear un repo nuevo con "git init", la rama inicial se llamara main(en vez de master).

    git config --global init.defaultBranch main
```

```cmd
# Al hacer git pull, en vez de mezclar con un merge, hace rebase de tus commits locales encima de la rama remota.
# Otro ejemplo seria que el hacer pull a veces se genera un M de merge entre los commits, con esto todo queda mas limpio.
# Esto se llama pull rebase, en vez de usar el pull merge por default.

    git config --global pull.rebase true
```

```cmd
# Si tienes cambios sin commit y haces git pull (con rebase), Git hara stash automatico antes del rebase y luego lo restaurara.
    git config --global rebase.autoStash true
```

```cmd
# Convierte los saltos de linea a CRLF en tu working copy (Lo que ves en archivos en Windows).

    git config --global core.autocrlf true
```

```cmd
# Establece VS Code como editor por defecto para mensajes de commit, rebase interactivo, resolucion de merges, etc.

    git config --global core.editor "code --wait"
```

- Al final para verificar que todo este bien configurado establecemos

```cmd
    git config --list
```

## 3 - GENERATE SSH KEY PUBLIC AND PRIVATE WITH PASSPHRASE

- Crearemos nuestro SSH KEY , tomaremos el camino de generar clave por repositorio (git hub y git lab) mediante el uso de alias para mejor separacion de responsabilidades.
- Es posible que la carpeta ~/.ssh/ , no exista asi que se creara al crear las claves ssh.

```cmd
# Genera la clave SSH
    ssh-key gen

# Tipo de clave seguro y moderno
    -t ed2559

# Comentario para establecer correo
    -C

# Ruta + nombre del archivo de la clave
    -f ~/.ssh/id_ed25519_github
```

 
- Te preguntaran si desean establecer un passphrase, y le pones es como un codigo pin para acceder a tus claves.

```cmd
# Genera el ssh en formato ed2559 y le agrega seguridad con passphrase para github
    ssh-keygen -t ed25519 -C "tu-correo-github@ejemplo.com" -f ~/.ssh/id_ed25519_github
```

```cmd
# Genera el ssh en formato ed2559 y le agrega seguridad con passphrase para gitlab
    ssh-keygen -t ed25519 -C "tu-correo-github@ejemplo.com" -f ~/.ssh/id_ed25519_gitlab
```

- Finalmente ingresamos a la carpeta con este comando y verificamos que todo este correcto.
- Y verificamos que debemos tener todo esto creado

```cmd
    cd ~/.ssh/ 
    ls
```

```cmd
# Listado de archivos en carpeta ~/.ssh/
    id_ed25519_github
    id_ed25519_github.pub
    id_ed25519_gitlab
    id_ed25519_gitlab.pub
```

## 4 - ADD SSH KEY IN TO AGENT 

### 4.1 - ADD AGENT ( BY SESSION )
- Vamos agregar nuestro agente e iniciarlo solo en la terminal actual.
- Es el camino mas rapido para no configurar el automatized.
- Al cerrar el bash y abrirlo se tiene que hacer los pasos denuevo.

```cmd
# Con 
    eval "$(ssh-agent -s)"
```

- Ahora cargaremos nuestras claves

```cmd
# Estamos agregando nuestra ssh al agent con esto, nos pedire el passphrase.
    ssh-add ~/.ssh/id_ed25519_github
    ssh-add ~/.ssh/id_ed25519_gitlab
```

- Finalmente verificamos que liste nuestros agentes

```cmd
# Lista nuestros agentes
    ssh-add -l
```

- Podemos verificar tambien las variables del agente

```cmd
# Lista las variables del agente
    echo "$SSH_AUTH_SOCK"
    echo "$SSH_AGENT_PID"

```

### 4.2 - ADD AGENT SHELL WINDOWS(AUTOMATIZED)

- Vamos agregar nuestro ssh keys al agente en este caso de Windows.
- Establecer estos comandos como administrador y en el powershell de Windows.

```cmd
# Habilitamos el servicio (PowerShell Administrador)
    Get-Service ssh-agent
    Set-Service -Name ssh-agent -StartupType Automatic
    Start-Service ssh-agent
```

```cmd
# Cargamos nuestras dos claves en Git bash o Power Shell
    ssh-add ~/.ssh/id_ed25519_github
    ssh-add ~/.ssh/id_ed25519_gitlab
```

```cmd
# Verificar que este todo correcto
    ssh-add -l
```

- Salio error luego lo verificaremos


## 5 - CREATE ALIAS

- Crearemos alias por buenas practicas para cada host.
- Por ejemplo para github y para gitlab
- Crearemos el archivo de configuracion

```cmd
# Crearemos el archivo de configuracion en la carpeta .ssh/ y abriremos para agregar.
    cd ~/.ssh/
    touch config
    code .
```

```cmd
# Agregaremos esta configuracion para crear los alias

# GitHub (clave dedicada)
    Host github.com-diego
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_github
    IdentitiesOnly yes
    AddKeysToAgent yes

# GitLab (clave dedicada)
    Host gitlab.com-diego
    HostName gitlab.com
    User git
    IdentityFile ~/.ssh/id_ed25519_gitlab
    IdentitiesOnly yes
    AddKeysToAgent yes
```

- Ahora subiremos las llaves publicas a cada repositorio de github y gitlab
- Cada uno en settings en la opcion de SSH-KEY

```cmd
# Copia en portapapeles el ssh key public para ponerlo en el repositorio.
    clip < ~/.ssh/id_ed25519_github.pub
```

```cmd
# Copia en portapapeles el ssh key public para ponerlo en el repositorio.
    clip < ~/.ssh/id_ed25519_gitlab.pub
```

- Si todo va correcto podemos probar la conexion

```cmd
# Verificando la conexion ambos repositorios
    ssh -T github.com-diego
    ssh -T gitlab.com-diego
```

- You've successfully authenticated , todo correcto.



## 6 - CONCEPTOS
- SSH(ssh-keygen) se puede dejar sin contrasena o protegerla con una passphrase.
- El passphrase es como un candado que protege tu clave privada(id_ed25519)
- El ssh-key es tu tarjeta de credito y el passphrase es el PIN para acceder a la tarjeta de credito.
- ssh-agent : Como llavero en memoria.

## 7 - TERMINOLOGIA

- Passphrase = “PIN” para tu clave privada.
- ssh-agent = “llavero” que recuerda ese PIN mientras trabajas.
- El método moderno recomendado = clave ed25519 + passphrase + ssh-agent activo.

## 8 - HELPER

eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_github
ssh-add ~/.ssh/id_ed25519_gitlab
ssh-add -l   # verifica que ves 2 identidades