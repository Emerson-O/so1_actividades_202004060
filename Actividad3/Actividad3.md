

# Actividad 3 - Gestión de Permisos


## Parte 1: Gestión de Usuarios

###  1. Creación de Usuarios


comando utilizado " sudo adduser usuario1"

*Salida Final

     Adding new user `usuario1' to supplemental / extra groups `users' ...
      Añadiendo al usuario `usuario1' al grupo `users'

     Adding new user `usuario2' to supplemental / extra groups `users' ...
     Añadiendo al usuario `usuario2' al grupo `users' ...

     Adding new user `usuario3' to supplemental / extra groups `users' ...
     Añadiendo al usuario `usuario3' al grupo `users' ...


### 2. Asignación de Contraseñas.

Despues de crear al usuario , se solicita por defecto que se le ingrese una contraseña.

     [sudo] contraseña para emerson: 
     Añadiendo el usuario `usuario1' ...
     Añadiendo el nuevo grupo `usuario1' (1001) ...
     Adding new user `usuario1' (1001) with group `usuario1 (1001)' ...
     Creando el directorio personal `/home/usuario1' ...
     Copiando los ficheros desde `/etc/skel' ...
     Nueva contraseña: 

Nota: Ese resultado es la misma para cada usuario creado.

### 3. Información de Usuarios:

Comando utilizado para mostrar información de los usuarios
 "id usuario1 "

*Salida del comando 

    uid=1001(usuario1) gid=1001(usuario1) grupos=1001(usuario1),100(users)

    uid=1002(usuario2) gid=1002(usuario2) grupos=1002(usuario2),100(users)

    uid=1003(usuario3) gid=1003(usuario3) grupos=1003(usuario3),100(users)



### 4. Eliminación de Usuarios:

Comando utilizado para eliminar usuarios 
"sudo deluser --remove-home usuario3"


     Buscando archivos para guardar/eliminar ...
     Eliminando archivos ...
     Eliminando el «crontab» ...
     Eliminando al usuario `usuario3' ...
     Hecho.

## Parte 2: Gestión de Grupos

### 1. Creación de Grupos
 El comando utilizado para la creacion de grupos es el siguiente "sudo addgroup grupo1"

*Salida del comando

     Añadiendo el grupo `grupo1' (GID 1001) ...
     Hecho.

     Añadiendo el grupo `grupo2' (GID 1002) ...
     Hecho.


### 2. Agregar Usuarios a Grupos
 Comando utilizado para agregar usuarios a los grupos

*Salida del comando "sudo adduser usuario1 grupo1"

    Añadiendo al usuario `usuario1' al grupo `grupo1' ...
    Hecho.

    Añadiendo al usuario `usuario2' al grupo `grupo2' ...
    Hecho.

### 3. Verificar Membresía
Comando utilizado para verificar mebresia de los usuarios "groups usuario1"

*Salida de comando

    usuario1 : usuario1 users grupo1
    usuario2 : usuario2 users grupo2

### 4. Eliminar Grupo:

Comando utilizado para eliminar usuario "sudo delgroup grupo2
"

*Salida de comando

     Eliminando al grupo `grupo2' ...
     Hecho.

## Parte 3: Gestión de Permisos

### 1. Creación de Archivos y Directorios:

Comando utilizado para la creacion de archivos y directorios 
Cambiar al directorio de usuario1

"cd ~usuario1"

Crear archivo1.txt y escribir algo en él

"echo "Contenido del archivo 1" > archivo1.txt"

Crear directorio1 y archivo2.txt dentro de él
mkdir directorio1

"echo "Contenido del archivo 2" > directorio1/archivo2.txt"

     Nota: Las salidas no se reflejaron en consola

### 2. Verificar Permisos:
Comando utilizado para la verificación de permisos archivos"ls -l archivo1.txt"

Comando utilizado para la verificación de permisos directorio "ls -ld directorio1"

*Salidas

    -rw-rw-r-- 1 emerson emerson 24 ago  9 18:24 archivo1.txt
    drwxrwxr-x 2 emerson emerson 4096 ago  9 18:25 directorio1



### 3. Modificar Permisos usando `chmod` con Modo Numérico:
Comando utilizado para modificar permisos con modo numérico
"chmod 640 archivo1.txt"

    Nota: Las salidas no se reflerjaron en consola

### 4. Modificar Permisos usando `chmod` con Modo Simbólico
Comando utilizado para modificar oermisos con modo simbólico
"chmod u+x directorio1/archivo2.txt"

    Nota: Las salidas no se reflerjaron en consola


### 5. Cambiar el Grupo Propietario:

Comando utilizado para cambiar de grupo propetario "sudo chown :grupo1 directorio1/archivo2.txt"

    Nota: Las salidas no se reflerjaron en consola

### 6. Configurar Permisos de Directorio:

Comando utilizado para cambiar permisos del directorio "chmod 750 directorio1"


     Nota: Las salidas no se reflerjaron en consola


### 7. Comprobación de Acceso:

Comando utilizado para la comprobación de acceso "cat archivo1.txt " y "cat directorio1/archivo2.txt"

*Salida comandos

    Contenido del archivo 1
    Contenido del archivo 2


### 8. Verificación Final:

Comando utilizado para la verificacion final de archivo "ls -l archivo1.txt"
Comando utilizado para la verificación final del directorio "ls -ld directorio1"

*Salida de comandos

    -rw-r----- 1 emerson emerson 24 ago  9 18:24 archivo1.txt

     drwxr-x--- 2 emerson emerson 4096 ago  9 18:25 directorio1


# ¿Por qué es importante gestionar correctamente los usuarios y permisos en un sistema operativo?

Es esencial por razones de seguridad, privacidad, prevención de errores, responsabilidad, cumplimiento normativo y control de recursos. Estas prácticas ayudan a proteger datos sensibles, prevenir cambios accidentales, mantener la privacidad, rastrear acciones y cumplir con regulaciones, además de administrar eficientemente los recursos del sistema.

