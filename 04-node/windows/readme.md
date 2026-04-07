# INSTALLATION NODEJS

## 1 - INSTALLATION NVM

- Ingresar al enlace oficial de Windows NVM [LINK](https://github.com/coreybutler/nvm-windows)
- Dependiendo como tengas configurado tus usuario , y en que contexto te encuentras te recomiendo instalarlo en el C .
- Te pedira dos rutas para la instalacion , una ruta para la carpeta /nvm y otra para la carpeta de /nodejs para las versiones.

```cmd
# Las rutas de las dos carpetas que deberias escoger.
    C:\nvm
    C:/nodejs
```


## 2 - LIST OF COMMANDS NVM
- Listaremos los principales comandos para usar NVM , instalando, desinstalando , configurando , etc.

```cmd
# Verificar la version de nvm.
    nvm version
```

```cmd
# Lista las versiones de node disponible para descargar
    nvm list available
```

```cmd
# Lista las versiones de node instalados
    nvm list
```

```cmd
# Instalar version de node en especifico
    nvm install 20.12.2
    nvm install 20.x
```

```cmd
# Selecciona la version de node para utilizar
    nvm use 20.12.2
```

```cmd
# Selecciona la version de node por default al abrir una nueva terminal
    nvm use 20.12.2 default
```

```cmd
# Desinstala version de node
    nvm uninstall 20.12.2
```

```cmd
# Verifica que version de node tienes
    node -v
    npm -v
```