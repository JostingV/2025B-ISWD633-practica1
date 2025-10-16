# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
<img width="1011" height="396" alt="image" src="https://github.com/user-attachments/assets/6dd66cde-6d2b-4829-817d-89a683619b96" />


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
<img width="979" height="220" alt="image" src="https://github.com/user-attachments/assets/e3980bf9-ab65-406b-ade7-32a67bed66c6" />


### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="1383" height="170" alt="image" src="https://github.com/user-attachments/assets/0b2f1075-8207-4fb3-aad3-35d0a653cd96" />

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
<img width="502" height="111" alt="image" src="https://github.com/user-attachments/assets/be1e581c-e80d-4369-9a20-dac591844e9b" />

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="1288" height="111" alt="image" src="https://github.com/user-attachments/assets/1254d5d4-2d11-4125-b875-8a2e32b69988" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```
<img width="468" height="110" alt="image" src="https://github.com/user-attachments/assets/855b89ad-d09c-43f0-b315-6dc955950fda" />

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
<img width="1231" height="854" alt="image" src="https://github.com/user-attachments/assets/f0b270bf-edb5-4b0a-b800-aaf2d354942b" />


**¿Qué sucede luego de la ejecución del comando?**
# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
<img width="894" height="104" alt="image" src="https://github.com/user-attachments/assets/2f5a24fb-f9c8-433f-afbe-985641a8827b" />


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
<img width="642" height="104" alt="image" src="https://github.com/user-attachments/assets/d2c09cab-3dcd-4e79-a2c1-59ffad6dd4f6" />

Verificar que el contenedor que se eliminó
<img width="1337" height="124" alt="image" src="https://github.com/user-attachments/assets/2d1c809b-037d-4d3c-933d-00b08cbe7f8b" />

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
<img width="572" height="104" alt="image" src="https://github.com/user-attachments/assets/17c16273-f0eb-447b-8fc5-6f11631858e0" />


Verificar que el contenedor que se eliminó
<img width="1025" height="109" alt="image" src="https://github.com/user-attachments/assets/4341b14b-59ee-428c-ab3b-dadf5ee529cf" />

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
<img width="1918" height="938" alt="image" src="https://github.com/user-attachments/assets/724fe1b1-1b0d-4cca-b23e-46ae8ab9155c" />

