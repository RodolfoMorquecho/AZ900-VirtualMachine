# AZ900-VirtualMachine
Guía para crear un recurso y configurarlo para utilizar una Máquina virtual dentro de Azure.

Lo primero que debemo hacer, es dirigirnos al portal de [Azure](https://portal.azure.com/#home).

## Paso 1
En el menu seleccionamos la opcion "todos los servicios".

![1](https://user-images.githubusercontent.com/99112892/173168353-5edd58c0-777d-478a-b69e-6d23b8e9cc43.png)

## Paso 2
En la sección categorias elegimos 'compute' y dentro de sus servivios encontramos las 'Máquinas virtuales'.

![2](https://user-images.githubusercontent.com/99112892/173168365-b476b2b2-6c90-4351-bb1a-6053eed97e02.png)

## Paso 3
Nos dirigimos a la pestaña 'crear' y dentro de su desplegado de opciones elegimos 'Máquina virtual de Azure'.

![3](https://user-images.githubusercontent.com/99112892/173168376-48461d17-4c4a-46cb-83ef-a7cb281df8fc.png)

## Paso 4
### Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra máquina virtual dentro de la nube, lo nombramos como: lab01_dr.
- Le damos un nombre a nuestra máquina virtual, en este caso la nombro: mv01-dr.
- En Región seleccionamos (US) Central US
- Las opciones de disponibilidad son para tener respaldada nuestra información en otro centro de datos en caso de que el primero falle,pero debido a que solo es una prueba no los requerimos.
- La seguridad se queda en 'Estándar'.
- Para la Imagen escogemos: Windows Server 2019 Datacenter - Gen2. El cual sera nuestro sistema operativo con el que trabajara la VM.

![4 ](https://user-images.githubusercontent.com/99112892/173168393-bca3f85a-7c37-45d8-8bb1-fb42831ade51.png)

- Seleccionamos un tamaño al que tengamos acceso considerando nuestro credito y requerimientos, para eso podemos ir a la pestaña ´ver todos los tamaños' y decidir el que nos convenga, para esta situación me decidí por el 'DS2' que esta dentro de 'Tamaños de generaciones anteriores'. 

![4-5 _tamanio](https://user-images.githubusercontent.com/99112892/173168406-0c9644ac-ee20-4f96-8f54-7780ca83c870.png)

- Ponemos un nombre de usuario:Rivan y una contraseña mayor o igual a 12 digitos y al menos una letra mayuscula.

![4 1](https://user-images.githubusercontent.com/99112892/173168426-dca44dd1-8fd6-4e1c-87dc-d4ed100a6cc0.png)

- Aceptamos para usar una licencia de Windows Server existente.

![4 1_2](https://user-images.githubusercontent.com/99112892/173168431-92f5d2aa-d0c4-4bd1-9e05-835a99f430b0.png)

### Pestaña:Disks(Discos)
- El tipo de disco duro lo dejamos con la opción predeterminada junto a los demas campos de la parte inferior.

![4 2](https://user-images.githubusercontent.com/99112892/173168440-d62bbc60-1409-4178-adc2-9dc43bf71946.png)

### Pestaña:Networking(Redes)
- Observamos que ya nos crea una red virtual, una mascara de subred y los puertos permitidos.

![4 3](https://user-images.githubusercontent.com/99112892/173168445-904fa573-968b-409b-8cd8-dadff25c3319.png)

### Pestaña:Management(Administración)
- Usamos las opciones predeterminadas por Azure.

![4 4](https://user-images.githubusercontent.com/99112892/173168458-3886c7d5-cffd-4963-a9c2-a670fa5aeeae.png)

### Pestaña:Advanced(Opciones avanzadas)
- Usamos las opciones predeterminadas por Azure.

![4 5](https://user-images.githubusercontent.com/99112892/173168470-fe643da7-5026-4382-8c4e-5df2447d46e8.png)

### Pestaña:Tags(Etiquetas)
Las etiquetas nos sirven para cuando hay muchas personas trabajando dentro de una organización, es importante saber quien esta subiendo que cambios.
- En el campo nombre es muy usual poner: CreatedBy y para el campo valor ponemos por quien fue creado.

Podemos observar que hay 12 recursos que se crean de manera automatica
- Agregamos otra etiqueta con Nombre:Area y Valor:Skilling
- Finalizamos con una ultima, Nombre:Ciclo y Valor:7maEd 

![4 6](https://user-images.githubusercontent.com/99112892/173168483-0bfaa75d-7cc5-4a91-ae76-823b1c4a4bcf.png)

### Pestaña:Review+Create(Revisar y Crear)
Como su nombre lo dice ya que configuramos las caracteristicas y requerimientos necesarios para nuestra máquina virtual, Azure revisara toda la información y nos creara lo solicitado cuando nos indique 'Validación superada'.

![4 7](https://user-images.githubusercontent.com/99112892/173177252-939ce9c9-cd0b-4547-8a10-fabddd8d4f0f.png)

- Le damos en crear

![4 7_1](https://user-images.githubusercontent.com/99112892/173177265-51d27bf1-b724-4043-9234-e6ec599c877d.png)

- Nos muestra que se completó la implementación y tambien podemos ver los detalles de la
implementación, como los recursos, que tipo de recurso es y su estado.

![4 8](https://user-images.githubusercontent.com/99112892/173177300-7ac6b8e4-84a9-47e5-899f-097918d185d1.png)

- Para verificar nuestra máquina virtual, seleccionamos 'ir al recurso'.

![4 8_1](https://user-images.githubusercontent.com/99112892/173177313-50380288-04d0-4852-b4af-3bbb60754c4d.png)

- Exploramos nuestra máquina virtual, para eso presionamos en 'conectar' y despues 
elegimos 'RDP'.

![4 9](https://user-images.githubusercontent.com/99112892/173177329-65939a30-4003-47fb-96c7-97e7c57cc5be.png)

## Paso 5
- Descargamos el archivo 'RDP' y lo abrimos.

![5](https://user-images.githubusercontent.com/99112892/173177370-43387ce5-526e-482d-a4d2-51603b45a2d2.png)

## Paso 6
- Nos saldra una ventana emergente, en la cual nos preguntara si nos queremos conectar, por 
lo que elegiremos 'conectar'.

![6](https://user-images.githubusercontent.com/99112892/173177407-3fa2d910-ec45-4212-97d2-ecd97ab57d5b.png)

## Paso 7
- Nos pedira los datos con los que creamos nuestra máquina virtual y le damos en aceptar.

![7](https://user-images.githubusercontent.com/99112892/173177419-f78e6b0f-cb5e-4938-821d-ad5dff4ff661.png)

## Paso 8
- Volvera a salir una ventana emergente donde preguntara si nos queremos conectar, ya que es
la primera vez que lo hacemos, le diremos que 'si'.

![8](https://user-images.githubusercontent.com/99112892/173177438-22acb2f5-8f4b-42d3-85e7-7c1ec761f1eb.png)

## Paso 9 
- Obtendremos acceso a nuestra máquina virtual en la que podremos realizar cualquier cosa que necesitemos, ya que es una computadora a nuestras especificaciones requeridas, incluso vemos que tenemos conexión a internet.

![9](https://user-images.githubusercontent.com/99112892/173177464-94516d20-1ca5-4ec2-a3eb-3916db9efb78.png)

![9 1](https://user-images.githubusercontent.com/99112892/173177471-2ba0c606-d505-4dc7-ae50-3760647673e9.png)

![9 2](https://user-images.githubusercontent.com/99112892/173177475-9ed063e9-7ade-4405-aca2-c046d9a822c0.png)

### Nota: 
Cuando creamos una máquina virtual vamos a tener un disco duro, que aunque apaguemos nuestra máquina virtual el disco va a seguir ocupado por lo que nos van a continuar cobrando ese servicio.

## Paso 10
- Ya comprobado que la guía concluyo satisfactoriamente, ahora nos desconectaremos de la máquina virtual y la apagaremos.

![10](https://user-images.githubusercontent.com/99112892/173177541-08c38881-7f07-44d1-9ff5-fe8ce086bfc6.png)

## Paso 11
Eliminaremos la VM:
- Primero iremos a Home en el portal de Azure y seleccionamos 'grupo de recursos'.

![11](https://user-images.githubusercontent.com/99112892/173177573-bad07530-7c74-4cc2-8f09-1e2dec51175e.png)

- Seleccionamos 'lab01_dr' y presionamos 'eliminar grupo de recursos'.

![11 1](https://user-images.githubusercontent.com/99112892/173177588-b4c818c4-5018-49a3-8042-a5905dc73419.png)

- Escribimos el nombre de nuestra máquina virtual y presionamos 'eliminar', repetiremos el proceso ya que algunas veces no se eliminan a la primera.

![11 2](https://user-images.githubusercontent.com/99112892/173177597-0646196f-1910-4147-845d-eb6bbf9e0fd2.png)

- Por ultimo tambien eliminaremos 'NetworkWatcherRG' el cual se encarga de vigilar la red del grupo de recursos.

![11 3](https://user-images.githubusercontent.com/99112892/173177613-43c7de88-4ccf-467d-ad2b-72901bca6058.png)

### Nota:
Siempre es recomendable tener limpia nuestra area de grupos de recursos.

![11 4](https://user-images.githubusercontent.com/99112892/173177640-17a4cfa4-f60c-4794-a554-7cefa9857b78.png)








