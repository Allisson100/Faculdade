# Aula 02

### Falácias formais

Alguns argumentos lógicos têm aparência de válidos, mas não são.

A esses argumentos, damos o nome de falácias. 

Portanto, falácias são argumentos inválidos, comumente proferidos por falta de atenção.

Quando falamos de falácias formais, procuramos erros na estrutura formal do argumento. 

Vamos, a seguir, avaliar a estrutura das duas principais falácias formais.

### Falácia da afirmação do consequente

Considere o argumento a seguir:

𝑎 → 𝑏: Se Mizu for um cachorro, então tem quatro patas. 
𝑏: Mizu tem quatro patas. 
𝑎: Logo, Mizu é um cachorro.

Nesse cenário, não podemos afirmar que Mizu é um cachorro, pois a única informação que temos sobre Mizu é que se trata de um ser de quatro patas.

Com isso, podemos estar falando de um coelho, de um gato, de um cavalo, de um cachorro, ou qualquer outro ser de quatro patas.

A conclusão, portanto, não é necessariamente verdadeira.

### Validação por tabelas-verdade

Esse método serve tanto para provar que um argumento é válido, quanto para testar sua validade, em casos de dúvida.

Para isso, testamos se a conjunção das premissas implica a conclusão.

Por isso, esse método, por mais que seja sistemático e relativamente simples, não costuma ser muito utilizado, já que o processo pode ser muito extenso.

Valide, por meio de tabelas-verdade, o argumento disposto a seguir:

- Se Alexandre não vai à praia, então Célia faz o almoço.
- Se Célia faz o almoço, então Vanda não almoça no restaurante. 
- Vanda almoça no restaurante ou Guilherme lava as verduras. 
- Portanto, se Guilherme não lava as verduras, Alexandre vai à praia.

Resolução

O enunciado traz um argumento, em linguagem corrente, que podemos transformar em símbolos para que possamos trabalhar com ele.

Num primeiro momento, vamos identificar por uma letra minúscula cada uma das proposições simples que compõem o argumento.

Usaremos letras de 𝑎 a 𝑑.

~𝑎 → 𝑏: Se Alexandre não vai à praia, então Célia faz o almoço. (P1)
𝑏 → ~𝑐: Se Célia faz o almoço, então Vanda não almoça no restaurante. (P2)
𝑐 ∨ 𝑑: Vanda almoça no restaurante ou Guilherme lava as verduras. (P3) 
~𝑑 → 𝑎: Portanto, se Guilherme não lava as verduras, Alexandre vai à praia. (Q)

Podemos, então, dispor o argumento de forma simbólica.

~𝑎 → 𝑏,𝑏 → ~𝑐,𝑐 ∨ 𝑑 ⊢ ~𝑑 → �

𝑎: Alexandre vai à praia. 
𝑏: Célia faz o almoço.
𝑐: Vanda almoça no restaurante.
𝑑: Guilherme lava as verduras. 

Agora, vamos transformar cada uma das premissas e a conclusão em símbolos, levando como base as letras de identificação de proposições simples.

No argumento em linguagem corrente, cada premissa é separada da outra por pontos finais.

Temos, portanto, três premissas.

A conclusão é a última sentença apresentada, iniciada pelo termo “portanto”.

Esse argumento resulta na implicação: 

(~𝑎 → 𝑏) ∧ (𝑏 → ~𝑐) ∧ (𝑐 ∨ 𝑑) ⇒ ~𝑑 → 𝑎. 

Por meio de tabelas-verdade, vamos verificar se aimplicação é válida.

Para quatro proposições simples, precisaremos de 16 linhas em nossa tabela.

Pelos resultados da tabela, vemos que a conjunção de premissas implica a conclusão. 

Com isso, sabemos que o argumento apresentado no enunciado é um argumento válido.

FIGURA 1.2

### Validação por regras de inferência

Podemos encadear as regras de inferência para testarmos a validade de argumentos lógicos.

Essa prática é conhecida na literatura como prova.

Nas provas, podemos utilizar não apenas as regras de inferência, mas também as equivalências notáveis estudadas.

Toda equivalência funciona, também, como uma regra de inferência.

Dependendo do argumento em questão, podem ser adicionados alguns artifícios de dedução. 

Com isso, temos três tipos principais de dedução por regras de inferência: prova direta, prova condicional e prova por redução ao absurdo.

### Pergunta

Todos os homens são mortais. Sócrates é homem, portanto Sócrates é mortal.
Sobre o argumento acima, é correto afirmar que:

a- Se trata de um non-sequitur.
b- Se trata de um argumento válido.
c- Se trata de uma falsa analogia.
d- Se trata de uma petição de princípio.
e- Se trata de um entendimento.

A resposta é a letra B.


