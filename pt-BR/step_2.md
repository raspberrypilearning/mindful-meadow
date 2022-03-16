## Resize your flower

--- task ---

Abra o projeto inicial do Scratch on-line em [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} ou faça o download do projeto inicial em [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

Você deve ver um campo em uma floresta, com uma única flor grande no meio do palco. Há também um controle deslizante no palco que controlará o número de flores que você vê.

--- task ---

A flor é um pouco grande demais, então a primeira coisa a fazer é redimensioná-la. Adicione este código ao seu ator:

```blocks3
quando a bandeira for clicada
mude o tamanho para [pontuação v] %
```

You don't have to use this size, experiment with different `set size to`{:class="block3looks"} numbers until you have a flower size you like.

--- /task ---

--- task ---

Click the green flag to see the new size of your flower.

--- /task ---
======= Now let's generate more flowers. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage, which sets the number of flowers. You can use the blocks below to create clones of your flower:

```blocks3
quando a bandeira for clicada
definir tamanho para [5] %
+ repetir (flores)
+ criar clone de (eu mesmo v)
```

--- /task ---

If you click the green flag, you'll probably not notice anything happen. This is because all the clones are created at the same position as the original flower.

--- task ---

When a clone is created, use this block to make it go to a random position:

```blocks3
quando eu começar como um clone
vá para (posição aleatória v)
```

Don't forget to adjust the slider to change the number of flowers that you want.

--- /task ---

At the moment, the flowers appear all over the Stage — some look like they're in the sky. To fix this, make sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

Add these blocks to move the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis:

```blocks3
quando eu começar como um clone
vá para (posição aleatória v)
+ repita até <(posição y) < (-60)>
+ vá para (posição aleatória v)
```

--- /task ---

The flowers look a little dull, they are all the same size and the same colour. You can use a random number generator block to fix this.

--- task ---

Add a `pick random`{:class="block3operators"} block to change the `color`{:class="block3looks"} and `size`{:class="block3looks"} of the flowers:

```blocks3
quando eu começar como um clone
vá para (posição aleatória v)
repita até que <(posição y) < (-60)>
vá para (posição aleatória v)
fim
+ mude (número aleatório entre (-10) e (10)) no tamanho
+ mude (número aleatório entre (1) e (100)) ao efeito [cor v]
```

--- /task ---

You can now play around with the numbers to get different sizes, colour effects, and numbers of flowers.

You might also like to add a few more things to your meadow. How about some bees or a few rabbits? You could even change the backdrop to the night sky, and swap your flowers for stars and planets.
