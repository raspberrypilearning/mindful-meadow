## 나만의 초원을 만들어요

--- task ---

온라인 [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"}에서 입문자 스크래치 프로젝트를 열거나 [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)에서 입문자 프로그램을 다운로드하세요.

--- /task ---

숲 속의 초원이 보입니다. 무대의 중심에는 한 송이의 큰 꽃이 있습니다. 그리고 슬라이더가 있는데, 이는 당신에게 보이는 꽃의 수를 즉시 바꿀 수 있습니다.

--- task ---

꽃이 좀 너무 큰 듯합니다. 따라서 먼저 꽃의 크기를 다시 정해야 합니다. 이 블럭들을 꽃 스프라이트에 추가하세요.

```blocks3
when flag clicked
set size to [5] %
```

초록색 깃발을 클릭하여 꽃의 바뀐 크기를 보세요.

--- /task ---

--- task ---

이제 더 많은 꽃들을 만들어야 합니다. `꽃들`{:class="block3variables"} 이라는 변수가 있으며, 이는 무대의 슬라이더로 조절이 가능합니다. 슬라이더는 꽃의 수를 설정합니다. 아래의 블럭들을 사용해 꽃의 복제본들을 만들 수 있습니다.

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

그 순간, 꽃들이 무대 사방에 다 나타날 것입니다. 몇몇은 하늘에 있는 것처럼 보일 거예요. 이것은 꽃의 `y좌표`{:class="block3motion"} 가 항상 큰 바위보다 아래에 있게함으로써 해결할 수 있습니다.

--- task ---

이 블럭들을 추가하여 꽃이 `y`{:class="block3motion"} 좌표의 `-60`{:class="block3motion"}보다 아래에 있으면서 무작위의 위치로 이동하도록 하십시오.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

현재는 꽃들이 조금 지루해 보일 수 있습니다. 전부 같은 크기에 같은 색깔이기 때문입니다. 이를 해결하기 위해 난수 생성 블럭을 사용할 수 있습니다.

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

이제 당신은 숫자로 꽃들의 크기, 색깔, 수를 바꾸면서 놀 수 있습니다.

당신의 초원에 몇 가지를 더 넣고 싶을 수 있습니다. 벌들과 무작위의 토끼들을 추가해보는 것은 어떨까요. 또는 배경을 밤하늘로 바꾸고 꽃들 대신에 별들을 추가해 볼 수도 있습니다.





