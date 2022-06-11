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
Como su nombre lo dice ya que configuramos las caracteristicas y requerimientos necesarios para nuestra máquina virtual, Azure revisara toda la información y nos creara lo solicitado.




