# Cours 7. Les tuples (06/06/2023)

Les **tuples** sont une structure de données. Ils s’utilisent comme des variables, donc ils ont un nom. Ils listent des variables avec ou sans clés. Ils se notent :

`tuple = (variable1, variable2, variable3, ...)`

> [!TIP]
> Les parenthèses sont **facultatives**.

Avec une clé, on note le tuple :

`tuple = (nomVariable1 = variable1, nomVariable2 = variable2, nomVariable3 = variable3, ...)`

> [!TIP]
> En utilisant cette notation, on peut appeler les variables en utilisant leur nom avec le tuple définit. Par exemple, `tuple.nomVariable1` appelle la `variable1` du tuple.

Un tuple **n**’est **pas modifiable**, ni dans ses valeurs, ni dans son ordination. On ne peut par conséquent ni ajouter, ni supprimer les variables. Il est dit persistant, c’est-à-dire en lecture seule.

On peut appeler une variable par sa position dans le tuple. Par exemple,

`tuple[1]` renvoie la `variable1`.

> [!TIP]
> L’indice des tuples commence par 1, et non par 0 comme dans d’autres langages de programmation.

On peut parcourir les tuples avec une boucle de type `for`... `in`... (cf. cours sur les boucles).

Maxime Forriez.