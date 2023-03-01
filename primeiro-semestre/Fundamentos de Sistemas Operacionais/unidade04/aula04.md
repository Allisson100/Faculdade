# Aula 04

### Teclado, mouse e monitor – visão geral

Nos computadores pessoais, os dispositivos, como teclado, mouse e monitor são praticamente indispensáveis. Mesmo os equipamentos portáteis, quando não munidos de mouse, possuem a opção do touch screen ou algum outro método que faz a função similar à do mouse.

Para os servidores de rede, nem sempre são disponibilizados teclados, mousee monitor. Isso acontece até por uma questão de economia de espaço ou até mesmo por segurança. Em muitas empresas de outsourcing o data center é praticamente uma sala apagada, ou seja, somente máquinas instaladas nos racks. Muitas vezes, em outro prédio, que pode estar a quilômetros de distância, fica a equipe técnica que suporta ou executa as atividades nos servidores.

Normalmente, quando acontece um problema mais específico, o operador do data center, que fica no próprio local onde estão os servidores, vai até o equipamento danificado com um console ou então faz uso do teclado, mouse e monitor. Em alguns casos é instalado, juntamente com os servidores, um conjunto com teclado, mouse e monitor embutido, que pode ser retraído e guardado de forma a não ocupar um espaço considerável. 

Esse dispositivo possui cabos e entradas para atender vários servidores, necessitando apenas selecionar por chave qual servidor quer obter controle e acesso.

### Software do teclado

Entre os dispositivos disponíveis para os usuários que servirão de entrada, temos o teclado, que possui um circuito impresso e um conjunto de teclas, sendo conectado ao computador por meio de uma porta serial ou USB. Toda vez que é pressionado ou liberado, uma interrupção é imediatamente gerada.

O código de varredura é o número composto por 7 bits e que irá compor uma identificação distinta para cada tecla, sendo necessário para o driver controlador o oitavo bit para definir se a tecla encontra-se pressionada (igual a zero) ou solta (igual a um).

Quando uma tecla é pressionada, o código da tecla é colocado no registrador de E/S. O driver é capaz de determinar se a tecla é minúscula, maiúscula, precedida de CRTL, ALT ou CTRL-ALT.

### Software do mouse

Os modelos de mouse mais antigos possuem internamente dois dispositivos mecânicos com pequenos orifícios. É fixado em um dos lados de cada roda um emissor de luz e do outro lado, o receptor. Conforme movimentação do mouse, a esfera de borracha irá, por consequência, girar as rodas perfuradas e, com base nos movimentos e passagem de luz por cada orifício, serão determinadas as coordenadas para os eixos "X" e "Y".

Os mouses ópticos modernos possuem um processador de imagens que, continuamente, tira fotos de baixa resolução da superfície e as compara em busca de alteração.

Quando é detectada a movimentação do mouse, com o botão sendo pressionado ou liberado, uma informação é enviada para o computador. As informações são compostas por três itens:

- Deslocamento do eixo 'X'.
- Deslocamento do eixo "Y".
- Informação dos botões.

### Resumo

O sistema de arquivos é um exemplo claro de abstração no mundo da computação. Pela visão do usuário, o sistema de arquivos é um conjunto de arquivos de sistema, documentos e figuras, todos dispostos em pastas de acordo com a necessidade do sistema e do usuário. Os usuários leigos no assunto não imaginam que os sistemas de arquivos possuem características intrínsecas de acordo com suas necessidades e plataformas. Há até usuários que tentam ler um arquivo que não é compatível entre sistemas de arquivos e mesmo assim dizem que existem problemas na máquina ou até mesmo que o arquivo está corrompido.

Os arquivos possuem características que permitem que sejam lidos e escritos (alterados); os diretórios podem ser criados e excluídos e também podem armazenar outros subdiretórios e arquivos “dentro deles”.

Arquivos contíguos, lista encadeada, tabelas de alocação de arquivos e i-nodes são possíveis formas de descobrir como o sistema operacional aloca a memória e monitorar qual bloco vai para qual arquivo.

As estruturas de diretórios podem ser diferentes entre os sistemas. Os atributos podem ficar nos diretórios ou em outro lugar, como no i-node. O espaço em disco pode ser gerenciado por listas de espaços livres ou mapas de bits.

Os sistemas mais modernos possuem mecanismos para melhorar a confiabilidade. Isso só é possível com técnicas de cópia incrementais e de programa que possa reparar sistemas de arquivos danificados.

Técnicas como a inclusão de cache de bloco, a leitura antecipada e a disposição de blocos relacionados próximos uns dos outros melhoram a performance do sistema de arquivos.

Diversos sistemas de arquivos foram comentados ao longo do material, porém, são somente uma pequena parte das opções existentes no mercado. Entretanto, são os sistemas de arquivos que estão na quase totalidade dos computadores no mundo.

O sistema de entrada e saída (E/S) pode ser implantado de três maneiras:

- E/S programada: a CPU escreve ou lê cada palavra ou byte, então espera em um laço estreito até que seja obtido ou haja possibilidade de enviar o próximo dado.

- E/S por interrupção: a CPU escreve ou lê cada palavra ou byte, então segue para outra tarefa até que ocorra uma interrupção informando a conclusão da E/S.

- E/S por DMA: um chip separado da CPU gerencia a transferência de um bloco de dados. Somente quando o bloco for totalmente transferido, então haverá uma interrupção.

Os quatro níveis de uma estrutura de E/S são:

- Rotinas dos serviços de interrupção.
- Drivers dos dispositivos.
- Software de E/S independente de dispositivo.
- Software de E/S do espaço do usuário.

Existem vários tipo de mídias, incluindo as magnéticas, ópticas e as tecnologias de RAID.

Estudamos os relógios com o objetivo do entendimento a respeito do controle do tempo real, da definição exata do tempo de execução dos processos, do tratamento de temporizadores e para fins de contabilidade.

Os terminais são estruturados com base em caracteres pontos, como as questões referentes aos caracteres especiais. Baseado na necessidade de controle que cada programa pode exigir são possíveis duas formas de entrada:

- Entrada em modo natural.

- Entrada em modo preparado.

Atualmente, quase que a totalidade dos computadores usam GUIs como saída. Os programas para as interfaces gráficas do usuário são baseados em eventos que são enviados para serem processados praticamente de imediato.

Em muitos sistemas em que é necessário pouco ou praticamente nada de “inteligência e capacidade de processamento” nas pontas, os equipamentos denominados “clientes magros” possuem vantagens quando comparados com os PCs tradicionais. Entre outras, o preço por unidade e a simplicidade dos dispositivos. 

Para os equipamentos portáteis que estão a cada dia conquistando mais o mercado de computadores, a bateria ainda é um ponto crucial.

Os programas podem contribuir para otimizar tarefas de tal forma que deem preferência à longevidade da carga da bateria, porém, sacrificando algo.

Esse mecanismo permite que os usuários que estejam em um local desprovido de fonte de energia externa para recarga da bateria ou sem bateria extra, tenham pelo menos mais alguns minutos de carga para continuar sua atividade.

### Pergunta

Entre os dispositivos disponíveis para os usuários, que servirão de entrada, temos o teclado que possui um circuito impresso e um conjunto de teclas sendo conectado ao computador por meio de uma porta serial ou USB. Toda vez que é pressionado ou liberado, uma interrupção é imediatamente gerada.

O código de varredura compõe uma identificação distinta para cada tecla. Por quantos bits ele é composto?

a- Composto por 7 bits.
b- Composto por 14 bits.
c- Composto por 21 bits.
d- Composto por 28 bits.
e- Composto por 35 bits.

A resposta certa é a letra A.

