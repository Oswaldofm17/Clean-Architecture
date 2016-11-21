#The Clean Architecture

Surge con la problemática que en la mayoría de los desarrollos en los cuales existe un framework se encuentra más código que lo representa, en lugar del problema que está resolviendo, es decir la idea es centrarse en lo que tiene que hacer la aplicación como tal y es por ello que dice que debemos de pensar en él framework como el mecanismo de paso de mensajes hacia nuestro software, el cual se debe mirar como una herramienta o plugin de lo que queremos realizar.

El autor dice en varias de sus charlas que más que una arquitectura sólo son una serie de condiciones que se deben cumplir para que una arquitectura de considere ”clean”, solo son una serie de reglas que lo único que van a hacer es dividir el software en capas.

![alt text](https://github.com/Oswaldofm17/Clean-Architecture/blob/master/clean.png "Logo Title Text 1")

Antes de comenzar a describir los componentes importantes del esquema debes tener en cuenta que no es obligatorio ni mucho menos mandatorio usar solo 4 círculos ya que de acuerdo a Uncle Bob solo son esquemáticos y quizás tu problema necesita de más para poder ser resuelto.

Lo único que nos dice es que hay que respetar la Dependency Rule: “El código fuente sólo puede apuntar hacia adentro“.

####Entities
Son aquellos objetos que van a representar los actores importantes de la lógica de negocio de nuestra aplicación.

####Use Cases
Están muy relacionados con las entidades y son los encargados de implementar lógica de negocio de nuestra aplicación, ya que van a orientar todas aquellas interacciones del flujo de datos y entidades dejando al framework fuera de todo esto (en nuestro caso el sdk android), también se conocen como interactores.

(En ingeniería de software un caso de uso se define como: “Una secuencia de interacciones que se encargan de modelar alguna acción que quiero que mi software realice”)

####Interface Adapters
Convierten los datos en el formato más conveniente para los casos de uso y entidades. (De manera recurrente aqui encontraras controladores y presentadores.)

####Frameworks and Drivers
Aquí es donde residen los detalles y todo ese conjunto de plataformas externas y herramientas como puede ser la UI, Web, DB , Devices, etc. Generalmente solo se deben comunicar con el siguiente círculo a su interior.


