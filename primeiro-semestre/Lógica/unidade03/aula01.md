# Aula 01

### Argumentos lógicos

Um argumento lógico é uma coleção de sentenças ou proposições que se relacionam mutuamente, de forma que pelo menos uma tem a função de premissa e uma tem a função de conclusão.

Observe o exemplo seguinte:

- Todo homem é mortal. (Premissa 1)
- Sócrates é um homem. (Premissa 2)
- Portanto, Sócrates é mortal. (Conclusão)

Temos, nesse argumento lógico, duas premissas verdadeiras e que, por meio do nosso raciocínio, levam a uma terceira sentença, também verdadeira, que é a conclusão.

As premissas, portanto, são capazes de construir a sentença de conclusão, por meio do raciocínio lógico.

Um silogismo é um argumento constituído por duas premissas.

Sendo uma delas de conteúdo mais abrangente (premissa maior) e outra de conteúdo mais específico (premissa menor), além, é claro, de uma conclusão. 

No caso, a premissa 1 é a premissa maior, a premissa 2 é a premissa menor.

### Formatos simbólicos

No tópico passado, vimos um exemplo de argumento lógico expresso em linguagem corrente. 

Podemos, também, expressar a forma de argumentos de maneira simbólica.

Nesse caso, podemos usar qualquer um dos formatos destacados na tabela a seguir, em que P1, P2 e Pn representam as premissas e Q representa a conclusão do argumento.

FIGURA 1.0

### Argumento válido

Para que uma estrutura argumentativa seja considerada válida, é necessário que a conclusão seja necessariamente verdadeira sempre que todas as premissas também o forem.

Portanto, em um argumento válido, a veracidade das premissas é incompatível com a falsidade da conclusão.

Nesse caso, podemos definir argumento válido da seguinte forma: a conjunção das premissas do argumento implica a conclusão. Simbolicamente, temos a relação a seguir:

P1 ⋀ P2 ⋀ ... ⋀ Pn ⇒ Q

Como a relação de implicação entre conjunção de premissas e conclusão pode ser testada para confirmar se um argumento é válido ou não, podemos utilizar tabelas-verdade para tal finalidade.

Exemplo:

- Testando a relação de implicação entre a conjunção de premissas e a conclusão, verifique a validade do seguinte argumento: 𝑎 → 𝑏, 𝑎 ⊢ 𝑏. 

Resolução:

No argumento apresentado no enunciado, temos duas premissas que se encontram separadas entre si por vírgula, e uma conclusão, posicionada após o símbolo ⊢.

Se expressarmos o argumento no formato vertical, conseguimos enxergar isso mais claramente. 
Observe a seguir.

a → b (P1)
a (P2)
---
∴ b (Q)

Para testar a validade do argumento, devemos verificar se P1 ∧ P2 ⇒ Q, ou seja, se é válida a implicação (𝑎 → 𝑏) ∧ 𝑎 ⇒ 𝑏.

Para isso, vamos montar a tabela-verdade de (𝑎 → 𝑏) ∧ 𝑎 e comparar com a tabela-verdade de 𝑏, de forma a avaliar se é válida a relação de implicação entre premissas e conclusão.

FIGURA 1.1

Repetimos a coluna de 𝑏 na última coluna da estrutura apenas para facilitar a visualização.

Em cada uma das 4 linhas, não devemos encontrar o estado VF da coluna verde para a coluna roxa, caso a relação de implicação seja verdadeira.

Observe que a alternativa VF não ocorreu em nenhuma linha, quando comparamos uma coluna com a outra. Isso significa que é válida a relação (𝑎 → 𝑏) ∧ 𝑎 ⇒ 𝑏.

Consequentemente, sabemos que o argumento 𝑎 → 𝑏, 𝑎 ⊢ 𝑏 é um argumento válido.

Na prática, esse formato válido representa que, se 𝑎 → 𝑏 e 𝑎 forem premissas verdadeiras dentro do contexto no qual se encontram, necessariamente, 𝑏 será uma conclusão verdadeira. Isso ocorre em razão da própria estrutura formal do argumento. 

### Regras de inferência

Inferência é o processo pelo qual afirmamos a verdade de uma proposição (Q) em decorrência de sua ligação com outras, já assumidas como verdadeiras (P).

As regras de inferência nada mais são do que argumentos válidos notáveis, utilizados frequentemente na dedução de proposições de conclusão. 

Apresentaremos as regras de inferência no formato vertical para facilitar sua visualização.

É interessante que, ao ler as premissas em linguagem corrente, você procure deduzir a conclusão do argumento por conta própria.

Fazendo isso você cria familiaridade com cada estrutura argumentativa abordada.

Todas as premissas serão consideradas como fatos conhecidos, ou seja, proposições verdadeiras, o que nos leva a conclusões também verdadeiras.

### Regras de inferência

𝑎: Eu falo inglês. (V)
𝑏: Eu falo espanhol. (V) 
𝑎 ∧ 𝑏: Portanto, eu falo inglês e espanhol. (V)
Resulta na implicação válida: (𝑎 → 𝑏) ∧ 𝑎 ⇒ 𝑏.

Modus Ponens (MP)
a → b (P1)
a (P2)
---
∴ b (Q)

Temos uma condicional entre duas proposições, 𝑎 → 𝑏, considerada verdadeira. 

A outra premissa afirma que o antecedente dessa condicional, 𝑎, é verdadeiro. 

Com isso, podemos inferir corretamente que o consequente, 𝑏, também será verdadeiro, afinal, se a condicional era verdadeira e a causa aconteceu, a consequência também deve acontecer. 

Acompanhe o exemplo:

𝑎 → 𝑏: Se Maria nasceu em SP, então ela é brasileira. (V) 
𝑎: Maria nasceu em SP. (V)
𝑏: Logo, Maria é brasileira. (V)

### Pergunta

Posso dizer que sou amigo de Carlos, porque temos os mesmos gostos.
Qual é a conclusão e a(s) premissa(s) do argumento acima?

a- Não se trata de um argumento.
b- "Sou amigo de Carlos", essa é a conclusão e a premissa é "temos os mesmos gostos".
c- "Sou amigo de Carlos", essa é a premissa e a conclusão é "temos os mesmos gostos".
d- A conclusão é que "temos os mesmos gostos" e a premissa é "somos amigos".
e- A conclusão é que "somos amigos" e a premissa é "temos os mesmos gostos".

A resposta certa é a letra B.





