# Cours 10. Les chaînes de caractères – Approche complémentaire (09/12/2023)

Maintenant que vous connaissez les tableaux, on peut finir le cours sur les chaînes de caractères.

chaine = "..." est un tableau. On peut par conséquent appliquer toutes les fonctions des tableaux. Néanmoins, certaines sont plus intéressantes que d’autres.

collect(...) crée un tableau de caractères.

split(...) crée un tableau de chaînes de caractères en utilisant l’espace comme séparateur.

N.B. On peut changer le séparateur.

split(chaine, ‘caractère’)

join(table) crée une chaîne de caractères concaténée.

N.B. On peut utiliser un séparateur.

split(table, ‘caractère’)

\uXXXX : caractère UTF 4-digit HEX

\UXXXX : caractère UTF 8-digit HEX

On peut parcourir une chaîne de caractères :

for caractere in "caractere"

println(caractere)

end

findfirst(isequal(‘i’), "chaine") donne le premier caractère de la chaîne correspondant à isequal(...).

lastindex(chaine) donne le dernier indice de la chaîne de caractères.

replace("chaine", chaîne à modifier => modification) replace un caractère dans une chaîne.

replace("chaine", "a" => "e")

ce qui donne "cheine".

length(chaine) donne le nombre de caractères.

occursin("chaine2", "chaine1") vérifie si chaine2 apparaît dans chaine1.

repr(valeur, contexte) crée une chaîne de caractères à partir de n’importe quelle valeur. Le contexte est par défaut nothing et est facultatif. Il est défini par une paire :key => value.

chop("chaine", position du début, position de la fin) supprime sans options le dernier caractère et retourne une sous-chaîne ; avec options, il retourne l’intervalle des indices retenus.

Il existe bien entendu davantage de fonctions liées aux chaînes de caractères. À vous de les découvrir !

Maxime Forriez. 