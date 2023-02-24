# Exercice d'accessibilité des contenus

## Équipe
- Cloé Ouellette
- Prénom nom

## Objectifs
- Expérimenter le versionnage de fichiers avec GIT
- Acquérir des compétences en accessibilité des contenus

## Prérequis
- Avoir lu et pris connaissance des notes du cours 10
- Avoir un compte GitHub
- Avoir installé et configurer GIT sur votre ordinateur
- Avoir installé l'outil CCA (colour-contrast-analyzer)

## Instructions

### 0. 
- Initialiser un dépôt GIT dans le dossier du projet
- Créer un fichier `index.html` et un fichier `style.css`

### 1.	Donner une alternative textuelle aux images

#### 1.1 Baliser dans le fichier `index.html` les images du dossier `1-textes-alternatifs` 

Pour vous guider dans le choix des balises, des attributs et des valeurs d'attributs, utiliser l'arbre de décision et référez-vous aux notes de cours.

#### 1.2 Évaluer la pertinence des contenus textuels alternatifs

Pour chacune des pages ci-dessous, les textes alternatifs sont-ils adéquats ?Commenter votre observation. Pourrait-on faire mieux ? Donnez un exemple de ce que vous proposeriez.

- https://www.sail.ca/fr/chaussures/junior/multi-sport-et-plein-air 

Les textes alternatifs sont effectivement adéquats. Chaque image a son propre texte alternatif en plus d'une description dessous. 
Pour le logo, étant donné que qu'il est cliquable et qu'il permet de retourner à la page d'accueil, j'ajouterais dans le texte alternatif "home" ou "accueil". 

[capture-écran](images/1-textes-alternatifs/1-2/screencapture-sail-ca-fr-chaussures-enfant-chaussures-de-sport-2023-02-24-10_01_07.png)
- https://amzn.to/2NnbKPN 

Le site amazon a bel et bien intégré des textes alternatifs. Chaque image a son propre texte alternatif, en plus du texte d'une description sous les articles (images). Cependant, le logo d'Amazon ne contient aucun texte, ce qui rend la tâche de navigation plus complexe. 

[capture-écran](images/1-textes-alternatifs/1-2/screencapture-amazon-ca-fr-s-2023-02-24-10_06_05.png)
- https://www.lesoleil.com/  

Bons points : Chaque article / image contient son propre texte alternatif. De plus, même la navigation principale en tête du site en contient. 
Ajustement :  Il faudrait ajouter des mots-clés comme "accueil" pour indiquer la destination si on clique sur le lien. 

[capture-écran](images/1-textes-alternatifs/1-2/screencapture-lesoleil-2023-02-24-10_09_23.png)
- https://www.rad.ca/  

Le site ne contient aucun texte alternatif. La plupart des images ont été intégrés comme "background-image". Des figcaptions auraient peut-etre pu etre intégré à ce moment la. Cependant, j'ai l'impression que les images en tant que tel sont là que pour ajouter des éléments visuels. Elle répète, selon moi, une information présente dans le texte adjacent.

[capture-écran](images/1-textes-alternatifs/1-2/screencapture-rad-ca-2023-02-24-10_12_22.png)

Astuce  
Parfois, l’affichage des alt ne donnent pas un résultat facile à lire… lorsque cela se produit, faites un clic droit de la souris et choisir inspecter pour positionner l’inspecteur de DOM sur le HTML de l’image.
Essayer d’identifier l’emplacement du alt et puis regarder s’il y a une description tout de suite après.

### 2.Vérifier les contrastes de couleurs

#### 2.1	Utiliser l’outil d’analyse de contraste des couleurs (CCA) pour identifier les problèmes de contrastes sur cette page : http://2016.webaquebec.org/

Pour chaque problème de contraste identifié,
documenter le problème par une capture-écran incluant dans son cadre, la zone fautive à gauche et à droite, les résultats détaillés de l’outil, tel que démontré dans l’exemple ci-dessous.

Sauvegarder les captures dans le dossier images. Compléter les liens ci-dessous:
- [Contraste insuffisant 1](images/2-contrastes-couleurs/capture1.png)
- [Contraste insuffisant 2](images/2-contrastes-couleurs/capture2.png)
- [Contraste insuffisant 3](images/2-contrastes-couleurs/capture3.png)
- [Contraste insuffisant 4](images/2-contrastes-couleurs/capture4.png)

### 3. Structurer avec les h1-h6 une table des matières

#### 3.1 Vérifier la structure

D’après les captures-écrans que vous trouverez dans le dossier [images/3-table-des-matieres_h1-h6/3-1/](images/3-table-des-matieres_h1-h6/3-1) , est-ce que la table des matières du document est correcte?  

Sinon, expliquez le problème en vous basant sur les règles de base énoncées dans les notes de cours. 

__Tutoriel sur les formulaires du w3c__  
[Article](images/3-table-des-matieres_h1-h6/3-1/tuto-form-w3c.pdf)  

[Table des matières (outline)](images/3-table-des-matieres_h1-h6/3-1/tuto-form-w3c-outline.png) 

Réponse : 

Pour ce site, oui, la table des matières du document est correcte. Le `h1` représente le sujet et non le titre de la page. Les `h2` viennent à la suite du `h1` et ils sont bel et bien des sous-titres. 

__L’affaire Savtchenko__ 
[Article](images/3-table-des-matieres_h1-h6/3-1/article-savtchenko.pdf)  
[Table des matières (outline)](images/3-table-des-matieres_h1-h6/3-1/article-savtchenko-outline.png) 
  
Réponse : 

Pour ce site, malheureusement se retrouve quelques lacunes dans la table des matières du document. La hiérarchisation n'est pas tout à fait au point. Les informations communes dans l'en-tête de la page ne devraient pas se retrouver dans la hiérarchie de titres. Donc, c'est une erreur en soi d'avoir inclu les éléments de la navigation principale comme des `h2`. Par conséquent, le `h1` est lui correcte étant donné que c'est le titre de l'article. Les `h2` qui suivent jusqu'à "Échange de prisonniers entre la Russie et l'Ukraine" sont bons sauf le premier. Ce dernier n'est pas un sous-titre. Les `h2` qui suivent sont fautifs et devraient plutot etre des `h3` ou ...

#### 3.2 S'exercer à bien structurer

- Ouvrir la capture-écran [concevoir-un-design-sans-la-couleur](images/3-table-des-matieres_h1-h6/3-2/concevoir-un-design-sans-la-couleur.pdf) que vous trouverez dans le dossier `sources > h1h6-partie-2` dans le logiciel PhotoShop.  
- Ajouter un calque de blanc à 50% de transparence
- Dans un 3e calque, par-dessus, identifiez les titres et leurs niveaux (h1-h6) de manière voyante (couleur rouge et font-size suffisant)
- Sauvegarder au format .psd ou .png dans le même dossier.
- [Relier ce fichier-réponse ici](images/3-table-des-matieres_h1-h6/3-2/concevoir-un-design-sans-la-couleur.pdf)

### 4. Baliser un tableau de données pour qu’il soit accessible

D’après la capture-écran et le texte fourni dans le dossier [4-tableau-de-donnees](images/4-tableau-de-donnees), balisez de manière accessible ce tableau de données.  
  
Votre tableau de données doit comporter un titre (caption) : 

> "Recommandations de consommation de poissons selon l’âge, le sexe et la condition physique".  


Les __entêtes de rangées et de colonnes__ doivent être balisées comme des `<th>` plutôt que des `<td>` et puisque le tableau est *complexe*, vous devez utiliser des attributs `id` dans les `<th>`. 

Chaque cellule `<td>` du tableau doit avoir un attribut headers avec comme valeur(s), le ou les identifiants de ses entêtes de colonnes et de rangées.

Styler le tableau conformément au fichier [consommation-poissons.pdf](images/4-tableau-de-donnees/consommation-poissons.pdf).

#### Ressources
•	balisage accessible d’un tableau (voir les notes du cours 10)
•	balisage html : https://www.w3schools.com/TAGs/tag_table.asp
•	balisage css de tableau: https://www.w3schools.com/css/css_table.asp





