Describe los conceptos aprendidos sobre cómo usar la consola para navegar y crear directorios y archivos.

# Uso de la Consola Git Bash

## La consola de Git tiene 7 comandos cruciales para aprender a navegar y crear directorios y archivos:

- `pwd` : tiene la función de mostrar al usuario el directo en el que se encuentra actualmente.
- `cd` : tiene la función de cambiar a otro directorio, se utiliza escribiendo la ruta a la que se quiere ir después del comando. Puede usarse en conjunto con otro comando para darle más funcionalidad. Por ejemplo:
  - `cd ~` se utiliza para cambiar al directorio principal del usuario, algo parecido a la siguiente ubicación: `C:/Users/User/`
  - `cd ..` se utiliza para devolverse un directorio en la jerarquía.
  - Además, se puede escribir una ruta completa para dirigirse allí directamente, por ejemplo: `cd /Documents/Programacion_2025_Repos/prog-2510-git-github-SantiagoRios514/mi_proyecto/docs`
- `ls` : tiene la función de listar todos los archivos visibles del directorio en el que se encuentra el usuario. Se puede utilizar de la siguiente forma: `ls -al` para además listar los archivos y directorios ocultos del directorio. 
- `mkdir` : tiene la funcíón de crear un directorio nuevo, se utiliza escribiendo el comando, seguido del nombre del directorio que se quiere crear. Si se quiere crear un directorio con espacios en el nombre, se tiene que encerrar el nombre entre comillas dobles. Por ejemplo: `mkdir "Programacion 2025 Prueba"` 
- `touch` : tiene la función de crear un archivo nuevo, se utiliza escribiendo el comando, seguido del nombre del archivo nuevo y la extensión de este. Por ejemplo: `touch texto.txt`
- `mv` : tiene la función de mover o cambiar el nombre de un archivo. Se utiliza escribiendo el nombre o ubicación actual del archivo, seguido del nuevo nombre o el nombre del directorio destino. Por ejemplo: `mv texto.txt tutorial.txt`
- `rm` : tiene la función de eliminar archivos o directorios, se utiliza escribiendo el comando, seguido del nombre del archivo. Si lo que se quiere eliminar es un directorio, se utiliza el comando `rm -m`
- `vim` o `code` : tienen la misma función, que es editar un archivo de texto, sea un archivo `.txt`, o incluso un archivo `.py`. El comando `vim` abre el editor de textos por defecto de Git, Vim. Por otro lado, `code` abre el editor de textos Visual Studio Code. Ambos se utilizan de la misma manera, después de escoger el editor preferido, se ejecuta el comando seguido del nombre del archivo que se quiere editar, por ejemplo: `code tutorial.txt`

A través de estos comandos principales se pueden crear todo tipos de archivos, directorios y navegar fácilmente a través de los directorios de tu computador en la consola Git Bash.
