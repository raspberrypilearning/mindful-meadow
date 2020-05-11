## 創造你的療癒草地

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

點擊率色旗子，來看看新的花朵尺寸。

--- /task ---

--- task ---

現在我們需要產生更多的花朵。 `花朵`{:class="block3variables"}是由舞台上的滑桿控制的變數。 它可以用來設置花朵數量。 你可以使用下面這些積木來複製花朵：

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

這個時候，花朵將布滿整個舞台，所以有些看起來會像是在天空中漂浮著。 This can be fixed by making sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

增加這些積木讓花朵持續移動到隨機的位置，直到他們低於`-60`{:class="block3motion"}在`y`{:class="block3motion"}軸上。

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

目前看起來有點枯燥，因為花的大小還有顏色都是一樣的。 我們可以用隨機取數積木來解決這個問題。

--- task ---

增加這些積木來更改花朵的`顏色`{:class="block3looks"}和`尺寸`{:class="block3looks"}透過`隨機取數`{:class="block3operators"}積木。

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

現在你可以稍微修改一下數字來取得不同的花朵大小、顏色和數量

你可能還想在草地上加些新的東西。 加些蜜蜂或是幾隻隨機的兔子怎麼樣？ Or even change the backdrop to a nighttime sky and add stars and planets instead of flowers.





