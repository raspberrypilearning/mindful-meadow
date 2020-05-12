## 花さく草原を作る

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

花は少し大きすぎるので、まずサイズをかえます。 Add these blocks to the flower sprite:

```blocks3
⚑ が押されたとき
大きさを [5] %にする
```

緑の旗をクリックすると、花のサイズがかわります。

--- /task ---

--- task ---

次に、もっとたくさんの花をさかせましょう。 There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. スライダーを使って花の数を決めることができます。 このブロックを使うと、花のクローンを作成 (さくせい) できます。

```blocks3
⚑ が押されたとき
大きさを [5] %にする
+ (お花の数) 回繰り返す
+ (自分自身 v) のクローンを作る
```

--- /task ---

緑の旗をクリックしても、おそらく何も起こりません。 これは、すべてのクローンが元の花と同じ位置 (いち) に作成されるためです。

--- task ---

クローンが作成されるとき、花がランダムな位置 (どこかの場所) に移動 (いどう) するようにします。

```blocks3
when I start as a clone
go to (random position v)
```

スライダーを調整して、好きな花の数にかえることをわすれないでください。

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

以下のブロックを追加して、花の`色`{:class="block3looks"}と`大きさ`{:class="block3looks"}を、`(1)から(10)までの乱数`{:class="block3operators"}ブロックを使ってかえます。

```blocks3
クローンされたとき
(どこかの場所 v)へ行く
<(y座標) < (-60)> まで繰り返す
(どこかの場所 v)へ行く
end
+ 大きさを ((-10)から(10)までの乱数) ずつ変える
+ (色 v)の効果を((1)から(100)までの乱数)ずつ変える      
```

--- /task ---

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

草原に何かを追加するのもいいでしょう。 How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





