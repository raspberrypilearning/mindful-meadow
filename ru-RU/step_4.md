## Keeping on the grass

At the moment, flowers will appear all over the stage, so some look like they're in the sky.

This can be fixed by making sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock. The `y`{:class="block3motion"} position of a sprite is how far above or below the centre of the stage it is. A positive `y`{:class="block3motion"} larger than `0`{:class="block3motion"} is above the centre. A negative `y`{:class="block3motion"} below `0`{:class="block3motion"} is below the center.

--- task ---

Add these blocks to keep moving the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

