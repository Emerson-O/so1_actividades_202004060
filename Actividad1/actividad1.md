#  Kernel - Sistemas Operativos
Kernel o núcleo, es una parte fundamental del sistema operativo que se encarga de conceder el acceso al hardware de forma segura para todo el software que lo solicita, en otras palabras  kernel es el la parte central de un sistema operativo. También está presente y sirve para hacer funcionar todos los computadores que podemos encontrar hoy en día, como por ejemplo un ordenador de a bordo de un coche o un barco, una raspberry PI que ejecuta una versión adaptada de Linux Debian o los dispositivos móviles con Android e iOS, que también disponen de un Kernel basado en Linux / Unix.



## Tipos de Kernel
Existen diversos tipos de kernel en donde cada uno de ellos funciona a su manera y cumple diferentes características, por medio de las cuales se pueden diferenciar cuatro de ellos :
#### - ***Monolítico:*** 
Es un tipo de arquitectura de sistemas operativos donde el sistema operativo completo trabaja en el espacio del núcleo. Por lo tanto es un núcleo grande y complejo donde se concentran todas las funcionalidades del sistema.

Es decir un conjunto de primitivas o llamadas de sistema implementan todos los servicios del sistema operativo como la administración de procesos, la concurrencia y la administración de memoria. Los controladores de dispositivos (drivers) pueden se añadidos al kernel (núcleo) como módulos.



![](https://slideplayer.es/slide/4085729/13/images/6/KERNEL+MONOL%C3%8DTICO.jpg)

Los sistemas operativos que usan el kernel monolítico son Linux, OS X y Windows.
#### - ***Microkernel:*** 
Tambien conocidos como micronúcleos, debido a que son catalogados como mejores en comparación con el kernel monolítico, porque el mismo cumple una serie de pequeñas abstracciones mucho más simples que las comúnmente observadas en el kernel monolítico,es un tipo de diseño de kernel utilizado en sistemas operativos.

Es decir que minimiza el tamaño y la complejidad del núcleo del sistema al trasladar la mayoría de las funcionalidades fuera del espacio del kernel a módulos que se ejecutan en el espacio de usuario. En contraste con los kernels monolíticos, los microkernels siguen el principio de "mínimo privilegio", donde solo las funciones esenciales y críticas para el funcionamiento del sistema se implementan en el espacio del kernel, mientras que el resto de los servicios se proporcionan como procesos independientes en el espacio de usuario. 



![](https://scaler.com/topics/images/microkernel-operating-system-1.webp)
#### - ***Híbrido:*** 

Es una combinación de microkernel y arquitectura de kernel monolítico utilizada en sistemas operativos de computadora. Este enfoque de núcleo combina la velocidad y el diseño más simple del núcleo monolítico con la modularidad y seguridad de ejecución del microkernel.

Un kernel híbrido también implementa algunos servicios menos críticos y controladores de dispositivos como módulos que se ejecutan en el espacio de usuario, siguiendo el enfoque del microkernel. Estos módulos o servicios en el espacio de usuario se comunican con el núcleo a través de interfaces bien definidas, como llamadas de sistema o mecanismos de IPC (comunicación interprocesos).

![](https://universodigital.org/wp-content/uploads/Kernel-hibrido.png)
####  ***Exonúcleo:*** 
El enfoque central de los exokernels es permitir que las aplicaciones decidan cómo utilizar los recursos del sistema sin la intervención de un kernel intermedio que aplique políticas de gestión o imponga abstracciones innecesarias. Para lograr esto, los exokernels ofrecen tres principales mecanismos para las aplicaciones:

Los exokernel, la capa de exokernel, la capa de LibOS, y la capa de aplicaciones
El sistema es realmente robusto y flexible, debido a que la única tarea es impedir que tengan errores de permiso al hardware y conflicto entre los libOS.


![](https://zhu45.org/images/microkernels.png)




#  User vs Kernel Mode
Un procesador en una computadora que ejecuta un Sitema Operativo tiene dos modos diferentes: modo de usuario y modo kernel .

El procesador cambia entre los dos modos según el tipo de código que se esté ejecutando en el procesador. Las aplicaciones se ejecutan en modo usuario y los componentes principales del sistema operativo se ejecutan en modo kernel. Si bien muchos controladores se ejecutan en modo kernel, algunos controladores pueden ejecutarse en modo de usuario.
##  Modo usuario
Es un nivel de ejecución en un sistema operativo donde las aplicaciones y procesos se ejecutan con un conjunto restringido de privilegios y no tienen acceso directo al hardware. En este modo, las aplicaciones deben realizar llamadas al sistema para solicitar servicios al kernel del sistema operativo.
 
Los programas de modo de usuario tienen menos privilegios que las aplicaciones de modo de usuario y no se les permite acceder a los recursos del sistema directamente. Por ejemplo, si una aplicación en modo de usuario desea acceder a los recursos del sistema, primero deberá pasar por el kernel del sistema operativo mediante llamadas al sistema. 

## Modo Kernel
Es un nivel de ejecución en un sistema operativo donde el kernel tiene acceso completo a los recursos del hardware y tiene el control total del sistema. En este modo, el kernel puede realizar operaciones privilegiadas y gestionar los recursos del sistema, como la memoria y los dispositivos de hardware. Las aplicaciones en modo usuario acceden a los servicios del kernel a través de llamadas al sistema para realizar tareas que requieren privilegios. 

 Por lo tanto, es el programa más privilegiado, a diferencia de otros programas, puede interactuar directamente con el hardware. Cuando los programas que se ejecutan en modo de usuario necesitan acceso al hardware, por ejemplo, una cámara web, primero tiene que pasar por el núcleo mediante una llamada al sistema y, para llevar a cabo estas solicitudes, la CPU cambia del modo de usuario al modo de núcleo en el momento de la ejecución. 

![](https://i0.wp.com/www.differencebetween.com/wp-content/uploads/2017/12/Difference-Between-User-Mode-and-Kernel-Mode-fig-1.png?resize=500%2C500&ssl=1) 

 ##  Tabla Comparativa
 
 | Modo Usuario  | Modo Kernel  | 
| :------------ |:---------------:| 
| Solo puede hacer referencias a la memoria asignada para el modo de usuario.  | Es capaz de hacer referencia a ambas áreas de memoria. |
| Tiempo; el bit de modo del modo de usuario es 1. |El bit de modo de kernel-mode es 0. |  
|  El programa de aplicación se ejecuta y se inicia. | El programa tiene acceso directo y sin restricciones a los recursos del sistema. |
| Todos los procesos obtienen un espacio de direcciones virtuales separado. | Todos los procesos comparten un único espacio de direcciones virtuales. |   
| Necesita acceder a los programas del kernel, ya que no puede acceder a ellos directamente |  Puede acceder tanto a los programas del usuario como a los programas del kernel, no hay restricciones |  


![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/Kernel-simple.svg/1200px-Kernel-simple.svg.png)


