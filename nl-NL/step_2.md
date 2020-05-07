## Creëer je weelderige weide

--- task ---

Open het start Scratch-project online op [scratch.mit.edu/projects/392825864](https://scratch.mit.edu/projects/392825864){:target="_blank"} of download het startproject op [rpf.io/p/nl-NL/mindful-meadow-on](https://rpf.io/p/nl-NL/mindful-meadow-go)

--- /task ---

Je zou een weide in een bos moeten zien, met een enkele grote bloem in het midden van het speelveld. Er is ook een schuifregelaar op het podium die uiteindelijk het aantal bloemen dat je ziet, zal regelen.

--- task ---

De bloem is een beetje te groot, dus het eerste wat te doen is het verkleinen ervan. Voeg deze blokken toe aan de bloemsprite.

```blocks3
when flag clicked
set size to [5] %
```

Klik op de groene vlag om de nieuwe grootte van je bloem te zien.

--- /task ---

--- task ---

Nu moeten we meer bloemen genereren. Er is een `bloemen`{:class="block3variables"} variabele die wordt bestuurd door de schuifregelaar in het speelveld. Het kan het aantal bloemen instellen. Je kunt de onderstaande blokken gebruiken om klonen van je bloem te maken.

```blocks3
when flag clicked
set size to [5] %
+ repeat (bloemen)
+ create clone of (mijzelf v)
```

--- /task ---

Als je op de groene vlag klikt, zie je waarschijnlijk niets gebeuren. Dit komt doordat alle klonen worden gemaakt op dezelfde plaats als de oorspronkelijke bloem.

--- task ---

Wanneer een kloon wordt gemaakt, moet deze naar een willekeurige positie gaan.

```blocks3
when I start as a clone
go to (willekeurige positie v)
```

Vergeet niet de schuifregelaar aan te passen om het aantal gewenste bloemen te wijzigen.

--- /task ---

Op dit moment verschijnen er bloemen over het hele speelveld, dus sommige zien eruit alsof ze in de lucht hangen. Dit kan worden opgelost door ervoor te zorgen dat de `y`{:class="block3motion"} positie van de bloemen altijd lager dan de grote rots is.

--- task ---

Voeg deze blokken toe om de bloemen naar een willekeurige positie te laten bewegen, totdat ze lager zijn dan `-60`{:class="block3motion"} op de `y`{:class="block3motion"}-as.

```blocks3
when I start as a clone
go to (willekeurige positie v)
+ repeat until <(y-positie) < (-60)>
+ go to (willekeurige positie v)
```

--- /task ---

De bloemen zien er op dit moment een beetje saai uit, omdat ze allemaal dezelfde grootte en dezelfde kleur hebben. We kunnen echter een functieblok voor willekeurige getallen gebruiken om dit op te lossen.

--- task ---

Voeg deze blokken toe om de `kleur`{:class="block3looks"} en `grootte`{:class="block3looks"} van de bloemen te veranderen, met behulp van een `kies willekeurig`{:class="block3operators"} blok.

```blocks3
when I start as a clone
go to (willekeurige positie v)
repeat until <(y-positie) < (-60)>
go to (willekeurige positie v)
end
+ change size by (pick random (-10) to (10)
+ change (kleur v) effect by (pick random (1) to (100))
```

--- /task ---

Je kunt nu met de getallen spelen om verschillende grootten, kleureffecten en aantallen bloemen te krijgen.

Misschien wil je ook nog een paar dingen toevoegen aan je weide. Wat dacht je van het toevoegen van enkele bijen of een paar willekeurige konijnen. Of verander zelfs de achtergrond in een nachtelijke hemel en voeg sterren en planeten toe in plaats van bloemen.


***
Dit project werd vertaald door vrijwilligers:

Robert-Jan Kempenaar

Sanneke van der Meer

Dankzij vrijwilligers kunnen we mensen over de hele wereld de kans geven om in hun eigen taal te leren. Jij kunt ons helpen meer mensen te bereiken door vrijwillig te starten met vertalen - meer informatie op [rpf.io/translate](https://rpf.io/translate).


