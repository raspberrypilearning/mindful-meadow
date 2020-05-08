## أنشيء مرج أخضر خاص بك

--- task ---

افتح مشروع Scratch إما على الإنترنت في [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} أو قم بتحميل المشروع على [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

يجب أن ترى مرج في غابة، مع زهرة واحدة كبيرة في منتصف المنصة. هناك أيضا شريط تمرير على المنصة الذي سيتحكم في نهاية المطاف بعدد الزهور التي تراها.

--- task ---

الزهرة كبيرة جداً، لذا فإن أول شيء عليك فعله هو تغيير حجمها. أضف هذه التعليمات البرمجية إلى الزهرة.

```blocks3
when flag clicked
set size to [5] %
```

انقر على العلم الأخضر لرؤية الحجم الجديد للزهرة.

--- /task ---

--- task ---

الآن نحن بحاجة إلى أنشاء المزيد من الزهور. هناك متغير `زهور `{:class="block3variables"} الذي يتحكم به شريط التمرير على المنصة. يمكنها أن تحدد عدد الزهور. يمكنك استخدام الكتل أدناه لإنشاء نسخ للزهرة.

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

في الوقت الحالي، ستظهر الزهور في جميع أنحاء المنصة، لذا تبدو بعض الزهور وكأنها في السماء. يمكن إصلاح هذا عن طريق التأكد من أن موقع `ص`{:class="block3motion"} للزهور دائما اسفل الصخرة الكبيرة.

--- task ---

Add these blocks to keep moving the flowers to a random position, until they are below `-60`{:class="block3motion"} on the `y`{:class="block3motion"} axis.

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

تبدو الأزهار مملة بعض الشيء في الوقت الحالي، لأنها جميعها بنفس الحجم ونفس اللون. يمكننا استخدام كتلة مولد ألأرقام العشوائي لإصلاح هذا الامر.

--- task ---

أضف هذه الكتل لتغيير اللون `color`{:class="block3looks"} و `الحجم`{:class="block3looks"} من الزهور باستخدام كتلة `عدد عشوائي بين`{:class="block3operators"}.

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

يمكنك الآن تغيير الأعداد قليلاً للحصول على أحجام مختلفة وتأثير الألوان وأعداد الزهور.

قد ترغب أيضًا في إضافة بعض الأشياء الأخرى إلى المرج الخاص بك. ماذا عن إضافة بعض النحل أو بعض الأرانب العشوائية. أو حتى تغيير الخلفية إلى سماء الليل وإضافة النجوم والكواكب بدلاً من الزهور.





