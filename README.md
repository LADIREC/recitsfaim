# Corpus de presse pour l’analyse textuelle portant sur l’alimentation humaine à Montréal

## Qu’est-ce que ce corpus?
Le corpus médiatique sur l’alimentation humaine est un jeu de données décrivant 46 443 textes de presse concernant l’alimentation humaine à Montréal, publiés entre janvier 2005 et mai 2020 et provenant de soixante-trois sources médiatiques en ligne. Les textes sont de langues française et anglaise, selon les proportions suivantes :
- 33 151 textes de presse de langue française
- 13 292 textes de presse de langue anglaise

Ces textes identifiés au moyen de requêtes par combinaisons de mots-clefs ont été obtenus par moissonnage, soit du dépôt de textes Eureka (Cision), soit sur les sites de vingt-trois médias canadiens, selon les proportions suivantes :
- 27 665 moissonnés sur Eureka
- 18 778 moissonnés sur les sites de médias

Ce corpus primaire a fait l’objet de procédures de classification supervisée afin d’en resserrer le propos sur l’alimentation humaine, ayant eu pour résultat l’écartement de 12 497 documents. Sectionnés selon la langue principale des texte et publiés séparément, les sous-corpus résultants contiennent :
- 24 752 textes de langue française
- 9 194 texte de langue anglaise

## Quels sont les fichiers qui composent le jeu de données? 
Le corpus à proprement dit est composé de 6 fichiers tabulaires sectionnés selon la langue principale des textes. Pour le français et l’anglais, il y trois tables de données :
- Une table qui contient les données descriptives du corpus formé de l’ensemble des textes moissonnés
- Une table qui contient les données descriptives du corpus formé des textes moissonnés classés
- Une matrice TF/IDF

## À quoi peut-il servir? 
Les matrices TF/IDF sont des représentations vectorielles du corpus; elles peuvent être utilisées pour produire des analyses thématiques et exploratoires à partir de la théorie de la linguistique distributionnelle. 

Les tables de données descriptives peuvent être utilisées pour cibler des variables pour l’exploration, produire de nouvelles classifications, mais surtout, elles servent de référence pour permettre une contextualisation des documents pour l’analyste.

## Pourquoi le corpus original n’est pas disponible? 
En vertu de l’entente légale qui nous lie avec Eureka, il n’est pas possible de faire la diffusion des textes de manière à ce qu’ils puissent être reconstitués intégralement. Pour cette raison, les tables de données descriptives contiennent des versions tronquées des textes. Aussi, nous avons enrichi le fichier de métadonnée d’un résumé produit de manière automatique pour soutenir le travail de l’analyste. 

## Quels sont les champs de données et leurs sources? 
Les noms des champs sont conformes au format de description bibliographique RIS.
- TY - Type de référence selon un classification standardisée (par convention le premier champ)
- TI - Titre et sous-titre (le cas échéant)
- T1 - Titre principal
- AU - Auteurs (format: prénom nom)
- N2 - Citation des 31 premiers mots du corps principal du texte
- U1 - [ces données ont été retirées des tables diffusées]
- U2 - [ces données ont été retirées des tables diffusées]
- U3 - [ces données ont été retirées des tables diffusées]
- U4 - Corps principal du texte tronqué au vingt-cinquième centile
- U5 - Résumé automatique produit à partir d’un modèle de langue BERT
- L4 - Textes des légendes qui accompagnent les illustrations (le cas échéant)
- KW - Mots-clés
- SE - Sections ou rubricage
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

Remarque 1 : Dans les textes analysés, le caractère losange répété (◊◊) est utilisé pour signaler un saut de ligne ou attacher des énoncés, tandis que le caractère barre verticale (|) est utilisé pour séparer des valeurs distinctes. 

Remarque 2 : Le format des noms d’auteur (AU) a été standardisé et les entités ont été regroupées (en anglais: clustering).

## Quelle méthode a été utilisée pour déterminer quels textes moissonnés devaient être retenus et quels textes écartés? 
On se rapportera au Guide de classification et aux rapports de classification des analystes Pascal Brissette et Lisa Teichmann.

## Quelles sont les méthodes utilisées pour l’enrichissement du corpus par le laboratoire? 
La production de résumés automatiques a utilisé l’interface de Hugging face et des modèles BERT pour l’anglais et le français afin de produire automatiquement des synthèses de chaque textes. À noter que le résultat n’est pas parfait, certains résultats déficients s’expliquant notamment par la véritable impossibilité de produire un résumé pour cet ensemble continu de texte, c’est le cas par exemple des petites annonces ou un article qui liste les événements à venir dans un quartier.

## La production des matrices TF/IDF

## Qui est l’équipe qui a préparé ce corpus?
Le corpus a été produit dans le cadre d’une recherche-action menée sous le titre les Récits de la faim à Montréal par le Laboratoire d’analyse des discours et des récits collectifs du Centre de recherches interdisciplinaires en études montréalaises de l’Université McGill, dans le cadre du programme Montréal en commun.

Julien Vallières a constitué le corpus. Pascal Brissette et Lisa Teichmann ont procédé au classement supervisé des sous-corpus de langue française et anglaise. Alexia Wildhaber-Riley et Yu Chen Shi ont procédé au classement manuel préalable des textes. Elisabeth Doyon a procédé à l’enrichissement sémantique des tables diffusées.


[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
