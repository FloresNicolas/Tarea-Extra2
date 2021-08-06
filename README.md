# Tarea-Extra2
Resolución del ejercicio planteado como trabajo extra referente al Segundo Parcial de la materia Fundamentos de Circuitos Eléctricos.

Nombre: Nicolás Fabian Flores Castillo


**1 . OBJETIVOS**

Objetivos Generales
* El objetivo general de este trabajo es el desarrollo de una conexión hacia una base de datos My-SQL donde el usuario pueda tener acceso a datos apoyándonos de la herramienta de desarrollo Node-RED.


Objetivos Especificos
* Comprender la operatividad y utilidad de la base de datos MySQL dentro del editor Node-Red.
* Analizar y diferenciar la utilidad de cada tipo de conexión dentro de cada instancia en la base de Datos.
* Verificar la utilidad de la utilización de la base de datos MySql en cada nodo con el editor Node-Red.
 
 
 **2 . ANTECEDENTES**
 
 * ¿Qué es una base de datos MySQL?
MySQL es un sistema de gestión de base de datos (SGBD) de código abierto. El SGBD MySQL pertenece actualmente a Oracle. Funciona con un modelo cliente-servidor. Eso quiere decir que los ordenadores que instalan y ejecutan el software de gestión de base de datos se denominan clientes.

 * ¿Qué es Node-Red? 
Es un editor de flujo basado en el navegador donde se puede añadir o eliminar nodos y conectarlos entre sí con el fin de comunicar hardware y servicios entre ellos.


**3 . EXPLICACION Y RESOLUCION DEL EJERCICIO PLANTEADO**

  => Realizar un ejemplo para conexión a una base de datos My-SQL con Node-Red.
   
 En la actualidad muchos de los lenguajes de programación facilitan los controladores para las conexiones con una base de datos MySql por lo que realizar una conexión con Node-Red resulta mucho más accesible y fácil de comprender. 

* Prerrequisitos:
Para interoperar con MySQL (en nuestro caso, estamos usando Xampp que incluye PHPMyAdmin) usando Node.js, necesitará el siguiente paquete de nodo llamado MySql.

* ![image](https://user-images.githubusercontent.com/84397670/128445521-09fbd83e-e386-4f0d-8927-450adbf393d6.png)

Entonces podrá requerir el módulo MySql.

* Implementación:
Existen dos formas de acceder a una base de datos MySql, se puede elegir una conexión simple accediendo rápidamente cuando solo se tiene una base de datos. O la segunda es utilizar una conexión agrupada para facilitar el intercambio de una sola conexión o la gestión de varias conexiones.

* Conexión Simple
El siguiente ejemplo expone una conexión con sus componentes más básicos. Requerir el servicio MySql, agregar las credenciales como primer parámetro en el createConnection método, proceder a conectarse a la base de datos, realizar consultas y finalmente cerrar la conexión.

Puede leer todas las opciones disponibles para un objeto de conexión en la documentación oficial aquí.
* ![image](https://user-images.githubusercontent.com/84397670/128445644-94adc344-1688-410d-ac3a-f10b209f954c.png)

* Conexión Agrupada
* ![image](https://user-images.githubusercontent.com/84397670/128445678-89b9ec4d-1971-442e-8ffe-3c771b5e97a3.png)

* Ejemplo Práctico:

Para el ejemplo practico realizaremos una base de datos que nos pida la información de x número de empleados para aquello se seguirá los siguientes pasos:

**1º Estableceremos la Conexión a MySql:** Lo primero que hacemos en este ejemplo es crear un objeto de conexión a hacia la base de datos MySQL. Utilizaremos la tabla de empleados a modo de ejemplo, pero esta varía dependiendo del nombre de la base de datos al que se quiera utilizar o llamar. Del mismo modo, reemplaza USUARIO y PASS por los datos de usuario de MySQL.

* ![image](https://user-images.githubusercontent.com/84397670/128445794-8dd170dd-4a42-44e8-9176-092dfb7fc4e0.png)

Una vez se establecida la conexión ya podrás ejecutar consultas mediante el método query:
![image](https://user-images.githubusercontent.com/84397670/128445815-0e4a670b-a799-4904-a3cf-8e6b44ad6c15.png)

**2º Crea una base de datos MySQL:**  Para trabajar con la creación de la base de datos se puede dar el uso de aplicaciones externas como phpMyAdmin pero para este ejemplo se la realizara manualmente mediante la línea de comandos de MySQL.

Para crearla mediante la línea de comandos debes seguir estos pasos:
*Conéctate a MySQL desde la línea de comandos e introduce la contraseña cuando se te pida:
*![image](https://user-images.githubusercontent.com/84397670/128445888-a5bb0f09-12d8-42fe-bee5-6d2720104acb.png)

Crea una tabla de ejemplo, a la que en este caso llamaremos empleados:
*![image](https://user-images.githubusercontent.com/84397670/128445926-9393c989-8b44-4611-9492-2f855ec25e79.png)

Crea una tabla en la base de datos:
*![image](https://user-images.githubusercontent.com/84397670/128445943-5c5c2900-9ceb-45bb-b716-64aed234824b.png)

Inserta algunos datos de ejemplo en la tabla para verificar que todo funcione correctamente:
*![image](https://user-images.githubusercontent.com/84397670/128445963-87bb9942-798d-4caa-a8cc-4fa3cdccc2ba.png)
Ahora ya podrás ejecutar consultas sobre la tabla.

Y para finalizar la conexión se introducirá lo siguiente:![image](https://user-images.githubusercontent.com/84397670/128446018-1528cfac-1ac2-437e-8a76-61bf3d8a8b35.png)


**4 . CONCLUSIONES**

Mediante la realización de este trabajo se estudio la herramienta de programación Node-RED, de los sistemas de gestión de bases de datos, y su importancia y utilidad a la hora de almacenar, clasificar y manejar información, de cualquier tipo.

MySQL ha sido un gestor de bases de datos muy útil desde que fue creado, y con el tiempo, nuevas funciones se le añadieron, expandiéndolo y volviéndolo más útil, y convirtiéndose así en uno de los gestores de bases de datos más utilizados a nivel mundial, junto a Oracle.

SQL significó un gran avance para este fin, almacenar y clasificar información, además de que, gracias a su aparición, hoy en día existe una gran variedad de SGBD basados en el lenguaje SQL, como MySQL, PostgreSQL, Oracle, entre otros. Desde su estandarización, casi todos los programas que trabajan con bases de datos, utilizan este lenguaje, con diferentes variaciones y funciones, según el tipo de software y su objetivo.


**4 . BIBLIOGRAFIA**

1 . MySQL. En Wikipedia. Recuperado el 5 de agosto de 2021 de: https://es.wikipedia.org/wiki/MySQL.

2 .	Raspberry Pi 3 Modelo B, 2021. Raspberry Pi. [Online]. Disponible en: https://www.raspberrypi.org/products/raspberry-pi-3-model-b/.

3 .	Cómo programar NodeMCU con el IDE de Arduino, 2018. Programar fácil.com. [Online]. Disponible en: https://programarfacil.com/esp8266/como-programar-nodemcuide arduino/.

4 .	Node-RED. En Wikipedia. Recuperado el 5 de agosto de 2021 de: https://en.wikipedia.org/wiki/Node-RED.
