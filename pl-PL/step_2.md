## Resize your flower

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

You don't have to use this size, experiment with different `set size to`{:class="block3looks"} numbers until you have a flower size you like.

--- /task ---

--- task ---

Click the green flag to see the new size of your flower.

--- /task ---
======= Now let's generate more flowers. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage, which sets the number of flowers. You can use the blocks below to create clones of your flower:

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

If you click the green flag, you'll probably not notice anything happen. This is because all the clones are created at the same position as the original flower.

--- task ---

When a clone is created, use this block to make it go to a random position:

```blocks3
when I start as a clone
go to (random position v)
```

Don't forget to adjust the slider to change the number of flowers that you want.

--- /task ---

At the moment, the flowers appear all over the Stage — some look like they're in the sky. To fix this, make sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

Add these blocks to move the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis:

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

The flowers look a little dull, they are all the same size and the same colour. You can use a random number generator block to fix this.

--- task ---

Add a `pick random`{:class="block3operators"} block to change the `color`{:class="block3looks"} and `size`{:class="block3looks"} of the flowers:

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

You can now play around with the numbers to get different sizes, colour effects, and numbers of flowers.

You might also like to add a few more things to your meadow. How about some bees or a few rabbits? You could even change the backdrop to the night sky, and swap your flowers for stars and planets.
