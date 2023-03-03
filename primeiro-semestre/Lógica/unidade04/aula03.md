# Aula 03

### Definição de argumento quantificado

Um argumento quantificado é um argumento lógico que possui, em suas proposições, sentenças quantificadas.

Não precisamos nos preocupar com o valor lógico das premissas. 

Lembre-se de que, na lógica, estamos interessados na validade da estrutura argumentativa, e não na validação das premissas do nosso argumento.

Portanto, consideraremos que todas as premissas com a qual lidaremos serão verdadeiras.

Vamos trazer, novamente, o argumento mais clássico da lógica formal, que é um argumento quantificado.

P1: Todo homem é mortal.

P2: Sócrates é um homem.

Q: Portanto, Sócrates é mortal.

Se chamarmos o conjunto dos homens de 𝐻, o conjunto dos mortais de 𝑀, o elemento Sócrates de 𝑠, e elementos quaisquer do universo de 𝑥, podemos fazer a tradução simbólica dessa expressão, da maneira explicitada a seguir:

P1: ∀𝑥 (𝐻𝑥 → 𝑀𝑥) 
P2: 𝐻𝑠
Q: ∴ 𝑀𝑠

Seguindo a mesma lógica, podemos simbolizar as sentenças quantificadas a seguir, conforme explicitado:

Alguns vendedores são morenos: ∃𝑥 (𝑉𝑥 ∧ 𝑀𝑥).

Todas as universitárias são estudantes: ∀𝑥 (𝑈𝑥 → 𝐸𝑥).

Há pessoas que não gostam de chocolate: ∃𝑥 (𝑃𝑥 ∧ ~𝐶𝑥).

### Equivalência entre quantificadores

Para trabalharmos com a prova da validade de argumentos quantificados, é conveniente que os quantificadores se apresentem num formato não negado. 

No caso de haver quantificadores negados, podemos substituí-los por um formato equivalente. 

Para isso, utilizamos as equivalências expostas a seguir:

~∀𝑥 (𝑃(𝑥)) ⇔ ∃𝑥 ~(𝑃(𝑥))
~∃𝑥 (𝑃(𝑥)) ⇔ ∀𝑥 ~(𝑃(𝑥))

Vamos analisar cada equivalência individualmente. 

Quando dizemos que ~∀𝑥 (𝑃(𝑥)), dizemos que nem todos os elementos 𝑥 estão associados ao predicado 𝑃(𝑥).

Isso é equivalente a afirmar ∃𝑥 ~(𝑃(𝑥)), ou seja, que existe pelo menos um 𝑥 que não está associado ao predicado 𝑃(𝑥).

Observe o exemplo a seguir: ~∀𝑥 (𝑃(𝑥)) ⇔ ∃𝑥 ~(𝑃(𝑥)).

Não é verdade que todos os homens falam alemão. ⇔ Existe pelo menos um homem que não fala alemão.

Quando dizemos que ~∃𝑥 (𝑃(𝑥)), dizemos que não existe um elemento 𝑥 associado ao predicado 𝑃(𝑥). 

Isso é equivalente a afirmar ∀𝑥 ~(𝑃(𝑥)), ou seja, que todo elemento 𝑥 não está associado ao predicado 𝑃(𝑥).

Observe o exemplo a seguir:

~∃𝑥 (𝑃(𝑥)) ⇔ ∀𝑥 ~(𝑃(𝑥))

Não é verdade que existem alunos que são estudiosos. ⇔ Todos os alunos não são estudiosos (ou seja, nenhum aluno é estudioso).

Além das equivalências entre quantificadores, as equivalências lógicas já estudadas anteriormente podem ser usadas nas sentenças quantificadas.

### Validade de argumentos quantificados

Vamos aprender métodos para provar a validade de argumentos que envolvem sentenças quantificadas. Para isso, vamos utilizar métodos da exemplificação e da generalização.

É possível transformar tais argumentos com quantificadores, por meio da exemplificação, em argumentos sem quantificadores.

Dessa forma, a prova direta de validade para esses argumentos exemplificados pode ser utilizada, usando as mesmas regras de inferência e de equivalência já verificadas.

Finalizada a prova de validade do argumento exemplificado, podemos usar a generalização para obter a conclusão, caso ela seja uma sentença quantificada.

Vamos, a seguir, conhecer esses métodos.

### Exemplificação

O método da exemplificação consiste em escolhermos um elemento de exemplo, 𝑐, de dentro de uma expressão quantificada que se refere a elementos genéricos 𝑥.

Ela funcionará como uma regra de inferência. Há duas possibilidades: a exemplificação universal e a existencial.

Exemplificação universal (E.U.)

Se todos os elementos 𝑥 estão associados ao predicado 𝑃, escolhemos um deles, 𝑐, um termo constante. 

Isso é indicado pela exemplificação universal, demonstrada simbolicamente a seguir:

∀𝑥 (𝑃(𝑥))
∴ 𝑃c

Exemplificação existencial (E.E.)

Se existe um termo associado ao predicado 𝑃, estipulamos que tal termo seja 𝑐.

Isso é indicado pela exemplificação existencial, demonstrada simbolicamente em sequência. 

∃𝑥 (𝑃(𝑥)) 
∴ 𝑃c

### Generalização

O método da generalização reverte o que a exemplificação realiza. 

Há duas possibilidades: a exemplificação universal e a existencial.

### Generalização universal (G.U.) 

Se o termo 𝑐, tomado na exemplificação, pode ser qualquer um (ou seja, pode ser tomado aleatoriamente), então qualquer termo está associado ao predicado 𝑃. Isso é o que traduz a generalização universal, demonstrada a seguir:

𝑃c
∴ ∀𝑥 (𝑃(𝑥))

Generalização existencial (G.E.)

Se concluímos que um termo 𝑐 constante está associado ao predicado 𝑃, então existe um termo associado a 𝑃. Esse é o conceito da generalização existencial, demonstrada a seguir:

𝑃c
∴ ∃𝑥 (𝑃(𝑥))

Como exemplo, vamos aplicar a exemplificação e a generalização para provar a validade do argumento quantificado, disposto a seguir:

P1: Todos os jogadores são atletas.
P2: Todos os atletas sofrem contusões.
Q: Portanto, todos os jogadores sofrem contusões.

### Pergunta

Em um jogo de bingo são sorteadas, sem reposição, bolas numeradas de 1 a 75, e um participante concorre com a cartela reproduzida a seguir. Qual é a probabilidade de que os três primeiros números sorteados estejam nessa cartela?

FIGURA  1.3

a- 0,2%
b- 0,3%
c- 0,4%
d- 0,5%
e- 0,6%

A resposta é a letra B.








