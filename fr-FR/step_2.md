## Crée ta prairie relaxante

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

La fleur est un peu trop grande, donc la première chose à faire est de la redimensionner. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

Clique sur le drapeau vert pour voir la nouvelle taille de ta fleur.

--- /task ---

--- task ---

Nous devons maintenant générer plus de fleurs. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. Il peut définir le nombre de fleurs. Tu peux utiliser les blocs ci-dessous pour créer des clones de ta fleur.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Si tu cliques sur le drapeau vert, tu ne verras probablement rien qui se passe. C'est parce que tous les clones sont créés à la même position que la fleur d'origine.

--- task ---

Lorsqu'un clone est créé, il doit aller à une position aléatoire.

```blocks3
when I start as a clone
go to (random position v)
```

N'oublie pas d'ajuster le curseur, pour changer le nombre de fleurs que tu veux.

--- /task ---

At the moment, flowers will appear all over the Stage, so some look like they're in the sky. To fix this, make sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

Add these blocks to move the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

The flowers look a little dull, they are all the same size and the same colour. You can use a random number generator block to fix this.

--- task ---

Ajoute ces blocs pour changer la `couleur`{:class="block3looks"} et la `taille`{:class="block3looks"} des fleurs, en utilisant un bloc `nombre aléatoire`{:class="block3operators"}.

```blocks3
when I start as a clone
go to (random position v)
repeat until <(y position) < (-60)>
go to (random position v)
end
+ change size by (pick random (-10) to (10)
+ change (color v) effect by (pick random (1) to (100))
```

--- /task ---

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

Tu peux aussi ajouter quelques choses en plus à ta prairie. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





