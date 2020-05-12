## अपना शांतिदायक बगीचा बनाएँ

--- task ---

Open the starter Scratch project either online at [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} or download the starter project at [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

You should see a meadow in a forest, with a single large flower in the middle of the Stage. There's also a slider on the Stage that will eventually control the number of flowers that you see.

--- task ---

फूल थोड़ा बड़ा है इसलिए सबसे पहले इसके आकार को बदलते हैं। Add these blocks to the flower sprite:

```blocks3
when flag clicked
set size to [5] %
```

अपने फूल के नए आकार को देखने के लिए हरे झंडे पर क्लिक करें।

--- /task ---

--- task ---

अब हमें और फूल बनाने की ज़रूरत है | There is a `flowers`{:class="block3variables"} variable that is controlled by the slider on the Stage. यह फूलों की संख्या तय कर सकता है। आप अपने फूलों के क्लोन (clone) बनाने के लिए नीचे दिए गए ब्लॉक का उपयोग कर सकते हैं।

```blocks3
when flag clicked
set size to [5] %
+ repeat (flowers)
+ create clone of (myself v)
```

--- /task ---

यदि आप हरे झंडे पर क्लिक करते हैं तो आप शायद कुछ भी बदलता हुआ नहीं देखेंगे। ऐसा इसलिए है क्योंकि सभी क्लोन मूल फूल के समान स्थान पर बनाए गए हैं।

--- task ---

जब एक क्लोन बनाया जाता है, तो इसे यादृच्छिक (random) जगह में जाना चाहिए।

```blocks3
when I start as a clone
go to (random position v)
```

फूलों की संख्या बदलने के लिए स्लाइडर को खींचकर ऊपर नीचे करना मत भूलियेगा

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

फूल के `रंग`{:class="block3looks"} और `माप`{:class="block3looks"} बदलने के लिए इन ब्लॉक्स को जोड़ें, `pick random`{:class="block3operators"} ब्लॉक का उपयोग करते हुए |

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

You can now play around with the numbers to get different sizes, color effects, and numbers of flowers.

आप अपने बगीचे में कुछ और चीजें जोड़ सकते हैं। How about adding some bees or a few random rabbits? You could even change the backdrop to the night-time sky and add stars and planets instead of flowers.





