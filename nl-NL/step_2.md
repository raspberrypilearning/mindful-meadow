## Resize your flower

--- task ---

Open het start Scratch-project online op [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} of download het startproject op [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

Je zou een weide in een bos moeten zien, met een enkele grote bloem in het midden van het speelveld. Er is ook een schuifregelaar op het speelveld, waarmee je het aantal bloemen dat je ziet kunt regelen.

--- task ---

Deze bloem is een beetje te groot, dus het eerste wat je doet is het verkleinen ervan. Voeg deze blokken toe aan de bloemsprite:

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte [5] %
```

You don't have to use this size, experiment with different `set size to`{:class="block3looks"} numbers until you have a flower size you like.

--- /task ---

--- task ---

Click the green flag to see the new size of your flower.

--- /task ---
======= Now let's generate more flowers. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage, which sets the number of flowers. You can use the blocks below to create clones of your flower:

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte [5] %
+ herhaal (bloemen)
+ maak kloon van (mezelf v)
```

--- /task ---

If you click the green flag, you'll probably not notice anything happen. This is because all the clones are created at the same position as the original flower.

--- task ---

When a clone is created, use this block to make it go to a random position:

```blocks3
wanneer ik als een kloon start
ga naar (willekeurige positie v)
```

Don't forget to adjust the slider to change the number of flowers that you want.

--- /task ---

At the moment, the flowers appear all over the Stage — some look like they're in the sky. To fix this, make sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

Add these blocks to move the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis:

```blocks3
wanneer ik als kloon start
ga naar (willekeurige positie v)
+ herhaal tot <(y positie) < (-60)>
+ ga naar (willekeurige positie v)
```

--- /task ---

The flowers look a little dull, they are all the same size and the same colour. You can use a random number generator block to fix this.

--- task ---

Add a `pick random`{:class="block3operators"} block to change the `color`{:class="block3looks"} and `size`{:class="block3looks"} of the flowers:

```blocks3
wanneer ik als kloon start
ga naar (willekeurige positie v)
herhaal tot <(y positie) < (-60)>
ga naar (willekeurige positie v)
end
+ verander grootte met (willekeurig getal tussen (-10) en (10))
+ verander (kleur v) effect met (willekeurig getal tussen (1) en (100))
```

--- /task ---

You can now play around with the numbers to get different sizes, colour effects, and numbers of flowers.

You might also like to add a few more things to your meadow. How about some bees or a few rabbits? You could even change the backdrop to the night sky, and swap your flowers for stars and planets.
