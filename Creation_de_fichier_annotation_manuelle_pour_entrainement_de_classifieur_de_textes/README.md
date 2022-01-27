ModOAP : Création de fichier d'annotation manuelle pour entrainement de classifieur de textes


# ModOAP Création de fichier d'annotation manuelle "prêt à annoter" pour classifieur de textes

Ce script permet de générer des fichiers CSV de paragraphes de texte prêts à annoter, à partir de blocs textes de documents Gallica téléchargés au format JSON grâce au script ModOAP_Telechargement_structure_blocs_texte_Gallica.

Ces fichiers sont destinés à être annotés manuellement pour l'entraînement de classifieurs de textes via le script ModOAP_Classification_automatique_de_textes_(Entrainement) 

Trois types de classifications possibles :

    Classification binaire : associer un texte à une étiquette ou 0 (une seule étiquette possible)
    Classification multiclass : associer un texte à une étiquette parmi un jeu d'étiquettes
    Classification multilabel : associer un texte à une ou plusieurs étiquettes parmi un jeu d'étiquettes
    

Ce carnet nécessite de synchroniser un compte Google Drive.


## Utilisation

1. Ouvrir le carnet dans l'interface Google Colab [![Open In Colab](colab.svg)](https://colab.research.google.com/github/paulbin501/t1/blob/main/t1.ipynb) et se connecter à un compte Google Drive ?????????????????????

2. Lancer la première cellule et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

#### Pour créer un fichier d'annotation manuelle pour classification binaire :

3. Dans la cellule Créer un fichier d'annotation pour classification binaire :

	- Spécifier le chemin vers un ou plusieurs docs gallica au format json sur le drive
	Les fichiers json contenant les blocs de texte des documents Gallica sont obtenus via le script ModOAP_Telechargement_structure_blocs_texte_Gallica 
	- Spécifier le nombre maximal de blocs textes à conserver
	- Spécifier le nom de l'étiquette pour l'annotation binaire
	- Spécifier le dossier où sauvegarder le fichier d'annotation
	- Spécifier un nom pour le fichier d'annotation
	- Lancer la cellule

#### Pour créer un fichier d'annotation manuelle pour classification multiclass :

3. Dans la cellule Créer un fichier d'annotation pour classification multiclass :

	- Spécifier le chemin vers un ou plusieurs docs gallica au format json sur le drive
	Les fichiers json contenant les blocs de texte des documents Gallica sont obtenus via le script ModOAP_Telechargement_structure_blocs_texte_Gallica 
	- Spécifier le nombre maximal de blocs textes à conserver
	- Spécifier le dossier où sauvegarder le fichier d'annotation
	- Spécifier un nom pour le fichier d'annotation
	- Lancer la cellule
	
#### Pour créer un fichier d'annotation manuelle pour classification multilabel :

3. Dans la cellule Créer un fichier d'annotation pour classification multilabel :

	- Spécifier le chemin vers un ou plusieurs docs gallica au format json sur le drive
	Les fichiers json contenant les blocs de texte des documents Gallica sont obtenus via le script ModOAP_Telechargement_structure_blocs_texte_Gallica 
	- Spécifier le nombre maximal de blocs textes à conserver
	- Spécifier les noms des étiquettes du jeu d'annotation, séparés par un espace
	- Spécifier le dossier où sauvegarder le fichier d'annotation
	- Spécifier un nom pour le fichier d'annotation
	- Lancer la cellule

Consulter un tutoriel sur l'utilisation générale des carnets Colab (?????????????????????????)

