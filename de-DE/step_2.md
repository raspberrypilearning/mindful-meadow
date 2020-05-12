## Erstelle deine Blumenwiese

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

Die Blume ist etwas zu groß, daher muss zunächst die Größe geändert werden. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

Klicke auf die grüne Flagge, um die neue Größe deiner Blume zu sehen.

--- /task ---

--- task ---

Jetzt müssen wir mehr Blumen generieren. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. Sie bestimmt die Anzahl der Blumen. Mit den folgenden Blöcken kannst du Klone deiner Blume erstellen.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Wenn du auf die grüne Flagge klickst, wird wahrscheinlich nichts passieren. Das liegt daran, dass alle Klone an der gleichen Stelle wie die Originalblume erstellt werden.

--- task ---

Wenn ein Klon erstellt wird, sollte dies an einer zufällige Position erfolgen.

```blocks3
when I start as a clone
go to (random position v)
```

Vergiss nicht, den Schieberegler auf die von dir gewünschte Blumenanzahl einzustellen.

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

Füge diese Blöcke hinzu, um die `Farbe`{:class="block3looks"} und `Größe`{:class="block3looks"} der Blumen zu ändern, indem du einen `Zufallszahl von bis`{:class="block3operators"} Block benutzt.

```blocks3
Wenn ich als Klon entstehe
gehe zu (Zufallsposition v)
wiederhole bis <(y-Position) < (-60)>
gehe zu (Zufallsposition v)
end
+ ändere Größe um (Zufallszahl von (-10) bis (10)
+ ändere Effekt (Farbe v) um (Zufallszahl von (1) bis (100))
```

--- /task ---

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

Vielleicht möchtest du deiner Wiese noch ein paar Dinge mehr hinzufügen. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





