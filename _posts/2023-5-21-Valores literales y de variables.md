---
title: "01-02 Almacenamiento y recuperación de datos mediante valores literales y de variable en C#"
date: 2023-05-21
---

# Ejercicio: Impresión de valores literales

¿Qué es un valor literal?

Valor constante que nunca cambia

## Crea un literal caracter: 
Console.WriteLine('b'); *Recordar que comillas simples es para carácter y comillas dobles para string*

## Crea un literal entero: 
Console.WriteLine(123);

## Crea un literal de punto flotante: 

- float:         ~6-9 digits
    - Crea un literal float Console.WriteLine(0.25F);
- double:        ~15-17 digits
    - Crea un literal double: Console.WriteLine(2.625);
- decimal:        28-29 digits
    - Crea un literal decimal: Console.WriteLine(12.39816m);

## Crea un literal booleano

Console.WriteLine(true);
Console.WriteLine(false);

# Declaración de variables

Una variable es un contenedor para almacenar un tipo de valor. Las variables son importantes porque sus valores pueden cambiar o variar durante la ejecución de un programa. Las variables se pueden asignar, leer y cambiar.

string firstName;

## Reglas

- Los nombres de variable distinguen mayúsculas de minúsculas, lo que significa que string Value; y string value; son dos variables diferentes.
- Los nombres de variable no deben ser una palabra clave de C#. Por ejemplo, no se pueden usar las siguientes declaraciones de variable: decimal decimal; ni string string;.
- Los nombres de variable deben usar camel case, que es un estilo de escritura que usa una letra en minúscula al principio de la primera palabra y una letra en mayúscula al principio de cada palabra siguiente. Por ejemplo, string thisIsCamelCase;.

## Ejemplos

- char userOption;
- int gameScore;
- decimal particlesPerMillion;
- bool processedCustomer;

## Reasignación

Se puede reasignar una variable de la siguiente manera:

string firstName;

firstName = "Marlon";
Console.WriteLine(firstName);

firstName = "Margarita";
Console.WriteLine(firstName);

## Variables de tipo implícito

Se puede declarar una varible sin especificar su tipo de dato
EJ: 1
var message = 21;
Console.WriteLine(message);

EJ: 2

var message = "Hello world!";
Console.WriteLine(message);

Una vez se escribe la variable, si se queire sobreescribir debe ser con el mismo tipo de dato inicial

***UNA VARIABLE IMPLICITA NO SE PUEDE INICIALIZAR*** 
Ej
- error: var firstName;
- correct: var firstName = "Marlon";

## Ejercicio
string firstName = "Bob";
int messages = 3;
float temperature = 34.4f;

Console.Write("Hello, ");
Console.Write(firstName);
Console.Write("! You have ");
Console.Write(messages);
Console.Write(" in your inbox. The temperature is ");
Console.Write(temperature);
Console.Write("celsius.");