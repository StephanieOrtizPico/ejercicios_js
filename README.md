# Ejercicios Clase 16/04/2024

1. Mostrar por consola la tabla de multiplicar del 5 utilizando la sentencia for de la siguiente manera:
5 x 0 = 0
5 x 1 = 5
5 x 2 = 10
...

```Javascript
// Sentencia for para generar la tabla de multiplicar del 5
for (let i = 0; i <= 10; i++) 
{
    console.log("5 x " + i + " = " + (5 * i));
}
```

2. Modificar el programa anterior y mostrar las 10 tablas de multiplicar.

```Javascript
// generar las tablas de multiplicar del 1 al 10
for (let multiplicando = 1; multiplicando <= 10; multiplicando++) 
{
    console.log("Tabla de multiplicar del " + multiplicando + ":");
    for (let multiplicador = 0; multiplicador <= 10; multiplicador++) 
    {
        console.log(multiplicando + " x " + multiplicador + " = " + (multiplicando * multiplicador));
    }
    console.log("------------------");
}
```

3. Pedir por pantalla a través de prompt un texto y mostrar en un alert si el texto introducido es un valor numérico o es una cadena.

```Javascript
// Pedir al usuario un texto
let texto = prompt("Por favor, introduce un texto:");

// Comprobar si el texto es un número o una cadena
if (!isNaN(texto)) 
{
    // Si el texto es un número
    alert("El texto introducido es un valor numérico.");
} else {
    // Si el texto es una cadena
    alert("El texto introducido es una cadena.");
    }
```

4. Pedir dos textos por pantalla a través de prompt y mostrar en un alert las dos cadena concatenadas.

```Javascript
// Pedir al usuario dos textos
let texto1 = prompt("Por favor, introduce el primer texto:");
let texto2 = prompt("Por favor, introduce el segundo texto:");

// Concatenar los dos textos
let resultado = texto1 + " " + texto2;

// Mostrar el resultado en un alert
alert("La concatenación de los dos textos es: " + resultado);
```

5. Pedir dos números por pantalla con prompt y mostrar la suma de ambos.  Se debe validar que los números introducidos sean números.

```Javascript
function esNumero(valor) 
{
    return !isNaN(valor);
}

// Solicitar dos números y validarlos
let numero1 = prompt("Por favor, introduce el primer número:");
let numero2 = prompt("Por favor, introduce el segundo número:");

// Convertir los valores ingresados a números
numero1 = parseFloat(numero1);
numero2 = parseFloat(numero2);

// Verificar si ambos valores son números
if (esNumero(numero1) && esNumero(numero2)) 
{
    // Calcular la suma de los números
    let suma = numero1 + numero2;
    // Mostrar la suma en un alert
    alert("La suma de los dos números es: " + suma);
} else {
    // Mostrar un mensaje de error si alguno de los valores no es un número
    alert("Por favor, asegúrate de introducir dos números válidos.");
    }
```

6. Pedir dos números por pantalla y una operación (+, -, *, /) y mostrar en un alert el resultado de la operación.  Si la operación no es ninguna de las anteriores, se debe mostrar el mensaje "Operación incorrecta".  Se debe validar que los valores introducidos sean números.

```Javascript
    // Validar si un valor es un número
    function esNumero(valor) {
      return !isNaN(valor);
    }

    // Solicitar al usuario dos números y una operación
    let numero1 = prompt("Por favor, introduce el primer número:");
    let numero2 = prompt("Por favor, introduce el segundo número:");
    let operacion = prompt("Por favor, introduce la operación (+, -, *, /):");

    // Convertir los valores ingresados a números
    numero1 = parseFloat(numero1);
    numero2 = parseFloat(numero2);

    // Validar si ambos valores son números
    if (esNumero(numero1) && esNumero(numero2)) {
      // Realizar la operación seleccionada
      let resultado;
      switch (operacion) {
        case "+":
          resultado = numero1 + numero2;
          break;
        case "-":
          resultado = numero1 - numero2;
          break;
        case "*":
          resultado = numero1 * numero2;
          break;
        case "/":
          resultado = numero1 / numero2;
          break;
        default:
          // Mostrar mensaje de operación incorrecta si la operación no es válida
          alert("Operación incorrecta");
          // Salir del script para evitar mostrar el resultado incorrecto
          throw new Error("Operación incorrecta");
      }
      // Mostrar el resultado en un alert
      alert("El resultado de la operación es: " + resultado);
    } else {
      // Mostrar un mensaje de error si alguno de los valores no es un número válido
      alert("Por favor, asegúrate de introducir dos números válidos.");
    }
```

7. Leer tres notas de los estudiantes y calcular la media.  Tiene que indicar si está reprobado (nota < 3) o aprobado, junto con la nota media.  Si alguna nota no es un número, no dejar de pedirlas hasta que sea correcta.

```Javascript
// Validar si un valor es un número
    function esNumero(valor) {
      return !isNaN(valor);
    }

    // Pedir una nota hasta que sea un número válido
    function pedirNota(mensaje) {
      let nota;
      do {
        nota = prompt(mensaje);
        if (!esNumero(nota)) {
          alert("Por favor, introduce una nota válida.");
        }
      } while (!esNumero(nota));
      return parseFloat(nota);
    }

    // Pedir las tres notas a los estudiantes
    let nota1 = pedirNota("Por favor, introduce la primera nota:");
    let nota2 = pedirNota("Por favor, introduce la segunda nota:");
    let nota3 = pedirNota("Por favor, introduce la tercera nota:");

    // Calcular la media
    let promedio = (nota1 + nota2 + nota3) / 3;

    // Determinar si el estudiante está aprobado o reprobado
    let estado;
    if (promedio >= 30) {
      estado = "Aprobado";
    } else {
      estado = "Reprobado";
    }
```

8. Introducir dos números e indicar cuál es el mayor o si son iguales.

```Javascript
// Solicitar al usuario dos números
    let numero1 = prompt("Por favor, introduce el primer número:");
    let numero2 = prompt("Por favor, introduce el segundo número:");

    // Convertir los valores ingresados a números
    numero1 = parseFloat(numero1);
    numero2 = parseFloat(numero2);

    // Comparar los números e indicar cuál es el mayor o si son iguales
    if (numero1 > numero2) {
      alert("El primer número (" + numero1 + ") es mayor que el segundo número (" + numero2 + ").");
    } else if (numero2 > numero1) {
      alert("El segundo número (" + numero2 + ") es mayor que el primer número (" + numero1 + ").");
    } else {
      alert("Los dos números son iguales.");
```

9. Pintar un cuadrado de asteriscos de 5 por cada lado
*****
*     *
*     *
*     *
*****

```Javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejercicio 9</title>
</head>
<body>
    <script>
    var tamaño = 5;
    for (var i = 0; i < tamaño; i++) 
    {
      var linea = "";
      for (var j = 0; j < tamaño; j++){
        if (i === 0 || i === tamaño - 1 || j === 0 || j === tamaño - 1) {
            linea += "*";
        } else {
            linea += " ";
        }
        }
    console.log(linea);
    }

    </script>
</body>
</html>
```

10. Cree esta figura por pantalla con JS
       *
     ***
   *****
 *******
********
 *******
   *****
     ***
      *

```Javascript
 // Dibujar la figura con asteriscos
    function dibujarFigura() {
      let figura = "";
      // Parte superior de la figura
      for (let i = 1; i <= 5; i++) {
        figura += " ".repeat(5 - i) + "*".repeat(2 * i - 1) + "\n";
      }
      // Parte inferior de la figura
      for (let i = 4; i >= 1; i--) {
        figura += " ".repeat(5 - i) + "*".repeat(2 * i - 1) + "\n";
      }
      return figura;
    }

    // Elemento pre donde se mostrará la figura
    let figuraElement = document.getElementById("figura");

    // Dibujar la figura
    figuraElement.textContent = dibujarFigura();
```