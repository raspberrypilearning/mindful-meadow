## Colour and size

The flowers look a little dull currently, as they are all the same size and the same colour. We can use a random number generator block to fix this though.

The `pick random`{:class="block3operators"} block in Scratch will choose random numbers, so you can use this to change the size and colour of the sprites.

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

--- task ---

Try experimenting with the ranges in the `pick random`{:class="block3operators"} block, until you are happy with the results

--- /task ---


You can now play around with the numbers a little to get different sizes, color effects and numbers of flowers.






