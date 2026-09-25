# Projet transversal F1 — Python → Java → JavaScript

Pack complet : énoncé, données, squelettes, tests, extensions et corrigés.

```
ENONCE.md                    l'énoncé étudiant (à lire en premier)
donnees/resultats.csv        l'export brut du championnat
01-python/ingestion.ipynb    maillon 1 — On vérifie si ce qui a été rempli correspond pas au paramètre texte ou pas au paramètre texte suivi de strip qui enlève les espaces et caractères invisibles et dans ce cas là on retourne None. On sépare les minutes et les secondes avec texte.split(':'), définissons une variable pour convertir en un total de secondes avec int pour les minutes et float pour les secondes afin d'arrondir à 3 décimales suivi de round(total_secondes, 3) en return. On retourne None dans le cas d'une ValueError ou Exception.
La fonction lire_resultats lit un CSV de résultats de course en ignorant la première ligne et en s'adaptant automatiquement au séparateur. Elle extrait et nettoie les infos pour chaque pilote (en forçant la position à 0 en cas d'abandon et en convertissant le chrono). Au final, elle te renvoie toutes ces données bien rangées dans une liste de dictionnaires prête à être utilisée en Python.
La fonction ecrire_courses_propres génère un fichier CSV propre en y insérant d'abord l'en-tête. Ensuite, elle boucle sur tes données pour écrire chaque ligne avec f.write(), en utilisant les f-strings pour formater le chrono à 3 décimales.

02-java/src/                 maillon 2 — public static int pointsPourPosition vérifie si le pilote finit dans le top 10 pour aller récupérer le bon score dans le tableau BAREME, sinon elle renvoie simplement zéro.
classementPilotes utilise une HashMap pour regrouper les données en associant le nom de chaque pilote à un objet Resultat. Une boucle for cumule les points et les podiums de la saison. Les valeurs sont ensuite transférées dans une ArrayList pour être triées avec la méthode sort(). Une expression lambda sert de comparateur sur mesure pour trier par points décroissants, puis par victoires, deuxièmes places, et enfin par ordre alphabétique.
classementEcuries regroupe cette fois les scores dans la HashMap en utilisant le nom de l'écurie comme clé. Une boucle additionne les points et victoires des pilotes appartenant à la même équipe. La liste finale utilise exactement la même méthode sort() avec une expression similaire pour garantir un ordre de tri identique au classement individuel.
positionMoyenne calcule la place moyenne d'un pilote en se basant sur les résultats des courses avec une boucle for. Une condition if filtre les abandons en ignorant les valeurs de position égales à 0 pour ne garder que les courses terminées. Le calcul final exploite la méthode Math.round() (multiplié puis divisé par 100.0) afin de forcer l'arrondi du résultat à deux décimales.

03-js/                       maillon 3 — trierParPoints compare d'abord les points en ordre décroissant, puis les victoires en cas d'égalité grâce à la méthode native sort().

secours/                     résultats de référence, en cas de blocage
extensions/E1 à E4           les extensions et leurs tests
formateur/                   corrigés, grille, générateur — À RETIRER avant distribution
```

Prérequis : Python 3 avec Jupyter, un JDK (`javac -version`), un navigateur.
