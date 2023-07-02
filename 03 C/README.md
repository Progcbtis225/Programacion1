# PROGRAMACIÓN 1
Curso de Programación 1 CBTIS225

### Bienvenido al curso inicial de programación en lenguaje C.

<p style="color:#f92850; font-size: 16px; text-align:center;">¡ Pequeño repaso de conceptos !</p>

## Estructuras de datos

### ¿Qué son las Estructuras de Datos?

Las estructuras de datos se pueden entender como un tipo de dato compuesto (no complejo). Las estructuras de datos permiten almacenar de manera ordenada una serie de valores dados en una misma variable. Las estructuras de datos más comunes son los arrays, que pueden ser unidimensionales (de una dimensión) también conocidos como vectores, o multidimensionales (de varias dimensiones) también conocidos como matrices, aunque hay otras un poco más diferentes como son struct, las enumeraciones y los punteros.

### Arrays, arreglos y vectores

Los vectores son un tipo de array (arreglos). Son, de hecho, un array de una sola dimensión y forman parte de la amplia variedad de estructuras de datos que nos ofrecen los lengiajes, siendo además una de las principales y más útiles estructuras que podremos tener como herramienta de programación. Los vectores o arrays o arreglos de una dimensión (como los quieras llamar), son utilizados para almacenar múltiples valores en una única variable. En un aspecto más profundo, este tipo de arrays (vectores), permiten almacenar muchos valores en posiciones de memoria continuas, lo cual permite acceder a un valor u otro de manera rápida y sencilla. Estos valores pueden ser números, letras o cualquier tipo de variable que deseemos incluso tipos de datos complejos.

### ¿Cómo declarar un Array de una dimensión o Vector?

    tipo_de_dato nombre_del_vector[tamanio];
.

    int my_vector1[10];
    float my_vector2[25];
    string my_vector3[500];
    bool my_vector4[1000];
    char my_vector5[2];

### ¿Cómo inicializar un Array o Vector?
    string vector[5] = {"5", "hola", "2.7", "8,9", "adios"};
.

    int vector2[] = {1,2,3,4,10,9,80,70,19};
    
### Obtener el valor de una casilla específica en un array 

    float vector4[5] = {10.5, 5.1, 8.9, 10, 95.2}; //Array con 5 elementos
    float numero5 = vector4[4]; //Para acceder al elemento 5, se usa el índice 4
    float primerNumero = vector4[0]; //Para el primer elemento se usa el índice 0



### Recorrer un Array o Vector

Para obtener todos los datos que se encuentran al interior de un vector, es necesario recorrer el array o vector, para recorrerlo, se usa casi siempre un ciclo for, en algunos casos mas específicos un ciclo while, pero generalmente el ciclo for es el ideal para esto, dado que conocemos el tamaño del array. La lógica de este procedimiento es la siguiente, el ciclo for comenzara desde cero e ira hasta el tamaño del vector, de modo que la variable de control que generalmente llamamos "i", será la que va a ir variando entre cero y el tamaño del array, de esta forma al poner la i al interior de los corchetes, estaremos accediendo al valor de cada casilla del vector y podremos hacer lo que sea necesario con dicho valor.

Nota: A veces no es posible determinar con facilidad el tamaño exacto de un vector, pero en C++ existen varias formas de determinar el tamaño de un array o vector fácilmente, aquí explicare un método. Cabe notar que este tamaño es el que ira como tope del ciclo for y sería equivalente a que nosotros mismos, en caso de saber el tamaño del vector, lo pongamos allí, sin embargo como veremos en otra sección no siempre es posible saber con certeza el tamaño de un vector, es por esto que explico cómo hacerlo.

    #include "iostream"
    
    using namespace std;
    
    int main()
    {
        int edades[] = {1,2,9,8,16,32,9,50,36,20,1,87};
        int limite = (sizeof(edades)/sizeof(edades[0]));
        for (int i = 0; i < limite; i++)
        {
                cout<<edades[i]<<endl;
        }
    }


El operador sizeof en C++, retorna el tamaño en bytes del elemento que se indica. En este caso, como es un array, indica el tamaño total de ese array en bytes. Como el tipo de dato int tiene un tamaño de 4 bytes, un array de 12 elementos de tipo int tendrá 48 bytes. Luego, el tamaño del primer elemento (o cualquiera de ellos) será 4. Así, 48 dividido entre 4 es 12, que es el tamaño de nuestro array.


### Ejemplos Array o Vectores
#### El código funcional completo sería el siguiente:

    #include "iostream"
    
    using namespace std;
    
    int main()
    {
        char titulos[5];
        char autores[5];
        cout << "Por favor ingrese la siguiente información de los Libros: \n";
        for(int i = 0; i < 5; i++)
        {
            cout << "\n******* Libro " << i + 1 <<"********:\n";
            cout << "Titulo: ";
            cin >> titulos[i];
            cout << "Autor: ";
            cin >> autores[i];
        }
    }


#### El código funcional completo mejorado


    #include "iostream"
    #include "string"
    using namespace std;
    
    
    int main()
    {
        string titulos[5];
        string autores[5];
        cout << "Por favor ingrese la siguiente información de los Libros: \n";
        for(int i = 0; i < 5; i++)
        {
            cout << "\n******* Libro " << i + 1 << "********:\n";
            cout << "Titulo: ";
            cin >> titulos[i];
            cout << "Autor: ";
            cin >> autores[i];
        }
    }

#### El código funcional perfeccionado

    #include "iostream"
    #include "string"
    using namespace std;
    
    int main()
    {
        string titulos[5];
        string autores[5];
        cout << "Por favor ingrese la siguiente información de los Libros: \n";
        for(int i = 0; i < 5; i++)
        {
            cout << "\n******* Libro " << i + 1 << "********:\n";
            cout << "Titulo: ";
            //cin >> titulos[i]; //No funciona con espacios
            getline(cin, titulos[i]);
            cout << "Autor: ";
            //cin >> autores[i]; //No funciona con espacios
            getline(cin, autores[i]);
        }
    }

Como puedes apreciar, hemos reemplazado las líneas que usaban cin para leer los datos por la función getline(...) que recibe como primer argumento el flujo de entrada de cin y como segundo argumento la variable en la que queremos poner el valor.

