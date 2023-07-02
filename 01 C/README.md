# PROGRAMACIÓN 1
Curso de Programación 1 CBTIS225


### Bienvenido al curso inicial de programación en lenguaje C.

<p style="color:#f92850; font-size: 16px; text-align:center;">¡ Pequeño repaso de conceptos !</p>

## Sistema de tipos de datos. (Números, textos, booleanos, variables y constantes)

Demos una introducción a lo que se refiere al sistema de tipos de datos en C++. Hablaremos específicamente acerca de los tipos de datos o variables más comunes, sus características generales, su utilidad, entre otras cosas. 


### Tipos nativos o primitivos

Los tipos nativos, son los tipos de datos "fáciles de usar" es decir, son los tipos de datos más básicos y simples del sistema de tipos de C++ y por ello es bastante fácil usarlos.

Los condicionales Switch, son una estructura de control condicional, que permite definir múltiples casos que puede llegar a cumplir una variable cualquiera, y qué acción tomar en cualquiera de estas situaciones, incluso es posible determinar qué acción llevar a cabo en caso de no cumplir ninguna de las condiciones dadas.

### Declaración y asignación a variables

Una variable es un dato cuyo valor puede cambiar a lo largo de la ejecución de un programa.

En un nivel más lógico, una variable ocupa un espacio de memoria para contener sus valores durante la ejecución de un programa. Cada variable debe pertenecer a un tipo determinado dando también el tamaño del espacio de memoria ocupado por la variable, y el modo en que se manipulará esa memoria.

Los tipos fundamentales (básicos), que son: void, char, int, float y double; en C++ se incluye también el tipo bool. También existen ciertos modificadores, que permiten ajustar ligeramente ciertas propiedades de cada tipo; los modificadores pueden ser: short, long, signed y unsigned, y pueden combinarse algunos de ellos.

### ¿Cómo se declara una variable en C++?

La sintaxis para una variable es la siguiente:

    [modificadores] [tipo de variable] [nombre de la variable] [=] [valor];

En la declaración de una variable se debe colocar como mínimo el tipo de dato, el nombre y el punto y coma al final de la línea, los modificadores son opcionales, es decir no es necesario ponerlos y tampoco es obligatorio asignarle un valor a la variable de inmediato. Si no se pone ningún modificador, el compilador tomará nuestra variable como signed, es decir podría ser positivo o negativo.

En el momento de asignar un nombre a una variable se deben seguir algunas normas:

1. El nombre de una variable nunca debe comenzar con un numero.
2. No debes incluir algunos caracteres como símbolos matemáticos, guiones (el guión bajo"_" si es permitido), comas, punto y coma, comillas, signos de interrogación o espacios en blanco.
3. Deben tener un máximo de 40 caracteres
También, hay algunas palabras que son reservadas del lenguaje, es decir tus variables no podrán tener estos nombre (no creo que tengas problemas con esto, especialmente si escribes en español). Las palabras son las siguientes:

### Palabras reservadas de C++

    auto        const	    double	    float
    int         short	    struct	    unsigned
    break	    continue        else	    for
    long	    signed	    switch	    void
    case	    default	    enum	    goto
    register    sizeof	    typedef	    volatile
    char	    do	            extern	    if
    return	    static	    union	    while

### Tipos de Datos en C++

- `bool:` El tipo de dato bool, tiene un tamaño de 8 bits y un rango entre 0 y 1, en pocas palabras es cero o es uno (falso o verdadero). Este tipo de dato, es comúnmente usado en condicionales o variables que solo pueden tomar el valor de falso o verdadero. Las variables de tipo bool no suelen llevar modificadores, pues son innecesarios, ya que su rango es solo 0 y 1.
- `int:` El tipo de dato int, tiene un tamaño de 32 bits y un rango entre -2.147.483.648 y 2.147.483.647. Este tipo de dato, es usado para números enteros (sin cifras decimales). A continuación alguna combinaciones con los modificadores:
    - `short int:` Tiene un tamaño de 16 bits y un rango entre -32.768 y 32.767.
    - `unsigned short int:` Tiene un tamaño de 16 bits y un rango entre 0 y 65535.
    - `unsigned int:` Tiene un tamaño de 32 bits y un rango entre 0 y 4.294.967.295.
    - `long long int:` Tiene un tamaño de 64 bits y un rango entre -9.223.372.775.808 y 9.223.375.775.807.
    - `unsigned long long int:` Tiene un tamaño de 64 bits y un rango entre 0 y 2exp64.
- `float:` El tipo de dato float tiene un tamaño de 32 bits, es usado comúnmente en números con 6 o menos cifras decimales. Tiene un rango entre 1,17549*(e^-38) hasta 3,40282*(e^+38).
- `double:` El tipo de dato double tiene un tamaño de 64 bits, es usado para números de menos de 15 cifras decimales. Tiene un rango entre 2,22507*(e^-308) hasta 1,79769*(e^308).
- `long double:` Tiene un tamaño de 96 bits y una precisión de 18 cifras decimales. Tiene un rango entre 3,3621*(e^-4932) hasta 1,18973*(e^4932).

### Instrucciones de Asignación

Una instrucción de asignación, como su nombre bien lo dice, es una línea de código, que le asigna a una variable cualquiera un valor cualquiera, preferiblemente adecuado al tipo de dato o a las necesidades de dicha asignación. Una asignación tiene la siguiente sintaxis: nombre_variable = valor, con esto le estamos diciendo a nuestro programa que la variable llamada "nombre_variable", tendrá ahora como nuevo valor a "valor". Así entonces por ejemplo, al escribir contador = 0; estamos diciendo que la variable contador tendrá como nuevo valor 0, es de tener en cuenta que al realizar una asignación, si la variable tenía algún otro valor antes de esto, dicho valor se perderá y cambiaría por el nuevo que le hemos ordenado.

### Variables

Las variables son altamente imprescindibles al momento de programar, de hecho sería imposible conseguir una aplicación con una funcionalidad básica sin usar variables; por esta misma razón es necesario aprender a usarlas bien y lo tenemos muy fácil, pues su uso es bastante sencillo e intuitivo, tanto para declararlas como para asignarles valores.

Las variables son posiciones en memoria donde estarán guardados los diferentes valores que le damos o que toman duranet ejecución los datos que usamos y normalmente estarán disponibles a lo largo de la ejecución de nuestro programa. Para asignar valores a una variable en una gran variedad de lenguajes que incluye a C++ se usa el operador "=" seguido del valor que le daremos a la variable (no todos usan el "=" para esto). Veamos un ejemplo completo con todos los posibles usos que le damos a una variable.


    #include <iostream>
    using namespace std;
    
    int main()
    {
        char x = 'a'; // Declaramos y asignamos en la misma línea
    
        int num; //Declaramos el entero en una línea
        num = 5; //Le asignamos un valor en otra línea
    
        int num2 = 8; //Asignacion y declaracion al tiempo
    
        float numero; //Un numero decimal
        numero = 3.5; //Le asignamos un valor al decimal
    
        float res = numero + num2; //Sumamos dos variables y las asignamos a res
        //3.5 + 8 = 11.5
    
        res = res + num; //Al valor actual de res le sumamos el valor de num
        //11.5 + 5 = 16.5
    
        bool valor = false; //Variable booleana
        valor = true; // Pueden ser true o false
    
        res = res*2; //Duplicamos el valor de res 16.5*2 = 33
    
        cout << res << endl; //Mostramos el valor de res por pantalla
    
        return 0;
    }

### Salida de texto por pantalla en C++

Mostrar texto por pantalla en C++ es muy simple. Para imprimir una salida de texto en C++ se hace uso de la instrucción cout, junto con <<. Es importante tener en cuenta que la instrucción cout siempre va acompañada de << para controlar el flujo de datos que sale. No te fijes mucho en ellos, solo ten siempre presente que cout viene acompañado de << para tener cout << como resultado.

#### Veamos algunos ejemplos para mostrar texto por pantalla en C++

#### 1. impresión de texto por pantalla en C++, usando cout

    #include "iostream"
    
    using namespace std;
    
    int main()
    {
        //Se muestra un mensaje por pantalla.
        cout << "Hola Mundo" << " Desde ProgramarYa." << "\n";
    
        return 0;
    }

#### 2. impresión de texto por pantalla en C++, usando cout

    #include "iostream"
    #include "string"
    
    using namespace std;
    
    int main()
    {
        //El valor de esta variable se mostrará en pantalla
        string salida1 = "Ejemplo de salida";
    
        //Este valor también se mostrará en pantalla.
        int numero = 2;
    
        //Estos valores se concatenarán en una única salida
        string salida2 = "Desde ProgramarYa.";
    
        //Se concatenan y muestran los valores por pantalla con cout<<
        cout << salida1 << " " << numero << ". " << salida2 << "\n";
    
       return 0;
    }

### Entrada o lectura de datos en C++

Tal como mencioné hace un momento, la lectura de datos en C++ es bastante simple. Leer datos por teclado en C++ se hace usando el comando cin >> es importante notar el uso de los dos signos >> que son usados para controlar el flujo de datos. No te preocupes mucho por ellos, solo ten en cuenta que cada vez que vaya a usar la instrucción cin debes agregarle >> para quedar con un cin>>. Una manera muy sencilla de recordar esta instrucción es que in significa entrar y como estamos programando en C++ le añadimos la letra C al comienzo quedando así cin>> (sin olvidar los >>).

#### 1. lectura de datos en C++, usando cin

    #include "iostream"
    #include "string"
    
    using namespace std;
    
    int main()
    {
        cout << "Hola! Este es un ejemplo en C++" << "\n" << "Por favor ingrese su nombre:" << "\n";
        //La instrucción \n es un salto de línea Mostrando los textos separados
    
       string nombre;//En esta variable estará almacenado el nombre ingresado.
       cin >> nombre; //Se lee el nombre
    
       cout << "Bienvenido al sistema " << nombre << ". Gracias por usar nuestra aplicación" << "\n";
    
       return 0;
    }

#### 2. lectura de datos en C++, usando getline y cin

    #include "iostream"
    #include "string"
    
    using namespace std;
    
    int main()
    {
        cout << "Hola! Este es un ejemplo en C++" << "\n" << "Por favor ingrese su nombre:" << "\n";
        //Volvemos a mostrar el mismo mensaje, pues para mostrar datos no hay problemas
    
       string nombre;//Seguimos usando string para almacenar el nombre
       //cin >> nombre; //Esta línea da problemas si se lee un valor con espacios
       // En su lugar, usamos getline, con el flujo de entrada de cin y lo asignamos as nombre
       getline(cin, nombre); //Esta línea no dará problemas con los espacios en el nombre
    
       cout << "Bienvenido al sistema " << nombre << ". Gracias por usar nuestra aplicación" << "\n";
    
       return 0;
    }

## Los condicionales. Uso declaración y sintaxis.

Los condicionales en C++, son una estructura de control esencial al momento de programar y aprender a programar. Tanto C como C++ y la mayoría de los lenguajes de programación utilizados actualmente, nos permiten hacer uso de estas estructuras parea definir ciertas acciones condiciones especificas en nuestro algoritmo. Un condicional, permite establecer una serie de condiciones al interior de nuestro programa, que nos ayudan a determinar que acciones llevará cabo dadas ciertas circunstancias, por ejemplo si queremos decidir cuándo dar acceso a un usuario, dependiendo de si el nombre de usuario y contraseña son correctos, para algo como esto, es útil un condicional, nos permite verificar si determinada condición se cumple (en este caso si la contraseña y el nombre de usuario son correctos) y de acuerdo a que se cumpla o no, llevar a cabo un conjunto de acciones. Los condicionales aumentan la "expresividad" de un software, es decir nos permiten considerar diferentes situaciones con antelación, evitando o permitiendo sortear diferentes tipos de situaciones que son del interés de nuestra aplicación.


Existen diferentes tipos de condicionales, cada uno tiene una utilidad y funcionalidad diferente, que consideran diferentes situaciones que se pueden llegar a presentar durante la ejecución de un algoritmo. Depende entonces del conocimiento que tengamos acerca de cada uno de los condicionales saber determinar correctamente cuando es necesario implementar uno u otro. Tenemos a nuestra disposición los siguientes tipos de condicionales en C++:

- `Condicional If`
- `Condicional if-else`
- `Condicional Switch`

### ¿Cómo funciona un Condicional If?

Para comprender mejor cómo funciona el condicional if, una muy buena forma es partiendo de un ejemplo. Supongamos que queremos verificar si el resultado de una suma ingresada por el usuario es correcto o no. Para este ejemplo, el condicional if, es el encargado de verificar si el resultado ingresado corresponde o no a la respuesta correcta de la suma. El condicional if, funciona verificando la condición ingresada y de acuerdo a su valor de verdad (falso o verdadero) lleva a cabo o no una serie de instrucciones.

### Sintaxis del Condicional if

    if(condición a evaluar) //Por ejemplo X <= 10
    {
            ....
            ....
        Bloque de Instrucciones si se cumple la condición....
            ....
            ....
    }
    ....
    Bloque de Instrucciones restante DEL ALGORITMO....
    ....

### Ejemplos de Condicional If

    int resultado = 0;
    cout << "Cuanto es 39+50? ";
    cin >> resultado;
    if(resultado == 39+50)
    {
        cout << "Respuesta Correcta. Felicitaciones!\n";
    }

#### El código funcional completo sería el siguiente:
    #include "iostream"
    
    using namespace std;
    
    int main()
    {
        int resultado = 0;
        cout << "Cuanto es 39+50? ";
        cin >> resultado;
        if(resultado == 39+50)
        {
            cout << "Respuesta Correcta. Felicitaciones!\n";
        }
    
        system("PAUSE");
    }

### ¿Cómo funciona un Condicional If-Else?

Los condicionales if-else, son una estructura de control, que nos permiten tomar cierta decisión al interior de nuestro algoritmo, es decir, nos permiten determinar que acciones tomar dada o no cierta condición, por ejemplo determinar si la contraseña ingresada por el usuario es válida o no y de acuerdo a esto darle acceso al sistema o mostrar un mensaje de error.

Se les conoce también como estructuras selectivas de casos dobles (porque definen ambas posibilidades en la ejecución --si se cumple y si no se cumple --).

En resumen, un condicional if-else es una estructura que nos posibilita definir las acciones que se deben llevar a cabo si se cumple cierta condición y también determinar las acciones que se deben ejecutar en caso de que no se cumpla; generando así una separación o bifurcación en la ejecución del programa, ejecutando ciertas acciones u otras a partir de la evaluación de una condición dada.

### Sintaxis del Condicional if else

    if(condición a evaluar) //Por ejemplo 50 <= 10
    {
            ....
            ....
        Bloque de Instrucciones si se cumple la condición....
            ....
            ....
    }
    else
    {
            ....
            ....
        Bloque de Instrucciones si NO se cumple la condición....
            ....
            ....
    }

### Ejemplos de Condicional If-else

#### Sistema de logeo
    string password = "";
    cout << "Ingrese la contrasenia: ";
    cin >> password;
    if(password == "myClave")
    {
        cout << "Contrasenia correcta. Bienvenido";
    }
    else
    {
        cout << "Contrasenia incorrecta.";
    }

#### El código funcional completo sería el siguiente:

    #include "iostream"
    #include "string"
    #include "stdlib.h"
    
    using namespace std;
    
    int main()
    {
        string password = "";
        cout << "Ingrese la contrasenia: ";
        cin >> password;
        if(password == "myClave")
        {
            cout << "Contrasenia correcta. Bienvenido";
        }
        else
        {
            cout << "Contrasenia incorrecta.";
        }
    
        system("PAUSE");
    
        return 0;
    }

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
    
