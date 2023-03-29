# Motor DC con Encoder de Cuadratura

Este repositorio contiene un proyecto que tiene como objetivo mostrar cómo controlar un motor DC con encoder de cuadratura utilizando un microcontrolador y un algoritmo de control.

## Funcionamiento del Proyecto

El proyecto se basa en el uso de un arduino uno para leer la posición actual del motor DC a través del encoder de cuadratura y ajustar la velocidad del motor para que siga un setpoint dado. Se ha utilizado un algoritmo de control PID para lograr esto.

## Requerimientos del Proyecto

El proyecto requiere hacer uso de lo siguiente:

- Un Arduino uno.

-  Un motor DC 12V con encoder de cuadratura.

- Un driver para controlar el motor DC (L298N).

-  Una fuente de alimentación para el motor (12v).

- Tener instaldo ROS Melodic en tu computadora.
    
## Instrucciones para Ejecutar el Proyecto

Descarga el contenido del repositorio en .zip y descomprimelo.

Luego abre una terminal y ejecuta los siguientes comandos:

    cd ~/catkin_ws/
	cd src
	
Crea un nuevo paquete de ROS

	catkin_create_pkg mortor_drive rospy roscpp std_msgs
	cd motor_dirver
	
Copia el contenido del .zip descomprimido al paquete "motor_driver" que creaste anteriormente.

Dentro de la carpeta ***/src***  abre el archivo **inal.ino** y cargalo en el arduino uno.

Posteriormente en la termianal ejecuta los siguientes comandos:

	cd ~/catkin_ws/
	catkin_make && soruce devel /setup.bash
	roscore
	
Abre una nueva termianal y ejecuta

	source devel/setup.bash
	roslaunch motoro_driver  package_fn.launch

Si todo se ejecuta correctamente se deberia de abrir una ventana con varias graficas.
