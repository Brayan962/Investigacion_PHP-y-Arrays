#### Brayan Armando Ramirez Ramos
## INVESTIGAR ACERCA DE LOS ARRAY

### ¿Qué son los Arrays?
#### R) Un array en PHP es una estructura de datos que esta asociada a los valores con claves y esta se puede usar para organizar los datos de forma estructurada y compleja son una estructura de datos clave que te permite almacenar y organizar conjuntos de información. Para trabajar de manera eficiente con estos arrays, PHP proporciona una amplia gama de funciones especializadas
#### Un array es en realidad un mapa ordenado un mapa es un tipo de datos que asocia valores con claves y este tipo se optimiza para varios usos diferentes; se puede emplear como un array, lista (vector), tabla asociativa (tabla hash - una implementación de un mapa), diccionario, colección, pila, cola, y posiblemente más los Arrays son las herramientas mas esenciales para organizar datos de forma compleja y estructurada.

### como se Utilizan los arrays de manera adecuada se realizan las siguientes acciones sobre ellos:

+ Declarar el array
+ Crear el array e inicializarlo (Esto se puede ya estar incluida en la declaración)
+ Acceder y utilizar el array

### Ejemplo de Arrays
    `<?php $a = array (’a’ => 10, ’b’ => 20, ’cee’ => 30);
    echo $a['a']; //Devolverá 10
    print_r($a); //Imprimirá el array como un string
    var_dump($a); //Devolverá el array, incluyendo el tipo de variable pero interrumpiendo el resto del script
    echo "<pre>".print_r($a)."</pre>"; //Imprimirá el array par oder leerlo de una manera más "humana"
    ?>`

### Características principales de los arrays las principales características de un array son:

* Tiene un nombre de variable único que representa a cada elemento dentro de él y estos elementos son diferenciados por un índice.
* Los elementos dentro del array son guardados en posiciones de memoria de forma continua.
* Se puede acceder a cada elemento individual del array de manera directa o aleatoria.
* Se pueden usar como listas, tablas asociativas, diccionarios, pilas, colas, y más
* Se pueden acceder a los elementos de forma directa o aleatoria
* Se pueden añadir o eliminar elementos de forma flexible

### Algunas funciones del php en Arrays
Los arrays son una forma de organizar los datos y acceder a ellos de forma más fácil en el lenguaje PHP tiene más de 70 funciones diseñadas exclusivamente para manipular arrays.
Entre las funciones que encontramos:

+ array_all 
+ array_any 
+ array_change_key_case 
+ array_chunk
+ array_column
+ array_combine
+ array_count_values
+ array_diff.

### TIPOS DE ARRAY, CON EJEMPLO DE CADA UNO
#### En Lenguaje de PHP, existen tres tipos principales de arrays:

1. Arrays Indexados numéricamente: Un array indexado es un array donde cada elemento tiene un índice numérico y estos índices comienzan desde el numero 0 por defecto es la variable estructurada que almacena valores en posiciones numéricas.

`php
$numeros = [0, 10, 20, 30, 40, 50];
// Sumar todos los elementos del array
$suma = 0;
foreach ($numeros as $numero) {
$suma += $numero;
}
echo "La suma de los números es: " . $suma . "\n";
?>`

2. Arrays Asociativos: Un array asociativo utiliza las claves nombradas en (strings) en lugar de los índices numéricos y esto nos permite asociar valores con nombres clave.

`php
$clase = array(
"curso" => "Programación Web",
"profesor" => "Laura",
"alumnos" => array(
array(
"nombre" => "Carlos",
"nota" => 85
),
array(
"nombre" => "Ana",
"nota" => 90
),
array(
"nombre" => "Luis",
"nota" => 78
)
),
"horario" => array(
"lunes" => "10:00 - 12:00",
"miércoles" => "10:00 - 12:00",
"viernes" => "10:00 - 12:00"
)
);`

3. Arrays Multidimensionales: Los arrays multidimensionales son arrays que contienen uno o más arrays como elementos y estos son muy útiles cuando necesitamos representar datos en forma de tablas o matrices en php.


`php $estudiantes = array(
    array(
   "nombre" => "Juan",
   "edad" => 20,
   "notas" => array(85, 90, 78)
   ),
   array(
   "nombre" => "María",
   "edad" => 22,
   "notas" => array(92, 88, 95)
   ),
   array(
   "nombre" => "Pedro",
   "edad" => 21,
   "notas" => array(75, 80, 70)
   )
   );
// Acceder a los datos
foreach ($estudiantes as $estudiante){
echo "Nombre: ". $estudiante['nombre']. "\n";
echo "Edad: " . $estudiante['edad']. "\n";
echo "Notas: ".implode(",", $estudiante['notas']) . "\n";
echo "Promedio: ".(array_sum($estudiante['notas']) / count($estudiante['notas'])) . "\n\n";
}`

### Caracteristicas de los tipos Arrays
 #### Array Indexado Numéricamente
 * Los índices numéricos comienzan en 0 e incrementan de abajo a arriba y de izquierda a derecha.
 * Los índices numéricos pueden ser asignados y personalizados manualmente.
 * Los arrays indexados son el tipo de array por defecto en PHP.
 * Los arrays indexados se pueden utilizar para organizar datos y acceder a ellos de forma más fácil. 


### ¿COMO ACCEDER A LOS ELEMENTOS DE CADA ARRAY, EXPLICAR DETALLADAMENTE?
R) PHP nos ofrece una amplia variedad de funciones para trabajar con arrays, permitiéndonos el crear poder actualizar, eliminar y ordenar los elementos de un array de manera mucho más sencilla primeramente para acceder a los elementos de los Arrays debemos crear un Array y los arrays en PHP se pueden crear utilizando la función array() o con la sintaxis abreviada [].
Y ahora Acceder a Elementos de un Array Podemos acceder a los elementos de un array utilizando sus índices (para arrays indexados) o sus claves (para arrays asociativos) de esta forma.

Primero vamos a necesitar tener un array nosotros podemos definir un array de varias maneras de hacer un array simple:

`php
$frutas = array("manzana", "naranja", "plátano");
`

Segundo vamos a acceder a los Elementos del Array y los elementos de un array se acceden utilizando su índice En PHP, los índices de los arrays comienzan en el número 0 asi que para acceder a los elementos se hara lo siguiente:

`php
echo $frutas[0]; // Esto mostrará "manzana"
echo $frutas[1]; // Esto mostrará "naranja"
echo $frutas[2]; // Esto mostrará "plátano"
`

Tercero ahora que estámos trabajando con un array asociativo donde las claves son cadenas en lugar de números la forma de acceso es un poco diferente de esta forma quedaria:

`php
$persona = array(
"nombre" => "Juan",
"edad" => 30,
"ciudad" => "Madrid"
);
`

Cuarto y ahora para acceder a los elementos de este array vamos a usar las claves de esta forma:

`php
echo $persona["nombre"]; // Esto mostrará "Juan"
echo $persona["edad"];   // Esto mostrará 30
echo $persona["ciudad"]; // Esto mostrará "Madrid"
`

### Es importante saber que en el Lenguaje de PHP podemos acceder a los elementos de un array usando la sintaxis de array[key] y el var_dump($array["foo"]);.
#### la explicación de los elementos seria la siguiente:

+ Los corchetes ([]) y la clave se usan para poder acceder al valor que está apuntando una clave dada.
+ Para poder agregar los nuevos elementos a una matriz asociativa podemos usar el operador de asignación del simbolo (=).
+ Para hacer y cambiar los elementos existentes se puede usar la misma sintaxis que agrega nuevos elementos de la matriz.
+ Para poder obtener un array con las claves (keys) de un array asociativo podemos usar el método array_keys() para mayor facilidad.
+ Para poder obtener el array con los valores de un array asociativo es mejor usar el método array_values() para sacar los valores rapido.
+ Para hacer el array que recorra y sacar cada valor por separado, se puede usar el constructor foreach.
+ Para que podamos ver y verificar el contenido de un array podemos usar la función in_array().
+ Para hacer el conteo todos los elementos en un array utilizar la función count(). 

### ¿COMO  MODIFICAR ARRAY, AGREGAR ELEMENTOS Y ELIMINARLOS?
R) para modificar los Arrays se le pueden asignar valores a la matriz y especificando la clave entre corchetes también se le puede iterar sobre el array con foreach es importante saber que un 
array existente puede ser modificado estableciendo explícitamente valores en él por ejemplo:

 `php
 $estudiantes = [
"Brayan" => ["edad" => 20, "carrera" => "Ingeniería"],
"Carlos" => ["edad" => 22, "carrera" => "Medicina"],
"Pedro" => ["edad" => 21, "carrera" => "Arquitectura"]
];
echo "Array original:\n";
print_r($estudiantes);
$estudiantes["Pedro"]["edad"] = 21;
$estudiantes["Ana"] = ["edad" => 19, "carrera" => "Biología"];
unset($estudiantes["Pedro"]);
echo "\nArray modificado:\n";
print_r($estudiantes);
?>`

Para agregar o Adiciónar un nuevo elemento: vamos a Agregar a Ana al array con su edad y carrera
para luego hacer la Eliminación de un elemento de array con el unset()
para eliminar a Pedro del array y de esta forma podríamos modificar agregar y eliminar los arrays por otros.

### ¿COMO RECORRER ARRAYS USANDO FOREACH, FOR, ARRAY ASOCIATIVO?
R) En PHP se pueden recorrer arrays usando los bucles foreach y for en el Foreach es el específico para recorrer arrays mientras que for lo vamos a utilizar para ejecutar un bloque de código a un número específico de veces y el Foreach
se utiliza para iterar sobre cada par clave-valor de un array.
Son cada iteración, el valor del elemento actual se asigna a una variable.
Por ejemplo:
`foreach($miArray as $clave => $valor)`

Es importante saber que se pueden recorrer los arrays utilizando la estructura de control foreach o de forma recursiva y
recorrer un array asociativo en PHP se debe realizar utilizando un bucle foreach y este bucle nos permite iterar sobre cada par clave-valor del array para realizar alguna acción en cada iteración.

### ¿COMO BUSCAR ELEMENTOS EN UN ARRAY?
R) Existen muchas formas de buscar un elemento en un array con PHP le mejor de forma seria usar el codigo de (array_search) que 
busca un valor determinado en un array y devuelve la primera clave correspondiente en caso de éxito por ejemplo:

`<?php
$array = array(0 => 'azul', 1 => 'rojo', 2 => 'verde', 3 => 'rojo');
$clave = array_search('verde', $array); // $clave = 2;
$clave = array_search('rojo', $array);  // $clave = 1;
?>`

### ¿COMO MEZCLAR VARIOS ARRAY?
R) Para mezclar varios arrays en PHP podemos usar la función array_merge() o el operador de la unión de arrays de la tecla (+).
* array_merge(): este Combina los elementos de uno o más arrays y los valores del segundo array se anexan al final del primero y si las claves son numéricas, se añaden al final y se renumeran.

* Operador de unión de arrays (+) esto Permite anexar elementos del segundo array al primer array sin sobrescribir los elementos del primero y 
Conserva los valores de las claves numéricas.

También se puede fusionar dos objetos PHP y para ello, se deben convertir los objetos en matrices mediante la conversión de tipos (array) ejemplo:

`<?php
$array1    = array(0 => 'zero_a', 2 => 'two_a', 3 => 'three_a');
$array2    = array(1 => 'one_b', 3 => 'three_b', 4 => 'four_b');
$resultado = $array1 + $array2;
var_dump($resultado);
?>`