Se ingreso un numero pero no funciona el boton: el error estaba en que el eventlistener no estaba correctamente escrito "guessSubmit.addeventListener('click', checkGuess); -> guessSubmit.addEventListener('click', checkGuess);"

El color de los mensajes de numero incorrecto y numero correct esta cambiado, ademas los mensajes de felicitacion y juego perdido tambien estan cambiados.

El numero aleatorio no es un entero, por lo que la validacion no se puede realizar correctamente:  let randomNumber = Math.random() * 10; console.log(randomNumber); -> let randomNumber = Math.floor(Math.random() * 100) + 1;;

La funcion de verificar si el numero es mayor o menor no esta funcionando: el input del usuario no esta siendo validado como un numero, se agrega una validacion para confirmar que sea un numero entero dentro del rango establecido. 

La funcion de verificar si el numero es mayor o menor sigue sin funcionar: el error esta en el query selector, se modifica -> const lowOrHi = document.querySelector('.lowOrHi');

El juego no termina en los 10 intentos, termina antes: se modifica la variable ATTEMPS = 10
El juego no termina a los 10 intentos, la funcion de gameOver no esta incluida al terminar los intentos, se agrega dicha funcion.

La funcion de reset no esta funcionando, igual al error anterior es un error en el event listener:  resetButton.addeventListener('click', resetGame); -> resetButton.addEventListener('click', resetGame);.

Al resetear el juego el numero siempre es 1: error en la asignacion del numero en la variable randomNumber = Math.floor(Math.random()) + 1;, se modifica -> Math.floor(Math.random() * 100) + 1;