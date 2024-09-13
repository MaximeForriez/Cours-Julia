# Cours 4. Les chaînes de caractères – Première approche (23/05/2023)

Aujourd’hui, nous allons aborder les chaînes de caractères. Il faut avoir conscience que beaucoup d’éléments les concernant ne peuvent être explicités clairement à ce niveau du cours, mais elles demeurent indispensables pour programmer quoi que ce soit, d’où la nécessité d’en réaliser une première approche. Ce cours aura, de fait, un complément d’ici quelque temps, ce qui permettra de mieux comprendre et assimiler les traitements particuliers des chaînes de caractères.

Il n’est pas possible à ce stade de donner la vraie définition d’une chaîne de caractères. Dans ce chapitre, nous considérerons qu’il s’agit d’un type de variable ordinaire, ce qui est faux.

## La déclaration d’une chaîne de caractères (rappel)

Une chaîne de caractères se déclare comme une variable :

	nomDeLaChaine = "Je suis une chaîne de caractères."

ou

	nomDeLaChaine = """Je suis une chaîne de caractères."""

## L’affichage d’une chaîne de caractères

Pour afficher une chaîne de caractères, on utilise la fonction `println(`...`)`

	println("Je suis une chaîne de caractères.")

Toutefois, avec des guillemets simples, le saut de ligne est géré comme un alinéa.

Il faut utiliser les triples guillemets `"""` pour gérer un saut de ligne sans alinéa.

	println("""Je suis une chaîne de caractères.""")

En effet, la fonction `show(...)` affiche les guillemets :

	show("Je suis une chaîne de caractères.")

## La concaténation des chaînes de caractères

La concaténation est l’opération permettant de mélanger les chaînes de caractères entre elles.

	nom = "Maxime"

	println("Je m’appelle $nom.")

> [!TIP]
> Cela marche avec des nombres entiers ou réels.

> [!TIP]
> On peut additionner des nombres dans une chaîne de caractères.
>	num1 = 1
>	num2 = 1.5 println("Addition : $(num1 + num2)")

> [!TIP]
> On peut combiner des chaînes de caractères et des autres variables avec le $, ce qui est une autre manière de concaténer.

## Quelques fonctions natives utiles

À ce stade de votre apprentissage, il est bon de connaître quelques fonctions permettant de manipuler et de transformer les chaînes de caractères. Vous comprendrez ces fonctions d’ici quelques cours. Elles seront appliquées à une chaîne de caractères appelées nomDeLaChaine.

`first(nomDeLaChaine)` renvoie le premier caractère de la chaîne de caractères.

`nomDeLaChaine[indice]` renvoie au caractère à la position de l’indice, l’indice commençant à 0.

`length(nomDeLaChaine)` renvoie le nombre de caractères de la chaîne de caractères.

`sizeof(nomDeLaChaine)` renvoie le nombre d’octets de la chaîne de caractères.

On peut sélectionner des segments de chaîne de caractères :

	nomDeLaChaine[indice1:indice2]

Cela renvoie les caractères entre l’indice 1 et l’indice 2 inclus.

> [!TIP]
> On ne peut pas modifier un caractère de la chaîne de caractères. Elle est dite persistante. Il faut créer une nouvelle chaîne de caractères en utilisant par exemple la concaténation pour la modifier.

`uppercase(nomDeLaChaine)` convertit les lettres en majuscules.

`findfirst("test", nomDeLaChaine)` renvoie la position du premier caractère, ou de la première séquence de chaîne de caractères, testée.

## L’opérateur ϵ

L’opérateur ϵ s’obtient avec en écrivant `\in` + `tab`.

L’opérateur ϵ teste la présence d’un caractère dans une chaîne de caractères.

	lettre ϵ nomDeLaChaine

C’est fini pour l’instant. Nous reverrons les chaînes de caractères très rapidement.

Maxime Forriez.