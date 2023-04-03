# Corpus de presse pour l’analyse textuelle portant sur l’alimentation humaine à Montréal

## Qu’est-ce que ce corpus? 

27665 textes ont été obtenus par moissonnage du dépôt Eureka; 18852 obtenus par moissonnage direct des sites des médias. 

- 10963 en anglais
- 37841 en français  

Le corpus médiatique sur l’alimentation humaine est un jeu de données de plus de 40 milles articles de presse concernant la sécurité alimentaire à Montréal, publiés entre janvier 2005 et mai 2020 et provenant de ving-trois sources médiatiques en ligne. Les articles sont bilingues, avec 80% des documents écrits en français et 20% en anglais. 

## Quels sont les fichiers qui composent le corpus? 
Le corpus est composé de 6 fichiers sectionnés selon la langue (anglaise ou française) des textes. Pour chaque langue, il y deux tables de données, une qui contient les métadonnées récupérées par le moissonnage ainsi qu’une matrice TF/IDF.  

#### Les fichiers sont les suivants : 
- Corpus_media_EN_Food_metadata.csv
- Corpus_media_EN_Food_TFIDF.csv
- Corpus_media_FR_Alimentation_metadonnee.csv
- Corpus_media_FR_Alimentation_TFIDF.csv

## À quoi peut-il servir? 
Les matrices TF/IDF sont des représentations vectorielles du corpus; elles peuvent être utilisées pour produire des analyses thématiques et exploratoires à partir de la théorie de la linguistique distributionnelle. 

Les matrices de métadonnées peuvent être utilisées pour cibler des variables pour l’exploration, produire de nouvelles classifications, mais surtout, elles servent de référence pour permettre une contextualisation des documents pour l’analyste. 

## Pourquoi le corpus original n’est pas disponible? 
En vertu des ententes légales prises avec Eureka, il n’est pas possible de faire la diffusion des textes de manière à ce qu’ils puissent être reconstitués intégralement. Pour cette raison, les fichiers de métadonnées contiennent des versions tronquées des textes. Aussi, nous avons enrichi le fichier de métadonnée d’un résumé produit de manière automatique pour soutenir le travail de l’analyste. 

## Quels sont les champs de données et leurs sources? 
Les noms des champs sont conformes au format de description bibliographique RIS.
- TY - Type de référence selon un classification standardisée (par convention le premier champ)
- TI - Titre et sous-titre (le cas échéant) séparés par le caractère losange répété (◊◊)
- T1 - Titre principal
- AU - Auteurs (format: prénom nom); séparés par un caractère de barre verticale (|)
- N2 - Citation des 31 premiers mots du corps principal du texte
- U1 - Corps principal du texte (sauts de ligne remplacés par le caractère losange répété (◊◊))
- U2 - Chapeau ou texte mis en évidence en tête de l’article (sauts de ligne remplacés par le caractère losange répété (◊◊))
- U3 - Texte de l’encadré qui accompagne l’article (sauts de ligne remplacés par le caractère losange répété (◊◊))
- U4 - Corps principal du texte tronqué au vingt-cinquième centile (sauts de ligne remplacés par le caractère losange répété (◊◊))
- U5 - Résumé automatique produit à partir d’un modèle de langue BERT
- L4 - Textes des légendes qui accompagnent les illustrations (le cas échéant) séparés par le caractère losange répété (◊◊)
- KW - Mots-clés séparés par un caractère de barre vertical (|)
- SE - Sections ou rubricage séparés par un caractère de barre verticale (|)
- C1 - Titre de l’auteur
- C2 - Énoncé biographique sur l’auteur
- C3 - Sources du texte (exemple: La Presse canadienne)
- JF - Titre du média
- CY - Lieu de publication (par défaut: Montréal)
- VL - Volume number ou numéro de volume
- IS - Issue number ou numéro de livraison
- SP - Start Page ou page de début
- OP - Date de publication originale
- PY - Année de publication originale
- DA - Date (différente si mise à jour)
- Y2 - Date de la procédure de moissonnage
- LA - Langue principale du texte
- DB - Database ou nom du dépôt d’où le texte a été extrait s’il y s lieu
- UR - URL
- ID - Identifiant unique
- ER - End of Reference ou fin de description (doit être vide)

- *remarque 1* : Dans les textes analysés, le caractère losange répété (◊◊) est utilisé pour signaler un saut de ligne ou attacher des énoncés, tandis que le caractère barre verticale (|) est utilisé pour séparer des valeurs distinctes. 
- *remarque 2* : Le format des noms d’auteur (AU) a été standardisé et les entités ont été regroupées (en anglais: clustering).
- *remarque 3* : Dans certains cas, le corps principal de texte (U1) inclut une reprise du chapeau (U2). 

## Quelle méthode a été utilisée pour déterminer quel texte est sélectionné pour faire partie du corpus? 
*version abrégée du guide de classification avec le lien vers le document entier dans le GITHUB*

## Quelles sont les méthodes utilisées pour l’enrichissement du corpus par le laboratoire? 
*à complété*

## La production des matrices TF/IDF 
La production de résumés automatiques a utilisé l’interface de Hugging face et des modèles BERT pour l’anglais et le français afin de produire automatiquement un ensemble de synthèse. Le texte de chaque article a été segmenté, résumé et rejoint ensemble. La méthode produit des résultats (%%%%% besoin de l’analyse en échantillon). Aussi, un certain nombre de résultats sont déficients par la véritable impossibilité de créer un résumé pour cet ensemble continu de texte, c’est le cas par exemple les petites annonces ou un article qui liste les événements à venir d'un quartier. 

## Qui est l’équipe qui a préparé ce corpus?
*à complété*
