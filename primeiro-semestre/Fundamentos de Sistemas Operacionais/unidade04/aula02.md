# Aula 02

### Travas em arquivos

Por meio de uma ou mais travas (locks) aplicadas aos arquivos abertos, tipicamente os sistemas operacionais oferecem algum mecanismo de sincronização para acesso a arquivos. A sincronização pode ser feita aplicando-se a trava no arquivo inteiro ou somente em um trecho específico. Isso permitirá que dois ou mais processos possam trabalhar em partes distintas de um arquivo sem necessidade de sincronização entre eles.

As travas oferecidas pelo sistema operacional podem ser obrigatórias ou recomendadas.

- Travas obrigatórias: são impostas pelo núcleo do sistema operacional de forma compulsória, de modo que se um processo obtiver a trava do arquivo, então outros processos que solicitarem acesso ao arquivo serão suspensos até que a respectiva trava seja liberada.

- Travas recomendadas:  não são impostas pelo núcleo do sistema operacional. Portanto, um processo pode acessar um arquivo mesmo sem ter sua trava e caso sejam usadas travas recomendadas, fica a cargo do programador implantar em suas aplicações os controles de trava necessários para impedir acessos conflitantes aos arquivos. As travas sobre arquivos também podem ser exclusivas ou compartilhadas.

- Travas exclusiva: também chamada trava de escrita, garante acesso exclusivo ao arquivo, portanto, enquanto uma trava exclusiva estiver ativa, nenhum outro processo poderá obter uma trava sobre aquele arquivo.

- Trava compartilhada (ou trava de leitura): impede outros processos de criar travas exclusivas sobre o arquivo, mas permite a existência de outras travas compartilhadas.

Em conjunto, as travas exclusivas e compartilhadas implementam um modelo de sincronização leitores/escritores, no qual os leitores acessam arquivos usando travas compartilhadas e os escritores o fazem usando travas exclusivas.

Geralmente, as travas de arquivos são atribuídas a processos. Dessa forma, um processo só pode possuir um tipo de trava sobre um mesmo arquivo e todas as travas são liberadas quando o processo fecha o arquivo ou finaliza sua execução. 

Os sistemas Windows oferecem por default travas obrigatórias sobre arquivos, que podem ser exclusivas ou compartilhadas, ou travas recomendadas sobre trechos de arquivos.

### Semântica de trava de acesso

Quando um arquivo é usado por um único processo, o funcionamento das operações de leitura e escrita é simples e claro. 

Dessa forma, quando um dado é escrito no arquivo, ele está prontamente disponível para leitura. No entanto, arquivos podem ser abertos por vários processos simultaneamente e os dados escritos por um processo podem não estar prontamente disponíveis aos demais processos que estão lendo aquele arquivo. Isso ocorre porque as memórias secundárias em disco rígido são lentas em comparação com a memória principal, levando os sistemas operacionais a usar buffers intermediários para acumular os dados que deverão ser escritos/manipulados, otimizando o acesso aos discos.

A forma como os dados escritos por um processo é notada pelos demais processos que também abriram um determinado arquivo é chamada de semântica de compartilhamento.

Sessões concorrentes de acesso a um arquivo compartilhado podem ver conteúdos distintos para o mesmo arquivo. Essa semântica é normalmente aplicada a sistemas de arquivos de rede, usados para acesso a arquivos em outros computadores.

- Semântica imutável: se um arquivo pode ser compartilhado por vários processos, ele é marcado como imutável. Dessa forma, seu conteúdo não pode ser modificado. É a forma mais trivial que garante a consistência do conteúdo do arquivo entre os processos que compartilham seu acesso, portanto, usada em alguns sistemas de arquivos distribuídos.

Entre outras semânticas possíveis, as mais usuais são:

- Semântica Unix: toda modificação em um arquivo é imediatamente visível a todos os processos que mantêm o arquivo aberto, existindo também a possibilidade de vários processos compartilharem o mesmo ponteiro de posicionamento do arquivo. Esse tipo de semântica é comumente aplicada em sistemas de arquivos locais, ou seja, para acesso a arquivos nos dispositivos locais.

- Semântica de sessão: considera que cada processo usa um arquivo emuma sessão, iniciando com a abertura do arquivo e terminando com o seu fechamento. Modificações em um arquivo feitas em uma sessão somente são visíveis na mesma sessão e pelas sessões que iniciarem depois do encerramento desta, ou seja, depois que o processo fechar o arquivo.

### Diretórios

O sistema organiza logicamente os diversos arquivos contidos em um disco numa estrutura denominada diretório. O diretório é uma estrutura de dados que contém entradas associadas aos arquivos, na qual cada entrada armazena informações como localização física, nome e demais atributos.

Embora o sistema operacional possa tratar com facilidade da enorme quantia de arquivos existentes em um sistema de arquivos, essa tarefa está bem distante de ser trivial para os usuários. Identificar e localizar um arquivo específico em meio a milhões de outros arquivos de forma rápida e direta pode ser o mesmo que procurar uma "agulha num palheiro".

Para permitir a organização de arquivos dentro de uma partição, são usados diretórios. Um diretório, também chamado de pasta (folder), representa um contêiner de informações, que pode conter arquivos ou mesmo outros diretórios.

Da mesma forma que os arquivos, diretórios têm nome e atributos que são usados na localização e acesso aos arquivos neles contidos.

Cada espaço de armazenamento possui ao menos um diretório principal, denominado diretório raiz. Em sistemas de arquivos mais antigos e simples, o diretório raiz de um volume estava definido em seus blocos de inicialização, normalmente reservados para informações de gerência. Todavia, como o número de blocos reservados era pequeno e fixo, o número de entradas no diretório raiz era limitado. Nos sistemas mais recentes, um registro específico dentro dos blocos de inicialização aponta para a posição do diretório raiz dentro do sistema de arquivos, permitindo que este tenha um número muito maior de entradas. O uso de diretórios permite construir uma estrutura hierárquica (em árvore) de armazenamento dentro de um volume, sobre a qual os arquivos são distribuídos.

A figura abaixo representa uma parte da árvore de diretórios típica de um sistema Linux, cuja estrutura é definida nas normas Filesystem Hierarchy

FIGURA 1.0

### Sistema de diretórios em nível único

O nível mais simples de uma estrutura de diretórios é chamado de nível único single-level directory). Nessa estrutura, existe somente um único diretório contendo todos os arquivos do disco. Esse modelo é bastante limitado, já que não permite que usuários criem arquivos com o mesmo nome, o que ocasionaria um conflito no acesso aos arquivos.

O primeiro supercomputador da história foi um CDC 6600 e usava um sistema de diretório único. A próximafigura ilustra esse sistema.

FIGURA 1.1

### Sistema de diretórios hierárquicos

O sistema de nível único é bastante limitado, demandando uma evolução do modelo, então foi implantada uma estrutura na qual para cada usuário existiria um diretório particular denominado Diretório de Arquivo do Usuário, conhecido como sistema de diretório em dois níveis.

Pela perspectiva do usuário, a organização dos seus arquivos em um único diretório não permite uma organização adequada. A extensão do modelo de dois níveis para um de múltiplos níveis permitiu que os arquivos fossem logicamente melhor organizados. Esse novo modelo, chamado estrutura de diretórios em árvore, é adotado pela maioria dos sistemas.

FIGURA 1.2

### Tipos de sistemas de arquivos

Os sistemas de arquivos são desenvolvidos, muitas vezes, por motivos comerciais, outras, por alinhamento tecnológico com o propósito do hardware ou até mesmo motivados por interoperabilidade entre sistemas. Nesta próxima seção estudaremos alguns mais relevantes por serem os mais populares.

### Sistema de arquivos ISO 9660

O sistema de arquivos ISO 9660 é um padrão internacional e mais usado em tecnologia de CD-ROMs.

A quase totalidade dos CD-ROMs no mercado atual é compatível com esse padrão.

O objetivo principal do padrão ISO 9660 era tornar possível que todo CD-ROM fosse legível por todos os computadores, independentemente da ordem em que os bytes são armazenados e qual sistema operacional esteja carregado no hardware.

Tecnicamente, uma grande diferença dos discos rígidos para os CD-ROMs é que estes não possuem cilindros concêntricos, mas sim uma única espiral contínua que contém bits em uma sequência linear.

### Sistema de arquivo do FAT


Os primeiros computadores pessoais da IBM já utilizavam o sistema de arquivos MS-DOS e por anos foi o mais usado mundialmente. 

Até o Windows 98 e o ME, a Microsoft manteve o mesmo sistema de arquivos. O Windows 2000, XP e o Vista suportam esse sistema, porém, ele não é mais padrão nos equipamentos atuais.

O sistema de arquivos MS-DOS possui extensão FAT-32, que vem sendo usada amplamente em máquinas fotográficas, MP3 e outros. Atualmente, o sistema de arquivos MS-DOS e suas extensões são mais usados do que em qualquer outra época. O sistema de arquivo usado pela Microsoft atualmente é o NTFS.

### Sistema de arquivos do ambiente Unix

Antes de falarmos do sistema de arquivos Unix, é importante conhecermos sua origem para que possamos entender como um sistema de arquivos pode ter, logo em sua primeira versão, funcionalidades que são primordiais para ambientes multiusuários, por exemplo.

O Multics foi criado em 1964, fomentado pelo projeto liderado pelo MIT (com Fernando Corbató), e a divisão de produtos para grandes computadores da companhia General Electric e dos Laboratórios Bell de telefonia. O sistema Multicsseria implantado na plataforma GE 645 da GE. Uma visão geral da arquitetura desse sistema operacional tinha como ambição estar alinhada com quase todos os computadores existentes, suprindo as necessidades de computadores de grande porte, mesmo os que estariam à frente do seu tempo.

### Sistema de arquivos do Linux

A primeira versão do sistema de arquivos do Linux foi o Minix, porém, como ele seguia estritamente os padrões do Unix, ele também tinha arquivos com limites de nomes de 14 caracteres e seu tamanho máximo de arquivo era de 64 MB. Esse padrão atendia quase que na totalidade as necessidades da época, porém, com o passar do tempo, 64 MB passou a ser “brincadeira de criança”, demandando sistemas de arquivos mais robustos e melhorados. 

O sistema de arquivos ext apresenta melhorias com relação ao tamanho do nome que passou a suportar até 255 caracteres e arquivos com tamanho de até 2 GB. Por outro lado, a desvantagem do sistema de arquivos ext, comparado com o Minix, era seu desempenho, apresentando lentidão considerável.

### Pergunta

    O sistema de arquivos ISO 9660 é um padrão internacional e mais usado em tecnologia de CD-ROMs. A quase totalidade de CD-ROMs no mercado atual é compatível com esse padrão. Tecnicamente, uma grande diferença dos discos rígidos para os CD-ROMs é que estes não possuem cilindros concêntricos, mas sim uma única espiral contínua que contém bits em uma sequência linear.

    A partir dessa definição, é correto afirmar que:

    a- Mesmo estruturado em uma espiral contínua, é possível buscar o CD-ROM transversalmente às espirais.

    b- Mesmo estruturado em uma espiral contínua, é possível buscar o CD-ROM ortogonalmente às espirais.

    c- Mesmo estruturado em uma espiral contínua, é possível buscar o CD-ROM perpendicularmente às espirais.

    d- Mesmo estruturado em uma espiral contínua, é possível buscar o CD-ROM paralelamente às espirais.

    e- Mesmo estruturado em uma espiral contínua, não é possível buscar o CD-ROM.

    A resposta certa é a letra A.








