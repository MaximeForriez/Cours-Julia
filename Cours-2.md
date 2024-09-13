# Cours 2. Les variables (06/04/2023)

Toute formation à un langage informatique débute par l’écriture des variables. Pour ceux qui l’ignorent une variable est un nom donné à quelque chose dans votre code pour lequel un morceau de mémoire vive ou du registre sera affecté (une adresse codée si l’on veut être précis). La gestion de la mémoire étant automatique, comme pour la plupart des langages modernes, sous `Julia`, je ne m’y attarderai pas. Retenez tout de même cette idée. Il existe différents types de variables et quelques conseils pour bien les nommer. En `Julia`, les types sont dynamiques, donc automatiques, mais il est toujours possible de forcer le type d’une variable pour bien obtenir ce que l’on veut. Par ailleurs, les types vont bien au-delà des types classiques en informatique puisqu’ils prennent en compte la théorie mathématique des nombres (entiers, relatifs, rationnels, réels, irrationnels, ou complexes), ce qui reste rare pour un langage informatique.

## Les types de variables

Les types des variables ne sont pas universels d’un langage à l’autre, mais ils se ressemblent beaucoup. Il faut de fait bien vérifier les types disponibles dans un langage avant même d’affecter vos variables.

L’assignation du type de variable est **automatique** sous `Julia`. Cela peut-être :

- `Char` signifiant caractère

- `Int`*N* signifiant nombre entier avec `N ϵ {8, 16, 32, 64, 128}`

- `BigInt` signifiant grand entier

- `Float`*N* signifiant nombre à virgule flottante avec `N ϵ {16, 32, 64}`

- `BigFloat` signifiant grand nombre à virgule flottante

- `String` signifiant chaîne de caractères

- `Bool` signifiant booléen

Le choix effectué est **le plus précis possible**. Néanmoins, il est possible de choisir le type en utilisant des fonctions natives de `Julia`.

> [!TIP]
> `typemin(` type `)` et `typemax(` type `)` fournissent les valeurs minimales et maximales du type placé entre parenthèses (type = `Char`, `IntN`, `FloatN`, `String`, `Bool`).

## L’art de nommer une variable

Jadis, au tout début des langages informatiques, il fallait nommer les variables de manière très courte – entre six et huit caractères, voire moins. Aujourd’hui, cette règle n’existe plus, sauf si vous utilisez de très vieux langages. De fait, pourquoi éviter de nommer clairement du variable ? Le problème de la nomination n’est pas à prendre à la légère, surtout lors d’un travail collectif ou la reprise d’un vieux code. Comment voulez-vous que quelqu’un, y compris vous-même, comprenne naturellement qu’une variable appelée `"toto"` désigne une moyenne de quelque chose ? Dans ce cas, il est préférable de nommer clairement la variable `"moyenneDuChamp1"` par exemple.

Il existe plusieurs manières de nommer les variables, `"moyenneDuChamp1"` n’est qu’un exemple possible. Vous pouvez aussi envisager de l’écrire :

	`moyenne_du_champ_1`

	`moyenneduchamp1`

	`_moyenneduchamp1`

*etc*.

L’idée est que vous optiez pour une écriture cohérente et explicite sur l’ensemble de votre code, et que vous exigiez que quiconque travaille avec vous code de la même manière. Cela n’est pas simple, mais il faut tenter d’y parvenir.

Pour finir, **de manière générique, toute variable commence avec une minuscule** afin de la distinguer rapidement d’autres éléments informatiques tels que les objets conventionnellement codés avec une majuscule au premier caractère. Notez qu’aucun nombre ne peut être placé en tête d’une variable, car la machine l’interprète comme un nombre, suivi d’une variable.

> [!TIP]
> En `Julia`, il vaut mieux éviter la version avec des *underscore*, car elle peut poser des problèmes de compilation.

> [!TIP]
> Il existe des variables informatiques qui sont constantes. On les écrira en majuscules.

> [!TIP]
> Comme précisé rapidement lors du cours n°1, vous pouvez utiliser les émoticônes pour nommer une variable, mais, comme vous le constatez, cela ne fait pas partie des standard pour bien nommer une variable de manière "universelle". Imaginons que vous appreniez un autre langage, et que vous avez pris cette mauvaise habitude, vous pourriez être surpris par le fait que votre code ne fonctionne pas.

> [!TIP]
> Même si c’est possible en `Julia`, évitez de mettre des caractères `UNICODE` tels que les accents dans votre nom de variable. Si vous apprenez un jour un autre langage, vous aurez pris une très mauvaise habitude qu’il sera difficile de corriger. Juste pour information, `Julia` utilise les symboles `LaTeX` comme `\pi` pour le symbole pi pour l’afficher il faut taper sur la touche tabulation. En résumé, `\pi` + `tab`.

## L’affectation et la déclaration d’une variable

L’affectation d’une variable consiste à la nommer, à exiger la création d’un espace mémoire pour cette donnée précise. À cette étape, la variable n’a aucune valeur qui lui est liée. Il s’agit juste d’une adresse allouée dans la mémoire.

	`moyenneDuChamp1`

Cela sera rappelé lors du prochain chapitre qui généralisera la notion, mais la déclaration d’une variable utilise un opérateur `=`. Une valeur complète son affectation.

	`moyenneDuChamp1 = 10`

À partir du moment où la ligne a été lue par le compilateur `Julia`, `moyenneDuChamp1` est une variable valant `10`. Il suffit de taper son nom pour utiliser la valeur `10`. De manière plus imagée, dans la case `moyenneDuChamp1`, se trouve la valeur `10`.

La déclaration ne s’effectue que dans un sens.

	`10 = moyenneDuChamp1`

n’affecte rien du tout.

Cet ordre implicite est fondamental lorsque vous serez amené à renommer une variable. Par exemple,

	`moyenneDuChamp2 = 20`

	`moyenneDuChamp1 = moyenneDuChamp2`

Au terme de l’exécution de ce code, que vaut `moyenneDuChamp1 ? `10` ou `20`. Réponse : `20` ! Par la dernière ligne, vous avez déclaré à votre code de donner la valeur de `moyenneDuChamp2`, qui vaut toujours `20`, à `moyenneDuChamp1`. De même, il est possible de réaffecter une variable en utilisant simplement l’opérateur d’affectation `=`.

Rien de très compliquer dans l’affection et la déclaration des variables, mais il faut **être très rigoureux**.

Il faut remarquer que l’on déclare un caractère de la manière suivante :

	`caractere = 'lettre minuscule ou majuscule'`

et pour un chaîne de caractères deux cas sont possibles :

	`chaine = "chaîne de caractères"`

ou

	`chaine = """chaîne de caractères"""`

Les trois guillemets permettent d’utiliser le symbole " dans la chaîne de caractères. Si le guillemet est placé au début ou à la fin de la chaîne de caractères, il faut laisser un espace :

	`chaine =""" "chaîne de caractères" """`

Les nombres à virgule flottante sont matérialisés par un point `.`

Il est possible de vérifier le type affecté à la variable déclarée grâce à la fonction `typeof(`variable`)` qui renvoie le type de variable choisi par `Julia`.

Il faut noter que l’on peut déclarer plusieurs variables en même temps :

	`x, y = 1, 2`

ce qui équivaut à :

	`x = 1 y = 1`

Pour finir, il faut noter que certains mots sont interdits pour nommer une variable, car il faut partir des instructions de base de `Julia` :

- `abstract`

- `type`

- `baremodule`

- `begin`

- `break`

- `catch

- `const`

- `continue`

- `do`

- `else`

- `elseif`

- `end`

- `export`

- `finally`

- `for`

- `function`

- `global`

- `if`

- `import`

- `importall`

- `in`

- `let`

- `local`

- `macro`

- `module`

- `mutable`

- `struct`

- `primitive`

- `type`

- `quote`

- `return`

- `strict`

- `try`

- `using`

- `where`

- `while`

## Les constantes

Avant de coder les constantes, il faut bien comprendre que les constantes restent des variables, mais leur affectation en mémoire s’effectue en lecture seule ; il n’y a pas de réécriture possible. De fait, l’unique manière de modifier une constante reste de modifier son affectation initiale.

En `Julia`, le modificateur `const` permet de définir une constante.

	`const MOYENNEDUCHAMP1 = 10`

## La conversion des types

Les types de variables ne sont qu’un élément de ce que le langage `Julia` appelle `"type"`. Il faut bien assimiler ce troisième cours pour appréhender par la suite beaucoup plus sereinement le chapitre sur les types en `Julia`. Je reviendrai par conséquent beaucoup plus tard sur une généralisation des types de variables. Cela sera l’occasion d’expliquer pleinement la conversion des types. Néanmoins, dans le cadre d’une programmation basique, il faut déjà connaître quelques conversions :

- `string(`nombre`)` permettant la conversion d’un nombre en chaîne de caractères ;

- `convert(type, valeur)` permettant la conversion d’un nombre dans le type de nombre choisi ;

- `parse(`type`,` chaîne de caractères`)` permettant la conversion des chaînes de caractères. Cette fonction ignore les espaces, et ne convertit pas les autres caractères ;

- `typename(`valeur`)` permettant l’appel d’une conversion.

Maxime Forriez.