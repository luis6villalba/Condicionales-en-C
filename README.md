# Condicionales-en-C
Desarrollar una serie de ejercicios con su debida explicación, que indiquen el uso de condicionales en lenguaje "C".

## Reto numero 1 - Numero mayor y menor
Escribe un programa que pida al usuario 2 números, mostrando como salida cuál es el número mayor y la diferencia de uno respecto al otro. En caso de que los números sean iguales, mostrarlo también en pantalla.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluye la biblioteca -`stdio.h`- para funciones de entrada y salida.

2. Luego, se define la función principal -`main`-, que es el punto de entrada del programa.

3. Dentro de la función -`main`-, se declaran dos variables llamadas -`num1`- y -`num2`- de tipo -`int`- (entero) para almacenar los dos números ingresados por el usuario.

4. Se utiliza la función -`printf`- para mostrar un mensaje al usuario pidiéndole que ingrese el primer número.

5. Se utiliza la función -`scanf`- para leer el primer número ingresado por el usuario desde la entrada estándar (generalmente el teclado) y almacenarlo en la variable -`num1`-.

6. Se repiten los pasos 4 y 5 para pedir al usuario que ingrese el segundo número y almacenarlo en la variable -`num2`-.

7. Después, se utiliza un condicional -`if`- para verificar si el valor de la variable -`num1`- es mayor que el valor de la variable -`num2`-. Si es así, se muestra un mensaje utilizando la función -`printf`- indicando que el número mayor es -`num1`- y se muestra la diferencia entre los dos números.

8. Si el valor de -`num1`- no es mayor que el valor de -`num2`-, se entra en el bloque de código dentro del condicional -`else if`-, donde se verifica si el valor de la variable -`num2`- es mayor que el valor de la variable -`num1`-. Si es así, se muestra un mensaje utilizando la función -`printf`- indicando que el número mayor es -`num2`- y se muestra la diferencia entre los dos números.

9. Si ninguna de las condiciones anteriores se cumple (es decir, si los valores de las variables -`num1`- y -`num2`- son iguales), se entra en el bloque de código dentro del condicional -`else`-, donde se muestra un mensaje utilizando la función -`printf`- indicando que los dos números son iguales.

10. Finalmente, la función -`main`- retorna a cero para indicar que el programa terminó correctamente.

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo


#include<stdio.h>

int main()
{
  int num1, num2;
  printf("Introduce el primer numero: ");
  scanf("%d", &num1);
  printf("Introduce el primer numero: ");
  scanf("%d", &num2);
  if (num1 > num2)
    {
      printf("El numero mayor es: %d\n", num1);
      printf("La diferencia entre los dos numeros es: %d\n", num1 - num2);
    }
  
  else if(num2 > num1)
    {
      printf("El numero mayor es: %d\n", num2);
      printf("La diferencia entre los dos numeros es: %d\n", num2 - num1);
    }

  else
    {
      printf("Los dos numeros son iguales. \n");
    }

  return 0;
}

## Reto numero 2 - En el rango, por favor.

Pide al usuario que indique 2 números: uno que servirá como límite y otro para comparar. Si el segundo número es menor al primero, mostrarás un mensaje diciendo “El número ‘x’ se encuentra en el rango, gracias” y en caso contrario dirá “El número ‘x’ excede el límite permitido”.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluye la biblioteca `stdio.h` para funciones de entrada y salida.

2. Luego, se define la función principal `main`, que es el punto de entrada del programa.

3. Dentro de la función `main`, se declaran dos variables llamadas `limite` y `num` de tipo `int` (entero) para almacenar el límite y el número ingresado por el usuario, respectivamente.

4. Se utiliza la función `printf` para mostrar un mensaje al usuario pidiéndole que ingrese el límite.

5. Se utiliza la función `scanf` para leer el límite ingresado por el usuario desde la entrada estándar (generalmente el teclado) y almacenarlo en la variable `limite`.

6. Se repiten los pasos 4 y 5 para pedir al usuario que ingrese el número a comparar y almacenarlo en la variable `num`.

7. Después, se utiliza un condicional `if` para verificar si el valor de la variable `num` es menor que el valor de la variable `limite`. Si es así, se muestra un mensaje utilizando la función `printf` indicando que el número se encuentra en el rango.

8. Si el valor de `num` no es menor que el valor de `limite`, se entra en el bloque de código dentro del condicional `else`, donde se muestra un mensaje utilizando la función `printf` indicando que el número excede el límite permitido.

9. Finalmente, la función `main` retorna 0 para indicar que el programa terminó correctamente.

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo.

#include<stdio.h>

int main()
{
    int limite, num;
    printf("Introduce el limite: ");
    scanf("%d", &limite);
    printf("Introduce el numero para comparar: ");
    scanf("%d", &num);

    if (num < limite)
        {
            printf("El numero %d se encuentra en el rango, gracias\n", num);
        }
    
    else
        {
            printf("El numero excede el limite permitido, lo siento\n");
        }

    return 0;    
}

## Reto numero 3 - Rangos cambiantes.

Nuevamente pide a tu usuario que indique 3 números: un límite superior, un límite inferior y uno de comparación. Si el número de comparación se encuentra entre los 2 primeros, comunicarlo en pantalla. En caso estar por debajo del límite inferior o por arriba del límite superior, también mostrarlo en pantalla.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluye la biblioteca `stdio.h` para funciones de entrada y salida.

2. Luego, se define la función principal `main`, que es el punto de entrada del programa.

3. Dentro de la función `main`, se declaran tres variables llamadas `limite_sup`, `limite_inf` y `num` de tipo `int` (entero) para almacenar el límite superior, el límite inferior y el número ingresado por el usuario, respectivamente.

4. Se utiliza la función `printf` para mostrar un mensaje al usuario pidiéndole que ingrese el límite superior.

5. Se utiliza la función `scanf` para leer el límite superior ingresado por el usuario desde la entrada estándar (generalmente el teclado) y almacenarlo en la variable `limite_sup`.

6. Se repiten los pasos 4 y 5 para pedir al usuario que ingrese el límite inferior y almacenarlo en la variable `limite_inf`.

7. Se repiten nuevamente los pasos 4 y 5 para pedir al usuario que ingrese el número a comparar y almacenarlo en la variable `num`.

8. Después, se utiliza un condicional `if` para verificar si el valor de la variable `num` es mayor o igual que el valor de la variable `limite_inf` y menor o igual que el valor de la variable `limite_sup`. Si ambas condiciones se cumplen (es decir, si el número ingresado por el usuario está dentro del rango especificado), se muestra un mensaje utilizando la función `printf` indicando que el número se encuentra en el rango.

9. Si alguna de las condiciones anteriores no se cumple (es decir, si el número ingresado por el usuario está fuera del rango especificado), se entra en el bloque de código dentro del condicional `else`, donde se muestra un mensaje utilizando la función `printf` indicando que el número excede el límite permitido.

10. Finalmente, la función `main` retorna 0 para indicar que el programa terminó correctamente.

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo.

#include<stdio.h>

int main()
{
    int limite_sup, limite_inf, num;
    printf("Introduce el limite superior: ");
    scanf("%d", &limite_sup);
    printf("Introduce el limite inferior: ");
    scanf("%d", &limite_inf);
    printf("Introduce el numero para comparar: ");
    scanf("%d", &num);
    if (num >= limite_inf && num <= limite_sup)
        {
            printf("El numero %d se encuentra en el rango, gracias\n", num);
        }
    else
        {
             printf("El numero excede el limite permitido, lo siento\n");
        }
    return 0;    
}

# Reto numero 4 - I like turtles.

Escribe un programa que pida al usuario ingrese su animal favorito, si coloca ‘Tortuga’, ‘tortuga’, ‘TORTUGA’ o cualquier otra variante de la palabra entonces mostrar en pantalla “También me gustan las tortugas”. En caso contrario mostrar el mensaje “Ese animal es genial, pero prefiero las tortugas”.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluyen las bibliotecas `stdio.h` para funciones de entrada y salida, `string.h` para funciones de manipulacion de cadenas de texto y `ctype.h` para funciones de manipulacion de caracteres.

2. Luego, se define la función principal `main`, que es el punto de entrada del programa.

3. Dentro de la función `main`, se declara una variable llamada `animal` que es un arreglo de caracteres (una cadena de texto) con espacio para 20 caracteres para almacenar el animal favorito ingresado por el usuario.

4. Se utiliza la función `printf` para mostrar un mensaje al usuario pidiéndole que ingrese su animal favorito.

5. Se utiliza la función `scanf` para leer el animal favorito ingresado por el usuario desde la entrada estándar (generalmente el teclado) y almacenarlo en la variable `animal`.

6. Después, se utiliza un bucle `for` para recorrer cada carácter en la cadena `animal` y convertirlo a minúsculas utilizando la función `tolower`. Esto se hace para evitar posibles errores al comparar la respuesta del usuario con las opciones esperadas (`tortuga`).

7. Luego, se utiliza la función `strcmp` para comparar la cadena `animal` con la cadena `"tortuga"`. Si son iguales (es decir, si el animal favorito del usuario es una tortuga), se muestra un mensaje utilizando la función `printf` indicando que también nos gustan las tortugas.

8. Si las cadenas no son iguales (es decir, si el animal favorito del usuario no es una tortuga), se entra en el bloque de código dentro del condicional `else`, donde se muestra un mensaje utilizando la función `printf` indicando que ese animal es genial pero que preferimos las tortugas.

9. Finalmente, la función `main` retorna 0 para indicar que el programa terminó correctamente.

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo.

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main()
{
    char animal[20];
    printf("Introduce tu animal favorito: ");
    scanf("%s", animal);

    // Convertir a minusculas

    int i;
    for ( i=0; i < strlen(animal); i++)
        {
            animal[i] = tolower(animal[i]);
        }
    
    if (strcmp(animal, "tortuga") == 0)
        {
        printf("Tambien me gustan las tortugas\n"); 
        }
    
    else
        {
        printf("Ese animal es genial, pero prefiero las tortugas\n");
        }

    return 0;    
}

## Reto numero 5 - ¿Cómo está el clima?

Crea un programa que pregunte al usuario si está lloviendo, en caso de responder “sí” pregunta si está haciendo mucho viento y si responde “sí” nuevamente muestra un mensaje indicando que hace mucho viento para salir con una sombrilla. En caso contrario, anima al usuario a que lleve una sombrilla. Para el caso de responder “no” en la primer pregunta, entonces solo desea un bonito día.
Considera que las respuestas pueden pasarse a minúsculas para evitar posibles errores.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluyen las bibliotecas `stdio.h` para funciones de entrada y salida, `ctype.h` para funciones de manipulación de caracteres y `string.h` para funciones de manipulación de cadenas de texto.

2. Luego, se define la función principal `main`, que es el punto de entrada del programa.

3. Dentro de la función `main`, se declara una variable llamada `respuesta` que es un arreglo de caracteres (una cadena de texto) con espacio para 3 caracteres (2 para la respuesta y 1 para el carácter nulo que indica el final de la cadena).

4. Se utiliza la función `printf` para mostrar un mensaje al usuario pidiéndole que ingrese si está lloviendo o no.

5. Se utiliza la función `scanf` para leer la respuesta del usuario desde la entrada estándar (generalmente el teclado) y almacenarla en la variable `respuesta`.

6. Luego, se utiliza un bucle `for` para recorrer cada carácter en la cadena `respuesta` y convertirlo a minúsculas utilizando la función `tolower`. Esto se hace para evitar posibles errores al comparar la respuesta del usuario con las opciones esperadas (`si` y `no`).

7. Después, se utiliza la función `strcmp` para comparar la cadena `respuesta` con la cadena `"si"`. Si son iguales (es decir, si el usuario respondió que sí está lloviendo), se entra en el bloque de código dentro del condicional `if`.

8. Dentro del bloque `if`, se repiten los pasos 4 a 6 para preguntar al usuario si está haciendo mucho viento y leer su respuesta.

9. Luego, se utiliza nuevamente la función `strcmp` para comparar la cadena `respuesta` con la cadena `"si"`. Si son iguales (es decir, si el usuario respondió que sí está haciendo mucho viento), se muestra un mensaje indicando que hace mucho viento para salir con una sombrilla utilizando la función `printf`. En caso contrario (es decir, si el usuario respondió que no está haciendo mucho viento), se muestra un mensaje animando al usuario a llevar una sombrilla.

10. Si el usuario respondió que no está lloviendo en el primer condicional `if`, se entra en el bloque de código dentro del condicional `else`, donde se muestra un mensaje deseando al usuario un bonito día utilizando la función `printf`.

11. Finalmente, la función `main` retorna 0 para indicar que el programa terminó correctamente.

Recuerda digitar el especio en blanco en cada una de tus respuestas cuando estes ejecutando el programa, eso evitara que salte al final del codigo y se cierre, espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona.

#include <stdio.h>
#include <ctype.h>
#include <string.h>

int main() 
{
    char respuesta[3];
    printf("¿Esta lloviendo? (si/no): ");
    scanf("%s", respuesta);

    int i;
    for(i = 0; respuesta[i]; i++)
    {
        respuesta[i] = tolower(respuesta[i]);
    }

    if (strcmp(respuesta, "si") == 0) 
    {
        printf("¿Esta haciendo mucho viento? (si/no): ");
        scanf("%s", respuesta);

        int i;
        for(i = 0; respuesta[i]; i++)
        {
            respuesta[i] = tolower(respuesta[i]);
        }

        if (strcmp(respuesta, "si") == 0) 
        {
            printf("Hace mucho viento para salir con una sombrilla.\n");
        } 
        
        else 
        {
            printf("Deberias llevar una sombrilla.\n");
        }
    } 
    
    else 
    {
        printf("Que tengas un bonito dia.\n");
    }

    return 0;
}

## Reto numero 6 - Edad permitida

Pide al usuario que ingrese su edad y mostrarás un mensaje correspondiente si esta coincide con las siguientes condiciones:
Más de 30 años: Nunca es tarde para aprender ¿Qué curso tomaremos?
Entre 29 y 18 años: Es un momento excelente para impulsar tu carrera.
Menos de 18 años: ¿Sabes hacia dónde dirigir tu futuro? Seguro puedo ayudarte.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluye la biblioteca `stdio.h` para funciones de entrada y salida.

2. Luego, se define la función principal `main`, que es el punto de entrada del programa.

3. Dentro de la función `main`, se declara una variable llamada `edad` de tipo `int` (entero) para almacenar la edad del usuario.

4. Se utiliza la función `printf` para mostrar un mensaje al usuario pidiéndole que ingrese su edad.

5. Se utiliza la función `scanf` para leer la edad del usuario desde la entrada estándar (generalmente el teclado) y almacenarla en la variable `edad`.

6. Después, se utiliza un condicional `if` para verificar si la edad del usuario es mayor a 30. Si es así, se muestra un mensaje utilizando la función `printf` indicando que nunca es tarde para aprender y preguntando qué curso tomar.

7. Si la edad del usuario no es mayor a 30, se entra en el bloque de código dentro del condicional `else if`, donde se verifica si la edad del usuario está entre 18 y 29 años (inclusive). Si es así, se muestra un mensaje utilizando la función `printf` indicando que es un momento excelente para impulsar su carrera.

8. Si ninguna de las condiciones anteriores se cumple (es decir, si la edad del usuario es menor a 18 años), se entra en el bloque de código dentro del condicional `else`, donde se muestra un mensaje utilizando la función `printf` preguntando si sabe hacia dónde dirigir su futuro y ofreciendo ayuda.

9. Finalmente, la función `main` retorna 0 para indicar que el programa terminó correctamente.

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo.


#include <stdio.h>

int main() 
{
    int edad;
    printf("Por favor ingresa tu edad: ");
    scanf("%d", &edad);

    if (edad > 30) 
    {
        printf("Nunca es tarde para aprender ¿Que curso tomaremos?\n");
    } 
    
    else if (edad >= 18 && edad <= 29)
    {
        printf("Es un momento excelente para impulsar tu carrera.\n");
    } 
    
    else 
    {
        printf("¿Sabes hacia donde dirigir tu futuro? Seguro puedo ayudarte.\n");
    }

    return 0;
}

## Reto numero 7 - Mensajes opcionales

Crearás un un script para el que el usuario indicará un número entre 1 y 6. Como respuesta se le brindará un mensaje según el número leido:
1 - “Hoy aprenderemos sobre prorgamación”
2 - “¿Qué tal tomar un curso de marketing digital?
3 - “Hoy es un gran día para comenzar a aprender de diseño”
4 - ¿Y si aprendemos algo de negocios online?
5 - “Veamos un par de clases sobre producción audiovisual”
6 - “Tal vez sea bueno desarrollar una habilidad blanda en Platzi”
En caso indicar un número distinto, pedir al usuario que ingrese uno en el rango válido.

Explicacion de como funciona este codigo en lenguaje C:

1. Primero, se incluye la biblioteca `stdio.h` para funciones de entrada y salida.

2. Luego, se define la función principal `main`, que es el punto de entrada del programa.

3. Dentro de la función `main`, se declara una variable llamada `numero` de tipo `int` (entero) para almacenar el número ingresado por el usuario.

4. Se utiliza la función `printf` para mostrar un mensaje al usuario pidiéndole que ingrese un número entre 1 y 6.

5. Se utiliza la función `scanf` para leer el número ingresado por el usuario desde la entrada estándar (generalmente el teclado) y almacenarlo en la variable `numero`.

6. Después, se utiliza un bucle `while` para verificar si el número ingresado por el usuario es menor a 1 o mayor a 6. Si es así, se muestra un mensaje utilizando la función `printf` indicando que el número es inválido y pidiéndole al usuario que ingrese un número válido. Luego, se utiliza nuevamente la función `scanf` para leer el nuevo número ingresado por el usuario y almacenarlo en la variable `numero`. Este proceso se repite hasta que el usuario ingrese un número válido (entre 1 y 6).

7. Una vez que el usuario ha ingresado un número válido, se utiliza una estructura de control `switch` para evaluar el valor de la variable `numero`. Dependiendo del valor de esta variable, se ejecutará uno de los casos (`case`) dentro del `switch`.

8. Si el valor de `numero` es 1, se ejecutará el caso correspondiente y se mostrará un mensaje utilizando la función `printf` indicando que hoy aprenderemos sobre programación. Luego, se utiliza la sentencia `break` para salir del `switch`.

9. Si el valor de `numero` es 2, se ejecutará el caso correspondiente y se mostrará un mensaje utilizando la función `printf` preguntando qué tal tomar un curso de marketing digital. Luego, se utiliza la sentencia `break` para salir del `switch`.

10. Si el valor de `numero` es 3, se ejecutará el caso correspondiente y se mostrará un mensaje utilizando la función `printf` indicando que hoy es un gran día para comenzar a aprender de diseño. Luego, se utiliza la sentencia `break` para salir del `switch`.

11. Si el valor de `numero` es 4, se ejecutará el caso correspondiente y se mostrará un mensaje utilizando la función `printf` preguntando si deberíamos aprender algo de negocios online. Luego, se utiliza la sentencia `break` para salir del `switch`.

12. Si el valor de `numero` es 5, se ejecutará el caso correspondiente y se mostrará un mensaje utilizando la función `printf` indicando que deberíamos ver un par de clases sobre producción audiovisual. Luego, se utiliza la sentencia `break` para salir del `switch`.

13. Si el valor de `numero` es 6, se ejecutará el caso correspondiente y se mostrará un mensaje utilizando la función `printf` indicando que tal vez sea bueno desarrollar una habilidad blanda en Platzi. Luego, se utiliza la sentencia `break` para salir del `switch`.

14. Finalmente, la función `main` retorna 0 para indicar que el programa terminó correctamente.

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo.


#include <stdio.h>

int main()
{
    int numero;
    printf("Por favor ingresa un numero entre 1 y 6: ");
    scanf("%d", &numero);

    while (numero < 1 || numero > 6) 
    {
        printf("Numero invalido. Por favor ingresa un numero entre 1 y 6: ");
        scanf("%d", &numero);
    }

    switch (numero) 
    {
        case 1:
            printf("Hoy aprenderemos sobre programacion\n");
            break;
        case 2:
            printf("¿Que tal tomar un curso de marketing digital?\n");
            break;
        case 3:
            printf("Hoy es un gran dia para comenzar a aprender de diseno\n");
            break;
        case 4:
            printf("¿Y si aprendemos algo de negocios online?\n");
            break;
        case 5:
            printf("Veamos un par de clases sobre produccion audiovisual\n");
            break;
        case 6:
            printf("Tal vez sea bueno desarrollar una habilidad blanda en Platzi\n");
            break;
    }

    return 0;
}

Gracias por llegar hasta aqui, los retos fueron planteados en el Curso de Control de Flujo en "C" de Platzi.
