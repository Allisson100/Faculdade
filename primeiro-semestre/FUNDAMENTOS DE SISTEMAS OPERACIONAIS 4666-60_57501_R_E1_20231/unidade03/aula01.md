# Aula 01

Os sistemas computacionais atuais são capazes de desenvolver uma grande variedade de tarefas simultaneamente.

Em todos os sistemas com suposto conceito de paralelismo, temos a CPU trabalhando por algumas dezenas ou centenas de milissegundos numa única aplicação e subsequente na próxima até o ciclo se completar.

Somente nos casos de sistemas com múltiplos processadores é que teremos de fato múltiplos programas sendo atendidos no mesmo instante. Controlar múltiplas atividades em parelelo é algo que vem sendo desenvolvido e aprimorado com base num modelo conceitual de processos sequenciais que facilita o paralelismo.

Todos os computadores são capazes de fazer várias coisas ao mesmo tempo:

- Executar um programa 
- Ler dados do disco 
- Exibir mensagem na tela.

Tudo sendo executado "ao mesmo tempo".

Esse mecanismo de trocas rápidas é chamado de multiprogramação.

### Processo

Os softwares de computador são organizados em processo sequenciais.

Um processo é um programa em execução, acompanhado dos valores correntes do contador de programa, dos registradores e das variáveis.

Uma CPU pode executar um processo por vez.

Vale destacar que um processo e um programa possuem conceitos distintos, sendo que o processo constitui uma atividade , possuindo programa, entrada, saída e um estado.

Os processos podem conter mais de uma tarefa, conceituando, então, que tarefa e processo são distintos.

### Criação de processos

Processos são criados e destruídos constantemente nos sistemas.

Essas operações disponibilizam aplicações por meio de chamadas de sistemas que diferem entre sistemas operacionais.

Para os sistemas de propósitos gerais, é necessário algum mecanismo para criar e terminar processos durante a operação quando for necessário.

Teremos nos sistemas quatro eventos que fazem que processos sejam criados: no início do sistema, um processo em execução procedendo a uma chamada de sistema de criação de um processo, requisição do usuário para criar um novo processo e gerenciar a tarefa em lote (batch job) que está sendo iniciada.

Ao iniciar o sistema operacional, tipicamente vários processos são criados. Entre esses processos, temos os que estão em primeiro plano e interagindo com o usuário e outros que estão em segundo plano, portanto, não estão diretamente interagindo com o usuário.

Para exemplificar umm processo em segundo plano, podemos pegar o caso de um servidor FTP (File Transfer Protocol) que fica inativo durante boa parte do tempo, sendo ativado somente quando um cliente FTP solicita a abertura de uma nova conexão - usamos o termo daemons para descrever processos que fica em segundo plano com a finalidade de lidar com atividade como a descrita.

Podemos falar também sobre o antivírus, que o usuário não mexe nele, porém ele está sendo executado em segundo plano.

Processos que estão em execução podem fazer chamadas de sistema (system calls) para criar um ou mais processos.

Criar processos é indicado quando a tarefa a ser executada puder ser facilmente dividida em vários processos relacionados, interagindo, entretanto, de maneira independente.

Os usuários podem iniciar um novo processo começando um programa no ambiente GUI ou no ambiente Shell.

No caso de sistemas em lot, tipicamente encontrados em computadores de grande porte, o usuário, administrador ou até mesmo alinhamento prévio, pode submeter tarefa em lote para sistema.

O sistema operacional criará um novo processo e o executará quando tiver recurso disponível e/ou redefinindo prioridades e executando o processo no momento determinado.

Se usarmos como exemplo o ambiente Unix, teremos a chamada de sistema fork para criar um processo. Essa chamada cria uma réplica do processo solicitante.

No ambiente Windows, uma única chamada denominada CreateProcess de função do Win32 trata o processo de criação e carga do programa correto no novo processo.

O processo Win32 possui dezenas funções para gerenciar e sincronizar processos e tópicos relacionados.

Tanto no Unix quanto no Windows, quando um novo processo filho é criado, o processo pai e filho possuirão seus próprios espaços de endereçamento de memória, prmitindo, assim, que se o processo pai ou filho alterar uma palavra em seu espeçao de endereçamento, a mudança não impacte o outro processo.

### Término de processos 

Após o término, o processo é finalizado com base nas quatros condições típicas: normal, por erro, erro fatal e cancelado por terceiros - sendo as duas primeiras voluntárias e as duas últimas involuntárias.

Processos terminados de forma involuntária não são comuns num sistema em perfeito funcionamento (verificamos as quatros condições e notaremos por qual motivo essa afirmação é um fato).

O primeiro caso, que é a condição normal de se encerrar um processo, é verificado pela chamada exit no Unix ou ExitProcess no Windows. Nesses casos, o processo termina após finalizar as tarefas que estavem previstas, mesmo que seja um usuário finalizando um programa, fechando a janela no ambiente GUI ou pela opção relativa no ambiente Shell.

Num ambiente Unix, a chamada de sistema exist serve para informar ao núcleo do sisteam operacional que o processo em questão não é mais necessário e pode ser eliminado, liberando todos os recursos a ele empregados.

Processos podem solicitar ao núcleo o encerramento de outros processos, mas essa operação só é aplicável a processos do mesmo usuário ou se o processo solicitante pertencer ao administrador do sistema.

Os processos que interagem com outros não podem ser concluídos quando algum parâmetro errado é fornecido.

Vamos considerar o caso de um usuário tentando colocar o nome duplicado entre dois arquivos no sistema, então, uma caixa de diálogo emerge e pergunta ao usuário se ele quer tentar novamente; desta forma, teremos por consequência a segunda condição que é a saída por erro.

Erro fatal é um erro causado pelo processo e, normalmente, por um erro de programa. Como exemplo podemos ter a execução de uma instrução ilegal, a referência à memória inexistente ou a divisão por zero; em todos esses casos, teremos como resultado um erro fatal.

O cancelamento por outro processo ocorre quando um processo x executa uma chamda de sistema determinando que o sistema operacional cancele outro(s) processo(s) n.

Tanto o Unix/Linux, a chamada é o kill, no ambiente Windows, a função Win31 correspondente é a TerminateProcess.

### Pergunta

Verifique as afirmações a seguir sobre a “criação de processos”:

|- Processos são criados e destruídos constantemente nos sistemas. 
||- Para os sistemas de propósitos gerais, é necessário algum mecanismo para criar e terminar processos durante a operação quando for necessário.
|||- Temos nos sistemas quatro eventos que fazem que processos sejam criados: no início do sistema, um processo em execução procedendo a uma chamada de sistema de criação de um processo, requisição do usuário para criar um novo processo e uma tarefa em lote sendo iniciada. 

Selecione a alternativa que contém as afirmações corretas:

a-  Apenas a I afirmação.
b- Apenas a II afirmação.
c- Apenas a III afirmação.
d- Todas as afirmações.
e-  Nenhuma das afirmações.

A resposta certa é a letra D.






