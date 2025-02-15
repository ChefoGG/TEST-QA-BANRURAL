# DOCUMENTO DE INFORMACIÓN DE FALLOS

### Estilos css
- La casilla lastResult no se ve
En los estilos de css el color de texto era blanco, se cambió a negro para poder ser visible

### Ingreso de datos de INPUT ln.31
- Tipo de input como text
Para evitar que se ingrese otro valor que no sea numerico se cambio el tipo del input a number

- Paso, minimo y máximo
Se agregaron limites indicados en 1 y 100, además, se agregó un paso de 1 para que automaticamente no seleccione numeros no enteros

### Funcion script
- No hacia nada al hacer click en input submit
El comando .addeventListener necesita llevar Event con E Mayuscula para que pueda reconocer correcto el comando. Se cambió la e a mayuscula

- Cantidad de intentos 5
Se amplió a 10 intentos la variable ATTEMPS

- El codigo random genera numeros decimales de 0 a 10
Se agregó la funcion Math.floor para poder recibir un numero del 1 al 100 y que sea entero

- Condición if(guessCount === 1) modificada
Se cambio el campo para que indique todos los numeros que el usuario ha ingresado.

- En la condición if(userGuess === randomNumber) no detecta si el usuario ingresa un valor
Se modifica el operador a == para que pueda comparar el valor ingresado y no estrictamente
Se cambia el color de fondo a verde, ya que en esta condicion es cuando el jugador gana.
Se cambió el texto resultado a Felicidades!

- Ultimo else ln. 74
Se cambia el color a anaranjado

- No captura etiqueta lowOrHi
la constante const lowOrHi = document.querySelector('lowOrHi'); le hace falta el punto en el selector para poder ubicar la etiqueta.
Se coloca el punto