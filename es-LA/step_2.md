## Crea tu prado relajante

--- task ---

Abre el proyecto inicial de Scratch en línea en [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} o descárgalo en [rpf.io/p/es/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

Deberías ver un prado en un bosque, con una sola flor grande en medio del escenario. También hay un control deslizante en el escenario que eventualmente controlará la cantidad de flores que ves.

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

No olvides ajustar el control deslizante, para cambiar la cantidad de flores que quieres.

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

Añade estos bloques para cambiar el `color`{:class="block3looks"} y el `tamaño`{:class="block3looks"} de las flores, al usar un bloque `número al azar`{:class="block3operators"}.

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

También te podría gustar agregar otras cosas en tu prado. ¿Qué tal agregar algunas abejas o algunos conejos al azar?. O incluso cambiar el fondo a un cielo nocturno y agregar estrellas y planetas en lugar de flores.





