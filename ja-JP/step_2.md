## Create you mindful meadow

--- task ---

[rpf.io/dm-meadow-start ](https://rpf.io/dm-meadow-start){:target="_blank"}から基本 (きほん) の Scratch プロジェクトを開きます。または[rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)から基本のプロジェクトをダウンロードします。

--- /task ---

森の中の草原の真ん中に大きな花が1つあります。 ステージには、表示 (ひょうじ) される花の数をあとで調整するスライダーもあります。

--- task ---

The flower is a little too large, so the first thing to do is resize it. このブロックを花のスプライトに追加 (ついか) します。

```blocks3
when flag clicked
set size to [5] %
```

緑のフラグをクリックすると、花のサイズがかわります。

--- /task ---

--- task ---

次に、もっとたくさんの花をさかせましょう。 ステージ上に、スライダーで調整できる`お花の数`{:class="block3variables"}という変数 (へんすう) があります。 花の数を決めることができます。 You can use the blocks below to create clones of your flower.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

緑の旗をクリックしても、おそらく何も起こりません。 This is because all the clones are created at the same position as the original flower.

--- task ---

When a clone is created, it should go to a random position.

```blocks3
when I start as a clone
go to (random position v)
```

Don't forget to adjust the slider, to change the number of flowers you want.

--- /task ---

At the moment, flowers will appear all over the stage, so some look like they're in the sky. This can be fixed by making sure that the `y`{:class="block3motion"} position of the flowers is always below the big rock.

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





