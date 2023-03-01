# Aula 03

### Introdução a gerenciamento de entrada e saída

Como foi descrito no primeiro capítulo desta série, o gerenciamento de entrada e saída tem como princípio básico a abstração, tornando a interação do programador com a máquina algo muito mais fácil e permitindo que os programas e os hardwares evoluam de forma independente, porém estruturada.

O gerenciamento de entrada e saída na visão de dentro do sistema operacional é algo complexo e que exige dos desenvolvedores de sistemas operacionais boa parte do tempo e dos esforços para obter um sistema estável e confiável. E não poderia ser diferente, pois toda a lógica e complexidade de controlar os diversos dispositivos demandam muita ação e dinamismo.

Estudaremos, a partir desse momento, os fundamentos do hardware de entrada e saída (E/S) e o software de E/S. Com esses conceitos poderemos tratar de dispositivos, como discos, relógios, teclados e vídeos.

### Dispositivos de entrada e saída

Os dispositivos de entrada e saída típicos e os que estaremos dando ênfase são divididos em duas categorias:

- Dispositivos de blocos: entre outras características, armazenam informações em blocos de tamanho fixo e endereço próprio. Todas as transferências estão em unidades consecutivas de um ou mais blocos. Para essa categoria, cada bloco pode ser lido ou escrito independentemente de todos os outros.

Pen drives, HD, etc.

- Dispositivos de caractere: nesse caso há o envio e recebimento de caracteres. Diferentemente da categoria anterior, os dispositivos de caractere não são endereçáveis e não possuem funcionalidades de posicionamento.

impressora, mouse, etc.

### Controladores de dispositivos (driver)

As unidades de entrada e saída típicas são constituídas por dois componentes:

- Componente mecânico:  é o dispositivo mais aparente para o usuário final, ou seja, impressora, teclado, mouse e outros. 

- Componente eletrônico: conhecido como controlador de dispositivo ou adaptador. Esses adaptadores são inseridos em um conector de expansão localizado na placa-mãe do computador.

Os componentes mecânicos e eletrônicos são mostrados em destaque na próxima figura.

FIGURA 1.3

### Software de E/S

Existem alguns pontos importantes para alinharmos quando estamos tratando de software de entrada e saída, os quais estão destacados a seguir:

O software de entrada e saída deve estar suportado pelo conceito de independência do hardware. Isso parte do pressuposto que deveria ser possível que os programas pudessem acessar os dispositivos de E/S sem a necessidade específica de conhecer o dispositivo. Então, um programa que tem no seu conjunto de funcionalidades a possibilidade de ler um arquivo de entrada deveria, de forma transparente e sem ter que mudar o programa, poder ler tanto um disco rígido, CD e DVD, quanto um USB.

Um outro ponto é que os programas de E/S deveriam estar alheios ao tratamento de erros, ficando a cargo dos níveis mais próximos ao hardware esse tratamento, ou seja, o controlador deveria resolver o problema e, se não conseguisse, então o driver do dispositivo deveria tratar.

Ainda primordial é o tipo de transferência síncrona ou assíncrona. Na transferência síncrona o modo é de bloqueio e na assíncrona é orientada a interrupção.

A utilização de buffers para armazenamento temporário envolve frequentes e elevadas operações de cópia, gerando um impacto considerável no desempenho da entrada e saída.

O último ponto que devemos nos atentar com a mesma importância dos apresentados anteriormente é o de dispositivos dedicados versus compartilhados. Pode parecer contraditório, porém, nos dias atuais os dispositivos não compartilhados (dedicados) podem apresentar grandes problemas, bem como impasses. Se imaginarmos dois processos necessitando acessar a mesma fita magnética, mas com dados em endereços distintos, certamente um dos processos ficará esperando por um tempo muito grande.

### Camadas de software de E/S

Conforme ilustrado na Figura, tipicamente, os softwares de E/S possuem quatro camadas e estão logo acima do hardware. Cada camada do software de entrada e saída tem função específica e interface com as camadas vizinhas.

FIGURA 1.4

Como cada sistema operacional possui características próprias do software de entrada e saída, é uma generalidade para estudos acadêmicos, sem entrar nos detalhes específicos de cada plataforma física e lógica.

### Hardware de E/S

Para todos os tipos de plataformas de computadores, necessitamos de algum tipo de dispositivo para informar entradas e receber resultados, constituindo o que chamamos genericamente de dispositivos de Entrada e Saída (E/S).

Com base no sentido do fluxo de dados entre o computador e o dispositivo, denominamos esses dispositivos como periféricos de entrada, periféricos de saída, ou ainda, periféricos de entrada e saída. Um periférico é qualquer dispositivo conectado a um computador, possibilitando sua interação com o mundo externo.

Um componente de hardware denominado interface permite que os periféricos sejam conectados ao computador. Portanto, os periféricos não estão conectados diretamente aos barramentos do computador. Dessa forma, as interfaces constituem um elemento primordial para que a transferência de dados entre periférico e processador, ou entre periférico e memória, ocorra.

Outro componente de hardware denominado controlador integra as interfaces. Um controlador corresponde a um processador/chip projetado para realizar uma função específica, como controlar um disco rígido.

Os hardwares de E/S têm como principais componentes os chips, as ligações elétricas e os componentes físicos.

Os dispositivos de E/S estão divididos em três classes:

- Dispositivo de bloco: armazena informação em blocos de tamanho fixo, com endereço (exemplo: disco).

- Dispositivo de caractere: envia ou recebe fluxo de caracteres sem considerar qualquer estrutura de blocos (exemplo: impressoras, interface de rede, mouse).

- Outros dispositivos: relógio.

### Relógio

Os temporizadores (timers – relógios) são extremamente necessários por algumas razões, porém, em sistemas operacionais, o mais relevante é:

Manter o funcionamento de segundos, minutos, horas, data e ano, mesmo que o computador esteja desligado.

Com isso, quando o equipamento estiver ligado e em funcionamento, é o relógio que irá fornecer o tempo real e atual para o ambiente. Portanto, o sistema pode calcular quanto tempo um processo já está na CPU e, de ciclos em ciclos, quanto irá alternar entre os demais processos.

Apesar do temporizador não ser um dispositivo de bloco nem um dispositivo de caractere, o software desse componente pode tomar a forma de um driver de dispositivo.

Hardware do relógio – visão geral.

Os computadores típicos e atuais utilizam um relógio interno que não é parecido com os nossos relógios de pulso ou de mesa. Os relógios dos computadores são formados por três componentes:

- Oscilador de cristal.
- Controlador.
- Registrador de apoio.

Devido ao processo extremamente preciso da seleção, corte e montagem sob pressão de um fragmento de cristal de quartzo, é possível obter um sinal cíclico de alta precisão medido em centenas de megahertz. 

Somando a capacidade da eletrônica, podem ser obtidas frequências de 1.000 MHz ou superiores. O sinal gerado pelo circuito eletrônico descrito anteriormente servirá como referência de sincronização para os vários elementos do computador que necessitem desse tipo de interação. O sinal gerado alimenta um controlador que irá realizar uma contagem regressiva até zero.

Quando o controlador chega à contagem igual a zero, este, por sua vez, irá gerar uma interrupção na CPU. A bateria que vem juntamente com a placa-mãe é necessária para manter o relógio funcionando até quando o computador está desligado ou mesmo desconectado da tomada.

Se o relógio não estiver presente no sistema, então será solicitado ao usuário informar a data e a hora no momento do processo de inicialização da máquina.

Para sistemas em rede, existe outra forma, que é o uso de um computador remoto de sincronismo de data e hora. Com isso, todos os equipamentos na rede estarão no mesmo tempo ou, em outras palavras, estarão sincronizados.

FIGURA 1.5

### Pergunta

    O gerenciamento de entrada e saída tem como princípio básico a abstração, tornando a interação do programador com a máquina algo muito mais fácil e permitindo que os programas e os hardwares evoluam de forma independente, porém estruturada. Os dispositivos de entrada e saída típicos são classificados em:

    a- Dispositivos voláteis e dispositivos não voláteis.
    b- Dispositivos locais e dispositivos de armazenamento.
    c- Dispositivos mecânicos e dispositivos eletrônicos.
    d- Dispositivos dedicados e dispositivos compartilhados.
    e- Dispositivos de blocos e dispositivos de caractere.

    A respota certa é a letra E.