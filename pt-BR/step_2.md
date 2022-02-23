## Crie o seu campo florido

--- task ---

Abra o projeto inicial do Scratch on-line em [scratch.mit.edu/projects/411751978](https://scratch.mit.edu/projects/411751978){:target="_blank"} ou faça o download do projeto inicial em [rpf.io/p/pt-BR/mindful-meadow-on](https://rpf.io/p/pt-BR/mindful-meadow-go)

--- /task ---

Você deve ver um campo em uma floresta, com uma única flor grande no meio do palco. Há também um controle deslizante no palco que controlará o número de flores que você vê.

--- task ---

A flor é um pouco grande demais, então a primeira coisa a fazer é redimensioná-la. Adicione este código ao seu ator:

```blocks3
when flag clicked
set size to [5] %
```

Clique na bandeira verde para ver o novo tamanho de sua flor.

--- /task ---

--- task ---

Agora vamos gerar mais flores. Há uma variável `flores`{:class="block3variables"} que é controlada pelo controle deslizante do palco, que define o número de flores. Você pode usar os blocos abaixo para criar clones da sua flor:

```blocks3
when flag clicked
set size to [5] %
+ repeat (flores)
+ create clone of (myself v)
```

--- /task ---

Se você clicar na bandeira verde, provavelmente você não verá nada acontecer. Isso porque todos os clones são criados na mesma posição que a flor original.

--- task ---

Quando um clone é criado, use este código para fazê-lo ir para uma posição aleatória:

```blocks3
when I start as a clone
go to (random position v)
```

Não se esqueça de ajustar o controle deslizante para alterar o número de flores que você deseja criar.

--- /task ---

No momento, as flores aparecem por todo o palco - algumas parecem estar no céu. Isto pode ser corrigido certificando-se de que a posição `y`{:class="block3motion"} das flores esteja sempre abaixo da grande rocha.

--- task ---

Adicione estes blocos para continuar movendo as flores para uma posição aleatória, até que elas estejam abaixo de `-60`{:class="block3motion"} no eixo `y`{:class="block3motion"}:

```blocks3
when I start as a clone
go to (random position v)
+ repeat until <(y position) < (-60)>
+ go to (random position v)
```

--- /task ---

As flores parecem um pouco sem graça atualmente, já que têm o mesmo tamanho e a mesma cor. Você pode usar um código gerador de números aleatórios para corrigir isso.

--- task ---

Adicione um bloco `número aleatório`{:class="block3operators"} para mudar a `cor`{:class="block3looks"} e `tamanho`{:class="block3looks"} das flores:

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

Agora você pode brincar um pouco com os números para obter diferentes tamanhos, efeitos de cor e números de flores.

Você também pode adicionar mais algumas coisas ao seu campo. Que tal adicionar algumas abelhas ou alguns coelhos? Você pode até mudar o cenário para o céu noturno e trocar suas flores por estrelas e planetas.





