## 나만의 초원을 만들어요

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

초록색 깃발을 클릭하여 꽃의 바뀐 크기를 보세요.

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

If you click the green flag, you'll probably not notice anything happen. 복제본들이 기존 꽃 위에 겹쳐져 있기 때문입니다.

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
복제되었을 때
(무작위 위치) (으)로 이동하기
<(y좌표) < (-60)> 까지 반복하기 
  (무작위 위치) (으)로 이동하기
끝
+ 크기를 ((-10) 부터 (10) 사이의 난수 만큼 바꾸기
+ (색깔) 효과를 ((1) 부터 (100) 사이의 난수) 만큼 바꾸기
```

--- /task ---

You can now play around with the numbers to get different sizes, colour effects, and numbers of flowers.

당신의 초원에 몇 가지를 더 넣고 싶을 수 있습니다. How about some bees or a few rabbits? You could even change the backdrop to the night sky, and swap your flowers for stars and planets.





