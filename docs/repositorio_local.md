# Cómo crear un repositorio local con comandos en la consola de Git

## Para crear un repositorio local en Git, se debe seguir el siguiente paso a paso

### 1. Verificar la configuración de la consola

Utilizando el comando `git config --list` se pueden verificar las configuraciones globales de la consola, en este caso se deben revisar 3 configuraciones principales:

- `user.name`: esta configuración debe tener el nombre, o nombre de usuario, del autor de los commits para poder tener un control de quién hace los cambios en el repositorio.
- `user.email`: esta configuración también debe tener correcto el correo electrónico del autor.
- `init.defaultbranch`: por convención de la industria, esta configuración debe ser igual a `main`, aunque muchos sistemas hoy en día todavía la configuran por su nombre antiguo `master`.

En el caso en que estas configuraciones no estén escritas de la forma correcta, se debe utilizar el siguiente comando: `git config --global` seguido por la configuración que se quiere cambiar, después un espacio y el texto correcto para la configuración. Por ejemplo, si el nombre que aparece ahí no es el mío, debo ejecutar el siguiente comando: `git config --global user.name "Santiago Rios"`.

En el momento en que se cambie la configuración, se debe corroborar utilizando de nuevo el comando `git config --list` y si aparece la misma configuración dos veces, hay que tener en cuenta que tomará prelación la configuración más nueva, es decir, la que aparezca abajo en la lista de configuraciones.

### 2. Iniciar el repositorio en Git

Cuando ya se tengan las configuraciones correctas, se debe iniciar el repositorio con Git. Este repositorio será un directorio que escoja el usuario, por lo que si aún no existe, se debe crear con el comando `mkdir`. Cuando el directorio ya esté disponible, hay que entrar en él y escribir el comando `git init` para iniciar ese directorio como un repositorio.

Para verificar que el repositorio se haya iniciado correctamente, se puede utilizar el comando `git status` para conocer el estado del respositorio, apenas se cree un repositorio, la respuesta de este comando se debe ver así:

```bash
$ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

### 3. Stage y commits

Para añadir un archivo al repositorio se utilizan los mismos comandos en la consola, por ejemplo, `touch`. Al añadir este archivo aún no estará disponible en la branch `main`, para esto hay que hacer **tracking** y **commits.** Cuando se edita y guarda un archivo dentro del repositorio, este aparecerá en el estado del repositorio como **untracked**, esto quiere decir que al momento de registrarlo en el repositorio este no se tendrá en cuenta.

Para que el repositorio sepa a qué archivos tener en cuenta, se debe utilizar el comando `git add` seguido del nombre del archivo que se quiere *trackear*, también se pueden incluir varios archivos en el comando, separándolos por espacios.

Así, los archivos ya estarán en el **Stage**, que es como un punto medio entre el directorio y el repositorio en Git. Finalmente, para guardar la versión de los archivos en el repositorio se debe utilizar el comando `git commit -m "Mensaje"`, el cual guardará en el repositorio la versión de todos los archivos en el **Stage**, también registrando un mensaje para el log, el cuál se puede revisar en el historial de los commits con el comando `git log`.

### 4. Actualizaciones

Así, para cada actualización que se le haga a un archivo, se agregar al repositorio con los dos comandos comentados anteriormente. Cada actualización quedará como un commit nuevo en el historial, el cual también incluye la fecha y hora del commit, así como el nombre y correo electrónico del autor del commit.
