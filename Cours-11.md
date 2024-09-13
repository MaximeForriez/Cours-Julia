# Cours 11. Les fonctions (09/12/2023)

La création d’une fonction

Dans tout langage de programmation, la base est de créer des fonctions.

function nomDeLaFonction(arguments)

instructions

end

N.B. Les variables dans les fonctions sont locales.

N.B. On peut initier les arguments avec des variables par défaut.

La fonction est appelée par :

nomDeLaFonction(paramètres)

Les fonctions mathématiques de base

log(...) : logarithme naturel

exp(...) : exponentielle de base e

log10(...) : logarithme décimal

sqrt(...) : racine carrée (ou \sqrt + tab)

cos(...) : cosinus

sinus(...) : sinus

minimum(...) : valeur minimale

maximum(...) : valeur maximale

round(...) : arrondi normalement la valeur flottante

round(Int, nombre) : arrondi un nombre à virgule flottante en entier

eps(...) : précision de la machineLes nombres aléatoires – Première approche

rand() crée un nombre aléatoire suivant une loi uniforme.

rand(n) crée un tableau ayant n éléments aléatoires.

rand(m, n) crée une matrice à deux dimensions m × n

rand(m, n, p) crée une matrice à trois dimensions m × n × p

Le retour d’une fonction

function nomDeLaFonction

instructions

return valeurs à retourner

end

La valeur de retour peut être une chaîne de caractères, un nombre ou un booléen.

N.B. Par convention, on peut retourner la valeur nothing.

return nothing

Les variables globales

En utilisant le modificateur global, on peut modifier et appeler une variable qui est en dehors de la fonction.

variable = true function testGlobal()

global variable

variable = true

end

Les fonctions anonymes

Il existe deux manières d’écrire une fonction anonyme :

(1) soit : X -> X^2 + 2X – 1

(2) soit :

function(X)

X^2 + 2X – 1 end

La fonction map

La fonction map(...) permet d’appliquer une fonction à un tableau :

map(fonction, tableau)

Exemple : map(round, [ 1.2, 3.5, 1.7]) renvoie [ 1.0, 4.0, 2.0]

On peut coupler map et fonction anonyme.

Exemple : map(x -> x^2 + 2x -1, [ 1, 3, -1 ]) renvoie [ 2, 14, -2]

Le symbole !

Le symbole ! est indicatif. Par convention, une fonction qui aura un effet de bord, notamment la modification d’un objet en place, contient un point d’exclamation.

Exemple :

sort() trie une copie d’un tableau et la renvoie.

sort!() trie directement le tableau.

Conclusion de la première partie

Avec les fonctions, vous venez de voir toute la base du langage Julia.

Maxime Forriez. 