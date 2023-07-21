# Cheat Sheet de Git

## Configuración Inicial

- Configuración del nombre que estará asociado a tus commits:
    ```bash
    $ git config --global user.name "Tu Nombre"
    ```
- Configuración del correo que estará asociado a tus commits:
    ```bash
    $ git config --global user.email tuemail@example.com
    ```

## Crear o Inicializar Repositorios

- Inicializar un repositorio git en un directorio existente:
    ```bash
    $ git init
    ```
- Clonar (copiar) un repositorio remoto:
    ```bash
    $ git clone url_del_repositorio
    ```

## Hacer cambios

- Verificar el estado de los archivos:
    ```bash
    $ git status
    ```
- Agregar los cambios de un archivo para el próximo commit:
    ```bash
    $ git add nombre_del_archivo
    ```
- Agregar todos los cambios para el próximo commit:
    ```bash
    $ git add .
    ```
- Hacer commit de los cambios agregados:
    ```bash
    $ git commit -m "mensaje del commit"
    ```

## Ver el Historial de Cambios

- Mostrar el historial de commits:
    ```bash
    $ git log
    ```
- Mostrar el historial de commits con detalle de los cambios:
    ```bash
    $ git log -p
    ```

## Deshacer Cambios

- Descartar los cambios en el directorio de trabajo:
    ```bash
    $ git checkout -- nombre_del_archivo
    ```
- Revertir un commit:
    ```bash
    $ git revert SHA_del_commit
    ```
- Resetear el HEAD a un commit específico (¡CUIDADO!):
    ```bash
    $ git reset --hard SHA_del_commit
    ```

## Trabajar con Ramas

- Listar todas las ramas:
    ```bash
    $ git branch
    ```
- Crear una rama:
    ```bash
    $ git branch nombre_de_la_rama
    ```
- Cambiar a una rama:
    ```bash
    $ git checkout nombre_de_la_rama
    ```
- Crear y cambiar a una rama en un solo comando:
    ```bash
    $ git checkout -b nombre_de_la_rama
    ```
- Combinar los cambios de una rama a la rama actual:
    ```bash
    $ git merge nombre_de_la_rama
    ```
- Eliminar una rama:
    ```bash
    $ git branch -d nombre_de_la_rama
    ```

## Trabajar con Remotos

- Ver los repositorios remotos:
    ```bash
    $ git remote -v
    ```
- Agregar un repositorio remoto:
    ```bash
    $ git remote add nombre_del_remoto url_del_repositorio
    ```
- Cambiar la url de un repositorio remoto:
    ```bash
    $ git remote set-url nombre_del_remoto nueva_url
    ```
- Eliminar un repositorio remoto:
    ```bash
    $ git remote rm nombre_del_remoto
    ```
- Traer los cambios de un repositorio remoto:
    ```bash
    $ git fetch nombre_del_remoto
    ```
- Traer los cambios de un repositorio remoto y combinar con la rama actual:
    ```bash
    $ git pull nombre_del_remoto nombre_de_la_rama
    ```
- Enviar los commits al repositorio remoto:
    ```bash
    $ git push nombre_del_remoto nombre_de_la_rama
    ```
