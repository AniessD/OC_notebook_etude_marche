# Etude de marché : Développement à l'international

## Objectif du projet
Ce projet a été réalisé dans le cadre de ma formation OpenClassrooms. Il consiste à analyser le marché international de la volaille pour définir un pays ou un groupe de pays propice au développement de l'entreprise à l'export.
Les données sélectionnées pour l'analyse doivent répondre aux exigences suivantes : 
- **100** pays représentés minimum
- **60%** de la population représentée minimum
- **8** critères de sélection minimum

L'analyse a été réalisée en Python, dans 2 notebook Jupyter, en utilisant les librairies Pandas, NumPy, Scikit learn, Matplotlib et Seaborn.

## Critères sélectionnés
Les données proviennent de la FAO et de la Banque Mondiale et couvrent plusieurs thématiques réparties en **9 critères** : 
- Score de stabilité politique
- Consommation de viande de volailles (kg/personne/an)
- Taux d'exportation
- Taux de dépendance à l'importation
- Nombre d'habitants
- PIB par habitant
- Indice de performance logistique
- Distance avec la France (en km)
- Score de climat des affaires

Le dataset final après nettoyage et jointures représentent **117 pays** et **86% de la population** (en 2017).

## Méthodologie
1. Préparation et nettoyage des données
   - Extraction des données
   - Nettoyage des données
   - Analyses univariées
   - Etude des corrélations entre variables

2. Analyse en composantes principales (ACP)
   - Standardisation des données
   - Etude de l'éboulis des valeurs propores
   - Analyse du **cercle des corrélations**
   - **Projection des individus** sur les plans factoriels

3. Clustering
   - **K-means**
   - **Classification hiérarchique ascendante (CAH)**
   - Visualisation et analyse des clusters
   - Comparaison des clusters via une matrice de contingence

## Principaux résultats
L'analyse a mis en évidence 2 groupes de pays à prioriser pour l'entreprise : 
- **hubs logistiques** (Belgique, Hong-Kong, Pays-Bas) : Zones de transit commercial majeures avec des taux d'exportation et d'importation très importants
- **Marché premium à proximité** : Pays économiquement stables, proches de la France avec un taux de dépendance aux importations proche de 50%

Une stratégie commerciale différenciée est recommandée en fonction des pays ciblés.

## Compétences
- Réduire la dimension d'un jeu de données grâce à l'ACP
- Segmenter un groupe d'individus pour mieux les comprendre grâce au clustering
- Traduire des résultats statistiques en recommandations business exploitables

## Perspectives d'amélioration (retours de soutenance)
Bien que le projet ait été validé tel quel, il reste des axes d'amélioration à mettre en place pour obtenir des résultats encore plus pertinents :
- Filtrage en amont de l'ACP : Exclure les variables initiallement très décorrélées (exemple : Stabilité politique) pour éviter qu'elles parasitent les axes principaux. Elles pourraient être utilisées ensuite comme filtres supplémentaires en fin de projet.
- Viser un seuil d'inertie cumulée plus important (90%) pour garantir une restitution presque totale de l'information
- Clustering hybride : Au lieu de comparer le K-meands et la CAH, adpoter une approche mixte. Utiliser la CAH pour fixer le nombre idéal de clusters et les centroïdes, puis les utiliser comme points de départ dans le k-means.
