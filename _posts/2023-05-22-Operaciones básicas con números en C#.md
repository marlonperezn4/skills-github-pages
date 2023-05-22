---
title: "01-04 Realización de operaciones básicas en C#"
date: 2023-05-21
---

# Sumas con conversión implícita de datos

Atento a la diferencia

string firstName = "Bob";
int widgetsSold = 7;

***CONCATENA***
El compiladorentiende que se debe concatenar
Console.WriteLine(firstName + " sold " + widgetsSold + 7 + " widgets.");

***SUMA***
Al momento de ponerle parentisis el compilador entiende que se debe sumar
Console.WriteLine(firstName + " sold " + (widgetsSold + 7) + " widgets.");

## Operadores

int sum = 7 + 5;
int difference = 7 - 5;
int product = 7 * 5;
int quotient = 7 / 5;

Console.WriteLine("Sum: " + sum);
Console.WriteLine("Difference: " + difference);
Console.WriteLine("Product: " + product);
Console.WriteLine("Quotient: " + quotient);

## Decimales

Para operar (dividir) dos números enteros y guardarlos en una variable decimal debe ser:

(decimal)variableint

int first = 7;
int second = 5;
decimal quotient = (decimal)first / (decimal)second;
Console.WriteLine(quotient);

## Resto de la división

Con el operador %. El resto de la división tiene dos posibles resultados.. 0 y 1
Si es par debería ser 0 el residuo, pero si es impar debería ser 1

## Orden de la división

Se hará primero lo que esté en parentesis

int value1 = 3 + 4 * 5;
int value2 = (3 + 4) * 5;
Console.WriteLine(value1);
Console.WriteLine(value2);

Se sigue el orden

int value1 = 3 + 4 * 5 + 2;
int value2 = (3 + 4) * 5 + 2;
int value3 = (3 + 4) + 2 * 5;
Console.WriteLine(value1);
Console.WriteLine(value2);
Console.WriteLine(value3);

## Incremento y decremento

Sumar valor

int value = 1;

value = value + 1;
Console.WriteLine("First increment: " + value);

value += 1;
Console.WriteLine("Second increment: " + value);

value++;
Console.WriteLine("Third increment: " + value);

Restar valor

value = value - 1;
Console.WriteLine("First decrement: " + value);

value -= 1;
Console.WriteLine("Second decrement: " + value);

value--;
Console.WriteLine("Third decrement: " + value);

## Uso del operador de incremento antes y después del valor

int value = 1;
value++;
Console.WriteLine("First: " + value);
Console.WriteLine("Second: " + value++);
Console.WriteLine("Third: " + value);
Console.WriteLine("Fourth: " + (++value));

Si se usa el incremento o decremento después.. se sumará o restará pero no se mostrará en es linea, sino que será efectuada la operación y se mostrará en la otra linea

Si se usa antes entonces si se sumará y se mostrará den una vez

Los parentes en la última linea son para mejorar visibilidad, sería muy raro ver tres *+* seguidos

## Desafío convertir Fahrenheit a Celsius

int fahrenheit = 94;
decimal celsius = (fahrenheit - 32m) * (5m / 9m);
Console.WriteLine($"The temperature is {celsius} Celsius");

## Apuntes

int result = 3 + 1 * 5 / 2;

Primero se hace la división, después la multiplicación después suma

Console.WriteLine(5 / 10);
El diez cabe 0 veces en el 5.. Me muestra el valor 0

Console.WriteLine(5 / 1);
El uno cabe 5 veces en el 5.. Me muestra el valor 5