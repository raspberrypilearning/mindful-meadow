## Створи свій мирний луг

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

Ця квітка трохи завелика, тож перше, що потрібно — це змінити її розмір. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

Натисни на зелений прапорець, щоб побачити новий розмір твоєї квітки.

--- /task ---

--- task ---

Тепер нам потрібно згенерувати більше квітів. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. Тут можна встановити кількість квітів. Ти можеш використовувати блоки наведені нижче, щоб створити клони своєї квітки.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

Якщо клікнути на зелений прапорець, то, ймовірно, нічого не станеться. Це тому, що клони створюються в такому ж місці, що й початкова квітка.

--- task ---

Коли створюється клон, він повинен перейти у випадкове місце.

```blocks3
when I start as a clone
go to (random position v)
```

Не забудь налаштувати повзунок, щоб змінити бажану кількість квітів.

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

Додай такі блоки, щоб змінити `колір`{:class="block3looks"} і `розмір`{:class="block3looks"} квітів, використовуючи блок `випадкове від`{:class="block3operators"}.

```blocks3
коли я починаю як клон
перейти до (випадкова позиція v)
повторити до <(значення y) < (-60)> 
  перейти до (випадкова позиція v)
end
+ змінити розмір на (випадкове від (-10) до (10))
+ змінити ефект (колір v) на (випадкове від (1) до (100))
```

--- /task ---

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

Ти також можеш додати до лугу ще дещо. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





