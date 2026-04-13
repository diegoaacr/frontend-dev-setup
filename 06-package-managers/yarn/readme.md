# USAGE NPM

## 1 - INIT PROJECT
- Inicializar proyecto con NPM.
- Te pedira nombre, version etc. 

```cmd
# Iniciamos proyecto con npm , yarn o pnpm.
    npm init
    yarn init
    pnpm init
```

```cmd
# Iniciamos proyecto por default con npm, yarn o pnpm.
    npm init -y
    yarn init -y
    pnpm init -y
```

## 2 - INSTALLATION DEPENDENCIES

- Para instalar dependencias del proyecto basandonos en el package.json 

```cmd
# Instalacion dependencias de node_modules, leyendo package.json.
    npm install
    yarn install
    pnpm install
```

### 2.1 - INSTALL PROD DEPENDENCIES
- Para instalar dependencias de tipo produccion se utilizara el siguiente comando.
- Tomaremos como ejemplo el paquete lodash.
- Esto lo guardara en el package.json en la propiedad dependencies.

```cmd
# Instalacion paquete(prod)
    npm install lodash
    yarn add lodash
    pnpm add lodash
```

### 2.2 - INSTALL DEV DEPENDENCIES
- Para instalar dependencias de tipo desarrollo se utilizara el siguiente comando.
- Esto lo guardara en el package.json en la propiedad devDependencies.
- Tomaremos como ejemplo el paquete typescript.

```cmd
# Instalacion paquete(dev)
    npm install -D typescript
    yarn add -D typescript
    pnpm add -D typescript
```

### 2.3 - INSTALL GLOBAL DEPENDENCIES
- Para instalar dependencias de tipo global se utilizara el siguiente comando.
- Esto no lo guardara en el package.json, sino en todo el sistema.
- Tomaremos como ejemplo el paquete nodemon.

```cmd
# Instalacion paquete(global)
    npm install -g nodemon
    yarn global add nodemon
    pnpm add -g nodemon
```

## 3 - UNINSTALL DEPENDENCIES
- Para desinstalar o remover dependencias del proyecto se usa el siguiente comando.
- Borra el paquete y lo saca de package.json.
- Tomaremos como ejemplo el paquete lodash.

```cmd
# Desinstala el paquete.
    npm uninstall lodash
    yarn remove lodash
    pnpm remove lodash
```

## 4 - UPDATE DEPENDENCIES
- Para actualizar un paquete del proyecto se usa el siguiente comando.
- Tomaremos como ejemplo el paquete lodash.

```cmd
# Actualiza todos los paquetes segun rango en package.json
    npm update
    yarn upgrade
    pnpm update
```

```cmd
# Actualiza el paquete lodash
    npm update lodash
    yarn upgrade lodash
    pnpm update lodash
```

```cmd
# Actualiza el paquete lodash a una version en especifico
    npm install lodash@4.17.21
    yarn add lodash@4.17.21
    pnpm add lodash@4.17.21
```

## 5 - RUN SCRIPTS
- Para lanzar scripts , del package.json de la propiedad scripts.

```cmd
# Ejecuta un script
    npm run build
    yarn build
    pnpm build
```

## 6 - VERIFY PACKAGE MANAGER VERSION
- Para verificar las versiones instaladas.

```cmd
# Verifica version
    npm -v
    yarn -v
    pnpm -v
```

```cmd
# Lista el arbol de dependencias del proyecto
    npm list
    yarn list
    pnpm list
```

```cmd
# Limpia cache de dependencies
    npm cache clean --force
    yarn cache clean
    pnpm store prune
```