# Aula 04

### Troca de mensagem

Semáforos e monitores não permitem troca de informações entre máquinas, que é primordial no mundo dos sistemas distribuídos. Para essa condição, temos a troca de mensagens, que usa dois instrumentos: envio e recebimento, que devem ser colocados em rotinas de biblioteca.

Num ambiente de rede, um dos principais problemas é a perde de pacotes causados por algum motivador.

No caso da troca de mensagem entre máquinas, isso se dá por meio da rede e, como apresentado, essa mensagem pode ser extraviada ao longo do percurso.

### Escalonamento

Qunaod temos uma única CPU, ou uma máquina CPU disponível entre as diversas existentes no sistema, e mais de um processo estiver competindo para ser executado, então, caberá ao sistema operacional escolher qual dos processos será privilegiado e essa escolha chama-se algoritmo de escalonamento.

Em linhas gerais, o escalonamento é importante porque, dentre vários processos, á saudável que o sistema priorize aqueles que vão gerar mais impacto ao ambiente e seus usuários, caso não forem privilegiados durante a escolha de quem deve ser o próximo a ser processado.

Entre os processos, temos aqueles que passam a maior parte do tempo computando, computer bound(limitados pela CPU), enquanto outros passam a maior parte do tempo esperando por entrada e saída, I/O bound (limitados a entrada e a saída).

Devemos escalonar os processos em quatro situações descritas na sequência:

- Quando temos os processos pai e filho para serem executados. A definição de qual deve ser priorizado, em muitos casos, é essencial para o perfeito funcionamento das tarefas e do resultado correto.

- Quando temos um processo que terminou e já não está mais no sistema, há a necessidade da escolha de um novo processo e, portanto, o escalonamento, nessa situação, faze-se necessário.

- Quando o processo é bloqueado por alguma razão, então, outro processo deve ser selecionado para ser executado. Processos predecessores podem ser priorizados, pois, se forem executados os sucessore, pode haver dependências que irão gerar resultados inconsistentes.

- Ao ocorrer uma interrupção de E/S, pode ser necessária uma decisão de escalonamento. Os algoritmos de escalonamento podem trabalhar tipicamente de duas formas: não antecipado e antecipado.

No primeiro caso, o processo "não antecipado" pode ficar executando pelo tempo que for necessário, ou seja, por horas até que seja bloqueado ou até que libere a CPU.

No segundo, o algoritmo de escalonamento antecipado escolhe um processo e o deixa em execução por tempo máximo fixado.

Até, aproximadamente, o primeiro quarto dos anos 2000, as memórias RAM (também conhecidas como memória principal) eram extremamentes caras. Ficávamos completamente pasmos se comparássemos o valor dos pentes de memória em relação ao valor total do computador.

E como era possível ter programas tão eficientes com tão pouca memória? Na realidade, a resposta é dividida em duas partes. A primeiroa é que o programador daqulela epoca também conhecia as entranhas do computador e programar era algo qu exigia mais do que conhecimentos da linguagem de programação versus a necessidade de negócios que estava motivando aquele projeto.

Por isso, o programador, tipicamente, tinha que tirar "leite de pedra". A outra parte da resposta é que não tinhamos as múltiplas interfaces entre aplicações em rede, nem ambientes de trabalho com tanta qualidade gráfica, nem mesmo a complexidade que os programas atuais possuem.

### Introdução a gerencimaneto de memória

No sistema operacional, a parte parcialmente responsável por gerencia a hierarquia de memória é o gerenciador de memória, que tem como tarefa conhecer todo o espaço de memória, alocar para os processos que estão necessitando e liberar as partes que não estão mais em uso pelos processos.

Memória ROM - Sistema Operacional ou drivers
Memória RAM - Programa do Usuário ou programa do usuário e sistema operacional

Depende do caso.

Nos sistemas precursores não era possível mais que um programa ocupando a memória. Se isso ocorresse, causaria problemas aos dois programas, ao que estava na memória e aquele que tentasse fazer o uso.

Com o avanço e a necessidade de múltiplas aplicações em funcionamento simultaneamente, a opção encontrada foi o uso de swapping, ou seja, troca de processos.

Isso consiste no sistema operacional pegar o conteúdo completo da memória e movê-lo para um arquivo na memória em disco rígido e, subsequentemente, liberar a memória para o próximo processo.

Entretanto, no hardware também houve avanço que não demandava somente a troca de processos executada por software (pelo sistema operacional).

Esse processo consiste em dividir a memórial principal em blocos de 2 KB com chave de proteção de 4 bits para cada bloco e mantidas em registradores especiais dentro da CPU. Porém, nesse caso a divisão da memória em blocos, há "um problema quando se usa mais de um programa".

Os dois programas referenciam a memória física absoluta, enquanto, na relaidade, queriamos que cada programa referenciasse um conjunto de endereços.

Portanto, a solução é a realocação estática ou, em outras palavras, esse mecanismo de rotação visa a a rotular blocos da memória com uma chave de proteção e comparar a chave do processo em execução com a de cada palavra da memória recuperada.

### Pergunta

O escalonamento é importante porque, dentre vários processos, é saudável que o sistema priorize aqueles que vão gerar mais impacto ao ambiente e seus usuários,caso não forem privilegiados durante a escolha de quem deve ser o próximo a ser processado.

A partir dessa definição podemos afirmar:

|-  Os algoritmos de escalonamento podem trabalhar tipicamente de duas formas: não antecipado e antecipado.
||- O processo “não antecipado” pode ficar executando pelo tempo que for necessário até que seja bloqueado ou até que libere a CPU.
|||- O algoritmo de escalonamento antecipado escolhe um processo e o deixa em execução por tempo máximo fixado.

De acordo com o material estudado na unidade, selecione a alternativa que contém as afirmações corretas:

a- Apenas a I afirmação.
b- Apenas a II afirmação.
c-  Apenas a III afirmação.
d- Todas as afirmações.
e- Nenhuma das afirmações.

A resposta certa é a letra D.


