### Cours 6. Les boucles (06/06/2023)

Les **boucles** constituent des instructions de base de n’importe quel langage informatique. Elles s’utilisent très efficacement pour parcourir des tableaux, des dictionnaires. Elles se combinent avec les conditions afin de trouver le ou les éléments recherchés. Il existe deux types de boucles.

## La boucle `while`

La boucle `while` est une boucle qui peut être infinie, donc bloqué le calcul en cours. Il faut de fait prévoir une condition de fin définie par un test. La boucle la plus simple définit un variable que l’on va incrémenter ou décrémenter, notée `i`.

`i = 1`

`while` test avec la variable i

instructions de la boucle

`i = i + 1`

`end`

> [!TIP]
> Avec des conditions, on peut utiliser :
> - `continue` qui permet de passer à l’itération suivante ;
> - `break` qui quitte la boucle.

## La boucle `for`... `in`...

La boucle `for`... `in`... permet de parcourir les structures de données (tableaux, dictionnaires, *etc*.) en utilisant une variable temporaire et locale que l’on appelle généralement de manière explicite element. Elle s’écrit :

`for element in` structure de données

instructions

`end`

Maxime Forriez.