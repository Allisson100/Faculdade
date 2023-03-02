# Aula 03

### Prova direta

Na prova direta, conseguimos provar diretamente, por meio das regras conhecidas, a validade dos argumentos propostos. 

Não é necessária a inclusão de um artifício de dedução.

Na demonstração da prova, numeramos as linhas e inserimos, em cada uma, uma proposição verdadeira. 

Começamos inserindo as premissas.

À direita, indicamos a justificativa da veracidade de cada afirmação.

Nossa demonstração da prova direta termina na linha em que conseguimos provar que a conclusão do argumento é verdadeira.

Acompanhe os exemplos a seguir, que serão resolvidos passo a passo.

Exemplo:

Por meio da prova direta, demonstre que ~𝑠 é verdade, quando consideramos as premissas 𝑡, 𝑡 → ~𝑞 e ~𝑞 → ~𝑠.

Resolução:

O enunciado nos entrega três premissas simbólicas, que devem nos levar até a conclusão ~𝑠.

Para isso, na demonstração da validade por prova direta, vamos listar as premissas e fazer inferências, até concluirmos ~𝑠.

Começaremos apenas listando cada uma das premissas, pois cada uma delas nos entrega diretamente uma verdade. Elas serão identificadas à direita.

Demonstração:

1. 𝑡 (P1)
2. 𝑡 → ~𝑞 (P2)
3. ~𝑞 → ~𝑠 (P3)

A partir de agora, devemos continuar a demonstração fazendo inferências.

Para isso, precisamos combinar as premissas entre si de forma a conseguirmos inferir novas verdades.

Uma das estratégias que podemos tomar é nos atentarmos, quando possível, a proposições simples listadas na demonstração. 

Em seguida, podemos procurar a letra que identifica essa proposição simples em outra linha e, com sorte, conseguiremos extrair alguma inferência.

Se considerarmos a premissa simples da linha 1, 𝑡, e combiná-la com a premissa da linha 2, 𝑡 → ~𝑞, temos o formato Modus Ponens, já que 𝑡 é a afirmação do antecedente de 𝑡 → ~𝑞.

Com isso, podemos fazer a inferência a seguir.

𝑡 → ~𝑞
𝑡
----
∴ ~𝑞

Podemos, agora, inserir ~𝑞 como uma nova verdade em nossa demonstração, justificando que sua origem foi uma inferência do tipo Modus Ponens entre as proposições das linhas 1 e 2. Essas informações darão origem à linha 4, exposta a seguir.

Demonstração: 

1. 𝑡 (P1) 
2. 𝑡 → ~𝑞 (P2) 
3. ~𝑞 → ~𝑠 (P3) 
4. ~𝑞 (MP, 1 e 2)

Continuando, podemos agora utilizar a informação da linha 4 para nossa próxima inferência.

Perceba que ~𝑞 é, justamente, a afirmação do antecedente da proposição da linha 3, ~𝑞 → ~𝑠. 

Com isso, podemos fazer outra inferência do tipo Modus Ponens, exposta a seguir:

~𝑞 → ~s
~𝑞
----
∴ ~𝑠

Perceba que a nossa inferência nos levou à conclusão do argumento, ~𝑠.

Isso nos levará à última linha da nossa demonstração, exposta a seguir.

Demonstração: 

1. 𝑡 (P1)
2. 𝑡 → ~𝑞 (P2) 
3. ~𝑞 → ~𝑠 (P3) 
4. ~𝑞 (MP, 1 e 2) 
5. ~𝑠 (MP, 3 e 4) 

Agora que conseguimos provar que a proposição ~𝑠 é verdadeira, está provado que o argumento é válido, já que a conclusão derivou logicamente das premissas.

### Prova condicional

A prova condicional é mais um tipo de prova demonstrativa, que utiliza regras de inferência e equivalências lógicas em suas inferências.

Sua aplicação é útil quando a conclusão do argumento tem o formato condicional.

Considere uma conclusão condicional do tipo 𝑎 → 𝑏, que precisa ser provada.

A prova condicional parte do princípio de que, se a relação P1 ∧ P2 ∧ ... ∧ Pn ∧ 𝑎 ⇒ 𝑏 for válida, P1 ∧ P2 ∧ ... ∧ Pn ⇒ 𝑎 → 𝑏 também será.

Para provar uma conclusão de formato 𝑎 → 𝑏, basta incluirmos o antecedente 𝑎 como uma premissa provisória (PP) e provar 𝑏. 

Se for possível chegar em 𝑏, provamos 𝑎 → 𝑏, de acordo com o princípio das relações de implicação expostos anteriormente.

Após a inclusão da premissa provisória, a demonstração ocorre de acordo com as mesmas regras já vistas na prova direta. Acompanhe os exemplos a seguir.

Exemplo:

A partir das premissas 𝑎 → 𝑏 e 𝑐 → ~𝑏, prove 𝑐 → ~𝑎.

Resolução:

Inicialmente, devemos reparar que o formato da conclusão, 𝑐 → ~𝑎, é condicional.

Na demonstração, devemos inserir as premissas normalmente e, em sequência, inserir a premissa provisória (PP), que corresponde ao antecedente da conclusão.

No caso, o formato da nossa PP será 𝑐. 

Com isso, nossa inferência termina quando conseguirmos provar que o consequente da conclusão, ~𝑎, é verdade.

A resolução será apresentada a seguir. 

Demonstração:

1. 𝑎 → 𝑏 (P1) 
2. 𝑐 → ~𝑏 (P2)
3. 𝑐 (PP) 
4. ~𝑏 (MP, 2 e 3)
5. ~𝑎 (MT, 1 e 4)
6. 𝑐 → ~𝑎 (Prova Condicional, 3 a 5)

Perceba que, na linha 5, chegamos à conclusão desejada.

Em seguida, na linha 6, colocamos a conclusão original do argumento, no formato condicional.

Entre parênteses indicamos que fizemos a prova condicional, indicando a linha a partir da qual inserimos a premissa provisória, 3, até a linha da nossa última inferência, 5.

### Prova por redução ao absurdo

A prova por redução ao absurdo (ou prova por contradição) é mais um tipo de prova demonstrativa que utiliza regras de inferência e equivalências lógicas em suas inferências.

Sua aplicação é geralmente restrita a casos em que a conclusão do argumento não tem o formato condicional e não se consegue obter a prova direta de forma tão simples.

Desse modo, a prova por redução ao absurdo oferece uma maneira alternativa de provaruma conclusão.

Para aplicar essa técnica, devemos introduzir a negação da conclusão do argumento como premissa e fazer inferências até atingir uma contradição. 

Basta, então, introduzir a negação da conclusão do argumento como premissa provisória (PP).

As inferências devem levar até uma contradição do tipo 𝑎 ∧ ~𝑎. 

No momento em que isso acontece, conseguimos provar que a conclusão original do argumento é verdadeira, o que faz com que o argumento seja considerado válido. Acompanhe os exemplos a seguir.

Exemplo: 

A partir das premissas 𝑎 → ~𝑏 e 𝑐 → 𝑏, prove ~(𝑎 ∧ 𝑐). 

Resolução: 

Para usarmos o método da prova por redução ao absurdo na demonstração, devemos inserir as premissas normalmente e, em seguida, inserir a premissa provisória (PP), que corresponde à negação da conclusão do argumento.

No caso, o formato da nossa PP será ~(~(𝑎 ∧ 𝑐)).

Com isso, nossa inferência termina quando conseguirmos provar uma contradição do tipo a ∧ ~a. A resolução será apresentada a seguir.

Demonstração: 

1. 𝑎 → ~𝑏 (P1)
2. 𝑐 → 𝑏 (P2)
3. ~(~(𝑎 ∧ 𝑐)) (PP)
4. 𝑎 ∧ 𝑐 (Dupla Negação, 3) 
5. 𝑎 (S, 4)
6. 𝑐 (S, 4)
7. ~𝑏 (MP, 1 e 5)
8. 𝑏 (MP, 2 e 6)
9. 𝑏 ∧ ~𝑏 (U, 7 e 8)
10. ~(𝑎 ∧ 𝑐) (Prova por Absurdo, 3 a 9)

Perceba que nas linhas 7 e 8 chegamos às conclusões de que ~𝑏 é verdade e que 𝑏 é verdade.

Podemos colocar esses dois resultados em apenas uma linha por meio da regra da União.

Na linha 9 afirmamos 𝑏 ∧ ~𝑏, que é uma contradição que corresponde ao formato 𝑎 ∧ ~𝑎. Inserimos uma linha 10, com a conclusão original do argumento, e indicamos, entre parênteses, que fizemos a prova por absurdo, indicando a linha a partir da qual inserimos a premissa provisória, 3, até a linha da nossa última inferência, 9.

### Pergunta

Dois dados usuais e não viciados são lançados. Sabe-se que os números observados são ímpares. Então, a probabilidade de que a soma deles seja 8 é:

a- 2/36
b- 1/6
c- 2/9
d- 1/4
e- 2/18

A resposta é a letra C.










