## Create you mindful meadow

--- task ---

[rpf.io/dm-meadow-start ](https://rpf.io/dm-meadow-start){:target="_blank"}から基本 (きほん) の Scratch プロジェクトを開きます。または[rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)から基本のプロジェクトをダウンロードします。

--- /task ---

森の中の草原の真ん中に大きな花が1つあります。 ステージには、表示 (ひょうじ) される花の数をあとで調整するスライダーもあります。

--- task ---

花は少し大きすぎるので、まずサイズをかえます。 このブロックを花のスプライトに追加 (ついか) します。

```blocks3
when flag clicked
set size to [5] %
```

緑の旗をクリックすると、花のサイズがかわります。

--- /task ---

--- task ---

次に、もっとたくさんの花をさかせましょう。 ステージ上に、スライダーで調整できる`お花の数`{:class="block3variables"}という変数 (へんすう) があります。 スライダーを使って花の数を決めることができます。 このブロックを使うと、花のクローンを作成 (さくせい) できます。

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

緑の旗をクリックしても、おそらく何も起こりません。 これは、すべてのクローンが元の花と同じ位置 (いち) に作成されるためです。

--- task ---

クローンが作成されるとき、花がランダムな位置に移動 (いどう) するようにします。

```blocks3
when I start as a clone
go to (random position v)
```

スライダーを調整して、好きな花の数にかえることをわすれないでください。

--- /task ---

今のところ花がステージ全体にさくので、空にうかんでいるように見えるものもあります。 This can be fixed by making sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

--- task ---

Add these blocks to keep moving the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

The flowers look a little dull currently, as they are all the same size and the same colour. We can use a random number generator block to fix this though.

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

You can now play around with the numbers a little to get different sizes, color effects and numbers of flowers.

You might also like to add a few more things to your meadow. How about adding some bees or a few random rabbits. Or even change the backdrop to a nighttime sky and add stars and planets instead of flowers.





