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

## Arrays Multidimensionales
Utilizan más de un índice para acceder a sus elementos, la estructura más usada es la de dos dimensiones, normalmente conocida como tabla.

El formato de creación es el siguiente:

1. Creación de la tabla con las dos dimensiones fijadas:
```
<tipo><identificador>[][] = new <tipo>[num_filas][num_columnas];
```
Quedaría así:
```java
int tabla [][] = new int[5][7];
```

2. Inserción de datos en la tabla:
```java
tabla[2][4] = 3;
```

Esto es un programa que genera automáticamente una apuesta:
```java
Random aleatorio = new Random();
int apuestas = aleatorio.nextInt(10) + 1;
 
 // Crear array de dos dimensiones
 int[][] numeros = new int[apuestas][6];
 // Recorrer array de dos dimensiones
 // almacenando un valor en cada posición
 
 System.out.println(“Apuestas: “ + numeros.length);
 
 for (int i = 0; i < numeros.length; i++){
    for (int j = 0; j < numeros[i].length; j++) {
        numeros[i][j] = aleatorio.nextInt(49) + 1;
        }
    }
 // Recorrer array de dos dimensiones
 // accediendo a cada posición
    for (int[] apuesta : numeros) {
        for (int numero : apuesta) {
            System.out.print(numero + “\t”);
        }
    System.out.println();
    }
```

Los arrays bidimensionale también se pueden inicializar utilizando el formato de listas de literales:

```java
//Creamos el array:
String grupo[][] = {
    { "Pepe", "Madrid", "coordina" },
    {"Ana", "Sevilla", "colabora" },
    {"Luis", "Lugo", "escribe" }
};
//Lo recorremos con un bucle y lo vamos visualizando:
for(String[] persona: grupo){
    for (String dato: persona){
        System.out.print(dato + "\t\t");
    }
    System.out.print("\n");
}
```
## Enumeraciones
Son listas de constantes con nombres que definen un tipo nuevo. Para crear una enumeración se utiliza la palabra reservada enum del siguiente modo:

```java
enum EstadoCivil {
    SOLTERO, CASADO, VIUDO, SEPARADO, DIVORCIADO
}
```
Aquí tenemos un ejemplos de uso de un enum:

Asignado a una variable y comparando su valor:
```java
public static EstadoCivil ec = CASADO;

public static void main(String[] args){
    if (ec == EstadoCivil.CASADO){
        System.out.println("Estás Casado");
    }
}
```
Y aquí tenemos otro ejemplo con un switch:
```java
EstadoCivil es = EstadoCivil.DIVORCIADO;

switch(ec){
    case SOLTERO:
        System.out.println("Estás soltero");
        break;
    
    case CASADO:
        System.out.println("Estás casado");
        break;

    case VIUDO:
        System.out.println("Estás viudo");
        break;

    case SEPARADO:
        System.out.println("Estás separado");
        break;

    case DIVORCIADO:
        System.out.println("Estás divorciado");
        break;
}

En java la convención estilísta es poner las constantes en mayúsculas.

Todas las enumeraciones cuentan con métodos predefinidos:
- values(): devuelve un array que contiene la lista de constantes de la enumeración.
- valuesOf(String cadena): devuelve la constante de enumeración que se corresponde con la cadena pasada por parámetro.
- ordinal(): devuelve el número de la posición de la constante en la lista.

Este es un ejemplo de uso de values() y ordinal():
```java
//metemos la enumeracion en un array:
EstadoCivil [] valores = EstadoCivil.values();

//Ahora la recorremos con un bucle for each y la vamos imprimiendo:
for (EstadoCivil estado: valores) {
    int posicion = estado.ordinal();
    System.out.println("La constante número " + posicion + " es " + estado);
}
```

##Envoltorios de tipos
Cada variable o tipo tiene la equivalente clase envoltorio. Esto es debido a que en algunas situaciones no se van a poder utilizar variables de tipos primitivos sino objetos. Cuando utilizemos colecciones, se vera que son un conjunto de objetos.

|Tipo primitivo|Clase envoltorio|Clase atomic|
|--------------|----------------|------------|
|boolean|Boolean|AtomicBoolean|
|byte|Byte||
|char|Character||
|short|Short||
|int|Integer|AtomicInteger|
|long|Long|AtomicLong|
|float|Float||
|double|Double||

## Construcción:

```java
float sueldo = 1_245.8F;
Float oSueldo = new Float(sueldo);
```

```java
String sueldo = "1245.8";
Float oSueldo = new Float(sueldo);
```

## Método valueOf:

```java
Float peso = Float.valueOf("73,2");
Byteunbyte = Float.valueOf("00101011", 2);
```

## Metodo de Conversión xxxValue:

```java
Integer oNif = new Long("05221791");
long nif = oNif.longValue();
```

## Metodos de conversión parseXXX:
Lo utilizamos para convertir cadena a entero.
```java
int numero = Integer.parseInt("89789");
```

## Conversión String con toString:
Con este método convertimos a cadena.
```java
Double d = new Double(897_789_456E14);
String strd = d.toString();
System.out.println(strd);
System.out.println(d);
String cadena = "cadena de Java";
String cadena1 = cadena + ": tiene de longitud " + Long.toString(cadena.length());
```

## Conversion a binario, octal o hexadecimal con toXXXString:
```java
String octal = Long.toOctalString(4567895689L);
String binario = Integer.toBinaryString(44444);
String hexadecimal = Integer.toHexString(65535);
```

## Rango de valores y tamaño de los tipos:
```java
System.out.println("byte ===> MAYOR" + Byte.MAX_VALUE + "MENOR: " + Byte.MIN_VALUE + "SIZE: " + Byte.SIZE + "BYTES: " + Byte.BYTES);
```

## Autoboxing y Unboxing
En java se utilizan las sentencias break y continue para implementar saltos ocasionales en el flujo de control del programa. La sentencia break es utilizada en la estructura de switch, para interrumpir la ejecución de sentencias de cada una de las alternativas.

### Autoboxing
Consiste en la conversión automática de tipo primitivo a objeto de clase envoltorio. Se puede utilizar con todos los tipos base.
```java
Integer oint = 43;
Float ofloat = 125.8F;
Boolean oboolean = false;
```

### Unboxing
Es el procedimiento opuesto al autoboxing y se utiliza cuando es necesario volver a utilizar el valor.

```java
Integer oint = 125;
...
int i = oint;
```

## Modificadores de acceso y ámbitos

|Modificadores de acceso|Accesibilidad|
|-----------------------|-------------|

|..........................................|Clase|Variable|Método|
|---|---|---|---|
|private|Accesible sólo dentro del archivo o clase donde se define|Accesible dentro de la clase|Accesible dentro de la clase|
|protected|No se aplica|Accesible dentro de la propia clase y de sus herederos|Accesible dentro de la propia clase y las que la hereden|
|sin modificar|Accesible dentro de la propia clase las clases que esten en su mismo paquete|Accesible dentro de la propia clase las clases que esten en su mismo paquete|Accesible dentro de la propia clase las clases que esten en su mismo paquete|
|public|Accesible dentro de su propia clase y de las que la importen|Accesible dentro de su propia clase y de las que la importen|Accesible dentro de su propia clase y de las que la importen|

## Crear objetos: operador new
Para poder crear objetos de una clase se utiliza el operador new.

Estructura:
```
<nombre_clase><identificador> = new <nombre_clase>(<lista_parametros>);
```
Ejemplo de uso:

```java
Scanner escaner = new Scanner();
```

## Constructores y sobrecarga de Constructores
Son funciones que se ejecutan cuando se crean los objetos. Cuando se crea un objeto con new, primero se reserva el espacio para almacenar los valores. Cada constructor representa una forma distinta de crear los objetos de una clase.

- Constructor sin parametros:
```java
public class Clase02 {
    private int numero;
    private String nombre;

    public Clase02(){
        numero = 99;
        nombre ="antonio";

    }

}
```
Constructor con dos parametros:
```java
public class Clase02 {
    private int numero;
    private String nombre;

    public Clase02(int num, String cad){
        numero = num;
        nombre =cad;

    }

}
```
Constructor que recibe referencia objeto de Clase02:
```java
public class Clase02 {
    private int numero;
    private String nombre;

    public Clase02(Clase02 o){
        numero = o.numero;
        nombre = o.nombre;

    }

}
```
Los constructores se crean con el mismo nombre que la clase.

Ahora podemos crear objetos a partir del constructor según el que hayamos utilizado antes:

Para objeto de constructor sin parametros:

```java
Clase02 objeto1 = new Clase02();
        objeto1.leerDatos();
```
Para objeto de constructor con dos parametros:
```java
Clase02 objeto1 = new Clase02(18, "Pepe perez");
        objeto1.leerDatos();
```

Para objeto de constructor que recibe referencia:
```java
Clase02 objeto3 = new Clase02(objeto2);
objeto3.leerDatos();
```

## La referencia this
La palabra reservada this es una referencia al propio objeto. Solo se puede usuar dentro de las funciones de instancia y constructores. Cuando se usa this, se puede poner el identificador de cualquier miembro de instancia de la clase.

```java
public void modificaDatos(int num, String cad){
        this.numero = num;
        this.nombre = cad;

    }
```

Ejemplo de modificación de datos:

Clase02:
```java
package com.company.ejercicionavidadadivina;


import java.util.Scanner;

public class Clase02 {
    private int numero;
    private String nombre;

    public Clase02(int num, String cad){
        numero = num;
        nombre = cad;

    }

    public void modificaDatos(int num, String cad){
        System.out.println("Introduce un nuevo numero: \n");
        Scanner arreglar = new Scanner(System.in);
        num = arreglar.nextInt();
        this.numero = num;

        System.out.println("Introduce un nuevo nombre: \n");
        Scanner arreglar2 = new Scanner(System.in);
        cad = arreglar2.nextLine();
        this.nombre = cad;

    }



    public void leerDatos(){
        System.out.println("Nombre: " + nombre + " Numero: " + numero);
    }

}
```

Main:
```java
package com.company.ejercicionavidadadivina;

public class Main {

    public static void main(String[] args) {
        Clase02 objeto1 = new Clase02(18, "José");
        objeto1.leerDatos();
        objeto1.modificaDatos(18, "Jose");
        objeto1.leerDatos();

    }
}
```

o se puede hacer también así:

Clase04:
```java
package com.company.ejercicionavidadadivina;

import java.util.Scanner;

public class Clase04 {
    private static int numPersonas;

    private int numero;
    private String nombre;

    public static int cuentaPersonas(){
        return numPersonas;
    }

    public Clase04(){
        numPersonas++;
        numero = 99;
        nombre = "antonio";
    }

    public void imprime(){
        System.out.println(numPersonas + " " + numero +" " + nombre);
    }

    public void modifica(){
        System.out.println("Escoge un nuevo número: ");
        Scanner number = new Scanner(System.in);
        this.numero = number.nextInt();

        System.out.println("Escoge un nuevo nombre: ");
        Scanner name = new Scanner(System.in);
        this.nombre = name.nextLine();

    }


}
```
Main: 
```java
package com.company.ejercicionavidadadivina;

public class Main {

    public static void main(String[] args) {
        System.out.println("Número de personas: " + Clase04.cuentaPersonas());
        Clase04 clase = new Clase04();
        clase.imprime();
        clase.modifica();

        System.out.println("Número de personas: " + Clase04.cuentaPersonas());
        clase.imprime();
    }
}
```

## Variables y métodos de clase: miembros static
Los miembros de clase, vienen precededidos del modificador static. Las variables static son espacios compartidos por todos los objetos de la clase. Las funciones static son código de la clase, no de los objetos, por tanto no pueden utilizar la referencia this.

## Sobrecarga de métodos
Al igual que se sobrecargan los constructores, cualquier otro método o función puede estar sobrecargado. 

Este código presenta una función sobrecargada de 3 formas:

```java
package com.company.ejercicionavidadivina;

public class Clase06 {
    private static int numPersonas;

    final public static int edad_max = 65;
    private int numero;
    private String nombre;

    //Sobrecarga de tres formas:

    //Método 1:
    public void modificaDatos(String nombre, int numero){
        this.numero = numero;
        this.nombre = nombre;
    }

    //Método 2:
    public void modificaDatos(String nombre){
        this.nombre = nombre;
    }

    public void modificaDatos(String numero){
        this.numero = edad_max;
    }

    //Método 3:
    public void modificaDatos(){
        this.nombre = "anonimo";
        this.numero = edad_max;
    }

}
```
Y como se utiliza la función anterior:
```java
public class Main{
    public static void main(String[] args){
        //Método 1:
        Clase06 objeto1 = new Clase06();
        objeto1.modificaDatos("Luis Ruiz", 72);
        
        //Método 2:
        Clase06 objeto2 = new Clase06();
        objeto2.modificaDatos(Clase06.edad_max);

        Clase06 objeto3 = new Clase06();
        objeto3.modificaDatos(Clase06.nombre);

    }
}
```
## Métodos getter y setter
Son métodos de acceso a los datos de los objetos y son siempre públicos.
Cada método accede a un sólo dato (una sola variable de instancia) Para obtener su valor o cambiarlo.
Las funciones _getter_ retornan el valor de una variable de clase y las funciones _setter_ cambian el valor de una variable de clase. Por estilo estas funciones utilizan identificadores que comienzan por set o get seguidos del nombre de la variable comenzando por mayúsculas.

Este es un modo de definir las funciones getter y setter:

Desde una clase nueva llamada Clase07: 

```java
public class Clase07 {
    private int numero;
    private String nombre;

    public int getNumero(){
        return numero;
    }

    public void setNumero(int numero){
        this.numero = numero;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre){
        this.nombre = nombre;
    }

    //hemos creado un método sobrecargado para modificar los datos:
    public void modificaDatos(String nombre, int numero){
        this.nombre = nombre;
        this.numero = numero;
    }
}
```
Para obtener los getter y setter más rápido, podemos utilizar la opción de intelliJ alt+insert que los realiza automáticamente una vez seleccionadas las variables o.
Y este el modo de utilizarlas desde la clase Main en la función main:

```java
//vamos a crear el primer objeto en el que insertamos unos datos:
Clase07 objeto1 = new Clase07();
objeto1.modificaDatos("Luis Ruiz", 27);

//y ahora los imprimimos utilizando getter:
System.out.println("El nombre es " + objeto1.getNombre());
System.out.println(" y tiene un número igual a " + objeto1.getNumero());

//Ahora vamos a crear un nuevo objeto e insertaremos datos utilizando setter:
Clase07 objeto2 = new Clase07();
objeto2.setNumero(objeto1.getNumero()+1);
objeto2.setNombre("Rodolfo");

//y lo imprimimos para ver el resultado:
System.out.println("El nombre es " + objeto2.getNombre());
System.out.println(" y tiene un numero igual a " + objeto2.getNumero());

```
## toString
Cuando se llama a "print" o "println", se hace en referencia a un objeto instaciando de una clase llamando al método toString, si dicha clase no lo tiene implementado se ejecuta el de la clase Object.
Para que no se ejecute el código heredado de Object es necesario utilizar la función toString().
```java
//buscar referencias
```

## equals
El operador == no se puede utilizar para comparar si dos objetos son iguales o no. Para ello hay que sobreescribir la función equals(Object o)
de Object.

En este ejemplo vamos a utilizar la Clase07 usada antes:

```java
{
Clase07 objeto1 = new Clase07();
objeto1.modificaDatos("Luis Ruiz", 27);

Clase07 objeto2 = objeto1;

System.out.println(objeto1.equals(objeto2));
}
```
En este ejemplo estamos comparando dos objetos.







