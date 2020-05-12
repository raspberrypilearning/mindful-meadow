## أنشيء مرج أخضر خاص بك

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

الزهرة كبيرة جداً، لذا فإن أول شيء عليك فعله هو تغيير حجمها. Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

انقر على العلم الأخضر لرؤية الحجم الجديد للزهرة.

--- /task ---

--- task ---

الآن نحن بحاجة إلى أنشاء المزيد من الزهور. There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. يمكنها أن تحدد عدد الزهور. يمكنك استخدام الكتل أدناه لإنشاء نسخ للزهرة.

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

إذا قمت بالنقر على العلم الأخضر، ربما لن ترى أي شيء يحدث. لأن جميع النسخ يتم إنشاؤها في نفس الموضع الذي تم فيه إنشاء الزهرة الأصلية.

--- task ---

عندما يتم إنشاء نسخة، يجب أن يذهب إلى وضع عشوائي.

```blocks3
when I start as a clone
go to (random position v)
```

لا تنسى ضبط شريط التمرير، لتغيير عدد الزهور التي تريدها.

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

أضف هذه الكتل لتغيير اللون `color`{:class="block3looks"} و `الحجم`{:class="block3looks"} من الزهور باستخدام كتلة `عدد عشوائي بين`{:class="block3operators"}.

```blocks3
عندما أبدأ كنسخة
انتقل إلى (الموضع العشوائي v)
أكرر حتى <(المكان) y position) < (-60)>
انتقل إلى (الموضع العشوائي v)
end
+ تغيير الحجم بمقدار (اختيار عشوائي (-10) إلى (10)
+ تغيير التأثير (لون v) بمقدار (اختر عشوائي (1) إلى (100))
```

--- /task ---

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

قد ترغب أيضًا في إضافة بعض الأشياء الأخرى إلى المرج الخاص بك. How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





