# ModOAP Classification automatique de textes (Entraînement)

Ce carnet permet d'entraîner et d'évaluer des modèles pour la classification automatique de texte.

Ces modèles sont sauvegardés sous forme de dossiers sur un google Drive, et peuvent ensuite être importés dans le script ModOAP - Classification automatique de textes.

Trois types de classifications possibles :

   1 Classification binaire : associer un texte à une étiquette ou 0 (une seule étiquette possible)
   2 Classification multiclass : associer un texte à une étiquette parmi un jeu d'étiquettes
   3 Classification multilabel : associer un texte à une ou plusieurs étiquettes parmi un jeu d'étiquettes

L'entraînement nécessite des données annotées. Pour chaque type de classification, un fichier tableau différent doit être fourni au format CSV.

Le script permet la création de fichier csv de blocs texte prêts à être annotés.
Le script implémente la bibliothèque Simple Transformers : https://simpletransformers.ai/

Ce carnet nécessite de synchroniser un compte Google Drive.


## Utilisation

1. Ouvrir le carnet dans l'interface Google Colab [![Open In Colab](colab.svg)](https://colab.research.google.com/github/paulbin501/t1/blob/main/t1.ipynb) et se connecter à un compte Google Drive ?????????????????????

2. Lancer la première cellule et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

#### Pour entraîner un modèle à la classification binaire

3. Importer sur le drive un fichier .csv d'entraînement comme expliqué dans le script

4. Dans la cellule Entraîner un modèle binaire :
	- Spécifier le chemin vers le fichier csv d'entraînement sur le drive
	- Spécifier le chemin vers un dossier sur le Drive où sauvegarder le modèle (créé si inexistant)
	- Spécifier le nombre d'époques, c'est à dire le nombre d'itérations souhaité pour l'entraînement
	- Lancer la cellule

#### Pour entraîner un modèle à la classification multiclass

3. Importer sur le drive un fichier .csv d'entraînement comme expliqué dans le script

4. Dans la cellule Entraîner un modèle multiclass :
	- Spécifier le chemin vers le fichier csv d'entraînement sur le drive
	- Spécifier le chemin vers un dossier sur le Drive où sauvegarder le modèle (créé si inexistant)
	- Spécifier le nombre d'époques, c'est à dire le nombre d'itérations souhaité pour l'entraînement
	- Lancer la cellule
	
#### Pour entraîner un modèle à la classification multilabel

3. Importer sur le drive un fichier .csv d'entraînement comme expliqué dans le script

4. Dans la cellule Entraîner un modèle multilabel :
	- Spécifier le chemin vers le fichier csv d'entraînement sur le drive
	- Spécifier le chemin vers un dossier sur le Drive où sauvegarder le modèle (créé si inexistant)
	- Spécifier le nombre d'époques, c'est à dire le nombre d'itérations souhaité pour l'entraînement
	- Lancer la cellule

Consulter un tutoriel sur l'utilisation générale des carnets Colab (?????????????????????????)

