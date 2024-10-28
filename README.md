                      ** Analyse des ventes de Furniture**

**Contexte du Projet**
Ce projet se concentre sur la prévision des ventes dans la catégorie *Furniture* à l’aide de techniques de modélisation de séries temporelles. En analysant les ventes mensuelles historiques, le projet vise à fournir un modèle de prévision efficace pour mieux comprendre les tendances de ventes et soutenir la planification commerciale.

_ _ Objectifs
Les objectifs principaux du projet sont les suivants :
1. Préparer et explorer les données de vente pour la catégorie "Furniture", en identifiant les tendances et les éventuelles variations saisonnières.
2. Construire un modèle SARIMA (Saisonnier Auto-Régressif Intégré avec Moyenne Mobile) pour capturer les tendances et la saisonnalité.
3. Évaluer les performances du modèle pour s'assurer qu'il est bien adapté aux données et qu'il produit des prévisions précises.
4. Utiliser les prévisions du modèle pour améliorer la prise de décision dans la gestion des stocks et la planification des ventes.

**Description des Étapes du Projet**

1. Chargement et Exploration des Données
   - Importation des Données : Les données sont extraites d’un fichier Excel et vérifiées pour s'assurer qu'elles sont prêtes pour l'analyse (types de données, valeurs manquantes, etc.).
   - Filtrage des Données : Nous nous concentrons sur la catégorie *Furniture* pour simplifier l’analyse et rendre le modèle plus spécifique.

2. Préparation et Agrégation des Données
   - Nettoyage des Données: Les doublons sont supprimés pour éviter les biais et garantir la précision des données.
   - Transformation des Dates : La colonne des dates est convertie en format `datetime`, puis les ventes sont agrégées au niveau mensuel en utilisant le premier jour de chaque mois. Cette agrégation permet de créer une série temporelle mensuelle qui met en évidence les cycles et les tendances.

3. Visualisation de la Série Temporelle
   - Un graphique des ventes mensuelles est créé pour observer les variations au fil du temps. Cette visualisation révèle des tendances saisonnières et des pics récurrents dans les ventes, utiles pour déterminer la structure de la série temporelle.

4. Analyse de la Stationnarité
   - Test de Stationnarité (Dickey-Fuller Augmenté) : Pour appliquer un modèle SARIMA, il est important que la série soit stationnaire. Le test de Dickey-Fuller confirme que la série est stationnaire, ce qui est favorable pour le modèle.

5. Modélisation avec SARIMA
   - Optimisation des Paramètres: Les paramètres du modèle (p, d, q) sont choisis en utilisant le critère d'information d'Akaike (AIC), ce qui permet de trouver la meilleure combinaison pour une performance optimale sans surajustement.
   - Validation du Modèle : Le modèle est validé avec les tests de Ljung-Box et Shapiro pour vérifier la qualité des résidus, assurant ainsi que les prédictions ne contiennent pas de biais importants.

6. Prévisions et Comparaison avec les Données de Test
   - Prédictions sur les Données de Test : Le modèle SARIMA est appliqué pour prévoir les ventes des 11 derniers mois du jeu de données. Les prévisions sont comparées aux valeurs réelles pour évaluer la précision du modèle.
   - Visualisation des Résultats: Les ventes réelles et les prévisions du modèle sont tracées pour vérifier l'ajustement du modèle aux données. Un bon alignement entre les courbes des données réelles et prédites indique que le modèle est efficace.

**Conclusion**
Ce projet illustre une approche complète pour l’analyse de séries temporelles avec les ventes de la catégorie *Furniture* en utilisant un modèle SARIMA. En identifiant les tendances et la saisonnalité, ce modèle fournit des prévisions précises, permettant d’améliorer la planification et la gestion des stocks dans le secteur de la vente. 
