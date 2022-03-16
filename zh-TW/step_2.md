## Resize your flower

--- task ---

開啟入門Scratch專案透過線上版[rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){：target =“ _ blank”}或下載入門專案從[ rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

你應該會看到一片草地在森林裡, 有一朵大花在舞台的中央。 舞台上還有一個滑桿，用來控制你看到的花朵數量。

--- task ---

花有點太大，所以要做的第一件事就是調整它的大小。 在你的花朵角色上增加這些積木：

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
當分身產生
定位到 (隨機位置 v)
重複直到 <(y座標) < (-60)>
定位到 (隨機位置 v)
結束
+ 尺寸改變 (隨機取數 (-10) 到 (10)
+ 圖像效果 (顏色 v) 改變 (隨機取數 (1) 到 (100))
```

--- /task ---

You can now play around with the numbers to get different sizes, colour effects, and numbers of flowers.

You might also like to add a few more things to your meadow. How about some bees or a few rabbits? You could even change the backdrop to the night sky, and swap your flowers for stars and planets.
