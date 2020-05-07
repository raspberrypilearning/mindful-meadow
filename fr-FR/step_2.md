## Crée ta prairie relaxante

--- task ---

Ouvre le projet Scratch de démarrage soit en ligne à [scratch.mit.edu/projects/392825107](https://scratch.mit.edu/projects/392825107){:target="_blank"} soit télécharge le projet de démarrage à [rpf.io/p/fr/mindful-meadow-on](https://rpf.io/p/fr-FR/mindful-meadow-go)

--- /task ---

Tu devrais voir une prairie dans une forêt, avec une seule grande fleur au milieu de la scène. Il y a aussi un curseur sur la scène qui permettra éventuellement de contrôler le nombre de fleurs que tu verras.

--- task ---

La fleur est un peu trop grande, donc la première chose à faire est de la redimensionner. Ajoute ces blocs au sprite de fleur.

```blocks3
when flag clicked
set size to [5] %
```

Clique sur le drapeau vert pour voir la nouvelle taille de ta fleur.

--- /task ---

--- task ---

Nous devons maintenant générer plus de fleurs. Il y a une variable `fleurs`{:class="block3variables"} qui est contrôlée par le curseur sur la scène. Il peut définir le nombre de fleurs. Tu peux utiliser les blocs ci-dessous pour créer des clones de ta fleur.

```blocks3
when flag clicked
set size to [5] %
+ repeat (fleurs)
+ create clone of (moi-même v)
```

--- /task ---

Si tu cliques sur le drapeau vert, tu ne verras probablement rien qui se passe. C'est parce que tous les clones sont créés à la même position que la fleur d'origine.

--- task ---

Lorsqu'un clone est créé, il doit aller à une position aléatoire.

```blocks3
when I start as a clone
go to (position aléatoire v)
```

N'oublie pas d'ajuster le curseur, pour changer le nombre de fleurs que tu veux.

--- /task ---

Pour le moment, des fleurs apparaîtront sur toute la scène, certaines semblent être dans le ciel. Cela peut être corrigé en s'assurant que la position `y`{:class="block3motion"} des fleurs est toujours en dessous du grand rocher.

--- task ---

Ajoute ces blocs pour continuer à déplacer les fleurs à une position aléatoire, jusqu'à ce qu'elles soient en dessous de `-60`{:class="block3motion"} sur l'axe `y`{:class="block3motion"}.

```blocks3
when I start as a clone
go to (position aléatoire v)
+ repeat until <(ordonnée y) < (-60)>
+ go to (position aléatoire v)
```

--- /task ---

Les fleurs ont l'air un peu monotones, car elles sont toutes de la même taille et de la même couleur. Nous pouvons cependant utiliser un bloc générateur de nombres aléatoires pour résoudre ce problème.

--- task ---

Ajoute ces blocs pour changer la `couleur`{:class="block3looks"} et la `taille`{:class="block3looks"} des fleurs, en utilisant un bloc `nombre aléatoire`{:class="block3operators"}.

```blocks3
when I start as a clone
go to (position aléatoire v)
repeat until <(ordonnée y) < (-60)>
go to (position aléatoire v)
end
+ change size by (pick random (-10) to (10)
+ change (couleur v) effect by (pick random (1) to (100))
```

--- /task ---

Tu peux maintenant jouer un peu avec les chiffres pour obtenir des tailles différentes, des effets de couleurs et des nombres de fleurs.

Tu peux aussi ajouter quelques choses en plus à ta prairie. Que dirais-tu d'ajouter quelques abeilles ou quelques lapins aléatoires. Ou bien change même l'arrière-plan en un ciel nocturne et ajoute des étoiles et des planètes au lieu de fleurs.



***
Ce projet a été traduit par des bénévoles:

Michel Arnols

Jonathan Vannieuwkerke

Grâce aux bénévoles, nous pouvons donner aux gens du monde entier la chance d'apprendre dans leur propre langue. Vous pouvez nous aider à atteindre plus de personnes en vous portant volontaire pour la traduction - plus d'informations sur [rpf.io/translate](https://rpf.io/translate).

