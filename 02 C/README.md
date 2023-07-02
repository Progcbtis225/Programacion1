# PROGRAMACIÓN 1
Curso de Programación 1 CBTIS225


### Bienvenido al curso inicial de programación en lenguaje C.

<p style="color:#f92850; font-size: 16px; text-align:center;">¡ Pequeño repaso de conceptos !</p>

## Condicional switch

### ¿Qué es Condicional Switch?

Los condicionales Switch, son una estructura de control condicional, que permite definir múltiples casos que puede llegar a cumplir una variable cualquiera, y qué acción tomar en cualquiera de estas situaciones, incluso es posible determinar qué acción llevar a cabo en caso de no cumplir ninguna de las condiciones dadas.

### Sintaxis del Condicional Switch

    switch(opción) //donde opción es la variable a comparar
    {
        case valor1: //Bloque de instrucciones 1;
        break;
        case valor2: //Bloque de instrucciones 2;
        break;
        case valor3: //Bloque de instrucciones 3;
        break;
        //Nótese que valor 1 2 y 3 son los valores que puede tomar la opción
        //la instrucción break es necesaria, para no ejecutar todos los casos.
        default: //Bloque de instrucciones por defecto;
        //default, es el bloque que se ejecuta en caso de que no se de ningún caso
    }

### Ejemplos de Condicional Switch

#### Menú de Opciones
    cout << "Ingrese la Opción a ejecutar: ";
    int opcion = 0;
    cin >> opcion;
    switch(opcion)
    {
        case 1: cout << "Usted ha seleccionado la opción 1";
        break;
        case 2: cout << "Usted ha seleccionado la opción 2";
        break;
        case 3: cout << "Usted ha seleccionado la opción 3";
        break;
        default: cout << "Usted ha ingresado una opción incorrecta";
    }

#### El código funcional completo sería el siguiente:

    # include "iostream"

    using namespace std;

    int main()
    {
        cout << "Ingrese la Opción a ejecutar: ";
        int opcion = 0;
        cin >> opcion;
    
        switch(opcion)
        {
            case 1: cout << "Usted ha seleccionado la opción 1";
            break;
            case 2: cout << "Usted ha seleccionado la opción 2";
            break;
            case 3: cout << "Usted ha seleccionado la opción 3";
            break;
            default: cout << "Usted ha ingresado una opción incorrecta";
        }
        // system("PAUSE"); //Solo ponla si no te da error
        return 0;
    }
    
## Los bucles o ciclos

Los ciclos o también conocidos como bucles, son una estructura de control esencial al momento de programar. Tanto C como C++ y la mayoría de los lenguajes utilizados actualmente, nos permiten hacer uso de estas estructuras. Un ciclo o bucle permite repetir una o varias instrucciones cuantas veces lo necesitemos, por ejemplo, si quisiéramos escribir los números del uno al cien no tendría sentido escribir cien líneas mostrando un numero en cada una, para esto y para muchísimas cosas más, es útil un ciclo, permitiéndonos hacer una misma tarea en una cantidad de líneas muy pequeña y de forma prácticamente automática.

Existen diferentes tipos de ciclos o bucles, cada uno tiene una utilidad para casos específicos y depende de nuestra habilidad y conocimientos poder determinar en qué momento es bueno usar alguno de ellos. Tenemos entonces a nuestra disposición los siguientes tipos de ciclos:

 - `Ciclo for`
 - `Ciclo while`
 - `Ciclo do-while` 

 ### Sintaxis del Ciclo For

    for(int i = valor inicial; i <= valor final; i = i + paso)
    {
            ....
            ....
        Bloque de Instrucciones....
            ....
            ....
    }

### Ejemplos de Ciclo For

#### Mostrar en pantalla los números pares

    for(int i=50;i<=100;i+=2)
    {//Notemos que escribir i+=2 es similar a escribir i = i + 2
        cout << i << endl;
    }    

#### El código funcional completo sería el siguiente:

    #include "iostream"
    #include "stdlib.h"

    using namespace std;

    int main()
    {

        for(int i=50;i<=100;i+=2)
        {//Notemos que escribir i+=2 es similar a escribir i = i + 2
            cout << i << endl;
        }
        system("PAUSE");
        return 0;
    }    
    
#### Cuenta regresiva en un ciclo for
Para este caso, debido a que queremos ir de un número mayor a uno más pequeño, por lo tanto para este ejemplo el valor inicial será 10 y el valor final será cero. Adicional, el tamaño de paso será de 1 negativo, es decir, -1, así:

    for(int i=10;i > 0; i--)
    {//Notemos que escribir i-- es similar a escribir i = i - 1
        cout << i << endl;
    }
#### El código funcional completo sería el siguiente:

    #include "iostream"
    #include "stdlib.h"

    using namespace std;
    int main()
    {
    
        for(int i=10; i > 0; i--)
        {//Notemos que escribir i-- es similar a escribir i = i - 1
            cout << i << endl;
        }
        system("PAUSE");
        return 0;
    }

#### Contador con un ciclo for
Para este ejemplo haremos algo un poco más complejo. El ejemplo consiste en contar al interior de un ciclo for, cuántos números entre el 0 y el 10.000 son múltiplos del 13. Para ello haremos uso del operador % (modulo) que obtiene el residuo de una división y también usaremos un pequeño condicional para verificar que el modulo sea cero al dividir por 13.

Para este caso el valor inicial será 0 y el valor final será 10000. Adicional, el tamaño de paso será de 1. Al interior del ciclo, en cada iteración verificaremos si el número en el que estamos es divisible por trece o no y en caso afirmativo aumentaremos el contador en una unidad así:

    int contador = 0; //Iniciamos el contador en cero
    for(int i = 0; i < 10000; i++)
    {//Notemos que escribir i++ es similar a escribir i = i + 1
        if(i%13 == 0) //Si el residuo es cero es múltiplo de 13
        {
            contador++; //Si es múltiplo aumentamos el contador en 1
        }
    }
    //Mostramos el contador después de verificar todos los números
    cout << contador << endl;

#### El código funcional completo sería el siguiente:

    #include "iostream"
    #include "stdlib.h"
    
    using namespace std;
    int main()
    {
        int contador = 0; //Iniciamos el contador en cero
        for(int i = 0; i < 10000; i++)
        {//Notemos que escribir i++ es similar a escribir i = i + 1
            if(i%13 == 0) //Si el residuo es cero es múltiplo de 13
            {
                contador++; //Si es múltiplo aumentamos el contador en 1
            }
        }
        //Mostramos el contador después de verificar todos los números
        cout << contador << endl;
        system("PAUSE");
        return 0;
    }    

### Ciclo While

Los ciclos while son también una estructura cíclica, que nos permite ejecutar una o varias líneas de código de manera repetitiva sin necesidad de tener un valor inicial e incluso a veces sin siquiera conocer cuando se va a dar el valor final que esperamos, los ciclos while, no dependen directamente de valores numéricos, sino de valores booleanos, es decir su ejecución depende del valor de verdad de una condición dada, verdadera o falso, nada más. De este modo los ciclos while, son mucho más efectivos para condiciones indeterminadas, que no conocemos cuando se van a dar a diferencia de los ciclos for, con los cuales se debe tener claro un principio, un final y un tamaño de paso.

### Sintaxis del Ciclo While

    while(condición de finalización) //por ejemplo numero == 100
    {
            ....
            ....
        Bloque de Instrucciones....
            ....
            ....
    }

### Ejemplos de Ciclo While

#### Pedir números por pantalla hasta que alguno sea mayor a 100

    int numero;
    cin >> numero;
    while(numero <= 100)
    {
        cout <<  "Ingrese un numero ";
        cin >> numero;
    }

#### El código funcional completo sería el siguiente:

    #include "iostream"
    
    using namespace std;
    int main()
    {
        int numero;
        cout <<  "Ingrese un numero ";
        cin >> numero;
        while(numero <= 100)
        {
            cout <<  "Ingrese un numero ";
            cin >> numero;
        }
        system("PAUSE");
        return 0;
    }

### Ciclo Do-While

Los ciclos do-while son una estructura de control cíclica, los cuales nos permiten ejecutar una o varias líneas de código de forma repetitiva sin necesidad de tener un valor inicial e incluso a veces sin siquiera conocer cuando se va a dar el valor final, hasta aquí son similares a los ciclos while, sin embargo el ciclo do-while nos permite añadir cierta ventaja adicional y esta consiste que nos da la posibilidad de ejecutar primero el bloque de instrucciones antes de evaluar la condición necesaria, de este modo los ciclos do-while, son más efectivos para algunas situaciones especificas. En resumen un ciclo do-while, es una estructura de control cíclica que permite ejecutar de manera repetitiva un bloque de instrucciones sin evaluar de forma inmediata una condición especifica, sino evaluándola justo después de ejecutar por primera vez el bloque de instrucciones.

Para comprender mejor el funcionamiento del ciclo while, usemos de nuevo el ejemplo de la sección anterior sobre el ciclo while. Imaginemos entonces que por algún motivo, queremos pedirle a un usuario una serie de números cualquiera y que solo dejaremos de hacerlo cuando el usuario ingrese un número mayor a 100. Como vimos anteriormente, esto se puede hacer por medio de un ciclo while, pero vamos ahora a ver como lo podemos hacer usando un ciclo do-while mejorando así un poco nuestro algoritmo, evitando ciertos comandos, tal como se dijo con el ciclo while, en efecto aquí estamos en la situación de no tener ni idea de cuándo al usuario se le va a ocurrir ingresar un número mayor que 100, pues es algo indeterminado para nosotros, sin embargo el ciclo while y en efecto el do-while nos permite ejecutar cierta acción de forma infinita hasta que se cumpla alguna condición especifica, en nuestro caso sería que el numero ingresado sea mayor a 100. De modo que si el usuario nos ingresa de manera sucesiva los siguientes numero 1,50,99, 49, 21, 30, 100 ..., nuestro programa no finalizara, pues ninguno de estos números es mayor que 100, sin embargo si nos ingresara el numero 300, el programa finalizaría inmediatamente.

### Sintaxis del Ciclo Do-While

    do
    {
            ....
            ....
        Bloque de Instrucciones....
            ....
            ....
    }
    while(condición de finalización); //por ejemplo numero != 23

### Ejemplos de Ciclo Do-While

#### Pedir números por pantalla hasta que alguno sea mayor a 100

    int numero;
    do
    {
        cout <<  "Ingrese un numero ";
        cin >> numero;
    }
    while(numero <= 100);

#### El código funcional completo sería el siguiente:

    #include "iostream"
    
    using namespace std;
    int main()
    {
        int numero;
        do
        {
            cout <<  "Ingrese un numero ";
            cin >> numero;
        }
        while(numero <= 100);
        system("PAUSE");
        return 0;
    }
