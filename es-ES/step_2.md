## Crea tu pradera relajante

--- task ---

Abre el proyecto inicial de Scratch en línea en [scratch.mit.edu/projects/394000692](https://scratch.mit.edu/projects/394000692){:target="_blank"} o descárgalo en [rpf.io/p/es-ES/mindful-meadow-on](https://rpf.io/p/es-ES/mindful-meadow-go)

--- /task ---

Deberías ver una pradera en un bosque, con una sola flor grande en medio del escenario. También hay un deslizador en el escenario que eventualmente controlará el número de flores que ves.

--- task ---

La flor es un poquito grande, por lo que lo primero que debes hacer es cambiar su tamaño. Añade estos bloques al objeto flor.

```blocks3
when flag clicked
set size to [5] %
```

Haz clic en la bandera verde para ver el nuevo tamaño de tu flor.

--- /task ---

--- task ---

Ahora necesitamos generar más flores. Hay una variable ` flores ` {: class = "block3variables"} controlada por el control deslizante en el escenario. Con ella puedes fijar el número de flores. Puedes usar los bloques que están a continuación para crear clones de tu flor.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flores)
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

Por el momento, las flores aparecerán por todo el escenario, así que algunas parecen estar en el cielo. Esto se puede arreglar asegurando que la posición `y`{:class="block3motion"} de las flores esté siempre debajo de la roca grande.

--- task ---

Añade estos bloques para seguir moviendo las flores a una posición aleatoria, hasta que estén por debajo de `-60`{:class="block3motion"} en el eje `y`{:class="block3motion"}.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

Las flores por ahora se ven un poco aburridas, ya que todas son del mismo tamaño y color. Sin embargo, podemos usar un bloque generador de números aleatorios para arreglar esto.

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

Ahora puedes jugar un poco con los números para obtener diferentes tamaños, efectos de color y número de flores.

También puede que te guste añadir algunas cosas más a tu pradera. Qué tal añadir algunas abejas o algunos conejos aleatorios. O incluso cambiar el fondo a un cielo nocturno y añadir estrellas y planetas en lugar de flores.

***

Este proyecto fue traducido por voluntarios:

Chema Honrado
Laura Lurati

Gracias a los voluntarios, podemos dar a las personas de todo el mundo la oportunidad de aprender en su propio idioma. Puede ayudarnos a llegar a más personas ofreciéndose como voluntario para traducir; más información en [rpf.io/translate](https://rpf.io/translate).





