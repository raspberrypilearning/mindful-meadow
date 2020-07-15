## Crie o seu campo florido

--- task ---

Abra o projeto inicial do Scratch on-line em [rpf.io/dm-meadow-start](https://rpf.io/dm-meadow-start){:target="_blank"} ou faça o download do projeto inicial em [rpf.io/p/en/mindful-meadow-on](https://rpf.io/p/en/mindful-meadow-go)

--- /task ---

Você deve ver um campo em uma floresta, com uma única flor grande no meio do palco. Há também um controle deslizante no palco que controlará o número de flores que você vê.

--- task ---

A flor é um pouco grande demais, então a primeira coisa a fazer é redimensioná-la. Adicione este código ao seu ator:

```blocks3
quando a bandeira for clicada
mude o tamanho para [pontuação v] %
```

Clique na bandeira verde para ver o novo tamanho de sua flor.

--- /task ---

--- task ---

Agora vamos gerar mais flores. Há uma variável ` flores ` {: class = "block3variables"} que é controlada pelo controle deslizante do palco, que define o número de flores. Você pode usar os blocos abaixo para criar clones da sua flor:

```blocks3
quando a bandeira for clicada
definir tamanho para [5] %
+ repetir (flores)
+ criar clone de (eu mesmo v)
```

--- /task ---

Se você clicar na bandeira verde, provavelmente você não verá nada acontecer. Isso porque todos os clones são criados na mesma posição que a flor original.

--- task ---

Quando um clone é criado, use este código para fazê-lo ir para uma posição aleatória:

```blocks3
quando eu começar como um clone
vá para (posição aleatória v)
```

Não se esqueça de ajustar o controle deslizante para alterar o número de flores que você deseja criar.

--- /task ---

No momento, as flores aparecem por todo o palco - algumas parecem estar no céu. Isto pode ser corrigido certificando-se de que a posição `y`{:class="block3motion"} das flores esteja sempre abaixo da grande rocha.

--- task ---

Adicione estes blocos para continuar movendo as flores para uma posição aleatória, até que elas estejam abaixo de `-60`{:class="block3motion"} no eixo `y`{:class="block3motion"}:

```blocks3
quando eu começar como um clone
vá para (posição aleatória v)
+ repita até <(posição y) < (-60)>
+ vá para (posição aleatória v)
```

--- /task ---

As flores parecem um pouco sem graça atualmente, já que têm o mesmo tamanho e a mesma cor. Você pode usar um código gerador de números aleatórios para corrigir isso.

--- task ---

Adicione um bloco `pick random`{:class="block3operators"} para mudar a `color`{:class="block3looks"} e `size`{:class="block3looks"} das flores:

```blocks3
quando eu começar como um clone
vá para (posição aleatória v)
repita até que <(posição y) < (-60)>
vá para (posição aleatória v)
fim
+ mude (número aleatório entre (-10) e (10)) no tamanho
+ mude (número aleatório entre (1) e (100)) ao efeito [cor v]
```

--- /task ---

Agora você pode brincar um pouco com os números para obter diferentes tamanhos, efeitos de cor e números de flores.

Você também pode adicionar mais algumas coisas ao seu campo. Que tal adicionar algumas abelhas ou alguns coelhos? Você pode até mudar o cenário para o céu noturno e trocar suas flores por estrelas e planetas.





