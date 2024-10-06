# Git y GitHub

[![usuario1](https://github.com/gatonymous.png?size=50)](https://github.com/gatonymous)\
**Whyl**  \
**ACM.ai**

---

## Índice
1. [Introducción a Git y GitHub](#introducción-a-git-y-github)
2. [Instalar Git en Windows](#instalar-git-en-windows)
4. [Crear una Cuenta en GitHub](#crear-una-cuenta-en-github)
5. [Configuración Inicial de Git](#configuración-inicial-de-git)
6. [Crear un Repositorio Local](#crear-un-repositorio-local)
7. [Trabajar con Ramas](#trabajar-con-ramas)
8. [Realizar Commits](#realizar-commits)
9. [Eliminar Commits](#eliminar-commits)
10. [Repositorios Remotos](#repositorios-remotos)
11. [Subir un Repositorio a GitHub](#subir-un-repositorio-a-github)

---

## Introducción a Git y GitHub
**Git** es un sistema de control de versiones distribuido. **GitHub** es una plataforma que aloja repositorios de Git y permite colaborar con otros desarrolladores de manera remota.

Puedes revisar la documentación de Git...
<a href="https://git-scm.com/doc" target="_blank">
    <img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" alt="Documentación Git" width="48">
</a>

---

## Instalar Git en Windows
1. Ve al sitio oficial de Git: [Git for Windows](https://git-scm.com/download/win) y descarga la última versión.
2. Abre el instalador y sigue las instrucciones. Asegúrate de seleccionar la opción para agregar Git al `PATH`.
3. Una vez instalado, abre la terminal de Git Bash (instalada con Git) o usa el `Símbolo del sistema (cmd)`.

Para verificar que Git está correctamente instalado:
```bash
git --version
```
---

## Crear una Cuenta en GitHub
1. Ve a GitHub.com.
2. Haz clic en Sign up y sigue las instrucciones para crear tu cuenta.
3. Confirma tu correo electrónico para activar la cuenta.

Recuerda activar el token temporal en opciones de desarrollador

---

## Configuración Inicial de Git

Después de instalar Git, configura tu información básica.

1. Abre Git Bash o la terminal de VSCode.
2. Configura tu nombre de usuario:
   ```bash
    git config --global user.name "Usuario"
   ```
3. Configura tu correo electrónico:
   ```bash
    git config --global user.email "email@example.com"
   ```
4. Verifica la configuración:
   ```bash
    git config --list
   ```

---

## Crear un Repositorio Local

1. Crea una carpeta para tu proyecto:
   ```bash
    mkdir mi_proyecto
    cd mi_proyecto
   ```
2. Inicializa el repositorio de Git:
   ```bash
    git init
   ```
3. Crea un archivo ```README.md:``` o puede crear desde el explorador de archivos o vscode
   ```bash
    echo "# Mi Proyecto" > README.md
   ```
4. Agrega el archivo al área de preparación (staging):
   ```bash
    git add .
   ```
   en caso desee mapear solo un archivo
   ```bash
    git add archivo.py
   ```
5. Realiza el primer commit:
    ```bash
    git commit -m "Primer commit"
    ```

---

## Trabajar con Ramas
### Crear una Rama Nueva

1. Para crear una rama nueva:
   ```bash
    git branch nombre-de-la-rama
   ```
2. Cambia a esa rama:
   ```bash
    git checkout nombre-de-la-rama
   ```
3. O crea y cambia de rama al mismo tiempo:
   ```bash
    git checkout -b nombre-de-la-rama
   ```

### Ver Ramas Existentes
Para ver todas las ramas:
    ```bash
    git branch
    ```
    
    
    
### Fusionar Ramas

1. Cambia a la rama principal:
   ```bash
    git checkout main
   ```
2. Fusiona la rama:
   ```bash
    git merge nombre-de-la-rama
   ```

---

## Commits
### Realizar Commits

1. Después de hacer cambios en tus archivos, agrégalos al área de preparación:
   ```bash
    git add archivo1 archivo2
   ```
2. Realiza un commit con un mensaje descriptivo:
   ```bash
    git commit -m "Descripción de los cambios"
   ```

### Eliminar Commits

Si necesitas deshacer el último commit, puedes usar:
   ```bash
    git reset --soft HEAD~1
   ```
Esto dejará los cambios en tu área de preparación para que los puedas modificar o volver a commitear.


---

## Repositorios Remotos
### Agregar un Repositorio Remoto

1. Para vincular tu repositorio local a GitHub, agrega el repositorio remoto:
   ```bash
    git remote add origin https://github.com/tuusuario/mi_proyecto.git
   ```
2. Para verificar los repositorios remotos:
   ```bash
    git remote -v
   ```

### Trabajar con Ramas Remotas
1. Ver las ramas remotas:
   ```bash
    git branch -r
   ```
2. Para obtener los cambios de un repositorio remoto:
   ```bash
    git fetch origin
   ```
3. Para traer cambios y fusionarlos con la rama actual:
   ```bash
    git pull origin main
   ```


---

## Subir un Repositorio a GitHub

1. Para subir los cambios de tu repositorio local a GitHub, primero asegúrate de estar en la rama correcta (ej. ```main```):
   ```bash
    git checkout main
   ```
2. Sube los cambios:
   ```bash
    git push origin main
   ```
   ```bash
    git push
   ```
3. Si es la primera vez que subes un repositorio, usa:
   ```bash
    git push -u origin main
   ```









   






















   
