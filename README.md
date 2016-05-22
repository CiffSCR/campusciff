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
mostrar en el archivo readme.rd. tambien se van a subir las modificaciones del
readme.rd

    git add -A
    git commit -m "Commit inicial"

##Push inicial
Subimos al repositorio remoto los cambios en el readme.rd y la carpeta con los pantallazos

    git push origin master

##Ignorar archivos
    echo "privado.txt" >> .gitignore
    echo "privada" >> .gitignore
