# Aula 04

### Abstração - espaços de endereçamento da memória

Expor a memória física aos processos pode trazer problemas, chegando até a ocasionar o travamento do sistema operacional. 

Entretanto, hoje, depois da história toda ter acontecido, sabemos que existe um método para tratar essa situação, caso contrário, não seria possível estarmos com o nosso computador conectado à internet, acessando o editor de texto e/ou diversas combinações que fazem parte do nosso dia a dia. Para isso, temos de entender o processo de abstração da memória.

Com a abstração da memória e a implantação do espaço de endereçamento, cria-se uma memória abstrata para abrigar os programas.

Esta, por sua vez, possui um conjunto de endereços usado para que o processo realize endereçamento à memória (os processos possuem seu próprio espaço de endereçamento, diferente para cada processo).

Se um processo maior que a área livre, ou um processo, mesmo que pequeno, porém, sem nenhuma área de memória, estiver disponível; então, esse processo deverá ser transferido para disco e ficará por lá até que memória suficiente seja liberada.

### Memória virtual

Diante da elevada demanda por memória, os programas eram criados em módulos. 

Dessa forma, ao carregar um programa, o gerenciador de módulo era quem, na realidade, seria carregado e, em seguida, a sobreposição zero. Quando necessário, era carregado à próxima sobreposição desse programa ou de outros. Todas as sobreposições ficam gravadas em disco.

A memória virtual possui dois aspectos importantes: o primeiro é a quantidade de memória fisicamente instalada no equipamento, que chamamos de memória real. 

O outro tem muito mais capacidade que o primeiro e chamamos de espaço de memória virtual. 

No hardware, temos um componente de extrema importância que é a Unidade de Gerenciamento de Memória (MMU). 

O MMU suporta o sistema operacional na execução do mapeamento dos endereços da memória física e endereços da memória virtual, permitindo, assim, a eficaz maestria de mover as partes dos programas da memória virtual para o disco ou vice-versa.

Analisando pela perspectiva do programa, temos cada um com seu próprio espaçamento de endereços adjacentes que chamamos de páginas.

### Paginação

A técnica chamada paginação é usada na maioria dos sistemas de memória virtual. A memória virtual é dividida em unidades de espaçamento de endereços adjacentes chamadas de páginas. Estas correspondem a unidades das memórias chamadas de frames.

Enquanto o espaço de endereçamento virtual é dividido em unidades chamadas páginas (pages), temos as unidades correspondentes na memória física que são denominadas molduras de página (frames). Tanto as páginas quanto as molduras possuem o mesmo tamanho.

### Segmentação

Além da paginação, a segmentação de memória é uma das formas mais simples para se obter a proteção da memória. 

Com o uso da segmentação são atendidos os seguintes requisitos:

- Pode haver vários segmentos distintos.
- Cada segmento pode ter um tamanho próprio.
- Cada segmento é constituído de uma sequência linear de endereços.
- O tamanho dos segmentos pode variar durante a execução.
- O tamanho de cada segmento de pilha pode ser expandido sempre que algo é colocado sobre ela e diminuído sempre que algo é retirado dela.
- Segmentos diferentes podem crescer ou diminuir independentemente e quando for necessário.

### Resumo da unidade três

Os processos são oferecidos pelos sistemas operacionais, ocupando cada qual o seu próprio espaço de endereçamento. Eles podem ser criados e terminados de maneira dinâmica, de forma a evitar que dois processos estejam em suas regiões críticas simultaneamente. Os semáforos, os monitores e as mensagens são as formas nas quais os processos comunicam-se entre si.

Estados do processo:

- Executando.
- Passível de ser executado.
- Bloqueado.

É possível que o processo troque de estado quando ele, ou um outro processo, executa uma das unidades básicas (semáforos, monitores ou mensagens).

Algoritmos de escalonamento são importantes para o ambiente e alguns sistemas fazem distinção entre mecanismo de escalonamento e política de escalonamento, permitindo aos usuários controle sobre o algoritmo de escalonamento.


Algoritmo de escalonamento é a escolha feita pelo sistema operacional de qual dos processos será privilegiado quando há uma única CPU, ou uma única CPU disponível entre as diversas existentes no sistema, e mais de um processo estiver competindo para ser executado.

Nos sistemas mais triviais, quando um programa é carregado em memória, ele ficará ocupando a memória necessária até que sua finalização aconteça.

Alguns sistemas permitem somente um processo por vez carregado na memória principal, enquanto outros suportam a multiprogramação.

Quando é necessário que o sistema operacional use mais memória principal (RAM), que realmente existe fisicamente na máquina, então, é necessária a troca de processos entre a memória principal e o disco. Os espaços de endereçamento de cada processo são divididos em blocos e são chamados de páginas. 

Na memória fica a moldura de página que recebe os blocos dos processos. O sistema de paginação ajuda no tratamento de estrutura de dados que alteram seus tamanhos durante a execução, simplificando a ligação, o compartilhamento e facilitando a proteção customizada para cada segmento.

Segmentação e paginação são tipicamente combinadaspara fornecer uma memória virtual bidimensional.


### Pergunta

A técnica chamada paginação é usada na maioria dos sistemas de memória virtual. A memória virtual é dividida em unidades de espaçamento de endereços adjacentes chamadas de páginas. 

Estas correspondem a unidades das memórias que são chamadas por qual termo?

a- Segmentação.
b- Memória principal (RAM).
c- Paginação.
d- Memória virtual.
e- Frames.

A resposta certa é letra E.