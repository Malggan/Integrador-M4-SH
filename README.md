<h1> Resolución de la practica integradora

<h2> 0. Pasos Preliminares

<h3> Limpieza del disco duro

<br>


+ Borrar todo: 

  docker system prune -a

<h3> Limpiar Carpetas
<br>


+ Visualizar las carpetas:

    ls

+ Eliminar carpetas (una por una):

    rm -r <Nombre de carpeta> 

<h3> Limpiar Contenedores
<br>

+ Visualizar contenedores:

    sudo docker ps

+ Eliminar TODOS los contenedores:

    sudo docker rm -f $(sudo docker ps -a -q)

<h3> Limpiar Volumen
<br>

+ Visualizar volumen:

    sudo docker volume ls

+ Eliminar TODO los volumenes:

    sudo docker volume prune

<h3> Limpiar Imágenes
<br>

+ Visualizar Imágenes:

    sudo docker image ls

+ Eliminar TODAS las imagenes:

    sudo docker image prune

Verificar si está limpio maquina virtual (MV)
<br>

+ Visualizar espacio disponible:

    df -h

Finalmente, Clonamos y levantamos los contenedores
Clonamos el repositorio, nos posicionamos en la carpeta y levantamos el compose
Clonar repositorio
    git clone https://github.com/lopezdar222/herramientas_big_data

Posicionamos en la carpeta:
    cd herramientas_big_data

Levantamos los contenedores con el compose
    sudo docker-compose -f docker-compose.yml up -d
