## Create you mindful meadow

--- task ---

Abre el proyecto inicial de Scratch en línea en [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} o descárgalo en [rpf.io/p/es/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

Deberías ver una pradera en un bosque, con una sola flor grande en medio del escenario. También hay un control deslizante en el escenario que eventualmente controlará la cantidad de flores que ves.

--- task ---

La flor está demasiado grande, por lo que lo primero que debes hacer es cambiar su tamaño. Añade estos bloques al objeto flor.

```blocks3
when flag clicked
set size to [5] %
```

Haz clic en la bandera verde para ver el nuevo tamaño de tu flor.

--- /task ---

--- task ---

Ahora necesitamos generar más flores. Está la variable `flores`{: class = "block3variables"} que se ajusta con el control deslizante en el escenario. Te permite fijar el número de flores. Puedes usar los bloques que están a continuación para crear clones de tu flor.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Al hacer clic en la bandera verde, es probable que notes que nada sucede. Esto se debe a que todos los clones se crean en la misma posición que la flor original.

--- task ---

Cuando se crea un clon, debería ir en posición aleatoria.

```blocks3
when I start as a clone
go to (random position v)
```

Don't forget to adjust the slider, to change the number of flowers you want.

--- /task ---

At the moment, flowers will appear all over the stage, so some look like they're in the sky. This can be fixed by making sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

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

You can now play around with the numbers a little to get different sizes, color effects and numbers of flowers.

You might also like to add a few more things to your meadow. How about adding some bees or a few random rabbits. Or even change the backdrop to a nighttime sky and add stars and planets instead of flowers.





