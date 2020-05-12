## 創造你的療癒草地

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

The flower is a little too large, so the first thing to do is resize it. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

點擊率色旗子，來看看新的花朵尺寸。

--- /task ---

--- task ---

Now let's generate more flowers. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage, which sets the number of flowers. You can use the blocks below to create clones of your flower:

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

If you click the green flag, you'll probably not notice anything happen. 這是因為所有複製的花朵都和原本的花朵在同個位置。

--- task ---

When a clone is created, it should go to a random position:

```blocks3
when I start as a clone
go to (random position v)
```

Don't forget to adjust the slider to change the number of flowers you want.

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

你可能還想在草地上加些新的東西。 How about adding some bees or a few rabbits? You could even change the backdrop to the night sky, and add stars and planets instead of flowers.





