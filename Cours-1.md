# Cours 1. Installation (16/03/2022)

## Téléchargement de l’exécutif d’installation

Sur le site de `Julia` ([https://julialang.org/downloads/](https://julialang.org/downloads/)), il faut télécharger une version `Current stable release` pour votre système d’exploitation. Deux choix s’offrent à vous : soit vous prenez une version installer avec un `*.exe` (ce que je conseille pour ceux qui maîtrisent mal les installations manuelles), soit vous prenez une version portable avec un dossier d’installation pour les autres. L’unique différence est que l’exécutif placera le dossier automatiquement dans votre arborescence alors que, avec le dossier, vous êtes libre de choisir son emplacement. Néanmoins, il faudra lier `Julia` avec votre invite de commande manuellement. De fait, la version exécutive est plus intéressante, puisqu’il suffit de cocher `Add Julia to PATH` pour faire de `Julia` une variable d’environnement exécutable dans n’importe quel dossier. Il ne faut pas oublier de le faire.

L’installation de `Julia`, automatique ou manuelle, prend quelques minutes. Toutefois, vous n’avez installé que la version de base. J’y reviendrai lors de la troisième partie du cours, mais, pour optimiser `Julia`, comme avec `Python` ou `Mathematica`, il vous faudra installer un certain nombre de paquets non livrés par défaut sur [https://juliapackages.com/](https://juliapackages.com/). Pour ceux qui se posent la question, un paquet est un fichier `Julia` normal avec une extension `*.jl` contenant un code complexe écrit, utilisé et validé par la communauté de `Julia`. Par exemple, il est inutile de réécrire son propre code, sauf si cela est vraiment nécessaire ou pédagogique, pour obtenir une régression linéaire avec `Julia` alors que le paquet existe déjà.

Avec l’invite de commande, vous pouvez désormais lancer `Julia` en mode *Read-Eval-Print-Loop* (R.E.P.L.). En général, l’installation vous propose un raccourci pour l’ouvrir directement, mais, étant donné que `Julia` fait partie des variables d’environnement de votre système, en ouvrant l’invite vous pouvez lancer Julia dans n’importe quel dossier défini dans votre ligne de commande en tapant simplement `"julia"`.

`C:\Users\Desktop\> julia` (entrée)

(logo `Julia`)

`julia>`

(désormais, il faut insérer du code `Julia`, et non du code de l’invite de commande)

Sauf au cours de votre apprentissage, vous utiliserez peu la console de l’invite de commande. Néanmoins, elle est pratique. Par exemple,

`julia> ?` (entrée)

vous permet d’obtenir la fonction

`help?>` (taper le nom de la fonction Julia)

qui vous assure une aide rapide.

`julia> ]` (entrée)

vous permettra au cours de la troisième partie d’installer les paquets

`@v1.8pkg> add` (nom du paquet)

Vous pouvez également accéder à `PowerShell` avec :

`julia> ;` (entrée)

qui ouvre :

`shell>`

Il existe plein de fonctions de base comme

`julia> ans`

qui permet, comme sur la plupart des calculatrices, de récupérer le résultat numérique précédent.

Pour quitter, `help?>`, `@v1.8Pkg>` ou `shell>`, il suffit de faire `ctrl + c` (qui n’est pas la fonction copier dans l’invite de commande).

Pour quitter `Julia`, il suffit de taper :

`julia> exit()` (entrée)

## Installation du langage dans un éditeur de code non connecté

La plupart des installations de `Julia` que vous trouverez sur les tutoriels en ligne exigent une connexion, comme avec `Jupyter`. Cela étant, si vous n’avez pas la possibilité de vous connecter - eh oui ça arrive encore –, vous serez quelque peu limité pour exécuter votre code. Je vous conseille par conséquent d’installer `Julia` sur votre éditeur de code préféré. Pour ma part, j’utilise `Notepad++`, mais il en existe plein d’autres.

L’installation est manuelle. Ce n’est pas très compliqué, mais ne loupez pas une étape.

(1) Télécharger le dossier [https://www.dropbox.com/s/pzpxrbgtbgtogf6/julia_npp.zip?dl=0](https://www.dropbox.com/s/pzpxrbgtbgtogf6/julia_npp.zip?dl=0.).

(2) Décompresser le dossier

(3) Placer le dossier dans `C:\Programmes\Notepad++\`

(4) Ouvrir `Notepad++`

Vous constaterez que `Julia` n’est pas encore un langage par défaut. Il faut par conséquent l’installer dans la liste du menu Langage.

(a) Menu `Langage` → `Langage utilisateur` → `Définir votre langage...` → `Ouverture de la fenêtre Langage utilisateur`

(b) Cliquer sur `Importer...` → Aller dans le dossier `julia_npp` → ouvrir le fichier `*.xml`

Au terme de ces étapes, vous avez deux possibilités : soit l’importation est un succès, et, après avoir éteint le logiciel, puis l’avoir rouvert, `Julia` apparaît dans le menu Langage, mais pas dans la liste officielle, donc pas dans le dossier `J` ; il faut regarder sous Langage utilisateur ; soit l’importation est un échec, et là il faudra trouver un autre paquet d’installation en ligne contenant le bon fichier `*.xml`, chose que vous devrez faire si vous utilisez un autre éditeur de code.

## Lecture d’un fichier `Julia`

L’installation de `Julia` dans `Notepad++` permet de créer plus facilement que dans le `Bloc-notes` classique des fichiers `*.jl`. Pour exécuter un fichier, il suffit avec l’invite de commande d’ouvrir le répertoire contenant le fichier à exécuter, puis de lancer votre programme avec le mot-clé `"julia"`, comme vous pouvez déjà le faire avec `Java` (en deux étapes) ou `Python` (en une étape).

`C:\Users\Desktop\> julia test.jl` (entrée)

L’invite de commande exécutera votre code `Julia` et affichera le résultat de son exécution si vous avez défini des entrées ou des sorties, mais cela sera traité dans les prochains cours.

En bref, l’installation de Julia n’est pas très compliquée, mais elle nécessite un peu de rigueur. Si vous êtes grand commençant en informatique, allez-y étape par étape, et n’hésitez pas à compléter cette première leçon avec des lectures, des tutoriels, ou à contacter votre serviteur.

Maxime Forriez.