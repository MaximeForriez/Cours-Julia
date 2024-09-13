# Cours 3. Les opérateurs (24/04/2023)

Aujourd’hui, nous allons approfondir la notion d’opérateur. Elle peut paraître simple pour les initiés, mais elle peut causer pas de mal sueurs froides pour les autres. Voici une petite fiche technique pour ne plus se tromper et avoir les bons réflexes. Il ne s’agit pas de tout retenir, car certains opérateurs sont anecdotiques lorsque l’on code, mais il est bon de pouvoir retrouver facilement l’information et de savoir qu’ils existent. En effet, d’un langage à l’autre, vous n’avez pas les mêmes disponibles. Le langage Julia est particulièrement généreux, donc au terme de la lecture de ce post, vous aurez pris conscience de cette richesse.

L’opérateur d’affectation

L’opérateur d’affectation (=) a été rencontré lors du cours n°2 sur les variables. La liste proposée ici se voulant être complète, elle ne fait que rappeler son existence. Pour davantage d’informations, je vous renvoie audit cours.

Les opérateurs arithmétiques

Parmi tous les opérateurs, ce sont ceux qui vont vous servir au quotidien. De fait, vous finirez par les connaître très rapidement.

+ : addition

- : soustraction

* : multiplication

/ : division avec des nombres à virgule

÷ : division euclidienne sans reste

N.B. \div + tab permet d’obtenir l’obèle ÷

N.B. Il existe une fonction division euclidienne : div(numérateur, dénominateur).

^ : exposant

% : modulo (N.B. Il existe une fonction modulo : rem(numérateur, dénominateur))

// : simplification d’une fraction

(...) : parenthèses

Les opérateurs d’affectation

+= : ajout d’une valeur à une variable existante

Exemple : x = x + 2 équivaut à x += 2.

-= : soustraction d’une valeur à une variable existante

*= : multiplication d’une valeur à une variable existante

/= : division entre une variable existante et une valeur

%= : modulo entre une variable existante et d’une valeur

Remarque importante. Contrairement à de nombreux langages, les opérateurs d’implémentation de type ++ et -- n’existent pas en langage Julia.

Les opérateurs de comparaison

Parmi tous les opérateurs, ce sont ceux qui vont vous servir au quotidien. De fait, vous finirez par les connaître très rapidement.

= = : opérateur d’égalité (N.B. Il existe une fonction d’égalité : isequal(x, y))

!= : opérateur d’inégalité (≠)

= = = : opérateur d’identité (≡)

> : strictement supérieur

< : strictement inférieur

>= : supérieur (≥)

<= : inférieur (≤)

≈ : environ

N.B. On obtient le symbole en tapant \approx + tab.

Les opérateurs logiques

&& : ET (AND)

|| : OU (OR)

! : NON (NOT)

Les opérateurs de chaîne de caractères

* : opérateur de concaténation de chaîne de caractères

N.B. string(variable 1, variable 2, variable 3) est la fonction de concaténation.

On peut combiner * et string(), notamment pour convertir une variable en une chaîne de caractères.

Les commentaires

# : commentaire sur une ligne ou en fin de ligne

#= ... =# : commentaire sur plusieurs lignes

L’usage du point-virgule

Lors de l’utilisation de Julia en ligne de commande, le point-virgule en bout de ligne permet de ne pas afficher la réponse de la console. Il est par conséquent facultatif. À l’usage, vous mettrez plein de points-virgules dans votre code, car leur omission ne sert qu’à vérifier que le code exécute bien ce que vous lui avez demandé.

L’opérateur du non nombre

Il existe un opérateur pour exprimer l’idée de non nombre : NaN.Pour conclure, il existe d’autres opérateurs que l’on découvrira au fur et à mesure dans les autres cours prévus, mais il sera difficile de tous les passer en revue. Retenez que la plupart sont universels, mais ils peuvent avoir une syntaxe différente d’un langage à l’autre. L’informatique s’apprend avant tout par sa syntaxe. Tout le reste est de la logique pure.

Maxime Forriez. 