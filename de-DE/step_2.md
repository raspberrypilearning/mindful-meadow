## Erstelle deine Blumenwiese

--- task ---

Öffne das Scratch Starter-Projekt entweder online unter [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} oder lade das Starter-Projekt unter [rpf.io/p/de/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go) herunter.

--- /task ---

Du solltest eine Wiese im Wald sehen, mit einer einzigen großen Blume in der Mitte der Bühne. Es gibt auch einen Schieberegler auf der Bühne, der später die Anzahl der Blumen steuert, die du sehen wirst.

--- task ---

Die Blume ist etwas zu groß, daher muss zunächst die Größe geändert werden. Füge diesen Code zum Blumen-Sprite hinzu.

```blocks3
when flag clicked
set size to [5] %
```

Klicke auf die grüne Flagge, um die neue Größe deiner Blume zu sehen.

--- /task ---

--- task ---

Jetzt müssen wir mehr Blumen generieren. Es gibt eine `Blumen`{:class="block3variables"} Variable, die vom Schieberegler auf der Bühne gesteuert wird. Sie bestimmt die Anzahl der Blumen. Mit den folgenden Blöcken kannst du Klone deiner Blume erstellen.

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

Im Moment erscheinen Blumen auf der ganzen Bühne, so dass einige so aussehen, als wären sie im Himmel. Dies kann behoben werden, indem sichergestellt wird, dass die `y`{:class="block3motion"} Position der Blumen immer unterhalb des großen Felsen liegt.

--- task ---

Füge diese Blöcke hinzu, um die Blumen weiter an eine zufällige Position zu bewegen, bis sie unter `-60`{:class="block3motion"} auf der `y`{:class="block3motion"} Achse liegt.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

Die Blumen sehen im Moment etwas langweilig aus, da sie alle die gleiche Größe und Farbe haben. Wir können jedoch einen Generatorblock für Zufallszahlen verwenden, um dies zu beheben.

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

Du kannst jetzt ein wenig mit den Zahlen herumspielen, um verschiedene Größen, Farbeffekte und Blumenzahlen zu erhalten.

Vielleicht möchtest du deiner Wiese noch ein paar Dinge mehr hinzufügen. Wie wäre es, Bienen oder ein paar zufällige Kaninchen hinzuzufügen? Oder ändere den Hintergrund in einen Nachthimmel und füge Sterne und Planeten anstelle von Blumen hinzu.





