
### O que é?

Conjunto de computadores ou dispositivos interconectados por uma ou mais tecnologias e capazes de trocar informações e compartilhar recursos.


### Por que estudar redes?

É possível desenvolver algum sistema atual que não envolva comunicação? Como isso deve ser feito de forma eficiente.

### Como surgiu?

Resultado de um projeto militar, chamado ARPANET. Mas no brasil chegou em 91, com a criação da RNP, com o primeiro backbone interconectando instituições. 
E as conexões sem fio, também surgiram na década de 90, mas para o público só aconteceu há 16 anos.

## Evolução e Caracterização de Redes de Computadores

Computadores altamente centralizados, e fortemente acoplados, faziam execuções de um único processo (Batch), posteriormente surgiram os computadores com tempo compartilhado.

Máquinas descentralizadas, e fracamente acopladas, com compartilhamento de recursos, e processamento distribuído, onde as atividades eram quebradas em várias, e cada unidade de processamento, processava uma parte.

Evolução dos sistemas de comunicação + Evolução dos sistemas de processamento e armazenamento de informações => Melhoria da eficiência dos sistemas de computação + distribuição do poder computacional + redes.


### O que é uma rede?

"Uma rede é uma coleção de computadores autônomos interconectados, aptos a trocar informações e compartilhar recursos." - Tanenbaum


### Caracterização

Em termos de elementos, consideramos, unidades de processamentos independentes, e o sistemas de comunicação que permitem que elas estejam conectados, que são divididos em duas partes, a física, e a lógica, que são os meios de transmissão e os protocolos de comunicação, respectivamente. 


### Meios de transmissão 

Corresponde ao meio físico que será utilizado para realizar a comunicação entre hosts e aplicações.
Exemplo: Cabos, placas, modems, roteadores.

#### Núcleo da rede

Interconecta os sistemas finais. Enlaces de comunicação e roteadores. São encarregados de conectar as pequenas redes.

#### Redes de acesso

Rede física que conecta um sistema final ao primeiro roteador(Onde os usuários finais acessam o primeiro roteador do núcleo da rede) de um caminho partido de um sistema final até outro qualquer. Enlaces de comunicação. Tipo, móvel e cabeada.

##### DSL (Digital Subscriber Line)

A linha digital de assinante tem a ideia de utilizar uma infraestrutura já existente, no caso, a linha telefone, onde a voz humana era transmitida por cabos metálicos de maneira analógica.

Modem converte sinal digital para analógico. Splitter comprime o sinal enviado pelos cabos, e no provedor o sinal era divido novamente.

###### DSLAM?

##### Cabo, híbrida fibra-coaxial (13Mbits/s)

Utilizada pelas TV's, ainda utilizando dos modems, mas o cabo levava até um nó de fibra ótica, que funcionava como um armário que juntava vários sinais de coaxiais e transformava em apenas um único cabo de fibra ótica. Sendo bem mais vantajoso.

###### CMTS?
##### Fiber-to-the-Home (FTTH)

Tecnologia utilizada nos dias de hoje, onde o caminho de fibra ótica vai diretamente até a residência. (20 Mbits/s em 2011). Possuindo várias vantagens em relação aos cabos metálicos.


###### ONT?
###### OLT?


##### Ethernet (Redes locais)

Velocidades de cerca de 100 Mbts/s 1Gbits/s e 100Gbits/s (Na rede de acesso), limitado ao pouco comprimento.

##### Wifi (IEEE 802.11) 

Primeiro acesso sem fio, onde tenho dentro de dezenas de metros que posso me afastar do ponto de acesso. Há algumas versões da tecnologia, mudando algumas características, como velocidade, frequências, ou múltiplas antenas. 

##### Acesso sem fio de longa distância

Distância muito maior, chegando a dezenas de quilômetros da estação-base, utilizando da mesma infraestrutura sem fio da telefonia celular, tendo velocidade acima de 1Mbits/s (3G), e 10Mbits/s(4G).


### Protocolos de comunicação

Funciona de maneira que temos mensagem específicas que enviamos e ações específicas que realizamos em reação às respostas recebidas ou a outros fatos (Como falta de resposta). Um exemplo é em conversas cotidianas: Como um simples bom dia, esperamos receber outro de volta. Ou ainda um que horas são?

#### Protocolos de comunicação em redes

Máquinas no lugar de humanos, onde toda atividade de comunicação em redes é governada por protocolos.

Esses protocolos definem os formatos, a ordem das mensagens enviadas e recebidas pelas entidades de rede e as ações a serem tomadas na transmissão e recepção de mensagens. Onde é necessário ensinar o computador sobre eles.


### Categorias

- Tipo de de transmissão
- Dispersão geográfica
- Taxa de erros
- Propriedade privada ou não
- Entre outros.

### Tipos de transmissão

Temos dois tipos principais, as redes de difusão que são conhecidas como multiponto, ou broadcast, e redes ponto a ponto.

Difusão - 1 envio, todos recebem

Ponto a ponto - 1 único meio que conecta duas máquinas, são recebidas imediatamente pela máquina vizinha, mensagem tem que ser repassadas até chegar a máquina destino

#### Redes de difusão

É um canal único de comunicação compartilhado por todas as máquinas da rede, onde tem um tráfego de pequenas mensagem, que são enviadas por uma máquina e recebidas por todas. Só é possível uma máquina enviar por vez. Essa mensagem tem um campo de endereço que especifica para que máquina a mesma deve ser entregue.

A mensagem recebida tem seu campo de endereço verificado, se pertence a ela, ela processa a mensagem, mas se não, ela é descartada.

Temos casos onde a máquina destino não é apenas uma, como por exemplo o broadcasting, onde todas as máquinas devem receber a mensagem enviada.
Para isso, existe um valor reservado para essa ação que é passado dentro do campo de endereço.

Atualmente temos também o uso do multicasting, onde eu quero que a mensagem enviada seja recebida por apenas algumas máquinas.

Ou seja a rede de difusão deve ser mais utilizada quando tenho que utilizar de meios como broadcasting, ou multicasting.


#### Redes ponto-a-ponto

Rede, onde as máquinas tem um canal exclusivo de comunicação para interligação de quaisquer duas máquinas na rede. O tráfego de mensagens enviadas por uma máquina tem origem para uma única máquina de destino, porém para ela ir da origem até um destino, a mensagem pode ter de passar por uma ou mais máquinas intermediárias.

Um problema é que podem existir múltiplas rotas, de diferentes custos, sejam eles o tamanho, velocidade, e atraso, entre uma origem e seu destino, de modo que os algoritmos de roteamento se tornam essenciais, para a escolha da melhor rota, assim desempenhando um papel relevante nas redes.


### Dispersão geográfica

Relação com a distância entre os nós da mesma rede.

- Redes pessoais (PAN ou Personal Area Network)
- Redes de maior abrangência
- LAN (Local Area Network)
- MAN (Metropolitan Area Network)
- WAN (Wide Area Network)

Internet - Escalavel e distribuida
- Rede de redes (inter-rede)


#### PAN 

Redes que cobrem distâncias muito pequenas, em torno de 1 metro.
Destinadas a uma única pessoa, como por exemplo o Bluetooth.

#### LAN

Redes locais, limitadas a dezenas de metros, ou poucos quilômetros, entre taxas de transmissão consideradas altas, e baixos atrasos nessas transmissões, pois os nós estão ainda próximos.

Adota o padrão IEEE 802.3 - Ethernet ou o IEEE 802.11 - WIFI

Comunicação de baixo custo, pois é acessivel para as pessoas comprarem os componentes e montarem suas redes.

Como por exemplo, um servidor conectando computadores independentes, sendo conectados por rede ethernet, em uma distancia pequena, podemos chama-la de LAN


#### MAN

É uma rede projetada para interconectar sistemas de uma mesma cidade, atingindo uma taxa de transmissão bem alta, mas podem variar para taxas bem baixas também.
Ela adota o padrão SONET (Synchronous Optical Network) ou o SDH (Synchronous DIgital Hierarchy).
Diferente da LAN, o custo aqui é bem mais alto. Devido os equipamentos, e as distancias. 

Conexão entre  predios de uma cidade que utilizam redes LANs, conectadas por NPE, podem formar uma rede MAN.


#### WAN

A rede que possui a maior dispersão geográfica, podendo atingir áreas de um país ou até continente.
Porém a transmissão já se torna menos confiável, em média 1 erro em 100Mbits, as velocidades também são mais baixas.

Necessidade de diversos roteadores para suprir a demanda das grandes distancias, como por exemplo temos multinacionais que querem conectar sua infraestrutura afim de unifica-la. 

#### WLAN 

wireless LAN


#### Campus universitario (CAN)

Campus Area Network

conjunto de redes que tem divisões entre departamentos, com varias LANs.

Caso tenha outros campus na mesma cidade, podemos criar uma rede MAN, para interconectar as redes CANs

Entretanto se os campus forem em outras cidades, ainda tempos a possibilidade de ter uma rede WAN, onde todos os campus universitarios estariam interligados.


## Modelo de Referência OSI/ISO

### Por que estudar redes em diferentes "camadas" de protocolos?

É devido sua grande complexidade, que se divide em muitos "pedaços", como hosts, roteadores, enlaces de diversos meios, aplicações, protocolos, e hardware e software. O maior beneficio nessa estratégia é facilitar o estudo.
Um exemplo dessa mesma aplicação é a viagem aérea, onde temos a compra da passagem, o despache da bagagem, a embarcação do cliente, a decolagem do avião, entre outros. Ai vem a divisão em serviços, ou melhor, "camadas". Onde cada função só tem seu delimitado escopo, e não tem noção das demais atividades. Com isso ganhamos de certa forma, uma independência maior, entre esse conjunto. 

![[Exemplo-Camada-Aeroporto.png]]

Dessa maneira, irá ajudar a lidar com sistemas complexos, e estudar mais afundo os relacionamentos que ocorrem entre cada "camada", fazendo assim o sistema ser modular o que facilita a manutenção e atualização do sistema, assim, a implementação do serviço da camada é transparente para o resto do sistema. Mas com isso surgem algumas problemas, sendo deles, o principal, overhead

### Modelo de referencia OSI/ISO

Não se aplica a dispersão geográfica, vem com a ideia de ser aplicável a "qualquer" qualidade de comunicação/nível de serviço, propõe a tratar todos os aspectos do problema de sistemas abertos, que é aquele que está aberto à comunicação com outro sistema.

Ele separa as funcionalidades e as capacidades de arquitetura de rede em camadas. E também define os termos e objetos que são palavras reservadas no mundo de redes, entretanto, ele não nós ensina a implementar, mas sim com uma ideia conceitual. 

Destas camadas, são definidas desde aspectos físicos até aspectos abstratos da aplicação. 

O modelo é constituído de sete camadas: Aplicação, Apresentação, Sessão, Transporte, Rede, Enlace de dados e Física. Como na imagem a seguir:

![[Camada-OSI.png]]

Sendo 1 a camada mais "física" realmente, e o 7 o mais abstrato.

O modo com que há a comunicação é como na imagem abaixo: 

![[Exemplo-Comunicação-Nós.png]]

A conexão só ocorre quando há 2 nós interessados em trocar informações. A mensagem só começa a ser enviada, quando as aplicações querem se comunicar entre si. Ou seja, a mensagem é inicialmente passada entre todas as camadas, até chegar na física, onde é enviada para outro nó, no formato de bits, chegando lá, será interpretada na camada física, e sendo passada até a camada de aplicação, na qual é o destino da mensagem. 


Normalmente dividimos o modelo de referencia em camadas superiores, e camadas inferiores, onde temos:

Camadas superiores:
- Prestam serviços relacionados com a natureza da aplicação. Onde tratam de aspectos de interoperação de aplicações.
Camada inferiores:
- Possibilitam a interconexão de sistemas ou equipamentos individuais. Onde são relacionadas a aspectos de transmissão e interconexão.
Camada de transporte (Intermediaria):
- Provê a comunicação fim-a-fim entre aplicações.

### Princípios do modelo

A ideia foi agrupar as funções similares e separar de acordo com processos e tecnologias diferentes, onde as alterações de funções ou protocolos de uma camada não afetem as outras. Que cada camada possui fronteiras somente com a sua camada superior e inferior. 

E que cada camada seja composta, por serviços, que são relacionados a prover funcionalidade, e protocolos, que são relacionados a execução da funcionalidade.

#### Serviço

É a comunicação entre camadas, que é feita através da requisição de, e da resposta a, serviços. Cada camada é responsável por um conjunto de serviços. (Serviço = o que). A existência de uma camada está atrelada a prestação de serviço, sua justificativa. 

Uma camada (N) fornece serviços a uma camada (N+1)( Baixo para cima) através da invocação de primitivas de serviço, como connect, abort, data.


#### Protocolos

São comunicações que ocorrem entre camadas de mesmo número em nós distintos, e é feita através de protocolos. Eles são um conjunto de regras que governam a interação em sistemas distribuídos. Elas devem ser comuns para os dois nós para que tenha o exito na comunicação.
Eles existem como forma de viabilizar a prestação de serviços pelas camadas (protocolo = como).
Para que dois parceiros se comuniquem eles devem especificar o mesmo protocolo, e os serviços, tem caráter "vertical", enquanto os protocolos tem caráter, "horizontal".

um exemplo fica a respeito do trafego de bits pelas camadas físicas, como o reconhecimento de 0 e 1 ser por potencial elétrico, onde 5V representa 1, e 0V representa 0. Se os dois nós não tiverem o mesmo "acordo", ou melhor, protocolo, os dados serão interpretados erroneamente. 

As mensagens passadas de camada a camada, podem ser alteradas, adicionando informações a carga útil. 

Esse conjuntos de informações, e carga útil, recebem nomes, sobre o encapsulamento dos dados, que são dadas de acordo com cada camada.
As chamadas unidades de dados de protocol, ou (PDU), são definidas da seguinte maneira:

![[Nome-PDUS.png]]

Cada PDU é composto por cabeçalhos (headers), a carga útil, e a rabeira (trailer).

Normalmente as camadas adicionam headers, entretanto a camada de enlace de dados adiciona um header, e um trailer também.

![[Exemplo-headers-trails.png]]

Aqui fica visível um dos problemas do modelo em camadas, onde é ocupado um maior espaço devido ao acréscimo dos cabeçalhos, ocupando uma maior parte da infraestrutura, além de causar um overhead com o processamento de maiores dados.
## Arquitetura IEEE 802 e Modelo TCP/IP

Surgiu da tentativa de estabelecer uma arquitetura padrão, nos moldes do RM-OSI/ISO, orientada para redes locais. Ela define somente padrões equivalentes para os níveis físicos e de enlace do RM-OSI. 

Temos por exemplo:

- IEEE 802.3 - Ethernet e MAC (Media Access Control)
- IEEE 802.8 - Fibra ótica
- IEEE 802.11 - Wireless LAN, que resultou no WiFi
- IEEE 802.15 - Wireless Personal Area Network, que resultou no Bluetooth.


### Modelo TCP/IP

#### DARPA - Defense Advanced Research Projects;

#### TCP/IP - Transmission COntrol Protocol/Internet Protocol:

- Objetivo: Interconexão e coexistência de redes (LANs, MANs e WANs heterogêneas);
- Baseado no RM-OSI/ISO;
- Cobre níveis mais altos que a arquitetura IEEE 802;
- Não se trata de um órgão de padronização;
- Padrão "de mercado" para interconectividade.

![[Equivalência-OSI-TCP-IP.png]]

Exemplo simples do funcionamento do protocolo TCP/IP

![[Exemplo-Comunicação-TCP-IP.png]]

Maria envia uma mensagem à João dizendo Olá!
A camada de aplicação coloca o primeiro header, e envia para a camada de transporte, que adiciona a origem e o destino, sendo elas portas TCP, como header, e sua carga útil se torna tudo que foi recebido da camada anterior.
Chegando na camada de Internet, ele coloca como header também a origem e destino, porém agora com endereços IPs, e sendo a carga útil agora, tudo que ela recebeu da camada de transporte, ou seja, tanto os dados da própria camada de transporte, como a de aplicação.
Já na camada de Acesso á rede, coloca o seu header, contendo origem e destino, porém em endereços MACs, que por fim, é transformado em um sinal, e transmitido por um meio de transmissão até chegar no João.