# Aula 03

Relação de implicação e relação de equivalência

### Relação de implicação:

simbolo: => (é exatamente assim o simbolo com dois traços).

Exemplo:

a => a V b (verifique se a implica na proposição a "ou" b).

Tabela verdade:

a   b   aVb
V   V   V
V   F   V
F   V   V
F   F   F

Ou seja, A implica em A V B, pois não temos nenhuma relação de VF com A em AVB.
Também dizemos que como A implica em AVB, então toda vez que A é verdadeiro a sentença A V B também vai ser.

### Relação de equivalência

Nesse caso dizemos que houve a relação de equivalencia quando não ocorre a relação de VF ou FV na tabela verdade.

simbolo: <=>

Exemplo:

a ^ b <=> ~(~a V ~b) - Tem equivalência

Tabela verdade:

a   b   a^b   ~a   ~b   ~aV~b   ~(~aV~b)
V   V    V    F    F      F         V
V   F    F    F    V      V         F
F   V    F    V    F      V         F
F   F    F    V    V      V         F


### Equivalências notáveis

As equivalências são de grande interesse para o estudo da lógica.

O projetista de um circuito digital, por exemplo, quer montar o circuito mais barato e conveniente possível, que gere o resultado esperado.

Para isso, exeistem técnicas de redução de circuitos lógicos, que utilizam algumas equivalências conhecidas como base para o procedimento.

Essas equivalências são denominadas equivalências notáveis e aparecem com frequência nas diversas aplicações da lógica, inclusive na nossa linguagem.

Exemplos:

- Dupla negação: a <=> ~(~a)
Se for preposiçaõ for verdaeira o resultado final também vai ser verdadeiro, pois negamos duas vezes

### Pergunta

Uma afirmação equivalente para “Se estou feliz, então passei no concurso” é:

a- Passei no concurso e não estou feliz.
b- Estou feliz e passei no concurso.
c- Se não passei no concurso, então não estou feliz.
d- Se passei no concurso, então estou feliz.
e- Não passei no concurso e não estou feliz.

A resposta certa é a letra C.

