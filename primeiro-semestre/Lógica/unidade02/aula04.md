# Aula 04

### Leis de idempotência

A idempotência é a propriedade que algumas operações têm de poderem ser aplicadas diversas vezes, sem que o resultado se altere após a aplicação inicial.

Exemplo:

a ^ a <=> a  a V a <=> a

a = O cavalo é branco

a ^ a = O cavalo é branco e é branco
a V a = O cavalo é branco ou é branco

### Leis comutativas 

As leis comutativas dizem que ao relacionar duas proposições por uma operação de conjunção podemos, livremente, inverter a ordem na qual elas aparecem na sentença composta, pois não mudará o seu valor lógico. Isso vale também para operações de disjunção.

Exemplo:

a ^ b <=> b ^ a

a ^ b = O cavalo é branco e a casa é amarela
b ^ a = A casa é amarela e o cavalo é branco

Outro exemplo:

a V b <=> b V a

a V b =  O cavalo é branco ou a casa é amarela
b V a = A casa é amarela ou o cavalo é branco

### Leis associativas

As leis associativas permitem que troquemos a posição dos parâmetros dos parênteses, quando temos o mesmo operador lógico relacionando três proposições distintas.

Exemplo:

(a V b) V c <=> a V (b V c)
(a ^ b) ^ c <=> a ^ (b ^ c)

(a ^ b) ^ c = O cavalo é branco e a casa é amarela. Além disso, a rosa é vermelha.
a ^ (b ^ c) = O cavalo é branco. Além disso, a casa é amarela e a rosa é vermelha.

### Leis de Morgan

Seus formatos permitem que troquemos um conectivo "e" por um ocnectivo "ou", ou vice versa, mantendo a equivalência entre as expressões.

Exemplo:

~(a ^ b) <=> ~a V ~b

~(a ^ b) = Não é verdade que o cavalo é branco e a casa é amarela.
~a V ~b = o cavalo não é branco ou a casa não é amarela.

Outro exemplo:

~(a V b) <=> ~a ^ ~b

~(a V b) = Não é verdade que o cavalo é branco ou a casa é amarela.
~a ^ ~b = O cavalo não é branco e a casa não é amarela.

### Leis distributivas 

A leis distrbutivas se assemelham à propriedade distributiva da aritmética. Utilizando os conectivos "e" e "ou", podemos distribuir o conectivo de fora dos parênteses para dentro dos parênteses.

Exemplo:

a ^ (b V c) <=> (a ^ b) V (a ^ c)
a V (b ^ c) <=> (a V b) ^ (a V c)

a V (b ^ c) = Maria estuda lógica, ou, Maria estuda matemática e português.
(a V b) ^ (a V c) = Mari estuda lógica ou matemática, e Maria estuda lógica ou português.

### Leis condicionais

Os formatos de equivalências partem de uma condicional entre duas proposições.

a --> b <=> ~b --> ~a
a --> b <=> ~a V b

a --> b = Se estiver chovendo, então eu levarei um guarda-chuva
~b --> ~a = Se eu não levei um guarda-chuva, então não estava chovendo.
~a V b = Não está chovendo, ou eu levaria um guarda-chuva.

### Leis bicondicionais

a <--> b <=> (a --> b) ^ (b --> a)
a <--> b <=> ~(a _v(v com traço em baixo) b)

Se é verdade que a <--> b, então é verdade que a --> b e também é verdade que b --> a.

### Pergunta

Negando em linguagem corrente as seguintes proposições, qual delas terá negação dupla?

a- Atlético é alviverde e Coritiba é rubro-negro.
b- As vendas diminuem e os preços aumentam.
c- É falso que está frio ou que está chovendo.
d- Se João passar em Física então se formará.
e- Não tenho carro e não tenho moto.

A resposta certa é a letra C.







 






