# Taller_robotica_movil_manipuladores
Para seguir el taller de forma correcta es necesario crear una cuenta en ROSDS (ROS Development Studio).
ROSDS es una plataforma online que permite utilizar ROS sin la necesidad de instalarlo en una máquina.
  1. Ingresar a la página de ROSDS. https://auth.theconstructsim.com/auth/login/?next=/oidc/authorize/%3Fscope%3Dopenid%2Bprofile%2Bemail%26state%3DE2lGT0Bfv0EhIfxuZy5RAd79zkV91aIx%26redirect_uri%3Dhttps%253A%252F%252Frds.theconstructsim.com%252Foidc%252Fcallback%252F%26response_type%3Dcode%26client_id%3D983516
  ![Image of singin ROSDS](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image1.png)
  2. Ingresar con cualquiera de las opciones señaladas o crear una nueva cuenta. 
  3. Crear un nuevo "ROSject".
  ![Image of new ROSject](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image3.png)
  4. Crear el "ROSject" con las siguientes configuraciones.
  ![Image of ROSject configs](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image4.png)
  5. Abrir el "ROSject" recién creado. Click en "Open ROSject".
  6. Explorar el ROSject.
  7. Proceder a clonar este repositorio.<br/>
      Tools>Shell:<br/>
      ![Image of cloning repo](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image5.png)<br/>
      El enlace para clonar el repositorio es: https://github.com/AlexCC93/Taller_robotica_movil_manipuladores.git
      ![Image of cloning repo_success](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image6.png)<br/>
  NOTA: Al principio se va a solicitar que se ingrese su credenciales de su cuenta de github.
  ![Image of cloning repo_failed](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image7.png)<br/>
  El error que se muestra aquí, se debe a que el repositorio no estaba configurado como visible para el público.<br/>
  8. Para que todo lo que se ha agregado, funcione correctamente se ejecutan estos dos comandos en un shell:
    - source devel/setup.bash
    - catkin_make <br/>
  ![Image of catkin_make](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image9.png)<br/> 
Ejecución de aplicaciones.<br/>
-> Turtlesim.<br/>
  - Abrir un nuevo shell. Cada vez que se abra un nuevo shell se debe ejecutar "source devel/setup.bash". Luego, ejecutar "roscore".<br/>
  ![Image of roscore](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image10.png)<br/>
  Esto inicia el nodo maestro en ROS, éste se encarga de gestionar la comunicación entre los demás nodos dentro de ROS.<br/>
  - En un nuevo shell ejecutar "rosrun turtlesim turtlesim_node".<br/>
  ![Image of turtlesim spawn](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image11.png)<br/>
  Este comando hace que aparezca una tortuga en su interfaz gráfica de ROSDS.
  - Abrir Tools>Graphical Tools para observar la tortuga dibujada en su interfaz gráfica. Si el dibujo esperado (tortuga), no aparece, correr nuevamente el comando "rosrun turtlesim turtlesim_node".
  ![Image of graphical tools](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image12.png)<br/>
  - En un nuevo shell ejecutar "rosrun turtlesim turtle_teleop_key".
  ![Image of turtle_teleop_key](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image13.png)<br/>
  Este comando permite que se controle el movimiento de la tortuga desde el teclado. <br/>
  - Toda la aplicación se vería así.<br/>
  ![Image of turtlesim_app](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image14.png)<br/>
-> Publicación y suscripción a topics. <br/>
  - Para correr esta aplicación es necesario abrir un nuevo shell y ejecutar "roscore" nuevamente.<br/>
  - Luego, ejecutar "rosrun first_custom_nodes talker_node".<br/>
  ![Image of talker node](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image15.png)<br/>
    Este comando envía (publica) mensajes al topic llamado "chatter".<br/>
  - A continuación correr "rosrun first_custom_nodes listener_node".<br/>
  ![Image of listener node](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image16.png)<br/>
    Este comando se suscribe al topic "chatter".<br/>
  - Un nodo publica y el otro se suscribe. Aquí se ven lado a lado y los mensajes con los que interactuan. <br/>
  ![Image of talker and listener app](https://github.com/AlexCC93/Taller_robotica_movil_manipuladores/blob/main/imagenes/image17.png)<br/>
  
  

  
  
    
  
  
