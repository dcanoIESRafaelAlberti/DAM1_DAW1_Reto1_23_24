# DAM1_DAW1_Reto1_23_24
Juguemos al BlackJack

## Reto 1 (DAM1 y DAW1)

### Descripción:
```
Crear un programa en Python con funciones para jugar al Blackjack.

Al entrar debe preguntar el modo de juego:
1. Dos jugadores.
2. Un jugador contra la máquina.
```

### Premisas:
```
1. No se pueden usar listas, tuplas o diccionarios.
2. La baraja de cartas es la cadena de caracteres "A234567890JKQ"
3. Debéis crear funciones intentando seguir el principio de responsabilidad única, es decir, que la función tenga una única funcionalidad.
4. Entregar el programa, junto con las pruebas unitarias de las funciones utilizadas.
5. No es necesario realizar las pruebas a funciones que contengan un input().
6. El programa debe estar documentado con docstrings (ver https://revilofe.github.io/section1/u02/teoria/PROG-U2.5.-Documentar/)
7. Debéis realizar todas las comprobaciones necesarias para que el programa no genere un error, sin usar excepciones.
```

### Objetivo del juego:
	Conseguir 21 puntos o plantarse con más puntos que el otro jugador.

### Funcionamiento:
	1. Gana el jugador que tenga la puntuación más alta sin pasarse de 21 puntos.
	2. Las cartas tienen los siguientes puntos:
		A -> 1 o 10 (según le venga mejor al resto de cartas que tiene en su poder el jugador)
		2...9 -> el propio valor del número.
		0, J, Q, K -> 10
	3. Cada jugador irá solicitando cartas por turnos, después del primer turno obligatorio, un jugador puede plantarse cuando lo decida.
	4. Después de cada turno, se debe mostrar la información de las cartas y puntos de cada jugador:
		J1 - jugador1 - A3K (14)
		J2 - jugador2 - A44 (18)
	5. Cuando un jugador se pasa de 21, automáticamente pierde y gana el otro jugador.
	6. Las cartas de los jugadores y puntuaciones se revelan a la vez después de pasar el turno ambos jugadores, es decir, cada jugador decide pedir una carta más o plantarse y a continuación se muestra la información de cada jugador.
		J1 - jugador1 - 63K (19)
		J2 - jugador2 - J4Q **se pasa**
	7. El programa debe solicitar el modo de juego y a continuación el nombre o apodo del o los jugadores.
	8. Cada jugador pide una carta por turno o se planta. Como mínimo un jugador debe solicitar una carta, es decir, la primera vez no se le da la opción a plantarse. Pero el resto de turnos si.
	9. El juego acaba cuando ambos jugadores se plantan. Mientras que un jugador no se pase de 21 puntos y no se plante se debe preguntar si quiere una carta más.
	10 Cuando finaliza el juego se debe mostrar lo siguiente (4 posibilidades):

		JUEGO TERMINADO
		Game over ¡Los dos os habéis pasado!
		J1 - jugador1 - 4K9 (23)
		J2 - jugador2 - J70 (27)

		JUEGO TERMINADO
		¡Empate!
		J1 - jugador1 - 4K5 (19)
		J2 - jugador2 - A9 (19)
    
		JUEGO TERMINADO
		¡Gana J1 - jugador1!
		J1 - jugador1 - JQA (21)
		J2 - jugador2 - 491J (24)

		JUEGO TERMINADO
		¡Gana J2 - jugador2!
		J1 - jugador1 - 3K5 (18)
		J2 - jugador2 - 28Q (20)

