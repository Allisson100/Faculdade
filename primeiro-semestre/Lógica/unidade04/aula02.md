# Aul 02

### Quantificador existencial

Considere que 𝑃(𝑥) é uma sentença aberta em função da variável 𝑥.

O quantificador existencial expressa o fato de que existe pelo menos um elemento 𝑥 no universo, capaz de tornar 𝑃(𝑥) uma proposição verdadeira. 

Ou seja, ao ser utilizado junto a uma sentença aberta, o quantificador existencial transforma essa sentença em uma proposição, afirmando que a sentença é verdadeira para pelo menos um valor assumido pela variável.

Usaremos o símbolo ∃ para expressar o quantificador existencial.

Em linguagem corrente, ele é lido como “algum”, “para algum”, “existem pelo menos um” ou “existe algum”. 

A quantificação existencial da sentença “para algum 𝑥, 𝑃(𝑥)” é dada como exposto a seguir.

∃𝑥 (𝑃(𝑥))

Essa proposição significa que existe pelo menos um valor de 𝑥 do universo para o qual a sentença 𝑃(𝑥) é verdadeira. 

Nesse caso, para que tenhamos uma proposição verdadeira, basta que o conjunto verdade de 𝑥 não seja um conjunto vazio. Ou seja, 𝑉𝑝 ≠ Ø.

A própria sentença quantificada pode explicitar o universo.

Observe a sentença a seguir:

“Existe um 𝑥 inteiro, tal que 𝑥 é maior do que zero”.

Ela contém o quantificador existencial (existe um, ou ∃), o universo (conjunto dos números inteiros, ou ℤ) e a sentença aberta em função de 𝑥 (𝑥 é maior do que zero, ou 𝑥 > 0). Simbolicamente, ela pode ser expressa como o exposto a seguir:

(∃𝑥 ∈ ℤ)(𝑥 > 0)

Observe a sentença “Algum matemático é filósofo”. 

Ela tem a forma “Algum 𝐴 é 𝐵”.

Nesse caso, há a indicação de que existe uma interseção entre os conjuntos 𝐴 e 𝐵. 

Por isso, a palavra “algum” está associada à operaçãode conjunção.

### Quantificador universal

Quando temos uma proposição quantificada universalmente, seu valor lógico será verdadeiro se o seu conjunto verdade for igual ao seu conjunto universo, ou seja, 𝑉𝑝 = 𝑈. 

Observe a sentença quantificada a seguir:

(∀𝑥 ∈ ℕ*)(2𝑥 > 𝑥)

Lemos como: “para qualquer 𝑥 pertencente ao conjunto dos números naturais não nulos, 2𝑥 é maior do que 𝑥”.

O predicado é encontrado nos segundos parênteses da sentença.

Nesse caso, podemos isolar a variável 𝑥, conforme disposto a seguir:

𝑃(𝑥): 2𝑥 > x
𝑃(𝑥): 2𝑥 – 𝑥 > 0
𝑃(𝑥): 𝑥 > 0

O seu conjunto universo é expresso nos primeiros parênteses junto ao quantificador universal.

Ele é o conjunto dos números naturais não nulos. 

Simbolicamente, temos o que segue:
𝑈 = ℕ* = {1, 2, 3, 4, 5, ...}

Já o conjunto verdade é o conjunto de valores do universo que tornam a sentença 𝑃(𝑥) verdadeira.

Para isso, expressamos tanto o universo, quanto o predicado.

𝑉𝑝 = {𝑥 ∈ ℕ* | 𝑥 > 0} = {1, 2, 3, 4, 5, ...} 

Note que, nesse caso, o conjunto universo coincide com o conjunto verdade, ou seja, 𝑉𝑝 = 𝑈. Isso faz com que tenhamos uma proposição verdadeira. 

Qualquer divergência entre os elementos desses conjuntos tornaria a proposição falsa.

### Quantificador existencial

Quando temos uma proposição quantificada existencialmente, seu valor lógico será verdadeiro se o seu conjunto verdade tiver pelo menos um elemento, ou seja, 𝑉𝑝 ≠ Ø.

Observe a sentença quantificada a seguir:

(∃𝑥 ∈ ℤ)(2𝑥 > 𝑥)

Lemos como: “existe pelo menos um 𝑥 pertencente ao conjunto dos números inteiros, tal que 2𝑥 é maior do que 𝑥”. 

O predicado é encontrado nos segundos parênteses da sentença.

Nesse caso, podemos isolar a variável 𝑥, conforme disposto a seguir:

𝑃(𝑥): 2𝑥 > 𝑥
𝑃(𝑥): 2𝑥 – 𝑥 > 0
𝑃(𝑥): 𝑥 > 0

O seu conjunto universo é expresso nos primeiros parênteses, junto ao quantificador universal. 

Ele é o conjunto dos números inteiros. 

Simbolicamente, temos o que segue:
𝑈 = ℤ = {..., –2, –1, 0, 1, 2, 3, ...}

Já o conjunto verdade é o conjunto de valores do universo que tornam a sentença 𝑃(𝑥) verdadeira.

Para isso, expressamos tanto o universo, quanto o predicado.
𝑉𝑝 = {𝑥 ∈ ℤ | 𝑥 > 0} = {1, 2, 3, 4, 5, ...}

Lidaremos com argumentos lógicos quantificados, com foco em sentenças em linguagem corrente e em contextos que não envolvem conjuntos cujos elementos são numéricos.

Adotaremos um formato padronizado para simbolizar nossas sentenças, e seguiremos com ele até o fim da nossa unidade.

Desse modo, é mais fácil lidarmos com estruturas argumentativas.

Em sentenças quantificadas universalmente, no formato “todo A tem a propriedade B”, podemos usar a letra 𝑥 como representante de qualquer elemento do universo, expressando:

“Qualquer que seja 𝑥, se 𝑥 tem a propriedade A, então 𝑥 tem a propriedade B”.

Simbolicamente, representaremos essa expressão no seguinte formato: ∀𝑥 (𝐴𝑥 → 𝐵𝑥).

Nesse caso, ∀ é o quantificador universal, 𝑥 é a variável e (𝐴𝑥 → 𝐵𝑥) é o predicado.

Em sentenças quantificadas existencialmente, no formato ”algum A tem a propriedade B”, podemos usar a letra 𝑥 como representante de qualquer elemento do universo, expressando:

“Existe pelo menos um 𝑥 que tem a propriedade A e a propriedade B”. 

Simbolicamente, representaremos essa expressão no seguinte formato: ∃𝑥 (𝐴𝑥 ∧ 𝐵𝑥).

Nesse caso, ∃ é o quantificador existencial, 𝑥 é a variável e (𝐴𝑥 ∧ 𝐵𝑥) é o predicado.

### Pergunta

A alternativa que apresenta uma sentença quantificada universalmente é:

a- Em Macapá tem nota fiscal
b- A Região Oeste do Brasil emite notas fiscais.
c- Existe dentista no posto de saúde do município do SUS.
d- Alguns advogados de São Paulo são auditores fiscais.
e- Qualquer engenheiro de segurança do trabalho pode participar da auditoria.

A resposta certa é letra E.

