# Condicionales-en-C
Desarrollar una serie de ejercicios con su debida explicación, que indiquen el uso de condicionales en lenguaje "C"

/*Explicacion de como funciona este codigo en lenguaje C:

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

Espero que esta explicacion te sirva de ayuda para despejar posibles dudas de como funciona este codigo*/


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
