But du projet : Ce projet Python a été réalisé dans le cadre de la filière Biotechnologies et Chimie. Il permet de traiter automatiquement des données de laboratoires concernant l'impact d'un cocktail d'antibiotiques sur le microbiote intestinal de souris.

Description de projet : L'application analyse des fichiers CSV contenant des mesures de bactéries vivantes prélevées à différents stades de l'expérience (fécal, iléal, cécal). Elle génère des fichiers de données filtrés par type d'échantillon et des graphiques de synthèse, notamment une courbe d'évolution et deux diagrammes en violon, pour comparer les groupes traités au cocktail ("ABX") et les groupes témoin, contrôle négatif ("Placebo").

Instructions pour lancer le code:
  - Créer un dossier pour pouvoir placer le fichier de code ainsi que le fichier à analyser (cela vous permettra de retrouver plus facilement les résultats)
  - Placer à l'intérieur de ce dossier le fichier csv à analyser
  - Placer le fichier de code à l'intérieur du dossier
  - Pour ouvrir le fichier de code il vous faut un environnement de développement tel que "Spyder"
  - Ce code fonctionne pour le fichier csv "data_real.csv" si vous voulez analyser un autre fichier il faudra changer les lignes de codes:
	    - ligne 70: changer 'data_real.csv' par le fichier voulu => file_to_copy = 'fichier_voulu'
	    - ligne 80: changer 'data_real.csv' par le fichier voulu => path_in = "Input\'fichier_voulu'.csv"
  - Différents dossiers seront crées, s'ils n'existent pas déjà, où vous pourrez retrouver les données générées:
	    - Dossier input: contient une copie du fichier csv à analyser
    	- Dossier output: contient les trois fichiers csv générés par le programme (données fécale, caecal et iléal)
	    - Dossier image: contient les 3 graphiques générés

Résultats : Sur tout les graphiques, le rouge représente le groupe ABX et le bleu le groupe Placebo. Le graphique en ligne, nommé "Fecal matter", représente l'évolution du nombre de bactéries dans la matière fécale selon le jour de traitement, le jour 0 étant le jour de lavage (arrêt du traitement). Les deux graphiques en violon, nommé respectivement "Cecal matter" et "Ileal matter", montre la quantité de bactéries dans le caecum et l'iléum respectivement, au jour 21.

Observations attendues : Sur le graphique de la matière fécale, on observe une chute de la quantité de bactéries pendant le traitement ABX, puis une augmentation à partir du jour de lavage, où le microbiote tente de se reconstituer. Sur les graphiques en violon, on s'attend à ce que le groupe ABX ait moins de bactéries que le groupe Placebo.

Limite du code :
-Le code a été conçu pour des fichiers csv utilisant le point virgule (;) comme séparateur.
-Le programme nécessite un référencement spécifique des données dans le fichier source. Si l'ordre des colonnes du fichier source changent, les calculs seront erronés (par exemple, la quantité de bactéries est attendue à l'index 8 et le type d'échantillon à l'index 2)
-Le script repose sur un format d'identifiant spécifique pour trier les souris (ex: "ABX001").

