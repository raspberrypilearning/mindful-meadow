## अपना शांतिदायक बगीचा बनाएँ

--- task ---

Scratch के स्टार्टर प्रोजेक्ट (starter project) को खोलें या तो ऑनलाइन यहाँ से [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} अन्यथा [rpf.io/p/hi-IN/mindful-meadow-on](https://rpf.io/p/hi-IN/mindful-meadow-go) यहाँ से स्टार्टर प्रोजेक्ट को डाउनलोड कर सकते हैं

--- /task ---

आपको एक जंगल में एक बगीचा दिखना चाहिए जिसके बीच में एक काफी बड़ा फूल होगा। आपके स्क्रीन के बाएं तरफ एक स्लाइडर (slider) भी होगा जो अंत में आपके द्वारा देखे जाने वाले फूलों की संख्या को नियंत्रित करेगा।

--- task ---

फूल थोड़ा बड़ा है इसलिए सबसे पहले इसके आकार को बदलते हैं। इन ब्लॉक्स (blocks) को फूल स्प्राइट (sprite) में जोड़ें।

```blocks3
when flag clicked
set size to [5] %
```

अपने फूल के नए आकार को देखने के लिए हरे झंडे पर क्लिक करें।

--- /task ---

--- task ---

अब हमें और फूल बनाने की ज़रूरत है | एक `flowers` {:class="block3variables"} वेरिएबल (variable) है जो स्लाइडर (slider) द्वारा नियंत्रित किया जाता है। यह फूलों की संख्या तय कर सकता है। आप अपने फूलों के क्लोन (clone) बनाने के लिए नीचे दिए गए ब्लॉक का उपयोग कर सकते हैं।

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

फिलहाल, फूल पूरे जगह फैले हुए दिखाई देंगे | उनमें से कुछ तो ऐसे दिखेंगे जैसे वह आकाश में हों। आप इसे ठीक भी कर सकते है, आपको बस यह सुनिक्षित करना होगा कि फूल की `y`{:class="block3motion"} जगह हमेशा बड़ी चट्टान से नीचे हो।

--- task ---

फूलों को यादृच्छिक (random) जगहों में हमेशा आते रहने के लिए इन ब्लॉक्स को जोड़ें जब तक कि वे `y`{:class="block3motion"} अक्ष (axis) पर `-60`{:class="block3motion"} से नीचे हों।

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

सारे फूल फिलहाल थोड़े फीके दिख रहे हैं क्योंकि वे सभी एक ही आकार और एक ही रंग के हैं। हम इसे ठीक करने के लिए एक यादृच्छिक (random) संख्या जनरेटर (number generator) ब्लॉक का उपयोग कर सकते हैं।

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

अब आप विभिन्न आकारों, रंगों के प्रभाव और फूलों की संख्या प्राप्त करने के लिए संख्याओं के साथ थोड़ा सा खेल सकते हैं।

आप अपने बगीचे में कुछ और चीजें जोड़ सकते हैं। जैसे कि कुछ मधुमक्खी या कुछ खरगोश इधर-उधर जोड़ सकते हैं। या बैकड्रॉप (backdrop) को रात के आकाश में बदल दें और फूलों के बजाय तारों और ग्रहों को जोड़ दें।





