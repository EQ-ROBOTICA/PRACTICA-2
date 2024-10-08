# PRACTICA-2

# Integrantes:
 - Edgar Zahid Hernandez Garcia
 - Gael Mateo Rangel Chavez
 - Alejandro Saldaña Garcia

# Introducción
La robótica industrial es una gran industria y evoluciona a una gran velocidad. Hoy en día, los robots se encargan de numerosas tareas que antes realizaban 
los humanos, como ensamblar cosas (coches, electrodomésticos, aparatos), realizar cirugías, pintar piezas etc., una de las maneras de lograr tales hazañas es 
la implementacion de la programacion por codigo para asignar instrucciones determinadas a una accion especifica.
En esta practica se tiene el objetivo de implementar un codigo para lograr que un brazo robotico Epson C4 sea capaz de moverse, agarrar un objeto y despues 
dejarlo en un lugar especifico.

# Instrucciones
- Programación de coordenadas
  
  Para asegurar que el robot se desplace sin riesgo de colisión, se implementó un sistema de movimientos manuales utilizando el software EpsonRC+.
  A través de este software, se definió el punto de inicio o "Home" y las demás coordenadas necesarias para su movimiento.

  En nuestro caso, empleamos tres puntos: "Primero", "Segundo" y "Tercero". Cada uno de estos puntos fue almacenado con su respectivo nombre a medida que 
  íbamos moviendo el robot, creando así una trayectoria de tres puntos que luego se ejecutaría mediante código.

- Programación final mediante código
  
  Para implementar la lógica del movimiento según las coordenadas definidas, se accedió a la ventana "Main" del software y se escribió el siguiente código:

```
  Function main
  Home
  Go Primero
  Go Segundo
  Off 2
  Go Primero
  Go Tercero
  On 2
  Home
  Fend
  ```

  Básicamente, se estableció el punto de inicio "Home" y, mediante el comando Go, se indicó al robot que se desplazara al primer punto y, a continuación, al segundo. 
  Al llegar al segundo punto, el brazo robótico ya se encontraba sobre el objeto, por lo que con el comando Off y el valor 2 (predefinido para la garra) se cerró la 
  garra y se tomó el objeto. Seguidamente, se le ordenó regresar al primer punto para asegurar un movimiento seguro, y después se dirigió al tercer punto, donde se 
  encontraba el lugar de destino. Una vez allí, el comando On 2 permitió abrir la garra y soltar el objeto. Finalmente, el robot regresó al punto inicial "Home", y se 
  concluyó la secuencia con Fend.


# Conclusiones 
- Edgar Zahid Hernandez Garcia:
  Esta practica me dio una idea mas clara de como es que se implementa la robotica para realizar acciones especificas, personalmente creo que es demasiado util y
  eficiente su implementacion, esta vez la tarea a realizar fue demasiado simple por lo que para realizar tareas industriales creo que la complejidad del codigo
  aumentaria significativamente.


- Gael Mateo Rangel Chavez:
  Durante esta práctica se observó de una manera más clara como es que se crean las rutinas que siguen los robots para las disitintas tareas que se requieren, la tarea realizada en la práctica fue bastante sencilla pero es un paso más cerca a comprender mejor esta tecnología.

  
- Alejandro Saldaña Garcia:
  Dentro de la práctica se pudo visualizar un mejor manejo del robot respecto al espacio de la cabina así como memorizar las coordenadas para un funcionamiento adecuado ya que si no se tiene bien establecido se puede llegar a ocasionar una colisión, tomando como referencia que en algunas situaciones se necesita más pasos para evitar el fallo. Fuimos capaces de reutilizar coordenadas usadas para evitar el mayor uso de espacio en la memoria dentro del robot.

# Referencias bibliograficas
[1] Aula, «Cómo funciona la Robótica Industrial y cómo se programa», aula21 | Formación para la Industria, 17 de mayo de 2023. https://www.cursosaula21.com/como-funciona-la-robotica-industrial/
