# Cours 5. Les conditions (23/05/2023)

Les **conditions** font des instructions de base de n’importe quel langage de programmation.

## L’écriture d’une condition simple

Une condition s’écrit simplement. Toutefois, il faut respecter les alinéas pour que cela fonctionne.

`if` test

instructions si le test est vrai

`else`

instructions si le test est faux

`end`

> [!TIP]
> Les conditions peuvent s’imbriquer.

## L’enchaînement de conditions

`if` test1

si test1 vrai

`else if` test 2

si test2 vrai

`else if` test 3

si test3 vrai

`else`

sinon (par défaut)

`end`

## Les ternaires

test `?` si vrai `:` si faux

équivaut à :

`if` test

si vrai

`else`

si faux

`end`

## Les assertions

Une assertion est utilisée en tant qu’outil de débogage en création une `AssertionError`. Pour écrire une assertion, on utilise une macro. Nous reviendrons sur cette notion.

`@assert(`test`,` réponse à l’affichage si le test est faux`)`

Voilà, il n’y a rien de plus à savoir sur les conditions. Avec elles, vous pouvez commencer à coder en `Julia`. Leur puissance sera pleine après avoir vu une autre instruction de base, les boucles.

Maxime Forriez.