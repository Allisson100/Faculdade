# Aula 01

### Introdução a Sistemas de Arquivos

Em linhas gerais, no ambiente computacional, espera-se que dados inseridos na entrada saiam como produto final, informação processada. Essas informações podem ser compreendidas como textos, planilhas, figuras, filmes etc. As informações, que podem ocupar de alguns bytes a milhares de milhões de bytes, devem ser armazenadas em dispositivos não voláteis, ou seja, não podem ser perdidas com o desligamento do computador e podem ser acessadas por múltiplos processos de forma concorrente.

As informações são armazenadas tipicamente em disco e o armazenamento resume-se em sequências lineares de blocos de tamanho fixo que suportam duas operações: busca do bloco k e escrita no bloco k, surgindo, portanto, o conceito de arquivo.

### Arquivos

Podemos definir um arquivo como sendo um conjunto de dados armazenados em um dispositivo físico não volátil, com um nome e/ou referência que permita sua localização futura.

Arquivos podem ter diversos formatos, desde um simples arquivo de texto ASCII com alguns poucos bytes, até mesmo vídeos com vários megabytes ou gibabytes em diversos formatos.

Um sistema de armazenamento de arquivos pode conter milhões de arquivos que são organizados em estruturas hierárquicas denominadas diretórios. A estrutura e a organização física e lógica dos arquivos e diretórios dentro de um dispositivo de armazenamento são denominadas de sistema de arquivos.

### Atributos

Cada arquivo é diferenciado por um conjunto de atributos. Tipicamente, temos alguns atributos mais usados:

- Nome: uma sequência de caracteres para identificar de tal forma que um ser humano, ao vê-lo na tela, consiga identificá-lo. Exemplo: relatorio.doc.

- Data:  é muito útil no que tange ao gerenciamento do ambiente. Além de ajudar o usuário a saber quando um arquivo foi criado, pode também controlar a data e a hora do último acesso, da última modificação do conteúdo e até mesmo da última alteração de outro atributo, como o nome do arquivo, por exemplo.

- Tipo: indica se o formato do arquivo é áudio, vídeo, imagem, texto ou outro. O sistema de arquivos do Windows e outros usam a extensão, que é parte do nome, para indicar o tipo do arquivo.

Exemplo: “.doc” no arquivo com o nome “relatorio.doc” refere-se a um arquivo de texto (abreviação de document).

- Tamanho: esse atributo determina quanto de espaço em bytes (1 byte = 8 bits) ou registros. Exemplo: relatorio.doc 906.085 bytes.

- Proprietário:  atualmente, com os sistemas em rede e multiusuários, cada arquivo tem um proprietário, que deve estar corretamente identificado – em alguns casos o próprio sistema é o proprietário do arquivo e por isso nenhum usuário deveria alterá-lo.

- Permissões de acesso:  determinam quais usuários têm acesso ao arquivo e quais permissões são atribuídas a cada usuário (leitura, escrita, remoção etc.).

Um usuário de sistema Unix chamado root, na teoria, deveria ter acesso total ao arquivo, enquanto um usuário ou um processo que só deve consultar um arquivo de registros de log deveria ter acesso só de leitura.

- Localização: esse atributo indica o dispositivo físico onde o arquivo se encontra e a posição do arquivo dentro dele. Para o usuário do sistema, a localização do arquivo é demonstrada como uma estrutura hierárquica que parte da raiz, que é o pai de todos os demais repositórios filhos.

### Estrutura de arquivos

Os arquivos podem ser estruturados de várias formas.

A figura mostra uma sequência de estrutura de bytes. Para os sistemas operacionais Windows e Unix, a estrutura de um arquivo nada mais é que uma sequência desestruturada de bytes.

Isso oferece a máxima flexibilidade, tendo em vista que os programas dos usuários podem pôr qualquer coisa que seja necessária em seus arquivos e ter os nomes que mais forem convenientes.

Na figura b, é demonstrada uma forma estruturada.

Nessa estrutura, o arquivo é uma sequência de registros de tamanho fixo, cada um com alguma estrutura interna. A principal característica dessa estrutura é que a operação de leitura retorna um registro e a operação de escrita sobrepõe ou anexa um registro, entretanto, esse modelo não é mais aplicado nos sistemas atuais.

Um arquivo é constituído de uma árvore de registros, cada uma contendo um campo-chave em uma posição fixa no registro. Para que uma chave específica seja buscada de forma mais rápida, a árvore é ordenada pelo campo-chave.

O sistema operacional decide onde colocar novos registros no arquivo. Esse tipo de arquivo é bem diferente dos fluxos de bytes desestruturados que são usados pelo Windows e Unix, porém são ainda muito usados para alguns processamentos de dados comerciais.

### Operações

Os aplicativos e o sistema operacional armazenam e recuperam dados dos arquivos e por meio de um conjunto de operações fazem uso deles.

As operações básicas envolvendo arquivos são:

- Criar: a criação de um novo arquivo demanda a alocação de espaço no dispositivo de armazenamento e a definição de seus atributos (nome, localização, proprietário, permissões de acesso etc.).

- Ler:  permite transferir dados presentes no arquivo para uma área de memória da aplicação e, se necessário, enviar para um dispositivo de saída como monitor, impressora e outros.

- Abrir: antes que um aplicativo possa ler ou escrever dados em um arquivo, este deve solicitar ao sistema operacional que o arquivo seja aberto.

O sistema irá, primeiro, verificar se o arquivo existe, segundo, se as permissões associadas permitem acesso ao arquivo, terceiro, localizar seu conteúdo no dispositivo de armazenamento, então criar uma referência para ele na memória.

- Escrever: essa operação permite transferir dados da memória do aplicativo para o arquivo armazenado no dispositivo físico; os novos dados podem ser adicionados no final do arquivo ou sobrescrever dados já existentes.

- Fechar: ao concluir o uso do arquivo, a aplicação deve informar ao sistema operacional que esse arquivo não é mais necessário, a fim de liberar as estruturas de gerência do arquivo na memória do núcleo.

- Mudar atributos: usado para modificar outras características do arquivo, como nome, proprietário, localização, permissões etc.

- Remover: elimina o arquivo do dispositivo, descartando seus dados e liberando o espaço ocupado por ele.

Além dessas operações básicas, outras operações podem ser definidas, como copiar, mover ou renomear arquivos. Entretanto, essas operações geralmente podem ser construídas usando as operações básicas.

### Compartilhamentos

Em um sistema multitarefas e em redes, frequentemente se tem arquivos sendo acessados por mais de um processo ou por mais de um usuário.

O acesso simultâneo a recursos compartilhados pode gerar condições de disputa (race conditions), levando à inconsistência de dados e outros problemas. A possibilidade de escritas e leituras simultâneas tem de ser prevista e tratada com muito planejamento e controle de acesso desses elementos compartilhados.

### Pergunta

    Podemos definir um arquivo como sendo um conjunto de dados armazenados em um dispositivo físico não volátil, com um nome e/ou referência que permita sua localização futura. Cada arquivo é diferenciado por um conjunto de atributos.Tipicamente, podemos definir os seguintes atributos:


    |- Nome:  uma sequência de caracteres para identificar de tal forma que um ser humano, ao vê-lo na tela, consiga identificá-lo.

    ||- Data: é muito útil no que tange ao gerenciamento do ambiente. Além de ajudar o usuário a saber quando um arquivo foi criado, pode também controlar a data e a hora do último acesso, da última modificação do conteúdo e até mesmo da última alteração de outro atributo, como o nome do arquivo, por exemplo.

    |||- Tipo: indica se o formato do arquivo é áudio, vídeo, imagem, texto ou outro.

    De acordo com o material estudado na unidade, selecione a afirmativa que contém os atributos com os quais podemos diferenciar os arquivos.

    a- Apenas a afirmação I.
    b- Apenas a afirmação II.
    c- Apenas a afirmação III.
    d- Todas as afirmações.
    e- Nenhuma das afirmações.

    A resposta é a letra D.


