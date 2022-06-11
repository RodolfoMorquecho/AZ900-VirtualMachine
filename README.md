# AZ900-VirtualMachine
Guía para crear un recurso y configurarlo para utilizar una Máquina virtual dentro de Azure.

Lo primero que debemo hacer, es dirigirnos al portal de [Azure](https://portal.azure.com/#home).

## Paso 1
En el menu seleccionamos la opcion "todos los servicios".

<img style="border: 1px solid; color: black;;" src="![1](https://user-images.githubusercontent.com/99112892/173166390-7805926a-f7d4-45ef-afa3-17939fa3bd2e.png)"/>


## Paso 2
En la sección categorias elegimos 'compute' y dentro de sus servivios encontramos las 'Máquinas virtuales'.

![2](https://user-images.githubusercontent.com/99112892/173166487-470a252f-987c-4959-9a98-92b276c11bb1.png)

## Paso 3
Nos dirigimos a la pestaña 'crear' y dentro de su desplegado de opciones elegimos 'Máquina virtual de Azure'.

![3](https://user-images.githubusercontent.com/99112892/173166505-f4d34872-a7f4-4c2f-9409-36919aaf1d29.png)

## Paso 4
### Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra máquina virtual dentro de la nube, lo nombramos como: lab01_dr.
- Le damos un nombre a nuestra máquina virtual, en este caso la nombro: mv01-dr.
- En Región seleccionamos (US) Central US
- Las opciones de disponibilidad son para tener respaldada nuestra información en otro centro de datos en caso de que el primero falle,pero debido a que solo es una prueba no los requerimos.
- La seguridad se queda en 'Estándar'.
- Para la Imagen escogemos: Windows Server 2019 Datacenter - Gen2. El cual sera nuestro sistema operativo con el que trabajara la VM.

![4 ](https://user-images.githubusercontent.com/99112892/173166857-bbb5ad79-b05c-4471-a4cd-8110096f6638.png)

- Seleccionamos un tamaño al que tengamos acceso considerando nuestro credito y requerimientos, para eso podemos ir a la pestaña ´ver todos los tamaños' y decidir el que nos convenga, para esta situación me decidí por el 'DS2' que esta dentro de 'Tamaños de generaciones anteriores'. 

![4-5 _tamanio](https://user-images.githubusercontent.com/99112892/173166949-ad7df0d5-00ab-48ba-8cb0-e080663431d0.png)

- Ponemos un nombre de usuario:Rivan y una contraseña mayor o igual a 12 digitos y al menos una letra mayuscula.

![4 1](https://user-images.githubusercontent.com/99112892/173167029-304d89a2-7f21-4382-a72f-89a7654fdcc4.png)

- Aceptamos para usar una licencia de Windows Server existente.

![4 1_2](https://user-images.githubusercontent.com/99112892/173167041-642a8efa-a49b-46a8-a818-e57980c6260b.png)

### Pestaña:Disks(Discos)
- El tipo de disco duro lo dejamos con la opción predeterminada junto a los demas campos de la parte inferior.

![4 2](https://user-images.githubusercontent.com/99112892/173167090-a2d6b50d-dfc3-4f69-883d-1aa6cb196562.png)

### Pestaña:Networking(Redes)
- Observamos que ya nos crea una red virtual, una mascara de subred y los puertos permitidos.

![4 3](https://user-images.githubusercontent.com/99112892/173167148-94bf0951-389c-44b7-a71b-0d7818951620.png)

### Pestaña:Management(Administración)
- Usamos las opciones predeterminadas por Azure.

![4 4](https://user-images.githubusercontent.com/99112892/173167170-d810a159-13a7-43b1-92b2-9daf975938a5.png)

### Pestaña:Advanced(Opciones avanzadas)
- Usamos las opciones predeterminadas por Azure.

![4 5](https://user-images.githubusercontent.com/99112892/173167196-ee9c7001-eb7b-4b26-bdc5-8ae74e76416d.png)

### Pestaña:Tags(Etiquetas)
Las etiquetas nos sirven para cuando hay muchas personas trabajando dentro de una organización, es importante saber quien esta subiendo que cambios.
- En el campo nombre es muy usual poner: CreatedBy y para el campo valor ponemos por quien fue creado.

Podemos observar que hay 12 recursos que se crean de manera automatica
- Agregamos otra etiqueta con Nombre:Area y Valor:Skilling
- Finalizamos con una ultima, Nombre:Ciclo y Valor:7maEd 

![4 6](https://user-images.githubusercontent.com/99112892/173167246-d17011dd-e99f-4590-9706-4103fdaf57a0.png)


### Pestaña:Review+Create(Revisar y Crear)
Como su nombre lo dice ya que configuramos las caracteristicas y requerimientos necesarios para nuestra máquina virtual, Azure revisara toda la información y nos creara lo solicitado.




