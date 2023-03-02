# Aula 04

### Validação por fluxogramas

O método por fluxogramas é o último método de validação de argumentos que veremos.

Ele serve tanto para provar que um argumento é válido quanto para testar sua validade, em 
casos de dúvida. 

Para que seja aplicado corretamente, é importante estar ciente das definições das operações 
lógicas, assim como das técnicas de dedução por demonstração, pois os mesmos artifícios 
podem ser aplicados aqui. 

Desse modo, o fluxograma constitui um método alternativo às 
tabelas-verdade no teste de um argumento, no qual ilustramos 
o raciocínio, partindo das premissas até a conclusão.

Para aplicar esse método, devemos, primeiro, considerar as premissas verdadeiras.

Depois, aplicamos, etapa a etapa, as definições das operações lógicas em questão, até 
atingir a conclusão.

O fluxo de trabalho é indicado por setas, e cada proposição trabalhada é exposta dentro de 
uma estrutura retangular, de forma a compor a representação visual do raciocínio.

Seguimos o fluxo até atingir a proposição de conclusão. 

Caso ela seja verdadeira, o argumento é válido, do ponto de vista formal.

Caso ocorram situações em que não podemos provar o valor 
lógico da conclusão, ou ocorra uma contradição, o argumento 
é inválido. 

Vamos acompanhar a seguir exemplos em que fluxogramas 
relativamente simples são construídos, passo a passo.

Exemplo:

Por meio de um fluxograma, teste a validade do seguinte argumento: 𝑎 → 𝑏, ~𝑏 ⊢ ~𝑎.

Resolução: 

Vamos ver como um fluxograma pode nos mostrar que esse é um argumento válido.

Passo 1. Primeiro, vamos dispor as premissas do 
argumento em retângulos e indicar que consideramos 
cada uma delas verdadeiras.

    1: a → b = V       ~ b = V

Passo 2

Agora, vamos analisar as premissas e 
começar a fazer inferências com base 
nas definições dos operadores lógicos 
presentes. 

Se há uma proposição isolada, como é o 
caso de ~𝑏, procure começar por ela. 

Se sabemos que ~𝑏 é verdade, pela definição 
do operador de negação, sabemos que 𝑏 é 
falso, certo?

Vamos, então, puxar uma seta do retângulo 
original para baixo, para dispor essa 
inferência que acabamos de fazer.

    1: a → b = V       ~ b = V
                        ||
                        \/
    2:                  b = F

Passo 3

Perceba, agora, que a proposição 𝑏 aparece na premissa posicionada à esquerda.

Já sabemos o seu valor lógico.

Podemos, então, substituir nome da proposição pelo seu próprio valor lógico.

Faremos isso puxando uma seta para a esquerda, de forma a indicar que 𝑏 será inserido na 
proposição à esquerda. 

Puxaremos, também, uma seta para baixo, de forma a puxar a proposição original para 
baixo, assim conseguimos expor graficamente a substituição.

    1: a → b = V           ~ b = V
        ||                   ||
        ||                   \/
    2:   || <-------------- b = F
        ||
        \/
    3: a → F = V
 
Passo 4

Temos uma nova inferência para fazer, nesse momento, a partir de 𝑎 → F = V.

Para isso, devemos nos lembrar como a operação condicional funciona: seu resultado é falso 
apenas quando o antecedente é verdadeiro e o consequente é falso. 

Já sabemos que o consequente é falso.

Por estarmos lidando com uma premissa, sabemos que o resultado precisa ser 
considerado verdadeiro.

Logo, a única possibilidade que permite ter uma proposição 
composta verdadeira com um consequente falso é 
considerando o antecedente falso.

Com isso, sabemos que, necessariamente, 𝑎 = F.

Indicaremos isso em um novo retângulo abaixo da inscrição 
original, puxando uma seta para baixo.

    1:   a → b = V              ~ b = V
            ||                      ||
            ||                      \/
    2:      || <----------------  b = F
            ||
            ||
            \/
    3:   a → F = V
            ||
            ||
            ||
            \/
    4:    a = F

Passo 5

Já conseguiremos, agora, afirmar que a conclusão é verdadeira.

Ora, a conclusão do argumento é ~𝑎.

Se sabemos que 𝑎 = F, necessariamente, ~𝑎 = V.

Indicaremos isso em um novo retângulo, abaixo da indicação 𝑎 = F.

Como provamos que a conclusão é verdadeira, terminamos o nosso trabalho.

O fluxograma completo é exposto a seguir.

Perceba que cada premissa cria uma espécie de coluna 
no fluxograma, e suas inferências e substituições são 
feitas respeitando a disposição dessas colunas. 

Repare, também, que as setas indicam o “caminho” 
que seguimos.

Repare, também, que as setas indicam o “caminho” 
que seguimos.

    1:   a → b = V              ~ b = V
            ||                      ||
            ||                      \/
    2:      || <----------------  b = F
            ||
            ||
            \/
    3:   a → F = V
            ||
            ||
            ||
            \/
    4:    a = F

    5:    ~a = V

### Pergunta

Para a validação por Fluxograma, assinale a seguir qual dos passos é responsável pelo dizer:

"Vamos dispor as premissas do argumento em retângulos e indicar que consideramos cada 
uma delas verdadeira".

a- Passo 1.
b- Passo 2.
c- Passo 3.
d- Passo 4.
e- Passo 5.

A resosta certa é a letra A.

