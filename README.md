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


#Ejercicio 2

##Crear rama V0.2
la creamos y nos posicionamos en ella con una única instrucción

    git checkout -b V0.2

##Creamos un fichero nuevo en la rama
![](imagenes%20git/ficheroNuevo_V02.png)
Lo añadimos al repositorio local

    git add -A
    git commit -m "Archivo 2.tx en la rama V0.2"
    

##Crear rama remota V0.2

git push origin V0.2

##Merge directo
Nos posicionamos en la rama master

    git checkout master
    
Hacemos el merge de la rama V0.2 en la master

    git merge V0.2
    
##Merge con conflicto
Modificamos el fichero hola.txt en la rama master. Después del último merge ya nos encontramos en la rama correcta:
![](imagenes%20git/Hola.png)
Lo subimos al repositorio local

    git add 1.txt
    git commit -m "modificacion fichero 1.txt"
    
nos posicionamos en la rama V0.2

    git checkout V0.2
    
Modificamos el fichero 1.txt en la rama V0.2 y lo subimos al repositorio local, en la rama V0.2
![](imagenes%20git/Adios.png)
    
    git add 1.txt
    git commit -m "modificación fichero 1.txt en rama V0.2"
    
Nos posicionamos en la rama master y hacemos el merge de las dos ramas. Como lo que se ha cambiado es el fichero 1.txt, será el que se fusione

    git checkout master
    git merge V0.2
Al estar modificadas en ambos casos la linea 1 con distinto texto, no se  puede hacer el merge automático, por lo que nos genera un archivo 1.txt con la fusion de ambas ramas