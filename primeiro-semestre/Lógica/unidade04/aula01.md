# Aula 01

### Quantificadores

### Revisão de conjuntos numéricos

Em nosso sistema decimal de numeração, utilizamos apenas 10 algarismos, que vão de 0 a 9, para representar quantidades.

Quando combinamos algarismos entre si, formamos numerais, que representam qualquer número (quantidade) que desejarmos representar.

Esses números podem ser classificados por tipo e divididos em conjuntos.

A Matemática chama-os de conjuntos numéricos.

Podemos pensar que esses conjuntos identificam o nível de complexidade dos números em questão.

Veremos os principais conjuntos numéricos adotados, começando pelos mais simples.

Conjunto dos números naturais (ℕ)  N = {0, 1, 2, 3, 4, 5, ...}

Conjunto dos números inteiros (ℤ)  ℤ = {...,–3, –2, –1, 0, 1, 2, 3, ...}

ℤ* = {...,–3, –2, –1, 0, 1, 2, 3, ...} (conjunto dos números inteiros não nulos)

ℤ+ = {0,1,2,3,4,5,6, …} (conjunto dos números inteiros não negativos)

ℤ_ = {…,-4,-3,-2,-1,0} (conjunto dos números inteiros não positivos)

ℤ+ * = {1,2,3,4,5,6, …} (conjunto dos números inteiros não nulos e não negativos)

ℤ_ * = {… ,-4,-3,-2,-1} (conjunto dos números inteiros não nulos e não positivos)

### Conjunto dos números racionais (ℚ)

Vejamos alguns exemplos de número racionais, que incluem números decimais e dízimas periódicas:

- 3/5, que é uma fração entre inteiros

- -7/2 , que é uma fração entre inteiros

- 0,71, que pode ser escrito como 71/100

- -0,3, que pode ser escrito como -3/10

- 5, que pode ser escrito como 5/1

- 2,7, que pode ser escrito como 27/10

- 0,4444..., que pode ser escrito como 4/9

- 0,121212..., que pode ser escrito como 12/99

### Conjunto dos números irracionais (𝕀)

π = 3,141592653...

(simbolo de raiz quadrada) de 2 = 1,414221356...

(simbolo de raiz quadrada) de 5 = 2,23606797...

A constante π (pi) resulta da divisão do comprimento de uma circunferência por seu diâmetro.

Note que as casas decimais são infinitas e não periódicas, e não podemos expressar π como uma fração entre inteiros.

Conjunto dos números reais
(ℝ) -> ℝ = { 𝑥 | 𝑥 ∈ ℚ ou 𝑥 ∈ 𝕀} 

### Sentenças abertas

Uma sentença aberta (ou uma função proposicional) é uma sentença que contémuma ou mais variáveis, que são termos ou símbolos que podem ser substituídos por diferentes valores.

Se não há atribuição de um valor a cada variável, não somos capazes de identificar o nível lógico da sentença.

Logo, uma sentença aberta não é considerada uma proposição.

Acompanhe alguns exemplos de sentenças abertas, apresentadas a seguir.

𝑋 é um planeta do Sistema Solar.

Nesse caso, enquanto não soubermos o que a variável 𝑋 representa, não podemos atribuir um valor lógico à sentença.

Se, por exemplo, 𝑋 assumir o valor “Saturno”, temos a proposição “Saturno é um planeta do Sistema Solar”, cujo valor lógico é verdadeiro.

Se, por exemplo, 𝑋 assumir o valor “Lua”, temos a proposição “Lua é um planeta do Sistema Solar”, cujo valor lógico é falso.

### Conjunto universo e conjunto verdade

O conjunto universo de uma variável é o conjunto de possíveis valores que podem substituir a variável de uma sentença aberta.

Chamaremos, simbolicamente, esse conjunto de 𝑈.

O conjunto universo pode ser definido pelo próprio contexto da sentença, ou imposto por algum agente, como o próprio enunciado de uma questão.

O conjunto verdade de uma variável é o conjunto de possíveis valores, pertencentes ao universo, capazes de transformar a sentença aberta em uma proposição verdadeira.

Chamaremos, simbolicamente, esse conjunto de 𝑉𝑝.

Exemplo:

Considere a seguinte sentença aberta: “O planeta 𝑋 é o maior planeta do Sistema Solar”.

Pelo contexto, determine o conjunto universo e o conjunto verdade da variável 𝑋.

Resolução:

O conjunto universo é formado por todos os planetas do Sistema Solar.

Ele terá, portanto, 8 elementos, dispostos a seguir.

𝑈 = {Mercúrio, Vênus, Terra, Marte, Júpiter, Saturno, Urano, Netuno}

Já o conjunto verdade é composto por todos os elementos pertencentes ao universo que transformam a sentença aberta em uma proposição verdadeira.

Como o maior planeta do Sistema Solar é Júpiter, ele é o único elemento que integra o conjunto verdade.

𝑉𝑝 = {Júpiter}

### Quantificador universal

Um quantificador é um símbolo (ou um termo) lógico capaz de fazer uma verificação sobre o conjunto de valores do universo que se tornam sentenças verdadeiras. 

A função de um quantificador é tornar uma sentença aberta uma proposição lógica.

Trabalharemos com dois quantificadores: o universal e o existencial.

Considere que 𝑃(𝑥) é uma sentença aberta em função da variável 𝑥.

O quantificador universal expressa o fato de que, para todo elemento 𝑥 do universo, 𝑃(𝑥) será uma proposição verdadeira. 

Ou seja, ao ser utilizado junto a uma sentença aberta, o quantificador universal transforma essa sentença em uma proposição, afirmando que a sentença é verdadeira para qualquer valor assumido pela variável.

Usaremos o símbolo ∀ para expressar o quantificador universal. 

Em linguagem corrente, ele é lido como “todo”, “para todo”, “para qualquer” ou “qualquer que seja”.

A quantificação universal da sentença “para todo 𝑥, 𝑃(𝑥)” é dada como exposto a seguir: ∀𝑥 (𝑃(𝑥)).

∀𝑥 (𝑃(𝑥))

Essa proposição significa que para todos os valores de 𝑥 do universo, a sentença 𝑃(𝑥) é verdadeira.

Nesse caso, o conjunto verdade de 𝑥 deve coincidir com o próprio conjunto universo para que tenhamos uma proposição verdadeira. Ou seja, 𝑉𝑝 = 𝑈.

### Pergunta

Analise os casos a seguir:

|- Os números Naturais são aqueles inteiros não positivos mais o zero.
||- Os números Irracionais são aqueles que representam dízimas periódicas.
||| - Os números Reais representam a soma dos números Racionais com os Irracionais.

Assinale a alternativa correta:

a- Somente a assertiva II está correta.
b- Somente a assertiva III está correta.
c- Somente a assertiva I está correta.
d- Somente as assertivas II e III estão corretas.
e- Todas as assertivas estão corretas.

A resposta certa é letra B.











