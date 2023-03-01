### Aula 02

Sistemas operaconais

Embarcados:

- Um sistema operacional embarcado ou embutido é contruído para operar sobre um hardware com poucos recursos de processamento e armazenamento.

- Exemplos típicos são aparelhos de TV, repordutores MP3, aparelhos de DVD, etc. Um ponto positivo desses equipamentos que dependem deste tipo de sistema é que dificilmente será possível instalar algum software que não seja extremamente compatível, não permitindo o uso de software não confiável.

Exemplos desse sistema embarcado: QNX e VxWorks.

Tempo real:

- Esse sistema opercional é caracterizado por ter o tempo como parâmetro principal.

- Outras duas sundivisões são: sistemas de tempo real críticos, voltados tipicamente ao controle de processos industriais e militares, e os sistemas de tempo real não críticos, como os aplicados em sistemas de aúdio digital ou multimídia.

-  A grande diferença entre essas duas subcategorias é que, no caso de sistemas que dependem do tempo real crítico, eles não podem ter degradação de desempenho (como é o caso dos sitemas que controlam a linha de produção de veículos), já o não crítico, apesar de não desejado, se houver um pequeno atraso, não irá gerar tantos danos.

De computadores de grande porte:

- Sistema de grande porte é tipicamente utilizado por grandes corporações e, como carcterísticas predominantes desses sistemas, pode-se considerar a elevada capacidade de E/S(Entrada e Saída), sistema em lote (batch), processsamento de transações e tempo compartilhado.

Exemplos de sistema de grande porte são: OS/390 e S/400.

Multiprocessadores:
 
- O sistema operacional desta categoria pode tratar múltiplas CPUs simultaneamente. Equipamentos com multiprocessadores ou multinúcleos têm como objetivo principal melhorar a capacidade computacional dos equipamentos, trazendo melhor desempenho para o ambiente.

-  Com o advento dos processadores multinúcleos, até sistemas operacionais voltados para computadores pessoais estão começando a lidar com multiprocessadores.

Exemplos desse sistemas são Windows, Linux, Solaris e AIX.

Potáteis:

- Voltados para computadores como os PDA(Personal Digital Assistant) e telefones celualres.

- Os PDA e celulares não possuem disco rígido multigigabyte.

- Os sitemas operacionais pata portáteis são: Android, IOS, Symbian OS, Windows Mobile e Palm OS.

### Visão geral sobre hardware de computadores

- O hardware e o sistema operacional deverm ser extremamentes congruentes para que seja possível obter o melhor resultado desta combinação.

- Faz-se necessária uma homogeneidade entre os desenvolvedores de hardware e software.

- Independentes de ideologias, turma do harware e software, temos que ter conceitualmente um modelo pertinente à arquitetura do hardware de um computador pessoal para que possamos entender melhor os sistemas operacionais.

- Temos os barramento, que seria a nossa estrada, possibilitando a comunicação entre os elementos, a memória e os dispositivos de E/S.

Processadores:

- A CPU traz das memórias instruções, decodifica, interpreta a intruções a serem executadas e as executa; a partir daí, busca as intruções subsequentes e processa o ciclo novamente até ter instruções a serem executadas.

- Cada arquitetura de CPU tem um conjunto específico de instruções que pode executar.

- Todas as CPUs possuem registradores internos para armazenamento de variáveis importantes e de resultados temporários. Em adição aos registradores de propósito geral, usados para conter variáveis e resultados temporários, a maioria dos computadores possuem vários registradores especiais disponíveis de forma aparente para os programadores.

- O primeiro a se destacar é o contador de programa que contém o endereço de memória da próxima instrução a ser buscada, ou seja, ele é atualizado para apontar a próxima instrução.

- Outro registrador especial é o ponteiro de pilha, que aponta para o topo da pilha da memória, que contém uma estrutura para cada rotina chamada, mas que ainda não se finalizou. Uma estrutura de pilha da rotina contém oa prâmetros de entrada, as variáveis locais e as variáveis tamporárias que não são mantidas nos registradores.

- Outro registrador especial é o PSW (Program Status Word). Esse registrador contém os bits do código de condições, os quais são alterados pelas instruções de comparação, pelo nível de prioridade da CPU, pelo modo de execução e por vários outros bits de controle.

- CPUs modernas possuem recursos para executar mais de uma instrução em tempo concorrente, é o que chamamos de pipeline (elas podem executar uma busca, excutar decidificação e, simultaneamente, a execução de instrução).

Busca ===========> Decodificação =============> Execução

- Além do pipeline, temos o superescalar, esse tipo de processador possui múltiplas unidades de execução. Portanto, duas ou mais intruções são buscadas, decodificadas e armazenadas temporariamente em um buffer, até que possam ser executadas.

### Pergunta

Verifique as afirmações abaixo e selecione a opção que contém a referência correta do Sistema Operacional que se adequa com as características:

|- É tipicamente utilizado por grandes corporações.

|| -  Como características predominantes desses sistemas pode-se considerar a elevada capacidade de E/S, sistema em lote (batch), processamento de transações e tempo compartilhado.

a- Embarcados
b- Tempo Real 
c- Computadores de grande porte
d- Portáteis
e- Multiprocessadores

A resposta certa é a letra C.



