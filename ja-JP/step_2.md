## 花さく草原を作る

--- task ---

[scratch.mit.edu/projects/393998197](https://scratch.mit.edu/projects/393998197){:target="_blank"}から基本 (きほん) の Scratch プロジェクトを開きます。または[rpf.io/p/ja-JP/mindful-meadow-on](https://rpf.io/p/ja-JP/mindful-meadow-go)から基本のプロジェクトをダウンロードします。

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
+ repeat (お花の数)
+ create clone of (myself v)
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

今のところ花がステージ全体にさくので、空にうかんでいるように見えるものもあります。 この問題は花の`y`{:class="block3motion"}の位置を常に大きな岩より低くすることで、かいけつできます。

--- task ---

このブロックを追加すると、花の位置が`y`{:class="block3motion"}軸 (じく) 上で`-60`{:class="block3motion"}より下になるまで、ランダムな位置に移動しつづけます 。

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

花はすべて同じサイズかつ同じ色なので、今は少しつまらなく見えます。 でも乱数 (らんすう) 発生ブロックを使えば、もっと楽しくなります。

--- task ---

以下のブロックを追加して、花の`色`{:class="block3looks"}と`大きさ`{:class="block3looks"}を、`(1)から(10)までの乱数`{:class="block3operators"}ブロックを使ってかえます。

```blocks3
when I start as a clone
go to (random position v)
repeat until <(y position) < (-60)>
go to (random position v)
+ change size by (pick random (-10) to (10)
+ change (color v) effect by (pick random (1) to (100))     
```

--- /task ---

これで少し数字をいじくって、花の大きさや色、数をかえられるようになりました。

草原に何かを追加するのもいいでしょう。 ミツバチやたまに出てくるウサギなどはどうでしょうか？ 背景 (はいけい) を夜空にかえて、花のかわりに星や惑星 (わくせい) を追加するのもいいですね。

***

このプロジェクトは以下のボランティアによって翻訳されました。

大野 雅利
松原慧子

ボランティアのおかげで、世界中の人々に母国語で学ぶ機会を与えることができます。翻訳を引き受けていただくことで、より多くの人々に手を差し伸べることができます。詳しくは [rpf.io/translate](https://rpf.io/translate) をご覧ください。





