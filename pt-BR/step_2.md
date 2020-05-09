## Create you mindful meadow

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starer project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the stage. There's also a slider on the stage that will eventually control the number of flowers you see.

--- task ---

The flower is a little too large, so the first thing to do is resize it. Add these blocks to the flower sprite.

```blocks3
when flag clicked
set size to [5] %
```

Click the green flag to see the new size of your flower.

--- /task ---

--- task ---

Agora precisamos criar mais flores. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the stage. It can set the number of flowers. You can use the blocks below to create clones of your flower.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Se você clicar na bandeira verde, provavelmente você não verá nada acontecer. Isso porque todos os clones são criados na mesma posição que a flor original.

--- task ---

Quando um clone é criado, ele deve ir para uma posição aleatória.

```blocks3
when I start as a clone
go to (random position v)
```

Don't forget to adjust the slider, to change the number of flowers you want.

--- /task ---

No momento, as flores aparecerão ao longo do palco, então algumas parecem estar no céu. This can be fixed by making sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

Add these blocks to keep moving the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

The flowers look a little dull currently, as they are all the same size and the same colour. We can use a random number generator block to fix this though.

--- task ---

Add these blocks to change the `color`{:class="block3looks"} and `size`{:class="block3looks"} of the flowers, using a `pick random`{:class="block3operators"} block.

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

Agora você pode brincar um pouco com os números para obter diferentes tamanhos, efeitos de cor e números de flores.

Você também pode adicionar mais algumas coisas ao seu campo. How about adding some bees or a few random rabbits. Or even change the backdrop to a nighttime sky and add stars and planets instead of flowers.





