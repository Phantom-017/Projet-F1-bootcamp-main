# Projet transversal F1 — Python → Java → JavaScript

Pack complet : énoncé, données, squelettes, tests, extensions et corrigés.

```
ENONCE.md                    l'énoncé étudiant (à lire en premier)
donnees/resultats.csv        l'export brut du championnat
01-python/ingestion.ipynb    maillon 1 — On vérifie si ce qui a été rempli correspond pas au paramètre texte ou pas au paramètre texte suivi de strip qui enlève les espaces et caractères invisibles et dans ce cas là on retourne None. On sépare les minutes et les secondes avec texte.split(':'), définissons une variable pour convertir en un total de secondes avec int pour les minutes et float pour les secondes afin d'arrondir à 3 décimales suivi de round(total_secondes, 3) en return. On retourne None dans le cas d'une ValueError ou Exception.
La fonction lire_resultats lit un CSV de résultats de course en ignorant la première ligne et en s'adaptant automatiquement au séparateur. Elle extrait et nettoie les infos pour chaque pilote (en forçant la position à 0 en cas d'abandon et en convertissant le chrono). Au final, elle te renvoie toutes ces données bien rangées dans une liste de dictionnaires prête à être utilisée en Python.
La fonction ecrire_courses_propres génère un fichier CSV propre en y insérant d'abord l'en-tête. Ensuite, elle boucle sur tes données pour écrire chaque ligne avec f.write(), en utilisant les f-strings pour formater le chrono à 3 décimales.

02-java/src/                 maillon 2 — public static int pointsPourPosition vérifie si le pilote finit dans le top 10 pour aller récupérer le bon score dans le tableau BAREME, sinon elle renvoie simplement zéro.

03-js/                       maillon 3 — app.js à compléter, index.html à ouvrir
secours/                     résultats de référence, en cas de blocage
extensions/E1 à E4           les extensions et leurs tests
formateur/                   corrigés, grille, générateur — À RETIRER avant distribution
```

Prérequis : Python 3 avec Jupyter, un JDK (`javac -version`), un navigateur.
