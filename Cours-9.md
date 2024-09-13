# Cours 9. Les tableaux (09/12/2023)

Les **tableaux** ont quelques spécificités sur `Julia`. La syntaxe est la suivante :

	table = [ variable1, variable2, variable3 ]

On peut mélanger les types dans les tableaux, mais il reste ordonné.

Toutefois, on peut créer un tableau vide sans type :

	table = [ ]

On peut appeler un élément du tableau par son indice.

	table[1]

> [!TIP]
> Les indices commencent à 1, et non à 0. De fait, dans l’exemple, on appelle le premier élément.

On peut parcourir un tableau :

	for element in table

		println(element)

	end

On peut affecter un type aux valeurs du tableau.

Exemple : `Int[ variable1, variable2, variable3]` pour un tableau d’entiers

On peut insérer une variable à la fin du tableau :

	push!(table, valeur à insérer)

On peut supprimer la dernière valeur du tableau et la renvoyer :

	pop!(table)

On peut changer une valeur par sa position :

	table[1] = nouvelle variable

On peut créer des tableaux imbriqués :

	[ [...] , [...] , ... ]

On peut calculer le nombre d’éléments du tableau :

	length(table)

On peut sélectionner des segments :

	table[ 2 : 4 ]

pour le 2<sup>e</sup> élément et le 4<sup>e</sup> élément.

> [!TIP]
> `2:4` est une collection.

> [!TIP]
> On ne peut pas utiliser des positions négatives.

> [!TIP]
> On peut sélection jusqu’au dernier élément avec end.
>	table[ 2 : end ]

> [!TIP]
> `begin` désigne le premier élément.

On peut insérer un tableau `table2` dans un tableau `table` à la fin de ce dernier :

	table2 = [ ... ] 
	append!(table, table2)

On peut faire une insertion en début de tableau :

	prepend!(table, table2)

On peut trier par ordre croissant ou alphabétique un tableau :

	sort!(table)

On peut inverser l’ordre d’un tableau :

	reverse(table)

On peut additionner les éléments d’un tableau de nombres :

	sum(table)

On peut appliquer une fonction sur l’ensemble d’un tableau grâce à un dot (.)

- `[1, 2, 3] .^ 3` signifie `[1³, 2³, 3³]`

- `uppercase.(["abc", "def", "ghi"])` signifie `["ABC", "DEF", "GHI"]`

> [!TIP]
> Il y a : `.+`, `.*`, `.-`, `./`

On peut supprimer un élément à partir de sa position :

	slice!(table, position)

On peut supprimer le premier élément et le retourner :

	popfirst!(table)

On peut ajouter un élément en début de tableau et le retourner :

	pushfirst!(table, valeur)

On peut supprimer un élément à partir de sa position :

	deleteat!(table, position)

On ne peut pas copier un tableau. `table2 = table1` ne crée pas une copie de `table1`. Il faut écrire :

	table2 = copy(table1)

On peut créer une copie profonde de `table1` avec :

	table2 = deepcopy(table1)

Tout est alors copié récursivement, résultant en un objet totalement indépendant.

On peut créer des tableaux pré-remplis :

- `zeros(...)` : tableau de *n* éléments rempli de `0.0`

- `ones(...)` : tableau de *n* éléments rempli de `1.0`

- `Vector{`nom du type`}(undef,` *n*`)` : tableau de *n* éléments non initialisés

- `range(start = 0, stop = stop, length =` *n*`)` : tableau de *n* nombres équi-répartis entre `start` et `stop`

On peut remplir un tableau avec une même valeur :

- `fill!(table,` valeur`)`

- `fill(`valeur`,` nombre de colonnes`,` nombre de lignes`)`

On peut tester si une valeur est un élément du tableau :

	in(valeur, table)

ou

	valeur in table

On peut changer la dimension d’un tableau :

	reshape(1:6, nombre de colonnes, nombre de lignes`)

On peut filtrer les valeurs d’un tableau avec filter et une condition `is_______`.

	filtrer(condition, tableau)

Exemple : `filtrer(isadd, 1:10)`

`isadd` indique les nombres impairs : `[true, false, true, false, true, false, true, false, true, false]`.

On peut insérer un élement à l’indice *i* du tableau :

	insert!(table, indice, élément)

avec *i* entre 1 et l’infini.

On peut sélectionner le premier ou dernier élément :

	firstindex(table)

	lastindex(table)

On peut remplir un tableau avec un booléen :

- `true(`*n*`)` : tableau de *n* éléments rempli de `true`

- `false(`*n*`)` : tableau de *n* éléments rempli de `false`

- `collect(`collection`)` convertit une collection en un tableau.

On peut redimensionner un tableau par un nombre :

	resize!(table, nombre)

On peut permuter les lignes et les colonnes d’un tableau :

	permutedims(table)

On peut visualiser un morceau du tableau :

	view(table, colonne, ligne)

Maxime Forriez.