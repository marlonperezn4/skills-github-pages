---
title: "01-03 Aplicación de formato de cadena básico en C#"
date: 2023-05-21
---

# Combinación de cadenas mediante secuencias de escape de caracteres

Salto de linea:
\n 
Console.WriteLine("Hello\nWorld!");

Tabulación: 
\t
Console.WriteLine("Hello\tWorld!");

Insertar comillas:
\"
Console.WriteLine("Hello \"World\"!");

Mostrar la barra diagonal inversa
\\
Console.WriteLine("c:\\source\\repos");


## Literal de cadena textual

Con el **@** antes se pueden escribir y mostrar saltos de linea y el backslash de manera textual

Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)");

### Ejemplo

Console.WriteLine("Generating invoices for customer \"Contoso Corp\" ...\n");
Console.WriteLine("Invoice: 1021\t\tComplete!");
Console.WriteLine("Invoice: 1022\t\tComplete!");
Console.WriteLine("\nOutput Directory:\t");

Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)");
Console.Write(@"c:\invoices");
// Kon'nichiwa World
Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!");
// To generate Japanese invoices:
// Nihon no seikyū-sho o seisei suru ni wa:
Console.Write("\n\n\u65e5\u672c\u306e\u8acb\u6c42\u66f8\u3092\u751f\u6210\u3059\u308b\u306b\u306f\uff1a\n\t");
// User command to run an application
Console.WriteLine(@"c:\invoices\app.exe -j");

# Concatenación de cadenas

string firstName = "Bob";
string message = "Hello " + firstName;
Console.WriteLine(message);
o

string message = "Hello " + "Marlon";
Console.WriteLine(message);

## Evitación de variables intermedias

En los pasos anteriores, usó una variable adicional para almacenar la nueva cadena resultante de la operación de concatenación. A menos que tenga una buena razón para hacerlo, puede (y debe) evitar el uso de variables intermedias y llevar a cabo la operación de concatenación según sea necesario.

string firstName = "Bob";
string greeting = "Hello";
Console.WriteLine(greeting + " " + firstName + "!");

# Combinación de cadenas mediante interpolación de cadenas

Antecede un simbolo pesos $ y el entre corchetes se escribe la o las variables

string firstName = "Bob";
string greeting = "Hello";
string message = $"{greeting} {firstName}!";
Console.WriteLine(message);

Console.WriteLine($"Hola mi nombre no es {firstName}");

## Combinación de los literales textuales y la interpolación de cadenas

string projectName = "First-Project";
Console.WriteLine($@"C:\Output\{projectName}\Data");

# Desafío: aplicación de formato y visualización de las instrucciones

string projectName = "ACME";

string russianMessage = "\u041f\u043e\u0441\u043c\u043e\u0442\u0440\u0435\u0442\u044c \u0440\u0443\u0441\u0441\u043a\u0438\u0439 \u0432\u044b\u0432\u043e\u0434";

Console.WriteLine($@"View English output:
    c:\Exercise\{projectName}\data.txt
");

Console.WriteLine(russianMessage + $@":
    c:\Exercise\{projectName}\data.txt");