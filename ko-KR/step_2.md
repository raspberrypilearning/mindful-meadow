## 나만의 초원을 만들어요

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

꽃이 좀 너무 큰 듯합니다. 따라서 먼저 꽃의 크기를 다시 정해야 합니다. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

초록색 깃발을 클릭하여 꽃의 바뀐 크기를 보세요.

--- /task ---

--- task ---

이제 더 많은 꽃들을 만들어야 합니다. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. 슬라이더는 꽃의 수를 설정합니다. 아래의 블럭들을 사용해 꽃의 복제본들을 만들 수 있습니다.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

초록색 깃발을 클릭하면, 아무것도 일어나지 않는 것을 볼 수 있습니다. 복제본들이 기존 꽃 위에 겹쳐져 있기 때문입니다.

--- task ---

복제본이 만들어질 때, 이들은 무작위의 위치로 이동해야 합니다.

```blocks3
when I start as a clone
go to (random position v)
```

꽃의 개수를 원하는 만큼 변경하기 위해 슬라이더를 사용하는 것을 잊지 마세요.

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

이 블럭들을 추가하여 `난수 정하기`{:class="block3operators"}를 사용해 `색깔`{:class="block3looks"}과 `크기`{:class="block3looks"}를 변경합니다.

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

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

당신의 초원에 몇 가지를 더 넣고 싶을 수 있습니다. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





