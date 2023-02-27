# Aula 02

### Programa x processo

O programa é o algoritmo que expressa uma notação adequada, expressa em um conjunto organizado de instrução em linguagem natural ou codificada.

O processo é uma atividade desempenhada pela CPU de ler o algoritmo, buscar os dados e executá-los segundo o algoritmo ordena.

A comunicação entre processos é algo frequente nos sistemas atuais, havendo a necessidade de obtermos uma comunicação estruturada e sem interrupções acontecendo entre eles.

Temos três tópicos importantes na comunicação entre processos:

- Como um processo passa a informação para outro;
- Como garantir que múltiplos processos não entrem em conflito;
- Como haverá uma sequência adequada quando existirem dependências.

### Condição de corrida

Processos que trabalham juntos podem compartilhar algum armazenamento comum e serem capazes de ler e escrever.

O armazenamento compartilhado pode estar na memória principal ou em um arquivo compartilhado.

Para entendermos o processo de condição de corrida, vamos considerar como exemplo um spool de impressão.

Para imprimir um arquivo, um processo entra com o nome do arquivo numa posição da fila em um diretório de spool. Em paralelo e de forma constante, o deamon de impressão verifica na fila se há algum arquivo para imprimir. Se houver algum arquivo para imprimir, ele será impresso e, em seguida, seu nome será removido da fila.

Ainda pensando no cenário para exemplificar nosssa condição de corrida, imagine que há duas variáveis compartilhadas, sendo uma de saída com o nome out que apontará para o próximo arquivo a ser impresso, e uma de entrada como o nome de in que apontará para a próxima pposição livre no diretório de impressão.

É extremamente exaustiva a atividade de análise, depuração e resolução de códigos de programa que apresentam condições de corrida.

São necessárias quatro condições elementares para chegarmos a uma boa solução:

- Dois ou mais processos nunca podem estar simultaneamente em suas regiões críticas.

- Nada pode ser definitivamente afirmado no que tange á velociadade ou ao número de cores.

- Nenhum processo executado fora da sua região crítica pode bloquear outros processos.

- Nenhum processo deve esperar infinitamente para estar em sua região crítica.

### Exclusão mútua com espera ociosa

Quando estamos usando os sistemas mais antigos que possuíam somente uma CPU com único core, a forma mais trivial e segura para evitarmos que mais de um processo entre na região crítica é aplicada com desativação das interrupções assim que o primeiro processo entrar na região crítica e consectuivamente reabilitá-la assim que sair dessa região.

Portanto, quando se desativa a interrupção, a CPU não poderá chavear para outro processo, com isso não tem como ocorrer a condição de corrida apresentada anteriormente.

Podemos concluir que a desativação das interrupções é uma técnica coerente para o próprio sistema operacional, porém com alto nível de risco para os processos dos usuários que necessitem de exlusão mútua.

Como vimos anteriormente, quando um processo estiver ativo e executando tarefas na região crítica, então, outros deveriam ficar "dormindo" até o término dessa tarefa.

### Monitores

O monitor tem um papel fundamental para realizar a exclusão mútua pelo fato de que somente um processo pode estar ativo em um monitor num determinado tempo x.

Tipicamente, quando um processo executa uma chamada a uma determinada rotina do monitor, algumas das primeiras instruções da rotina deverão verificar se existe outro processo ativo dentro do monitor.

Caso confirme que outro processo encontra-se ativo dentro do monitor, então, o processo que realizou a chamda ficará suspenso até que o processo que estava previamente ativo saia do monintor.

Um processo que executar uma chamada ao monitor poderá entrar somente se não houver outro previamente ativo.

O monitor é uma construção da linguagem de programação e os compiladores tratam suas chamdas e rotinas de modo diferente de outras chamadas de procedimento.

É função do compilador implantar a exclusão mútua. Tendo em vista que para codificar um monitor, quem codifica não necessáriamente tem de conhecer como o compilador implanta a exclusão mútua, então, basta ter em mente que convertendo todas as regiões críticas em rotinas do monnitor, dois ou mais processos nunca poderão entrar em suas regiões críticas ao mesmo tempo.

Além de maneiras simples pela qual o monitor consegue tratar as exclusões mútuas, ele também apresenta variáveis condicionais que possibilitam bloquear processos quando não puderem continuar.

Linguagens como C, Pascal e outras diversas não possuem monitores. Entretanto, o monitor foi projetado para resolver o problema de exclusão mútua em CPU, acessando memória comum, porem quando estamos usando um sistema distribuído formado por múltiplas CPUs e cada uma com sua própria memória privada e conectada por uma rede, os monitores passam a não ter efeito.

### Semáforos 

Como vimos anteriormente, quando um processo estivesse ativo e executando tarefas na região crítica, então, outros deveriam ficar “dormindo” até o término dessa tarefa. 

Um semáforo poderia conter o valor 0, indicando que nenhum sinal de acordar foi salvo, ou algum valor positivo, sinalizando que um ou mais sinais de acordar estivessem pendentes. 

### Pergunta

O monitor tem um papel fundamental para realizar a exclusão mútua pelo fato de que somente um processo pode estar ativo em um monitor num determinado tempo x. Tipicamente, quando um processo executa uma chamada a uma determinada rotina do monitor, algumas das primeiras instruções da rotina deverão realizar qual verificação?

a- Verificar se existe um processo inativo dentro do monitor.
b- Verificar se existe outro processo ativo dentro do monitor.
c- Verificar se existe outro processo inativo dentro do semáforo.
d- Verificar se existe outro processo ativo dentro do semáforo.
e- Verificar se existe outro processo a partir da condição de corrida.

A reposta certa é a letra B.

