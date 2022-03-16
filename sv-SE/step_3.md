## Make more flowers

--- task ---

Now we need to generate more flowers. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the stage. It can set the number of flowers you will see. You can use the blocks below to create clones of your flower.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

If you click the green flag, you'll probably not see anything happen. This is because all the clones are created at the same position as the original flower.

--- task ---

When a clone is created, it should go to a random position, so that it might appear anywhere on the stage

```blocks3
when I start as a clone
go to (random position v)
```

--- /task ---

--- task ---

Click the green flag to see your flowers being created. Don't forget to adjust the slider, to change the number of flowers you want.

--- /task ---





