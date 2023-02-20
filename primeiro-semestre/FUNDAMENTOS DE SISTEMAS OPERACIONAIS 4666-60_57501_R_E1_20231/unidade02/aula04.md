# Aula 04

Dispositivos de entradas são aqueles que mandar informações para o sistema operacional, por exemplos: teclados, microfones, etc.

Dispositivos de saida são os monitores por exemplo, pois eles mostram a imagem na tela. E a impressora também é um exemplo.

Dispositivos E/S;

- São geralmentes os controladores e os dispositivos.

- O controlador é formado por um ou mais chips numa placa; esses controladores possuem a função de receber os comandos do sistema operacional e gerar as instruções mais adequadas para os dispositivos, fornecendo orientação exatamente de como o disco rígido armazena e acessa os dados, por exemplo.

- Os dispositivos possuem interfaces bastantes padronizadas. Isso ajuda, porque a controladora IDE pode controlar qualquer disco IDE.

- Estre o sistema operacional e o controlador, há outro software chamado driver de dispositivo.

- É função do driver de dispositivo se comunicar com o controlador, emitindo comando e recebendo respostas.

- Os fabricantes de cotroladores devem fornecer drivers específicos para cada sistema operacional a que dão suporte.

- Existem três maneiras diferentes para entra e saída (E/S): o método mais  simples é quando o programa de um usuário emite uma chamada de sistema, então o núcleo do sistema operacional a traduz em chamada ao driver relacionado, em seguida, o driver inicia a entrada e saída  e fica em constante checagem se o dispositivo terminou a operação; quando a operação é finalizada, o driver coloca os dados onde são necessários; o sistema operacional, então, remete o controle para quem originou a chamada.

- Nesse processo, a CPU fica ocupada durante a monitoração se a operação de E/S terminou ou não.

- No segundo método, o driver inicia o dispositivo e intrui que ele o informe quando terminar; durante esse período de intervalo, o sistema operacional retoma o controle da CPU para executar outra tarefa. Assim que o controlador recebe a informação do final da transferência, ele gerará uma interrupção para sinaliza o término.

- O DMA(Direct Memory Access) é o terceiro método para a implementação de entrada e saída. Nesse cenário, é utilizado um chip especial de acesso direto à memória, controlando o fluxo de bits entre a memória e algum controlador sem intervenção constante da CPU. Nesse processo, a CPU configura o chip DMA informando a quantidade de bytes que devem ser transferidos, e a direção. Então, a execução fica a cargo do DMA. Assim que o DMA finalizar a tarefa, haverá uma interrupção.

### Barramento

- O termo barramento é definido como elos de comunicação que consistem em um conjunto de vias.

- Ao longo da evolução da arquitetura computacional, os barramentos foram tomando forma mais heterogênea e estruturada para as necessidades modernas.

- Os processadores e memórias foram ficando cada vez mais velozes, e o computador antigo, que inicialemnte tinha somente um barramento, passou a não mais dar conta.

- A CPU se comunica com o  barramento   PCI por meio do barramento local que, por sua vez, se comunica com a memória por intermédio de um barramento dedicado. Usando, por exemplo, um sistema Pentium com um cache de nivel 1 dentro do chipe e uma cache de nível 2 mutio maior que fica na parte externa do chip e é concetada à CPU pelo barramento cache.

- Esse sistema contém também três barramentos específicos: IDE, USB, SCSI. O barramento IDE, como descrito anteriormente, pode ser usado para conectar discos físicos e unidade de CD-ROM.

O padrão USB foi desenvolvido por um consórcio de emepresas, entre as quais podemos citar: Microsoft, Apple, NEC, Intel, etc.

- Uma das carcterísticas fundamentais para o sucesso do USB, principalmente pela demanda de agilidade de interoperabilidade, é que esta tecnologia compartilha o mesmo driver entre os seus dispositivos, tornando dispensável instalar um novo driver para cada novo dispositivo USB.

- Isso traz como benefício maior o fato de podermos instalar dispositivos USB no computador sem precisar reiniciá-lo, ou seja, pluig and play.



Além da estrutura de hardware em que está montado o sistema operacional, os conceitos típicos sobre os quais todos os sistemas operacionais são contruídos são:

- Processo;
- Gerenciamento de memória;
- Gerenciamento E/S;
- Sistema de arquivos;
- Segurança

Os sistemas operacionais são, geralmente, entre outros, estruturados conforme as classificações abaixo:

- Sistema monolítico;
- Hierarquia de camadas;
- Micronúcleo;
- Sistema de máquina virtual;

- Exonúcleo: tem como finalidade permitir que uma aplicação solicite uma região específica da memória, simplesmente para assegurar que os recursos pedidos estejam disponíveis e que os recursos pedidos estejam disponíveis e que o programa tenha direito de acessá-los;

- Modelo cliente servidor

### Pergunta

O termo barramento é definido como elos de comunicação que consistem em um conjunto de vias. Ao longo da evolução da arquitetura computacional, os barramentos foram tomando forma mais heterogênea e estruturada para as necessidades modernas.

Sobre a comunicação da CPU e o barramento, é correto afirmar que:

a- A CPU se comunica com o barramento PCI por meio do barramento local. 
b- A CPU se comunica com o barramento PCI por meio da memória.
c- A CPU se comunica com o barramento PCI por meio do HD.
d- A CPU se comunica com o barramento PCI por meio do teclado e mouse.
e- A CPU se comunica com o barramento PCI por meio do barramento externo que, por sua vez, se comunica com a memória por intermédio de um barramento interno.

A respota comrreta é a letra A.


