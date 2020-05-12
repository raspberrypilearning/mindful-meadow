## Creëer je weelderige weide

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

De bloem is een beetje te groot, dus het eerste wat te doen is het verkleinen ervan. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

Klik op de groene vlag om de nieuwe grootte van je bloem te zien.

--- /task ---

--- task ---

Nu moeten we meer bloemen genereren. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. Het kan het aantal bloemen instellen. Je kunt de onderstaande blokken gebruiken om klonen van je bloem te maken.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Als je op de groene vlag klikt, zie je waarschijnlijk niets gebeuren. Dit komt doordat alle klonen worden gemaakt op dezelfde plaats als de oorspronkelijke bloem.

--- task ---

Wanneer een kloon wordt gemaakt, moet deze naar een willekeurige positie gaan.

```blocks3
when I start as a clone
go to (random position v)
```

Vergeet niet de schuifregelaar aan te passen om het aantal gewenste bloemen te wijzigen.

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

Voeg deze blokken toe om de `kleur`{:class="block3looks"} en `grootte`{:class="block3looks"} van de bloemen te veranderen, met behulp van een `kies willekeurig`{:class="block3operators"} blok.

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

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

Misschien wil je ook nog een paar dingen toevoegen aan je weide. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





