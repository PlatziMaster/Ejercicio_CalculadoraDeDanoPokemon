# Ejercicio_CalculadoraDeDañoPokemon
En este ejercicio tendrás que crear una función que calcule el daño de batalla en el ataque de un pokemon a otro. 
## descripción
En el juego japonés de pokemon, durante una batalla pokemon se tienen dos pokemon (asumiendo batallas individuales) y cuando uno ataca a otros, entonces el juego utiliza la siguiente fórmula para calcular el daño que ese ataque le hará a su contrincante:

<img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/b8c51fed93bb9a80ae8febc13700a40b8a5da402">

dónde:
- Level es el nivel del pokemon que ataca
- Power es el poder del ataque
- A es el valor de la estadística de ataque del pokemon basado en el tipo de ataque realizado (puede ser ataque físico o especial) que ataca
- D es el valor de la estadística de defensa del pokemon en el tipo de ataque realizado (puede ser ataque físico o especial) que defiende
- Target refiere a cuántos pokemon está atacando el pokemon, el valor de esta variable siempre es 1 en batallas individuales y 0.75 en batallas dobles cuando el ataque toca a más de un pokemon.
- Weather es si el tipo de ataque del pokemon es afectado por el clima del combate, por ejemplo en lluvia los ataques de agua se multiplican por 1.5 y los de fuego por 0.5
- Badge es 1 en todos los casos.
- Critical es una variable aleatoria que es 1 el 93.75% de los casos y 1.5 el 6.25% restante
- Random es una variable aleatoria uniforme que puede tomar cualquier valor entre 0.85 y 1
- STAB si el ataque es del mismo tipo que el tipo del pokemon que ataca, entonces tiene valor 1.5, si no es 1
- Type si el tipo del ataque es doblemente súper efectivo ante el tipo del atacante, entonces es 4, si es súper efectivo, entonces 2, si es normalmente efectivo es 1, si es poco efectivo entonces es 0.5, si es doblemente inefectivo, entonces 0.25 y si es nada efectivo 0. Por simplicidad de este ejercicio vamos a suponer que esta variable siempre es 1.
- Burn es 0.5 si el pokemon está quemado y usa un ataque físico 1 de otro caso
- Other es 1 en todo caso.

Entonces crea una función que dados dos pokemon y el ataque a utilizar este haga estos cálculos y te de como resultado el valor de cuántos puntos de daño va a realizar este ataque al pokemon defensor. Al final de hacer todos los calculos redondea al entero anterior. 

Te recomiendo hacer la variable pokemon una estructura de datos la cuál contenga al menos el nombre del pokemon, el nivel, el ataque físico, especial y la defensa física y especial. En este caso asume que los valores que tengan que ver con los tipos valgan 1.

Como ejemplo, imagina que tienes un Glaceon de tipo hielo nivel 75 con un estadístico de ataque físico de 123 y usa el ataque de Ice Fang con poder de 65 sobre un Garchomp de tipo Dregon/Tierra con un estadístico de defensa física de 163. ¿Cuál es el resultado de un ataque? ¿Cuál es el valor mínimo y máximo que puede dar este ataque?

## BONUS
Haz los cálculos de tal manera que la variable de pokemon tenga la información de los tipos, y calcule la variable de Type en la fórmula con base en estos, de igual manera haz los cálculos de tal manera de que siempre trunques al entero anterior siempre que realices una multiplicación o una división, en vez de hacerlo al final.
