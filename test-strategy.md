# DOCUMENTO DE INFORMACIÓN DE FALLOS

### Ingreso de datos de INPUT
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
guesses.textContent = 'Números ingresados anteriormente: ';  

- En la condición if(userGuess === randomNumber) no detecta si el usuario ingresa un valor  
Se modifica el operador a == para que pueda comparar el valor ingresado y no estrictamente  
Se cambia el color de fondo a verde, ya que en esta condicion es cuando el jugador gana  
Se cambió el texto resultado a Felicitaciones! adivinaste el número!  

- No captura etiqueta lowOrHi  
la constante const lowOrHi = document.querySelector('lowOrHi'); le hace falta el punto en el selector para poder ubicar la etiqueta.  
Se coloca el punto  

- La funcion setGameOver no funciona  
Se detectó que hacía falta la E mayuscula en addEventListener  

- Aviso de intentos  
Se creó un aviso en consola para indicar la cantidad de intentos utilizados  

- Funcion ResetGame  
Se colocó un aviso para que se pueda mostrar en consola el nuevo numero aleatorio  
Se modificó la funcion random, ya que unicamente estaba dando como resultado random el numero 1  
Se agregó la funcion Math.floor y Math.random * 100

# REQUISITOS SOLICITADOS
- Creación de funcion test para poder evitar ingreso de valores erroneos  
Dentro de la funcion checkGuess se ha colocado en la segunda linea la funcion test el cual envía el valor ingresado por el usuario para poder verificar las condiciones solicitadas antes de poder continuar  

- Creación de variable status la cual servirá para evitar que la funcion checkGuess siga corriendo en caso de falla  
En la funcion test() se encuentran las condicionales y en caso de alguna detecte algun fallo, utiliza la variable status para poder finalizar o impedir que el programa siga corriendo luego de la falla  

- En cada comprobación se adjunta la variable status para poder cambiar su estado a true en caso estos fallos se cumplan  

- Primera comprobación que el numero ingresado se encuentre en el rango de 1 a 100  

- Segunda comprobación que el numero ingresado no tenga decimales  

- El campo que indica al jugador si el numero es mayor o menor se ha colocado con fondo negro  

- Cuando el jugador pierde luego de 10 intentos, mostrará el mensaje "!!!Pérdistes!!!"  

- El usuario al ganar la partida, se mostrará el mensaje con fondo de color verde "Felicitaciones! adivinaste el número!"  


# SUGERENCIAS PARA MEJORA DE PROYECTO
- Se centró toda la información y campos para tener un orden  
En css se agregaron valores para poder centrar cada componente  

- Se agregó el numero que el usuario ingresa al texto que indica si es mayor o menor al numero a adivinar  

- Se agregó un nuevo apartado para que el usuario conozca cuantos intentos ha utilizado  
Se creó la etiqueta p con clase trys para poder utilizarla como indicador de intentos  

- Se eliminaron todas las salidas de consola para que no se de ninguna información del numero aleatorio generado  

- El campo hiOrLow se ha utilizado al momento de perder, ya que ahora se indicará al usuario cual era el numero aleatorio que no ha adivinado  

- Se ha colocado el historial de los numeros que se han ingresado para que el usuario sepa cuales no debe de volver a ingresar, sin emargo, puede volver a ingresarlos si así desea