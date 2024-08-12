
# Ejercicios de Práctica de Bash

Este repositorio contiene una serie de ejercicios para practicar el uso de comandos Bash. Los ejercicios están diseñados para ir desde lo más básico hasta conceptos más avanzados.

## Instrucciones

### Ejercicio 1: Navegación básica en el sistema de archivos
- **Comando**: `cd`, `ls`
- **Explicación**: Aprende a moverte entre directorios y listar su contenido.
- **Instrucciones**:
  1. Navega al directorio `/home` usando `cd`.
  2. Lista los archivos en el directorio usando `ls`.
- **Salida esperada**:
  ```bash
  $ cd /home
  $ ls
  user1  user2  user3
  ```

### Ejercicio 2: Creación y eliminación de archivos y directorios
- **Comando**: `mkdir`, `rmdir`, `touch`, `rm`
- **Explicación**: Crea y elimina archivos y directorios.
- **Instrucciones**:
  1. Crea un directorio llamado `prueba`.
  2. Dentro de `prueba`, crea un archivo vacío llamado `archivo.txt`.
  3. Elimina el archivo `archivo.txt` y luego el directorio `prueba`.
- **Salida esperada**:
  ```bash
  $ mkdir prueba
  $ cd prueba
  $ touch archivo.txt
  $ rm archivo.txt
  $ cd ..
  $ rm -rf prueba
  ```

### Ejercicio 3: Redirección de entrada y salida
- **Comando**: `echo`, `>`, `>>`, `cat`
- **Explicación**: Aprende a redirigir la salida de un comando a un archivo.
- **Instrucciones**:
  1. Usa `echo` para escribir "Hola Mundo" en un archivo llamado `saludo.txt`.
  2. Añade otra línea que diga "Este es un archivo de texto" a `saludo.txt`.
  3. Muestra el contenido del archivo con `cat`.
- **Salida esperada**:
  ```bash
  $ echo "Hola Mundo" > saludo.txt
  $ echo "Este es un archivo de texto" >> saludo.txt
  $ cat saludo.txt
  Hola Mundo
  Este es un archivo de texto
  ```

### Ejercicio 4: Uso de variables
- **Comando**: Asignación de variables, uso de variables
- **Explicación**: Almacena y utiliza valores en variables.
- **Instrucciones**:
  1. Crea una variable `nombre` y asígnale tu nombre.
  2. Usa `echo` para imprimir "Hola, [nombre]".
- **Salida esperada**:
  ```bash
  $ nombre="Matias"
  $ echo "Hola, $nombre"
  Hola, Matias
  ```

### Ejercicio 5: Condicionales
- **Comando**: `if`, `else`, `test`, `[ ]`
- **Explicación**: Realiza acciones basadas en condiciones.
- **Instrucciones**:
  1. Escribe un script que verifique si el archivo `saludo.txt` existe.
  2. Si existe, imprime "El archivo existe".
  3. Si no, imprime "El archivo no existe".
- **Salida esperada**:
  ```bash
  $ if [ -f saludo.txt ]; then echo "El archivo existe"; else echo "El archivo no existe"; fi
  El archivo existe
  ```

### Ejercicio 6: Bucles
- **Comando**: `for`, `while`
- **Explicación**: Repite tareas automáticamente.
- **Instrucciones**:
  1. Usa un bucle `for` para imprimir los números del 1 al 5.
  2. Usa un bucle `while` para imprimir los números del 5 al 1.
- **Salida esperada**:
  ```bash
  $ for i in {1..5}; do echo $i; done
  1
  2
  3
  4
  5

  $ i=5
  $ while [ $i -ge 1 ]; do echo $i; i=$((i-1)); done
  5
  4
  3
  2
  1
  ```

### Ejercicio 7: Funciones en Bash
- **Comando**: Definición de funciones, uso de funciones
- **Explicación**: Agrupa comandos en funciones reutilizables.
- **Instrucciones**:
  1. Define una función llamada `saludar` que tome un parámetro (nombre).
  2. La función debe imprimir "Hola, [nombre]".
  3. Llama a la función con tu nombre.
- **Salida esperada**:
  ```bash
  $ saludar() { echo "Hola, $1"; }
  $ saludar Matias
  Hola, Matias
  ```

### Ejercicio 8: Manejo de archivos y cadenas
- **Comando**: `grep`, `sed`, `awk`
- **Explicación**: Procesa archivos y filtra texto.
- **Instrucciones**:
  1. Busca la palabra "Hola" en `saludo.txt` usando `grep`.
  2. Reemplaza "Hola" por "Hola Mundo" en `saludo.txt` usando `sed`.
  3. Cuenta el número de palabras en `saludo.txt` usando `awk`.
- **Salida esperada**:
  ```bash
  $ grep "Hola" saludo.txt
  Hola Mundo
  $ sed -i 's/Hola/Hola Mundo/g' saludo.txt
  $ cat saludo.txt
  Hola Mundo Mundo
  Este es un archivo de texto
  $ awk '{print NF}' saludo.txt
  4
  5
  ```

### Ejercicio 9: Manejo de procesos
- **Comando**: `ps`, `kill`
- **Explicación**: Administra procesos en el sistema.
- **Instrucciones**:
  1. Muestra los procesos actuales usando `ps`.
  2. Encuentra el PID de un proceso (puedes usar `grep`) y termina el proceso usando `kill`.
- **Salida esperada**:
  ```bash
  $ ps aux | grep "nombre_proceso"
  usuario    1234  0.0  0.1  123456  1234 pts/0    S+   10:00   0:00 nombre_proceso
  $ kill 1234
  ```

### Ejercicio 10: Scripts de automatización
- **Comando**: Creación de scripts, uso de permisos de ejecución
- **Explicación**: Automatiza tareas comunes mediante scripts.
- **Instrucciones**:
  1. Crea un script llamado `mi_script.sh` que ejecute los comandos de los ejercicios anteriores.
  2. Dale permisos de ejecución al script.
  3. Ejecuta el script.
- **Salida esperada**:
  ```bash
  $ chmod +x mi_script.sh
  $ ./mi_script.sh
  ```

## Requisitos

- Tener un entorno Bash disponible (Linux, macOS, o WSL en Windows).
- Conocimientos básicos de terminal.

## Cómo usar este repositorio

1. Clona este repositorio:
   ```bash
   git clone git@github.com:yosoyfunes/bootcamp-devops-2024.git
   ```
2. Sigue los ejercicios en el orden sugerido.
3. Si tienes dudas, consulta la documentación oficial de Bash.

¡Buena suerte con tu práctica!
