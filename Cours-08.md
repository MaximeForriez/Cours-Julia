# Cours 8. Les dictionnaires (06/06/2023)

À la différence des tuples, les **dictionnaires** sont des structures de données **modifiables**, mais sans ordre. Ils sont définis par des **clés**. Ils s’écrivent comme une variable. Ils se notent :

	dictionnaire = Dict(clé1 => variable1, clé2 => variable2, clé3 => variable3, ...)

ou

	dictionnaire = Dict(:clé1 => variable1, :clé2 => variable2, :clé3 => variable3, ...)

> [!TIP]
> On peut créer un dictionnaire vide, puisque la structure est modifiable.

`dictionnaire = Dict()`

> [!TIP]
> Si, lors de sa création, le dictionnaire ne possède qu’un seul type de variable, il ne reconnaître que ce type. Pour obtenir un dictionnaire avec plusieurs types, il faut les créer dès sa déclaration ou créer un dictionnaire vide.

On peut appeler une variable par sa clé :

	dictionnaire[clé1]

On peut ajouter une nouvelle clé :

	dictionnaire[clé4] = variable4

On peut supprimer une variable par sa clé :

	pop!(dictionnaire, clé à supprimer)

La manipulation supprime la clé et la variable.

On peut mesurer la taille du dictionnaire :

	length(dictionnaire)

On peut retourner les clés contenues dans le dictionnaire :

	keys(dictionnaire)

On peut tester l’appartenance d’une clé au dictionnaire avec ϵ (`\in` + `tab`).

	clé à tester ϵ keys(dictionnaire)

On peut retourner les valeurs :

	values(dictionnaire)

On peut tester l’appartenance d’une valeur au dictionnaire :

	valeur à tester ϵ values(dictionnaire)

On peut parcourir un dictionnaire avec une boucle `for`... `in`... (cf. cours sur les boucles).

On peut placer des tableaux en valeur dans le dictionnaire (cf. cours sur les tableaux).

On peut vérifier la présence d’une clé en utilisant l’opérateur :

	haskey(dictionnaire, :clé à tester)

Maxime Forriez.