# Comparativa con Apache
## Nginx vs Apache: ¿Cuáles son las diferencias principales?
:one: _Sistema operativo: Compatibilidad_

Ambos servidores funcionan bien en sistemas como UNIX, LINUX y variaciones. Sin embargo, si el sistema operativo que se quiere usar es Windows, Apache tiene una mejor performance que Nginx. 

:two: _Administración y mantenimiento_

Por un lado, en Apache el soporte, las actualizaciones, el desarrollo y la corrección de errores es realizado por una comunidad de desarrolladores de todo el mundo. Mientras, en Nginx, todo el soporte y la administración es realizada por la compañía que la creó. 

:three: _Rendimiento o ‘performance’_

El servidor de Apache tiene un sólo hilo que está asociado con una sola conexión. Por otro lado, Nginx tiene la capacidad de manejar miles de conexiones que se gestionan de forma simultánea. Esto reduce la memoria, aumenta la velocidad y mejora el rendimiento.

:four: _Escalabilidad de la arquitectura_

Nginx sigue un enfoque que se basa en eventos asíncronos que sirven para poder administrar varias solicitudes de clientes. Esta arquitectura de Nginx basada en eventos es lo que permite tener un rendimiento mayor incluso si se trata de un tráfico pesado. Esto no es posible con Apache, ya que tiene una arquitectura de subprocesos múltiples que hacen difícil que esta escalabilidad se pueda lograr. 

:five: _Procesamiento de contenido dinámico_

Apache procesa contenido dinámico de forma nativa dentro del propio servidor web, algo que Nginx carece porque no tiene la capacidad de hacerlo internamente. Nginx depende de procesos que sólo se pueden ejecutar externamente.

:arrow_backward:[VOLVER](https://github.com/kikelopser/Nginx)

![NGINXvsAPACHE](https://github.com/kikelopser/Nginx/blob/main/Nginx/apache-vs-nginx.jpg)
