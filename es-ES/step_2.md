## Crea tu pradera relajante

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

La flor es un poquito grande, por lo que lo primero que debes hacer es cambiar su tamaño. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

Haz clic en la bandera verde para ver el nuevo tamaño de tu flor.

--- /task ---

--- task ---

Ahora necesitamos generar más flores. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. Con ella puedes fijar el número de flores. Puedes usar los bloques que están a continuación para crear clones de tu flor.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Si haces clic en la bandera verde, probablemente no verás que pase nada. Esto se debe a que todos los clones se crean en la misma posición que la flor original.

--- task ---

Cuando un clon es creado, debería ir a una posición aleatoria.

```blocks3
when I start as a clone
go to (random position v)
```

No olvides ajustar el control deslizante, para cambiar el número de flores que quieras.

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

Añade estos bloques para cambiar el `color`{:class="block3looks"} y el `tamaño`{:class="block3looks"} de las flores, usando un bloque `número al azar`{:class="block3operators"}.

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

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

También puede que te guste añadir algunas cosas más a tu pradera. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





