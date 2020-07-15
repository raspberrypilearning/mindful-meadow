## Stwórz swoją łąkę

--- task ---

Otwórz projekt startowy projekt Scratch online na [ rpf.io/dm-meadow-start ](https://rpf.io/dm-meadow-start) {: target = "_ blank"} lub pobierz projekt starowy na [ rpf.io/p/en/mindful-meadow-on ](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

Powinieneś zobaczyć łąkę w lesie, z jednym dużym kwiatkiem na środku sceny. Na scenie jest też suwak, który będzie kontrolował liczbę kwiatów, którą widzisz.

--- task ---

Kwiat jest trochę za duży, więc pierwszą rzeczą do zrobienia jest zmiana jego rozmiaru. Dodaj poniższy kod do duszka kwiatu:

```blocks3
when flag clicked
set size to [5] %
```

Kliknij zieloną flagę, aby zobaczyć nowy rozmiar kwiatu.

--- /task ---

--- task ---

Teraz musimy wygenerować więcej kwiatów. Zmienna `kwiaty`{:class="block3variables"} jest kontrolowana przez suwak na scenie. Możesz użyć poniższych bloków, aby utworzyć klony kwiatu:

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Jeśli klikniesz zieloną flagę, prawdopodobnie nic się nie stanie. Jest tak, ponieważ wszystkie klony są tworzone w tym samym miejscu, co oryginalny kwiat.

--- task ---

Po utworzeniu klonu, użyj tego bloku, aby przejść do losowej pozycji:

```blocks3
when I start as a clone
go to (random position v)
```

Nie zapomnij ustawić suwaka, aby zmienić liczbę kwiatów, jaką chcesz.

--- /task ---

W tym momencie, kwiaty pojawiają się na całej scenie -  niekóre wyglądają jakby były na niebie. Można to naprawić, upewniając się, że pozycja `y`{:class="block3motion"} kwiatów jest zawsze poniżej wielkiej skały.

--- task ---

Dodaj te bloki, aby przesuwać kwiaty do losowej pozycji, dopóki nie znajdą się one poniżej `-60`{:class="block3motion"} na osi  `y`{:class=„block3motion”}:

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

Kwiaty wyglądają obecnie nieco nudnie, ponieważ wszystkie mają ten sam rozmiar i ten sam kolor. Możemy jednak użyć bloku generatora liczb losowych, aby to naprawić.

--- task ---

Dodaj blok `losuj liczbę`{:class="block3operators"}, aby zmienić `color`{:class="block3looks"} i `rozmiar`{:class="block3looks"} kwiatów:

```blocks3
Gdy zaczynam jako klon
idź do (losowa pozycja v)
powtarzaj aż <(pozycja y ) < (-60)>
idź do (losowa pozycja v)
koniec
+ zmień rozmiar o (losuj liczbę od (-10) do (10))
+ zmień efekt (kolor v) o (losuj liczbę od (1) do (100))
```

--- /task ---

Możesz teraz pobawić się liczbami, aby uzyskać różne rozmiary, efekty kolorystyczne i liczbę kwiatów.

Możesz także dodać kilka dodatkowych rzeczy do swojej łąki. Co powiesz na kilka pszczół lub kilka królików? Możesz nawet zmienić tło na nocne niebo i zamienić kwiaty na gwiazdy i planety.





