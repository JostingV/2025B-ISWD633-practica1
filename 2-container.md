# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
<img width="1476" height="95" alt="image" src="https://github.com/user-attachments/assets/500de239-5d5c-4111-b716-79b747adf826" />


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
<img width="1482" height="105" alt="image" src="https://github.com/user-attachments/assets/8d5977f0-3634-4f40-b7b7-c4bc99de7c62" />

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="1491" height="183" alt="image" src="https://github.com/user-attachments/assets/a212de72-d5e2-42b9-9c0b-3805bf9757b6" />
### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
<img width="1477" height="116" alt="image" src="https://github.com/user-attachments/assets/b4c21c96-c51c-4fa6-808b-07cd6a651b0f" />


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="1479" height="155" alt="image" src="https://github.com/user-attachments/assets/216b004f-0536-4bb6-9644-2058756cf78c" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```
<img width="996" height="118" alt="image" src="https://github.com/user-attachments/assets/344c7d81-5179-4a46-870a-e0c57d3d74c7" />

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

<img width="1384" height="987" alt="image" src="https://github.com/user-attachments/assets/31a0667c-e55e-4eb2-b53f-4cfcb44da205" />

**¿Qué sucede luego de la ejecución del comando?**
Se ejecuta en 2do plano capturando la salida estandar del contenedor

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
<img width="1047" height="106" alt="image" src="https://github.com/user-attachments/assets/50fe5862-8f7f-458d-9823-37740aa566d2" />

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
<img width="592" height="104" alt="image" src="https://github.com/user-attachments/assets/e7362228-8e81-491f-9202-d46b2941933a" />

Verificar que el contenedor que se eliminó
<img width="1403" height="132" alt="image" src="https://github.com/user-attachments/assets/932d8256-5a7b-4cb1-aa31-804b979d3b01" />

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
<img width="916" height="107" alt="image" src="https://github.com/user-attachments/assets/6d94cf21-5ad8-49bf-bec2-65330796de0d" />

Verificar que el contenedor que se eliminó
<img width="972" height="117" alt="image" src="https://github.com/user-attachments/assets/7890ed8a-ab53-4a68-a948-8465cb4cf747" />

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
<img width="862" height="133" alt="image" src="https://github.com/user-attachments/assets/055cdc35-3999-4b44-b7c9-b7646354e2ff" />

