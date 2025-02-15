#### Brayan Armando Ramirez Ramos 0209200201974

## Las funciones en PHP y cuál es su estructura

#### R) Las funciones en PHP son bloques del código que estas realizan una tarea o serie de instrucciones y se pueden usar para dividir los código en unidades reutilizables es importante saber que todas las funciones y clases de PHP tienen ámbito global y se pueden llamar desde fuera de una función incluso si fueron definidas dentro, y viceversa es una de las herramientas más importantes en cualquier lenguaje de programación y son las funciones un conjunto de instrucciones que a lo largo del programa van a ser ejecutadas multitud de veces y es por ello, que este conjunto de instrucciones se agrupan en una función y estas funciones pueden ser llamadas y ejecutadas desde cualquier punto del programa.

### La estructura de una función PHP

* La palabra clave de (function): indica el inicio de la definición de la función 
* La palabra clave de (functionName): es el nombre de la función tendra o el que queramos colocar.
* Los (parameter1 y el parameter2): son los parámetros que se le pasan a la función
* Él (code block): es el código que realiza la tarea o las operaciones
* El (return o result) es opcional, y se usa para devolver un resultado

## ¿Cómo podemos definir una función PHP?
### Para definir una funcion se puede seguir estos pasos:
+ Primero Usar la palabra clave function
+ luego escribir el nombre de la función
+ Escribir los parámetros que recibe entre paréntesis
+ Hacer la Definicion el código que se ejecutará cuando se llame a la función, utilizando las llaves {}


## ¿Cuándo usar las funciones de php?
#### R) las funciones en PHP se pueden usan en cada momento de nuestros proyectos ya sea para simplificar, organizar y reutilizar el código o los códigos que queramos usar esto permite escribir código más limpio y funcional ademas de ahorrar el tiempo y esfuerzo los momentos de usar las funciones serian:
+ Para crear bloques de código reutilizables
+ Para dividir el código en bloques lógicos, facilitando su comprensión
+ Para facilitar el mantenimiento, ya que solo necesitas modificar la función en un solo lugar
+ Para incluir parámetros que pueden ser usados en tareas rutinarias, sin que sea necesario hacer uso de un código más extenso



## ¿Cómo podemos crear unas funciones en php?
#### R) Para crear una función en PHP, primeramente crear la sintaxis y después se utiliza la palabra clave function, seguida del nombre de la función y los parámetros que recibe de esta forma:

// Sintaxis

`<?php
function nombreFuncion(variables o argumentos a usar){
    // Instrucciones
}
// Así llamamos a una función para que se ejecute
nombreFuncion($mi_parametro);
?>`

// la variable

`<?php
function saludar($nombre) {
    return "Hola, " . $nombre . "!";
}
// Invocar la función y pasar un parámetro
$mensaje = saludar("Carmen");
// Imprimir el resultado
echo $mensaje;
?>`

### Ejemplos de funciones PHP
Ejemplo 1 Nombre Hola

`function greet($name = "Tim") { echo "Hello, $name"; } 
function incrementByOne(&$num) { $num++; }`

Ejemplo 2 Suma y resta

`<?php // Ejemplo funciones aprenderaprogramar.com
function operaciones($n1, $n2, $operacion) {
$resultado = 0;
if($operacion == "Sumar") {
$resultado = $n1 + $n2;
}else if($operacion == "Restar") {
$resultado = $n1 - $n2;
}else if($operacion == "Multiplicar") {
$resultado = $n1 * $n2;
}
return $resultado; // Devolver el resultado
}
// Llamar a la función operaciones
$r = operaciones(5, 7, "Sumar");
echo $r . "<br>";
// O podemos imprimir directamente
echo operaciones(15, 8, "Restar");
?>`

Ejemplo 3 Recursiva

`<?php
function recursividad($a)
{
    if ($a < 20) {
        echo "$a\n";
        recursividad($a + 1);
    }
}
?>`

Ejemplo 4 Una funcion dentro de otra

`<?php
function getNombre($nombre){
    $texto = "El nombre es: $nombre";
    return $texto;
}
function getApellidos($apellidos){
    $texto= "Los apellidos son: $apellidos";
    return $texto;
}
function devuelveElNombre ($nombre, $apellidos){
    $texto = getNombre($nombre)
            ."<br/>".
            getApellidos($apellidos);
    return $texto;
}
echo devuelveElnombre("Victor", "Robles");
?>`

### Explicacion de un ejemplo con funcion

`<?php
function sumar($a, $b) {
$resultado = $a + $b; 
return $resultado; 
}
$suma = sumar(5, 10);
echo "La suma es: " . $suma;`

### Explicación del ejemplo:

1. Definición de la función:
   function sumar ($a, $b) y después definir una función llamada sumar
   para que tome los dos parámetros: ($a, $b)
2. Cuerpo de la función: Dentro de la función, se realizara la suma de los dos parámetros y se almacena en la variable ($resultado)
3. Devolución del valor: La función debera de devolver el resultado de la suma usando él (return $resultado)
4. Llamada a la función: Se llama a la función con
   sumar(5, 10), lo que devuelve al valor de 15,que se almacena en la variable ($suma).
5. Salida: Finalmente se va imprimir el resultado de la sumatoria el 15.
