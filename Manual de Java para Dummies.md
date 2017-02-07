# 1. CONCEPTOS BÁSICOS

## Tipos de datos y como declarar las variables
Las variables son elementos que vamos a utilizar en nuestro código, este es su método de declaración:

Números enteros (int, byte, short, long "igual que el resto pero acabado en l o L"):
```java
int entero;
int entero = 1; 
```

Números decimales:
```java
float decimal;
float decimal = 1.5f;
```

Números Decimales dobles:
```java
double decimal = 1.77 * 2.72 / 2;
double decimal = 1.77f;

Cadena de texto:
```java
String texto;
String texto = hola Mundo;
```

Bouleanos "Si o No":
```java
Boolean cenado //valor por defecto false.
Boolean cenado = true;
```

Caracter único "1,a,\n"
```java
char uno = '1';
```
## Tipos de variables
Existen tres tipos:
- Locales: se declaran dentro de los bloques de una función, operan dentro de la función exclusivamente y siempre hay que inicializarlas.
```java
String nombre;
```

- De instancia: Son las que se declaran en el bloque de una clase, su ambito se especifica con los modificadores de ámbito como public, private o protected. 
```java
private String nombre;
```

- De clase: Son espacios de memoria que comparten todos los objetos de una clase. Están declaradas igual que las de instancia pero precedidas por el modificador static. 
```java
public static String nombre;
```
## Operadores y tipos 
- Aritméticos: +, -, *, %, ++, --
(Los operadores -- y ++ van junto a la variable y aumenta o reducen el valor en 1 cada vez que se usan). 
- De asignación: =, +=, -=, *=, /=, %= (los operadores se incrementan segun elegimos i += 5 seria i = i + 5)
- Relacionales: ==, !=, <, >, <=, >= (con estos operadores se comparan dos variables y != sirve para comparar booleanos si el valor es valor != true, decimos que la condición es que el valor no sea true)
- Lógicos: ^, &&, ||, !, &, | (comparar una condición y devuelven un booleano, si se trata de And "&&" la condición es que ambos sean true o false sino será false y cuando hablamos de Or "||" basta con que uno sea true para que ambos sean true)
- Concatenación: + (con este valor concatenamos cadena de datos ejemplo print("hola" + mensaje))
- Nivel u orden de bits: &, !, ^, <<, >>
- Especiales: ?, new, [], ()


## Como escribir un comentario
Los comentarios son de gran ayuda cuando queremos conocer mejor nuestro código:

Comentario de una sola línea:
```java
//Comentario de una linea
```
Comentario de varias líneas:
```java
/*
Hola esto es un
comentario con varias líneas.
No es nada del otro mundo.
*/
```
Comentario "Que hacer":
```java
//TODO: Hola soy un comentario TODO y sirvo para avisar de cosas pendientes, me tinto en amarillo.
```

## Bloques de sentencias
Un bloque de sentencia es un grupo de sentencias que va reunido entre llaves:
```java
{
System.out.println(“Hola mundo”);
}
```

## Identación del código
La Identación del código es mostrar el código por escalas, sangrado o tabulado. Es una buena práctica ir Identando el código para que sea más comprensible.
```java
public class HolaMundo{
    public static void main(String[] args) {
        System.out.println(“Hola mundo”);
    }
}
```
## Las Clases en JAVA
Las clases en java son grupos de código en los que podemos encontrar una o varias funciones. 


Para crear una clase:

En IntelliJ, nos vamos a nuestro paquete principal __com.tunombre.proyecto__ y pulsamos botón derecho del ratón, nos vamos a new y a Java Class. Ahí nos pedirá escribir el nombre de la clase y en kind el tipo de clase.
Eso nos creará la clase de este modo:
```java
package com.company.proyecto;

public class Clase {
    //aquí añadimos las funciones o métodos.
} 
```
Si queremos crear una clase automáticamente, nos dirigimos a __Main__ por ejemplo y escribimos el nombre de la clase y un nombre de función:
```java
Clase.imprime();
```
Si pulsamos ALT+INTRO sobre el nombre de la Clase nos creará la clase nueva, luego tendremos que crear la función "imprime".
## Las funciones
Las funciones o métodos son trozos de código que se ejecutan cuando son llamados. 
La función __Main__ es la función principal, y es la que llama al resto de funciones.

```java
public static void main(String[] args){
    //Sentencias
}
```
La función Main recibe también una serie de parametros con args, y es que main recibe cada parametro como cadenas de caracteres.

Así se crea una función o método:

```java
private static void imprime(){
    \\las sentencias que vayan a ejecutarse
}
```
El método debe ir dentro de una clase y fuera de cualquier otra función.

Para llamar a una función o método:
```java
imprime();
```
Esto deberá ir escrito en Main o en cualquier otra clase según el uso que vayamos a darle.

Si queremos que IntelliJ nos cree automáticamente una función o método, solo debemos de escribir la llamada a dicha función o método como hemos visto arriba y pulsar ALT+INTRO. Nos redigirá a la función dentro de la clase en la que estamos.

Para llamar a una función desde una clase externa debemos escribir el nombre de dicha clase seguido de la función que queremos usar:
```
Clase.imprime();
```

## Reglas para formar identificadores
- El primer carácter tiene que ser una letra, el carácter subrayado
_ o el carácter dólar $.
- Puede incluir números, pero no comenzar por uno de ellos.
- No se pueden incluir espacios en blanco.
- Se distingue entre letras mayúsculas y minúsculas.
- No se pueden utilizar las palabras reservadas como
identificadores.

## Reglas de convección o buenas prácticas de programación
- El nombre de una clase comienza por mayúscula. Ejemplo: Clase
- El nombre de una función comienza por minuscula seguido de mayusculas. Ejemplo: creaImpresión();
- El nombre de una variable comienza en minúscula. Ejemplo: String nombre;
- Las constantes van en mayúsculas. Ejemplo: PI

Las variables se pueden crear del siguiente modo:

```java
float sueldo = 1245f, complemento = 321.5f;
String saludo = "Hola", frasecilla = "Holita";
```
De este modo tendremos las variables del mismo tipo de datos juntas.

## Entrada y salida básica

### Salida de datos
Una sentencia es una línea de código en Java, para imprimir utilizamos print:
```java
System.out.print("Hola Mundo");
```
Si queremos imprimir añadiendo un retorno de carro para que salte a la línea siguiente utilizaremos println:
```java
System.out.println("Hola Mundo");
```
Esta sentencia nos imprime un mensaje en consola, si queremos que IntelliJ nos lo escriba solo, debemos escribir __sout__ y pulsar INTRO.

Y con esta imprimimos una alerta en rojo:
```java
System.err.println("Alerta");
```

### Entrada de datos
Para introducir datos utilizamos el objeto Scanner:
```java
Scanner teclado = new Scanner(System.in);
String cadena = teclado.nextLine();
```

Los datos introducidos por teclado se almacenan en una variable que lee según el parametro utilizado:
- next(): Lee como String
- nextXXX(): donde XXX puedes introducir un tipo de dato primitivo excepto char. (int, boolean, float, etc...)
- nextLine(): Saca del buffer dicho caracter ya que es un caracter terminador.


## Parámetros de una función
En la definición de una función se pueden distinguir tres partes:
- La cabecera o firma: ...
- El bloque de sentencias que se ejecutan: siempre encerrado entre llaves {y}.
- El valor devuelto: ...

La sintaxis puede ser del siguiente modo:

<acceso> <funcionalidad> <valor_devuelto> <nombre_función> (<parametros>)

así sería nuestra función:
```java
public static void sumar (int numero1, int numero2){

}
```

## El operador new
Se encarga de crear el espacio necesario para almacenar la información de un objeto, cadena o un array.


---
# 2. SENTENCIAS DE CONTROL

## El comparador IF
__if__ nos sirve para comparar uno o varios elementos:
```java
if (respuesta != false){
    System.out.println(“Respuesta recibida”);
}
else {
    System.out.println(“Respuesta fallida");
}
```
También nos podemos encontrar varios comparadores:
```Java
if (num1 < num2){
    System.out.println("El número 1 es menor");
} else if (num1 > num2){
    System.out.println("El número 1 es mayor");
} else{
    System.out.println("Son Iguales");
}
```

## La sentencia Switch
Es una sentencia de decisión múltiple. Permite elegir entre varias alternativas.

Su formato es el siguiente:
```java
switch (option){
                case "suma":
                    Calculadora.suma();
                    break;
                case "1":
                    Calculadora.suma();
                    break;
                case "resta":
                    Calculadora.resta();
                    break;
                case "2":
                    Calculadora.resta();
                    break;
                case "multiplicar":
                    Calculadora.multi();
                    break;
                case "3":
                    Calculadora.multi();
                    break;
                case "dividir":
                    Calculadora.div();
                    break;
                case "4":
                    Calculadora.div();
                    break;
                case "salir":
                    exit = true;
                    break;
                case "5":
                    exit = true;
                    break;
                default:
                    System.out.println("No entiendo lo que has escrito, por favor escribe un número o di que operación deseas realizar sin mayúsculas...");
                    break;
            }
}
```
El código se ejecuta según la opción elegida hasta el __break__ más próximo que encuentre.

## El bucle for 
Se utiliza para la ejecución de un bloque de sentencias durante un número concreto.

```java
for (int i = 0; i < 100; i++) {
            System.out.println("Te mando el saludo número: " + i);
        }
```
Con este bucle vamos a imprimir 100 saludos.
## El bucle While
Ejecuta un bloque de sentencias si se cumple una condición, cuando deja de cumplirse ya no se ejecuta y termina el bucle.

Su formato es:
```java
int total = 0;
        while (total < 7){
            System.out.println("Introduce un numero: \n");
            Scanner num1 = new Scanner(System.in);
            int numero1 = num1.nextInt();
            System.out.println("llevas: " + numero1 + " números.");

            total = numero1;
        }
```

## El bucle do while
Ejecuta un bloque de sentencias mientras cumpla la condición determinada:
```java
int total = 0;
        do {
            System.out.println("Introduce un numero: \n");
            Scanner num1 = new Scanner(System.in);
            int numero1 = num1.nextInt();
            System.out.println("llevas: " + numero1 + " números.");

            total = numero1;

        }
        while (total < 7);
```
La ejecución de do while es algo distinta a la de while.

---

# 3. TIPOS COMPUESTOS DE DATOS 

## Arrays de una dimensión
Un array es un conjunto de posiciones de memoria, todas del mismo tipo, que se referencian con el mismo nombre.
Los corchetes son los que demuestran que la estructura de datos es array.

1. Primero debemos declarar un array que puede tener una de las siguientes estructuras:

```
<tipo>[]<identificador>;
//o también:
<tipo><identificador>[];
```
Así quedaría declarado nuestro array:
```java
int []listanumeros;
//o también:
String nombres [];
```
2. A continuación, creamos el array que puede tener la siguiente estructura:
```
<tipo>[]<identificador> = new <tipo>[<numero_elementos>];
//o también:
<tipo><identificador>[] = new <tipo>[<numero_elementos>];
```
Esto quedaría así:
```java
int [] listanumeros = new int [10];
//o también:
String nombres = new String [5];
```
Si el identificador de array ya está declarado con anterioridad:

```
<identificador> = new <tipo>[<numero_elementos>];
```
Esto quedaría así:
```
listanumeros = new int[10];
```

3. Una vez tenemos creado el array, podemos ir introduciendo valores en las distintas posiciones que tenemos asignadas con la siguiente esctructura:
```
<identificador>[<indice>] = <valor>
```
Lo haríamos del siguiente modo:
```java
nombres[0] = "Jose Luis";
```

4. Si queremos usar algún elemento del array lo haremos con su identificador seguido de la posición que queremos leer.

Este es un ejemplo de lectura de array:
```java
System.out.println(nombres[0]);
```

5. Para saber el tamaño del array usaremos el atributo .lenght que compuesto con el arary anterior sería: __listanumeros.length__

Podemos imprimir el tamaño del array del siguiente modo:
```java
System.out.println(listanumeros.length);
```

Aquí dejo un ejemplo para imprimir una lista de nombres utilizando un array y un bucle for:
```java
String [] nombres = new String [5];
        nombres[0] = "Pepe";
        nombres[1] = "Luis";
        nombres[2] = "Antonio";
        nombres[3] = "Laura";
        nombres[4] = "Alfredo";
        
        for (int i = 0; i < nombres.length; i++) {
            System.out.println(nombres[i]);
        }
```

## Bucle For-each
El bucle for each se conoce como el bucle mejorado, que permite recorrer todos los elmentos de una colección de datos sin tener que recurrir a la utilización de índices.

El formato es el siguiente:
```
for(<tipo><identificador>:<coleccion>){
    <sentencias>
}
```

Este bucle nos sirve para recorrer colecciones y acceder a elementos para obtener su valor.
```java
//pendiente de insertar.
```

## cadenas
Las cadenas también pueden ser objetos instanciados de la clase String.

El formato para crear un objeto de tipo String es el siguiente:
```
String <identificador> = new String(<cadena>);
String <identificador> = <cadena>;
```
Así sería una cadena y como se imprimiría:
```java
String nombres = new String("pepe");
        System.out.println(nombres);
```
Y como la conocemos normalmente:
```Java
String nombres = "pepe";
```

### Lista de Métodos definidos en String:

|METODO|CLASE|FUNCIONALIDAD|
|------|-----|-------------|
|equals(<cadena>)|boolean|Devuelve true si la cadena que se invoca contiene los mismos caracteres que la cadena.|
|length()|int|Obtiene la longitud de la cadena.|
|charAt(<indice>)|char| Devuelve el caracter cuyo índice en la cadena es <índice>, los índices son siempre enteros|
|compareTo(<cadena>)|int| Retorna un valor negativo si la cadena que invoca es menor que <cadena>, valor positivo si es mayor que <cadena> y cero si son iguales|
|indexOf(<cadena>)|int| Busca en la cadena que invoca la subcadena específica por <cadena>. Devuelve el índice de la primera coincidencia o -1 en caso de no encontrarla|
|lastIndexOf(<cadena>)|int|Busca en la cadena que invoca la subcadena especifica por <cadena>. Devuelve el índice de la última coincidencia o -1 en caso de encontrarla.
|substring(<cadena>)|String|Devuelve un nuevo String que contiene todos los caracteres del String que invoca desde el indice hasta el final|


### Ejemplos de uso de cada método:
1. equals():
```java
System.out.println("¿Cómo te llamas?");
        Scanner escaner = new Scanner(System.in);
        String entrada = escaner.nextLine();

        if(entrada.equals("pepe")){
            System.out.println("Te llamas Pepe");
        } else {
            System.out.println("No te llamas Pepe, realmente te llamas " + entrada);
        }
```

2. length():
```java
System.out.println("¿Cómo te llamas?" + "\n" + ">>> ");
        Scanner escaner = new Scanner(System.in);
        String entrada = escaner.nextLine();

        System.out.println("Tu nombre tiene " + entrada.length() + " letras");
```
3. charAt():
```java
System.out.println("¿Cómo te llamas?" + "\n" + ">>> ");
        Scanner escaner = new Scanner(System.in);
        String entrada = escaner.nextLine();

        System.out.println("La primera letra de tu nombre es: " + entrada.charAt(0));
```

4. compareTo():
```java
System.out.println("¿Cómo te llamas?" + "\n" + ">>> ");
        Scanner escaner = new Scanner(System.in);
        String entrada = escaner.nextLine();
        String salida = new String();
        salida = "paco";

        System.out.println(entrada.compareTo(salida));
```

5. indexOf():
```java
System.out.println("¿Cómo te llamas?" + "\n" + ">>> ");
        Scanner escaner = new Scanner(System.in);
        String entrada = escaner.nextLine();
        String salida = new String();
        salida = "paco";

        System.out.println(entrada.indexOf(salida));
```

6. LastIndexOf():
```java
System.out.println("¿Cómo te llamas?" + "\n" + ">>> ");
        Scanner escaner = new Scanner(System.in);
        String entrada = escaner.nextLine();
        String salida = new String();
        salida = "paco";

        System.out.println(entrada.LastI
        ndexOf(salida));
```

7. substring():
```java
//pendiente de averiguar...
```











