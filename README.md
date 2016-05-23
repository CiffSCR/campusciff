#Ejercicio 1

##Crear repositorio
Creamos el repositorio en GitHub

![](imagenes%20git/creacionRepositorio.png)

##Clonar repositorio
clonamos el repositorio remoto en nuestro entorno local

    git clone git@github.com:CiffSCR/campusciff.git 

![](imagenes%20git/clonacionRepositorio.png)

##Commit inicial
Se añade al repositorio local la carpeta donde vamos a guardar las imágenes a
mostrar en el archivo readme.md. tambien se van a subir las modificaciones del
readme.md

    git add -A
    git commit -m "Commit inicial"

##Push inicial
Subimos al repositorio remoto los cambios en el readme.md y la carpeta con los pantallazos

    git push origin master

##Ignorar archivos
    echo "privado.txt" >> .gitignore
    echo "privada" >> .gitignore

se sube el archivo .gitignore al repositorio local para que mantenga el fichero

    git add -A
    git commit -m "Segundo commit para subir .gitignore
   
##Añadir fichero 1.txt
Creamos un fichero en la carpeta local del repositorio. Lo añadimos al control de Git y lo subimos al repositorio local.  En este caso sólo vamos a añadir el fichero creado, es decir, no se va a subir la modificación del readme.md

    git add 1.txt
    git commit -m "Commit para subir el fichero 1.txt"

##Crear el tag v0.1
Etiquetamos el estado actual del repositorio local
    
    git tag V0.1

##Subir el tag V0.1

    git push --tag origin master

##Cuenta de GitHub
###Poner foto en la cuenta de GitHub
![](imagenes%20git/FotoPerfil.png)
###Activamos el doble factor de autentificacion
![](imagenes%20git/DobleFactorOFF.png)
Vamos a usar el SMS
![](imagenes%20git/UsarSMS.png)
Después de seguir las instrucciones, nos confirman que se ha activado el doble factor de autentificación
![](imagenes%20git/ConfAct.png)
![](imagenes%20git/DobleFactorON.png)

###Clave publica:
En git se encuentra añadida mi clave pública para acceder desde este ordenador:
![](imagenes%20git/PublicKey.png)

##Uso social de GitHub
###Buscar y seguir a mis compañeros
Buscamos a algunos compañeros
![](imagenes%20git/BuscarUser.png)
Pinchamos en "Follow" para seguirlos
Mostramos la lista de usuarios a los que seguimos:
![](imagenes%20git/Followed.png)
Damos estrella al repositorio campusciff de los compañeros a los que seguimos
![](imagenes%20git/Star.png)

##Crear una tabla

| Nombre    | GitHub   |
| --------- |--------- |
| Anna Lawrenc | <https://github.com/annalawrenc> |
| Enrique Serrano | <https://github.com/eserranom> |
| Asier Matas | <https://github.com/asiermatas> |

#Colaboradores
Añadimos un colaborador al repositorio
![](imagenes%20git/AddColaborador.png)

##
