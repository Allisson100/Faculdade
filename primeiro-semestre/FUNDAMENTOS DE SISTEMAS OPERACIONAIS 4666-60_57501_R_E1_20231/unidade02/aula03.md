# Aula 03

Processadores multithread e multinúcleo:

- O Intel Pentium 4 e outros chips de processadores têm a propriedade chamada multithreading.

- No ambiente da ciência da computação, a execução de um thread é a menor unidade de processamento que pode ser atendida por um sistema operacional. Múltiplos threads podem existir num mesmo processo e compartilhar recursos como a memória, enquanto diferentes processos não compartilham esses recrusos.

- O thread de um processo compartilha as instruções e contextos. Analogicamente, múltiplos thread de um processo é o mesmo que múltiplos alunos lendo instruções em um mesmo livro, porém não necessariamente todos os alunos lendo a mesma página.

- Se um dos processos precisa ler uma palavra a partir da memória demandando muitos ciclos de relógios, uma CPU multithreading não oferece paralelismo, então apenas um processo por vez é executado, mas o tempo de chaveamento é reduzido para a ordem de um nanossegundo.

- O grande problema é que multithreading é compreendido pelo sistema operacional como uma CPU, portanto, se um computador tiver, por exemplo, duas CPUs, cada uma com dois threads, o sistema operacional entenderá e terá que gerenciar como se existissem 4 CPUs no sistema.

- Outra opção é a CPU com multinúcleo. Isso é o mesmo que fisicamente vermos um único chip, porém, internamente, temos múltiplos chips como se fossem várias CPUs. É importante destacar que sistemas com CPU multinúcleos requerem SO para multiprocessadores.

### Memória

- Na teoria, a memória deveria ser mais perfomática do que a execução de uma instrução processada por uma CPU, pois com isso, a CPU jamais teria que esperar pela resposta da memória; entretanto, na prática isso não é uma verdade.

- Para tentar resolver esse problema, a abordagem contemporânea é construir o sistema de memória seguindo uma hierarquia de camadas.

- No topo da pirâmide, temos os registradores que estão contidos nas CPUs. Esses são feitos do mesmo material que as CPUs e são tão rápidos quanto elas. Desta forma, o tempo do registrador para a memória é desprezível e a capacidade de memória disponível nos registradores é de 32 x 32 bits para CPU de 32bits e de 64 x 64 bits para CPU de 64 bits, sendo menos de 1 KB no caso das CPUs de 64 bits.

- Seguindo, no segundo nível, vem a memória cache, que é encontrada principalmente pelo hardware.

- Atualmente, vários dispositivos, como processsadores, discos rígidos, placas-mãe, placas controladoras e outros, possuem cache. A memória cache é a mais utilizada para armazenar informações frequentementes mais utilizadas, porém memória cache é muito cara e não é tão abundante nos sistemas.

- No próximo nível, é possível identificar a memória principal, também conhecida como memória RAM (Rando Access Memory - Memória de Acesso Aleatório).

- Todas as solicitações vindas da CPU e que não estão na memória cache são encaminhadas para a memória principal.

- ROM (Read Only Memory) e CMOS são outros tipos de memórias também presentes nos sistemas computacionais.

- A memória ROM é normalmente usada pelos fabricantes para gravar códigos controladores do hardware e são previamente programadas em fábrica, não sendo possível sua alteração, a não ser que se usem equipamentos específicos para essa finalidade.

- A memória CMOS é tipicamente usada para manter data e hora atualizadas e parâmetros de configurações do hardware, como sequência de boot e outros, mesmo que o computador esteja desligado.

- A memória CMOS necessita de uma bateria para manter seu conteúdo.

### Disco

- Os discos magnéticos estão na camada logo abaixo da memória principal, sendo conhecidos como discos rígidos ou , em inglês, hard disks, e também, de forma abreviada, HD.

- O grande atrativos do disco magnético em relação à memória é o preço bem menor se comparado R$/GB, entretanto, o cotraponto é a velocidade de acesso que é muito mais lenta por ser um dispositivo mecânico.

- Na estrutura de disco magnético, temos como umas das principais pasrtes o grupo de discos metálicos em que são gravadas as informações. Tipicamente, esses discos rodam a velocidade de 5400 a 1000 rpm (rotações por minuto) e têm uma média de transferência de 0,5 Gbit/s.

- Em ambiente projetados com servidores de rede e, principalmente, servidores de banco de dados transacional, normalmente, são instalados discos com velocidades de 15000rpm, podendo-se atingir a média de transferência acima de 1,6Gbits/s. Os discos de 10000 ou 15000 rpm usam discos menores para mitigar grandes demandas de energia, entretanto, isso acarreta que esses discos com maior capacidade de rotação por minuto possuam menos capacidade do que os discos magnéticos de menos rpm.

- As informações são escritas no disco em uma série de círculos que têm o mesmo cantro. Cada cabeça pode ler e gravar uma região circular chamada trilha. Juntas, as trilhas de uma posição do braço formam um cilindro. Mover o braço entre cilindros próximos leva aproximadamente 1ms e mover o braço de um determinado cilindro para outro distante leva em torno de 5 a 10ms.

### Fitas

- A fita magnética é o último tipo de memória na pirâmide. Esse meio é muito utilizado como mídia de cópia de segurança (backup), transportando uma cópia daquilo que está nos discos magnéticos para fitas magnéticas.

- Com base nas normas de segurança ISO 27001, e até mesmo do Banco Central Brasileiro, é obrigatório o uso de sistemas de backup para garantir que a informação esteja disponível em caso de o sistema principal apresentar problema. Grandes sistemas utilizam robôs que controlam a troca de fitas, bem como softwares especiais para backup, como o Veritas Backups Exec, Data Protector, ARCserver, Tivoli Storage Management e outros.

### Pergunta

Sobre os discos magnéticos, é correto afirmar que:

|- Estão na camada logo abaixo da memória principal.
||- O grande atrativo dos discos magnéticos em relação à memória é o preço bem menor se comparado R$/GB, entretanto, o contraponto é a velocidade de acesso que é muito mais lenta por ser um dispositivo mecânico.
|||- São conhecidos como discos rígidos ou, em inglês, hard disks, e também, de forma abreviada, como HD.

a-  Apenas as afirmações I e III estão corretas.
b- Apenas as afirmações II e III estão corretas.
c-  Apenas a afirmação I está correta.
d- Todas as afirmações estão corretas.
e-  Nenhuma afirmação está correta.

A resposta certa é a letra D.

