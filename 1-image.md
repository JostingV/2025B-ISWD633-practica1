# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```<img width="1473" height="756" alt="image" src="https://github.com/user-attachments/assets/9c5e2bb5-fcc0-48ad-8b1c-0545dfef4419" />


Descargar la imagen **hello-world**
# **¿Qué es nginx**


NGINX es una herramienta multifunción. Con NGINX, puede utilizar la misma herramienta que su balanceador de carga, proxy inverso, caché de contenido y servidor web, lo que minimiza la cantidad de herramientas y configuraciones que su organización necesita mantener.

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR
<img width="1462" height="753" alt="image" src="https://github.com/user-attachments/assets/991da279-8606-409d-a3d7-b7931f199002" />

### Listar imágenes

```
docker images
```
<img width="1467" height="753" alt="image" src="https://github.com/user-attachments/assets/d0b8068d-4cf0-4afc-b80b-913d0c65ee71" />

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
# img width="1460" height="753" alt="image" src="https://github.com/user-attachments/assets/bdeac61e-2953-4f38-aad5-9bf7cf8ad392" 


**¿Con qué algoritmo se está generando el ID de la imagen**
# sha256:54e66cc1dd1fcb1c3c58bd8017914dbed8701e2d8c74d9262e26bd9cc1642d31

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
