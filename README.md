But du projet : Ce projet Python a été réalisé dans le cadre de la filière Biotechnologies et Chimie. Il permet de traiter automatiquement des données de laboratoires concernant l'impact d'un cocktail d'antibiotiques sur le microbiote intestinal de souris.

Description de projet : L'application analyse des fichiers CSV contenant des mesures de bactéries vivantes prélevées à différents stades de l'expérience (fécal, iléal, cécal). Elle génère des fichiers de données filtrés par type d'échantillon et des graphiques de synthèse, notamment une courbe d'évolution et deux diagrammes en violon, pour comparer les groupes traités au cocktail ("ABX") et les groupes témoin, contrôle négatif ("Placebo").

Utilisation : Le programme nécessite l'installation d'un interpréteur Python ainsi que des bibliothèques "matplotlib" et "numpy". Avant de lancer le code, placer votre fichier source à la racine du projet, au ligne 70 et 80 en remplacement de "data_real". Lancer le script. Le programme va créer automatiquement les dossiers "Input", "Output" et "Images" s'ils n'existent pas déjà.

Résultats : Sur tout les graphiques, le rouge représente le groupe ABX et le bleu le groupe Placebo. Le graphique en ligne, nommé "Fecal matter", représente l'évolution du nombre de bactéries dans la matière fécale selon le jour de traitement, le jour 0 étant le jour de lavage (arrêt du traitement). Les deux graphiques en violon, nommé respectivement "Cecal matter" et "Ileal matter", montre la quantité de bactéries dans le caecum et l'iléum respectivement, au jour 21.

Observations attendues : Sur le graphique de la matière fécale, on observe une chute de la quantité de bactéries pendant le traitement ABX, puis une augmentation à partir du jour de lavage, où le microbiote tente de se reconstituer. Sur les graphiques en violon, on s'attend à ce que le groupe ABX ait moins de bactéries que le groupe Placebo.

Limite du code : 1) Le code a été conçu pour des fichiers csv utilisant le point virgule (;) comme séparateur.
                 2) Le programme nécessite un référencement spécifique des données dans le fichier source. Si l'ordre des colonnes du fichier source changent, les calculs seront erronés (par exemple, la quantité de bactéries est attendue à l'index 8 et le type d'échantillon à l'index 2)
                 3) Le script repose sur un format d'identifiant spécifique pour trier les souris (ex: "ABX001").
