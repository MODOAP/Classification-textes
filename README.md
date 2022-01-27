# ModOAP Classification automatique de textes

Ce script permet la classification automatique des blocs de texte d'un document Gallica, à partir d'un modèle de classification préalablement entraîné.

Les modèles entraînés doivent être importés : ils peuvent être créés via le script ModOAP - Classification automatique de textes (Entrainement)

Les blocs de texte d'un document Gallica sont contenus dans un fichier .json qui peut être créé via le script ModOAP_Telechargement_structure_blocs_texte_Gallica 

Le résultat de la classification est un fichier .json similaire au fichier initial où chaque bloc de texte qui a reçu une étiquette est annoté via l'entrée "étiquette". Le script génère également un fichier .csv permettant de visualiser les annotations sous forme de tableau.
 
Trois types de classifications possibles :

   1 Classification binaire : associer un texte à une étiquette ou 0 (une seule étiquette possible)
   2 Classification multiclass : associer un texte à une étiquette parmi un jeu d'étiquettes
   3 Classification multilabel : associer un texte à une ou plusieurs étiquettes parmi un jeu d'étiquettes

Le script implémente la bibliothèque Simple Transformers : https://simpletransformers.ai/

Ce carnet nécessite de synchroniser un compte Google Drive.

## Utilisation

1. Ouvrir le carnet dans l'interface Google Colab et se connecter à un compte Google Drive 

2. Lancer la première cellule et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

#### Pour une classification binaire :

3. Renseigner les paramètres de la seconde cellule "Classification binaire des blocs texte d'un document Gallica" :
	- Spécifier le chemin vers le dossier contenant modèle entraîné
	- Spécifier le chemin vers le fichier .json contenant les blocs de texte à classer
	- Spécifier le chemin vers un dossier sur le drive où sauvegarder les résultats (un fichier .json et un fichier .csv) 
	- Lancer la cellule

#### Pour une classification multiclass :

3. Renseigner les paramètres de la troisième cellule "Classification multiclass des blocs texte d'un document Gallica" :
	- Spécifier le chemin vers le dossier contenant modèle entraîné
	- Spécifier le chemin vers le fichier .json contenant les blocs de texte à classer
	- Spécifier le chemin vers un dossier sur le drive où sauvegarder les résultats (un fichier .json et un fichier .csv) 
	- Lancer la cellule
	
#### Pour une classification multilabel :

3. Renseigner les paramètres de la dernière cellule "Classification multilabel des blocs texte d'un document Gallica" :
	- Spécifier le chemin vers le dossier checkpoint à l'intérieur du dossier contenant modèle entraîné
	- Spécifier le chemin vers le fichier .json contenant les blocs de texte à classer
	- Spécifier le chemin vers un dossier sur le drive où sauvegarder les résultats (un fichier .json et un fichier .csv) 
	- Lancer la cellule
