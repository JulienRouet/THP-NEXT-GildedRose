# Projets : Gilded Rose 
  
## 1. Introduction

    Bonjour à toi, et bienvenue pour ce célèbre exercice des Gilded Rose.
    Dans les 2 prochains jours tu vas apprendre à déchiffrer du code absolument horrible et tu vas également écrire tes premiers tests unitaires !

    Pour ceci tu vas reprendre l'exercice de Gilded Roses, notamment la partie JavaScript - Jasmine

## 2. Les règles

    Spécification de la Rose dorée (Gilded Rose)
    Bonjour et bienvenue dans l'équipe de la Rose dorée.

    Comme vous le savez, notre petite taverne située à proximité d'une cité importante est dirigée par l'amicale aubergiste Allison.

    Nous achetons et vendons uniquement les meilleurs produits.
    Malheureusement, la qualité de nos marchandises se dégrade constamment à l'approche de leur date de péremption.

    Un système a été mis en place pour mettre à jour notre inventaire.
    Il a été développé par Leeroy, une personne pleine de bon sens qui est partie pour de nouvelles aventures.

    Votre mission est d'ajouter une nouvelle fonctionnalité à notre système pour que nous puissions commencer à vendre un nouveau type de produit.

    Mais d'abord, laissez-moi vous présenter notre système :

    Tous les éléments ont une valeur sellIn qui désigne le nombre de jours restant pour vendre l'article.
    Tous les articles ont une valeur quality qui dénote combien l'article est précieux.
    A la fin de chaque journée, notre système diminue ces deux valeurs pour chaque produit.
    Plutôt simple, non ?

    Attendez, ça devient intéressant :

    Une fois que la date de péremption est passée, la qualité se dégrade deux fois plus rapidement.
    La qualité (quality) d'un produit ne peut jamais être négative.
    "Aged Brie" augmente sa qualité (quality) plus le temps passe.
    La qualité d'un produit n'est jamais de plus de 50.
    "Sulfuras", étant un objet légendaire, n'a pas de date de péremption et ne perd jamais en qualité (quality)
    "Backstage passes", comme le "Aged Brie", augmente sa qualité (quality) plus le temps passe (sellIn) ; La qualité augmente de 2 quand il reste 10 jours ou moins et de 3 quand il reste 5 jours ou moins, mais la qualité tombe à 0 après le concert.
    Nous avons récemment signé un partenariat avec un fournisseur de produit invoqué ("Conjured").
    Cela nécessite une mise à jour de notre système :

    les éléments "Conjured" voient leur qualité se dégrader deux fois plus vite que les objets normaux.
    "Conjured" est un préfixe au nom des éléments cela signifie que tu dois identifier quels éléments en sont (exemple: "Conjured Dark Blade", "Conjured Magic Stick")

## 3. Travail attendu

    Comme tu peux le voir, la fonction updateQuality est presque incompréhensible, on a donc également besoin de toi (en plus de rajouter les éléments "Conjured") pour rendre tout ce code plus joli !
    Tu peux faire les changements que tu veux à la classe Shop et ajouter autant de code que tu veux, tant que tout fonctionne correctement.
    Cependant, nous devons te prévenir, tu ne dois modifier en aucun cas la classe Item ou ses propriétés car cette classe appartient au gobelin maléfique et il rentrera dans une rage instantanée et te tuera sans délai : il ne croit pas dans le partage du code.
    (Tu peux ajouter une méthode updateQuality et des propriétés statiques dans la classe Item si tu veux, nous te couvrirons).
    Penses à bien utiliser les nouveautés ES6 que tu as appris au début de la formation.

    Juste une précision, un produit ne peut jamais voir sa qualité augmenter au-dessus de 50, cependant "Sulfuras" est un objet légendaire et comme tel sa qualité est de 80 et il ne change jamais.

## 4. Les tests

    Tu as pu remarquer qu'un dossier spec était disponible, à quoi peut-il bien servir ?
    À l'intérieur, tu trouveras un fichier JS dans lequel il y a quelques tests qui permettront de tester si ton programme réponds aux attentes des différentes règles :

    Un test pour voir qualité baisse bien de 1
    Un test pour voir si la qualité augmente bien de 1 pour les items dont c'est le cas
    Mais comme tu peux le constater, il y a bien d'autres règles à tester, ce sera à toi d'écrire les tests supplémentaires ! Nous avons compté 9 règles qu'il faut tester (incluant les 2 tests déjà écrits). Nous vous donnons 2 règles supplémentaires à tester, à toi de trouver les restantes :

    Tester si la qualité augmente par 3 quand il reste 5 jours ou moins (Aged Brie et Backstage passes)
    Tester si la qualité de Sulfuras ne se modifie pas
    Essayes de reprendre le modèle des 2 tests déjà écrits en modifiant seulement les items que tu ajoutes et les valeurs du tableau expected. Il est préférable d'ajouter plusieurs items pour chaque test afin d'être plus fiable.

    Pour lancer la batterie de test, fais un npm install à la racine du dossier pour installer les différentes dépendances, puis lance le script npm test.
    N'hésite surtout pas à rajouter d'autres tests si l'envie t'en prend !

## 5. Conclusion

    Nous espérons que tu as pu aider la Guilde Dorée et notre aubergiste Allison comme il se doit ! Nous avions vraiment besoin de toi...
    Et nous espérons également que tu as pu comprendre l'utilité des tests unitaires !