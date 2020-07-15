## Creëer je weelderige weide

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

Klik op de groene vlag om de nieuwe grootte van je bloem te zien.

--- /task ---

--- task ---

Nu gaan we meer bloemen genereren. Er is een `bloemen`{:class="block3variables"} variabele die wordt bestuurd door de schuifregelaar. Je kunt de onderstaande blokken gebruiken om een aantal klonen van je bloem te maken:

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte [5] %
+ herhaal (bloemen)
+ maak kloon van (mezelf v)
```

--- /task ---

Als je op de groene vlag klikt, zie je waarschijnlijk niets gebeuren. Dit komt doordat alle klonen worden gemaakt op precies dezelfde plaats als de oorspronkelijke bloem.

--- task ---

Wanneer je een kloon maakt, gebruik dit blok, zodat deze kloon naar een willekeurige positie gaat:

```blocks3
wanneer ik als een kloon start
ga naar (willekeurige positie v)
```

Vergeet niet de schuifregelaar aan te passen om het gewenste aantal bloemen te wijzigen.

--- /task ---

Op dit moment verschijnen er bloemen over het hele speelveld. Dus sommige ervan zullen waarschijnlijk in de lucht hangen. Dit kan worden opgelost door ervoor te zorgen dat de `y`{:class="block3motion"} positie van de bloemen altijd lager is dan de grote rots.

--- task ---

Voeg deze blokken toe om de bloemen naar een willekeurige positie te laten bewegen, zodanig dat ze lager zijn dan `-60`{:class="block3motion"} op de `y`{:class="block3motion"}-as:

```blocks3
wanneer ik als kloon start
ga naar (willekeurige positie v)
+ herhaal tot <(y positie) < (-60)>
+ ga naar (willekeurige positie v)
```

--- /task ---

Al die bloemen zien er nu een beetje saai uit, omdat ze allemaal dezelfde grootte en dezelfde kleur hebben. Je kunt een functieblok voor willekeurige getallen gebruiken om dit op te lossen.

--- task ---

Voeg een `willekeurig getal`{:class="block3operators"} blok toe om de `kleur`{:class="block3looks"} en `grootte`{:class="block3looks"} van de bloemen te veranderen:

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

Je kunt nu met de getallen spelen om verschillende afmetingen, kleureffecten en aantallen bloemen te krijgen.

Misschien wil je ook nog een paar andere dingen toevoegen aan je weide? Wat dacht je van enkele bijen of een paar konijnen? Je kunt zelfs de achtergrond veranderen in een nachtelijke hemel en je bloemen te veranderen in sterren en planeten.





