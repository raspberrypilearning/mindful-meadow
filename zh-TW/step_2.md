## 創造你的療癒草地

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

花有點太大，所以要做的第一件事就是調整它的大小。 Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

點擊率色旗子，來看看新的花朵尺寸。

--- /task ---

--- task ---

現在我們需要產生更多的花朵。 There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. 它可以用來設置花朵數量。 你可以使用下面這些積木來複製花朵：

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

如果你點擊綠色旗子，可能什麼也不會發生。 這是因為所有複製的花朵都和原本的花朵在同個位置。

--- task ---

當花朵被複製時，都應該要到隨機位置去。

```blocks3
when I start as a clone
go to (random position v)
```

不要忘記調整滑桿來更改你想要的花朵數量。

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

增加這些積木來更改花朵的`顏色`{:class="block3looks"}和`尺寸`{:class="block3looks"}透過`隨機取數`{:class="block3operators"}積木。

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

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

你可能還想在草地上加些新的東西。 How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





