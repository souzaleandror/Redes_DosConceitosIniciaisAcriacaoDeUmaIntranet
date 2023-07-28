#### 28/07/2023

Curso de Redes: dos conceitos iniciais à criação de uma intranet

@01-Camadas, protocolos, ping e traceroute

@@01
Apresentação

Boas-vindas ao primeiro curso da formação de Redes! Meu nome é Lucas e sou instrutor na Alura.
Lucas é uma pessoa branca com cabelos e barba pretas. Usa óculos de grau redondo com armação preta e uma camiseta preta escrita "Alura". Ao fundo, estúdio com iluminação roxa. À direita, uma estante com decorações e à esquerda um vaso com planta.
Esse curso é voltado para pessoas que querem resolver problemas e entender mais sobre a implementação de redes de computadores.

O foco será na aplicação prática dos principais conceitos envolvidos na construção e operação de redes. Para realizar esse curso, não há pré-requisitos.

O que vamos aprender?
Como as redes estão organizadas;
Analisar o funcionamento da internet;
Selecionar e configurar dispositivos de rede;
Conectar servidores em uma rede, incluindo servidores DNS;
Construir redes corporativas;
Avaliar e selecionar conexões e protocolos de comunicação.
Aprenderemos tudo isso de forma prática. Usaremos um simulador de redes para construir uma rede corporativa no contexto de uma fábrica, por exemplo.

Assim poderemos configurar dispositivos de rede, inserir dispositivos computacionais, servidores e também analisar o funcionamento dos diferentes protocolos de comunicação, como DHCP e DNS.

Aproveite todos os recursos da plataforma! Além dos vídeos, teremos atividades, o fórum e a comunidade no Discord.

Bora começar nossa jornada pelo mundo das redes?

@@02
O que são redes?

A internet está presente no nosso dia a dia, seja nas atividades de lazer, trabalho ou estudo. Estamos sempre usando a conexão em rede.
Mas, você já parou para pensar como a internet funciona? Como os dispositivos que compõem uma rede de computadores estão organizados? Vamos explorar e investigar esses tópicos ao longo do nosso curso.

Começaremos utilizando um exemplo simples do cotidiano. Suponhamos que hoje você irá se atrasar para chegar em casa. Por isso, precisa avisar a sua mãe que houve um pequeno atraso no trabalho ou na escola para que ela não fique preocupada.

Você utilizará um aplicativo no smartphone para escrever a mensagem e clicar no botão "Enviar". Mas, depois disso o que acontece?

O que são redes
Seu dispositivo enviará essas informações como um pacote até um dispositivo de rede mais próximo. Você talvez conheça esse dispositivo. Sabe aquele que nós sempre ligamos e desligamos quando nossa rede para de funcionar? Isso mesmo, o roteador.

Do roteador, essa mensagem será encaminhada por outros dispositivos espalhados na cidade em que você mora, até que chegue no roteador da sua casa. Desse roteador a mensagem é encaminhada para o celular da sua mãe.

Observe por quantos dispositivos essa mensagem teve que passar até que alcançasse o celular final.
Quando falamos em rede, pensamos logo em uma rede de futebol ou uma rede de pesca. A ideia de redes de computadores segue basicamente esse mesmo pensamento.

Temos vários nós, que são os dispositivos. Isso inclui tanto os dispositivos computacionais, como celular, smart TV, computador, notebook e tantos outros, como também os dispositivos de rede.

Dispositivos de rede são aqueles nós que funcionam basicamente para prover a conexão entre os dispositivos.
Essa rede possui diferentes conexões com o mesmo nó para garantir que, mesmo que uma dessas conexões se rompa, seja possível manter a integridade e funcionamento da rede. O mesmo que acontece com uma rede de pesca.

Mas, como esses nós, que são diferentes, conseguem se comunicar? Como conseguem enviar uma mensagem de um para o outro e assim chegar de um dispositivo de origem para um dispositivo de destino?

Para isso é preciso que todos eles se comuniquem usando o mesmo padrão. Observaremos isso a partir de outro caso prático do nosso dia a dia.

Quando nos deparamos com um conhecido que não encontrávamos há um certo tempo, adotamos um padrão de fala. Começamos dizendo "olá" ou "oi", uma saudação.

Essa pessoa responderá com uma saudação e a pergunta "Como você está?", demonstrando interesse. Em resposta, diremos "Tudo tranquilo. E você?", também demonstrando interesse em saber como a pessoa está. Por fim, como resposta teremos algo como "Na correria do dia a dia, trabalho e faculdade".

Observe que, mesmo em uma comunicação informal na rua, acabamos seguindo um protocolo, um padrão de comunicação. Fazemos uma saudação, seguido de uma pergunta para saber como a pessoa está, aguardamos uma resposta e depois respondemos se essa pessoa também pergunta sobre como estamos.

Similarmente, a comunicação entre dois dispositivos também segue alguns protocolos. Quando enviamos uma mensagem de um dispositivo para o outro, primeiro, precisamos iniciar a conexão.

Depois, recebemos a mensagem de conexão iniciada e na sequência, podemos fazer o envio de uma mensagem. Por fim, recebemos a confirmação de que essa mensagem foi encaminhada ao outro dispositivo em que estávamos nos conectando.

É de forma semelhante que funcionam esses padrões, que esses diferentes nós que compõem a rede utilizam para se conectar e estabelecer uma interligação e o encaminhamento de mensagens entre dispositivos.

Nesse vídeo, entendemos o que são as redes, esse emaranhado de dispositivos interligados para encaminhamento e transmissão de informações.

Compreendemos que a internet é uma rede global de dispositivos e que eles estão interligados ao redor do mundo, por isso conseguimos enviar uma mensagem de onde estamos até uma pessoa conectada em outro país ou continente.

Também sabemos o que são os protocolos que todos os dispositivos devem seguir. Mas, como estão organizados? Será que basta apenas um único protocolo para que todos os dispositivos consigam enviar uma mensagem? A resposta é não. Mas, aprenderemos mais sobre isso em breve.

Agora é o momento de colocar em prática todo o conhecimento dessa aula.

Até o próximo vídeo!

@@03
Para saber mais: características da internet

A internet é uma parte tão importante da nossa rotina que é quase uma distopia o exercício de tentar imaginar uma realidade em que não possamos utilizá-la em nossas atividades diárias. Pensando a respeito dela, você já parou para refletir ou pesquisar sobre como a internet funciona? Conseguimos nos conectar em tempo real com pessoas em diferentes lugares do mundo, acessar dados de satélite, monitorar ambientes e interagir com uma grande variedade de dispositivos.
Chama-se interoperabilidade a capacidade de interação entre sistemas bem diferentes em termos de hardware e software. Trata-se de uma característica essencial para garantir que dispositivos bem distintos (smart tv, smartphone, desktop, servidor, microcontrolador etc) sejam capazes de trocar informações usando essa mesma tecnologia de comunicação fundamental no nosso cotidiano.

@@04
Camadas de rede

Aprendemos que uma rede é formada por diversos e, ao mesmo tempo, diferentes dispositivos. Então, como podemos entender a forma que uma rede está organizada e como conecta esses diferentes nós?
Manipular roteador, modem, cabo de conexão e utilizar diferentes dispositivos para montar umaa rede seria muito complicado. Por isso, utilizaremos uma ferramenta de simulação virtual chamada Cisco Packet Tracer, que permite criar, simular e testar a conexão entre diferentes dispositivos de uma rede.

Nesse primeiro momento, não se preocupe com a instalação. Disponibilizamos uma atividade específica com o passo a passo para que você possa utilizá-la no seu computador.
Camadas de rede
Ao abrir essa ferramenta, no canto inferior esquerdo, encontramos vários dispositivos que podemos utilizar para montar uma rede. Para começar, retomaremos o exemplo da aula anterior, de encaminhamento de uma mensagem de um celular para o outro.

A organização será feita da seguinte forma: cada nova conexão adicionada será posicionada ao lado direito superior da anterior, formando meio arco.
Como começamos com o celular, clicamos no botão "end device" indicado por um ícone com um computador. Feito isso, na lateral direita abre uma lista de seleção, clicamos em smartphone e arrastamos no centro da tela.

Para encaminhar uma mensagem o smartphone precisa estar ligado a um roteador. Então, no lado inferior esquerdo, clicamos em "Network Devices", os dispositivos de rede. Depois, logo abaixo, selecionamos o roteador wireless, escolhemos a opção "WRT300N" e arrastamos ao lado direito do smartphone.

Observe que automaticamente o celular detecta a presença do roteador e faz a conexão sem fio com ele, indicado por uma linha tracejada.

Depois, a mensagem era encaminhada para um roteador no qual o celular estava conectado. Em seguida, essa mensagem era encaminhada por outros roteadores que estavam no meio do caminho da rede.

Muitas vezes esses roteadores pertencem ao provedor de serviço de conexão à internet. Então, vamos inserir mais roteadores no caminho, simulando um trajeto na rede.

Para isso, clicamos no "1240" e arrastamos para a tela, repetimos esse procedimento mais duas vezes, totalizando mais três roteadores.

Nesse momento, vamos simular de forma ilustrativa, sem nos preocuparmos com os principais aspectos construtivos.
Agora faremos a conexão entre esses dispositivos. Clicamos no ícone identificado por um raio, no canto inferior esquerdo da ferramenta. Como estamos começando, utilizaremos a conexão que selecionará automaticamente uma conexão cabeada para conectar dois dispositivos ou selecionar uma dessas conexões específicas. Para isso, ao lado direito, clicamos no segundo ícone identificado por um raio.

Agora, para inserir o roteador que temos em casa, clicamos em "Network Devices" depois em "Wireless device" e arrastamos para a tela o "Home Router". Em seguida, adicionamos outro smartphone que será o destino da nossa mensagem.

Mas, como essa mensagem será encaminhada? Precisamos de um tipo de conexão física, ou seja, cabeada entre esses dispositivos, principalmente os roteadores.

No menu inferior esquerdo, clicamos em "Connections", indicado pelo ícone de um raio. Feito isso, la lateral direita visualizamos vários tipos de conexões diferentes.

Nesse momento, não vamos nos aprofundar nesse tema. Portanto, selecionamos novamente a conexão de modo automático indicada pelo raio e depois clicamos nos dispositivos que queremos conectar. Primeiro, no roteador wireless router 4 com o router 6, seguido do router 7, 8 e por fim no router 3.

Simulação de conexão entre diferentes dispositivos de uma rede. Organizados em um formato de meio arco, a conexão inicia com um *smartphone*, seguido por um roteador wireless, três outros roteadores, um roteador wireless e finaliza com o *smartphone*. A conexão entre os primeiros dois roteadores é indicada por uma linha contínua e os demais por uma linha tracejada.

Assim temos uma conexão na qual a mensagem pode trafegar do nosso celular para o celular que está em casa.

Repare que temos um roteador que está no ambiente no qual nos encontramos, um roteador que está em casa e vários outros roteadores no meio do caminho, que muitas vezes pertencem aos provedores de serviços de conexão com a internet.

Mas, como a mensagem irá trafegar por esses diferentes dispositivos? Quem definirá essa rota de tráfego? Como a mensagem vai saber qual é o seu dispositivo de destino nessa rede? Como esses dispositivos estão organizados?

Aprenderemos isso na aula seguinte!

https://cdn1.gnarususercontent.com.br/1/1319051/c8528c26-1016-440d-9013-c0ffef7e9cb7.jpg

@@05
Camadas de Rede 2

Acabamos de construir uma rede, agora vamos analisá-la.
Uma rede, além dos protocolos de comunicação, possui também algumas camadas.

Vamos relembrar como esse processo acontece. Começamos enviando uma mensagem de um smartphone para o outro.

Essa mensagem precisa ser encaminhada por meio de conexões físicas diversas, como pulsos luminosos, elétricos ou ondas eletromagnéticas.

Para que essa mensagem chegue de forma íntegra e privada no dispositivo final, precisamos seguir uma série de protocolos.

Esses protocolos serão organizados em quatro camadas específicas. Vamos conhecer cada uma delas.

Camada de aplicação
Tudo começa no smartphone. A mensagem é escrita em um aplicativo que está em contato direto com a primeira camada de rede chamada aplicação.

Um exemplo de protocolo que atua em conjunto com um aplicativo como o Web Browser é o http.
Camada de transporte
Na sequência, ao clicar no botão de envio da mensagem, ela será preparada para o transporte.

A mensagem será empacotada de forma com que possa ser transportada por meio da rede.

Camada de rede
A camada seguinte é a de rede, que atua no roteador e é responsável por conectar dispositivos diferentes.

O principal protocolo utilizado é o de endereçamento IP. A partir dele é apresentado um cabeçalho, identificando o endereço de origem e o destino.

Assim, é feito o cálculo da rota de tráfego, ou seja, os dispositivos pelos quais esse pacote de informação terá que passar até alcançar o smartphone que queremos enviar a mensagem.

Camada física
A quarta camada é a física e consiste na transmissão dos bits dessa mensagem por meio de dispositivos de rede.

Após trafegar pelos dispositivos da camada física e chegar ao roteador, que está em casa, a mensagem passará pelo processo reverso.

Isso significa que passará pelo desencapsulamento na camada de transporte até que fique disponível no aplicativo do celular da mãe.

É assim que funciona o modelo de camadas de uma rede de computadores, mais precisamente a internet.

Mas, será que conseguimos testar se o dispositivo está conectado com outro? Ou então se um servidor está ativo?

Será que é preciso de um software ou isso pode ser feito do próprio computador?

É isso que aprenderemos na aula seguinte. Até lá!

@@06
Protocolos de comunicação

Vimos que as seguintes ações são comuns em uma rede: a organização dos dados em pacotes, a transferência dos pacotes, a definição da rota de encaminhamento e a conversão física dos pacotes para transmissão a longas distâncias. Então, é parte do nosso cotidiano, por exemplo, encaminhar uma mensagem de um smartphone para outro.
Conectando dispositivos tão diversos e encaminhando uma grande variedade de dados em uma rede, como assegurar que cada dispositivo as execute do mesmo modo?

Padronizando as características físicas do sinal transmitido em uma rede.
 
Alternativa correta
Estabelecendo um conjunto de regras e padrões que definem todo o processo de comunicação, troca de dados entre dispositivos, em uma rede.
 
Essa é exatamente a definição dos protocolos de comunicação adotados para assegurar a interoperabilidade da internet.
Alternativa correta
Definindo um projeto de hardware padrão que deve ser observado por todos os fabricantes de dispositivos computacionais.

@@07
Internet organizada em camadas e protocolos

Quando acessamos um website como Youtube ou Google, utilizamos um conjunto de protocolos que são executados sobre diferentes camadas da rede. Um desses protocolos é o TCP (Transmission Control Protocol), que atua no estabelecimento de uma conexão segura entre um cliente e um servidor.
Dada sua importância no processo de comunicação, o protocolo TCP pode ser considerado como principal protagonista de qual camada da rede?

Camada de aplicação.
 
Alternativa correta
Camada de transporte.
 
TCP é o principal protocolo da camada de transporte. A principal função da camada de transporte é justamente prover comunicação segura e eficiente entre processos de aplicação em dispositivos computacionais. No caso do website, estamos falando em comunicação entre os processos do navegador - executados em nosso computador - e processos do website - executados em um servidor.
Alternativa correta
Camada de rede.
 
A camada de rede atua diretamente no encaminhamento de pacotes de dados entre dispositivos computacionais que podem estar em diferentes redes e posições ao redor do mundo. O principal protocolo da camada é o IP (Internet Protocol).

@@08
Ping e Traceroute

Já entendemos o que são os protocolos, as camadas e que as mensagens são enviadas por meio de pacotes.
Mas, como sabemos que um pacote alcançou o destino ou não? Como verificamos se um determinado computador está conectado em uma rede, se está ativo? E ainda, será possível testar a velocidade de conexão?

Acessando o terminal de comando
Para verificarmos isso, não utilizaremos a ferramenta de simulação e sim o próprio terminal de comando do nosso computador.

Para acessá-lo no sistema operacional Windows, clicamos no menu iniciar localizado no lado inferior esquerdo da tela do computador.

Na barra de busca, digitamos "cmd" seguido de "Enter". Feito isso, a primeira opção que aparece é o "Prompt de Comando", clicamos nele.

Ping e Traceroute
Para fazermos o teste de conectividade, utilizamos o comando ping seguido do endereço de rede do dispositivo que queremos testar a conectividade. Nesse primeiro momento, testaremos a conectividade com o website.

Sabemos que websites não são páginas que existem na nuvem de forma abstrata. São páginas estão armazenadas em um computador, como um servidor localizado na nossa cidade ou em países diferentes.

Então, logo pós o ping digitamos www.alura.com.br e apertamos "Enter".

ping www.alura.com.br
COPIAR CÓDIGO
Observe que esse comando envia um pacote com 32 bytes de dados. Esses são dados vazios, apenas para testar se esse pacote está alcançando o destino e com qual velocidade. Também encontramos a latência, ou seja, o tempo que levou para que esse pacote atingisse o endereço de destino.

Repare que, apesar de termos digitado o domínio da Alura, foi indicado o endereço de IP do dispositivo em que esse website está armazenado. Testaremos de outra forma.

Para isso, copiamos o endereço de IP, escrevermos ping e colarmos em sequência.

ping 104.26.5.131
COPIAR CÓDIGO
Ao rodar, percebemos que o processo de envio do pacote de dados ocorre da mesma maneira, obtendo os mesmos resultados. São enviados 4 pacotes. Todos eles foram recebidos, nenhum se perdeu pelo caminho. Além disso, o tempo mínimo, máximo e médio de resposta foi de 8 ms.

Também encontramos uma informação referente ao TTL (Time To Leave), ou seja, o tempo de espera até obter uma resposta do encaminhamento desse pacote. Se o tempo for superior ao TTL, o pacote será considerado perdido na rede.

Podemos fazer testes com outros websites, por exemplo, o youtube.com.

ping youtube.com
COPIAR CÓDIGO
Repare que o endereço de IP desse website foi identificado. Novamente foi enviado 32 bytes de dados e o tempo de resposta foi um pouco maior, 119 milissegundos. Já a latência foi menor, de 1 milissegundo. Todos os 4 pacotes enviados foram recebidos e nenhum foi perdido. Esse é o comando ping.

Sabemos que esse pacote não saiu do nosso computador nem foi para um servidor e voltou. Ele, na verdade, passou por dispositivos que estavam no meio do caminho.

Temos um comando que nos permite verificar a rota de tráfego desse pacote de dados, que se chama tracert. Se utilizarmos esse comando seguido de www.alura.com.br, dessa forma:

tracert www.alura.com.br
COPIAR CÓDIGO
Ao apertamos "Enter" obtemos a rota de tráfego do pacote que enviamos pela rede até que ele alcance o servidor no qual o site da Alura está armazenado. Também encontramos a informação referente ao número máximo de saltos para identificar o caminho que esse pacote tomou de 30 saltos.

Os saltos se referem ao número de roteadores pelos quais esse pacote de dados passou.
Repare que a primeira linha não apresenta o endereço de IP do dispositivo por questões de segurança. Já no fim, é concluído o rastreamento, identificando diferentes dispositivos pelos quais esse pacote passou até alcançar o endereço de IP onde o website da Alura está armazenado.

Se pegarmos endereço 104.26.5.131 e aplicarmos o traceroute, teremos um resultado idêntico.

tracert 104.26.5.131
COPIAR CÓDIGO
Lembrando que o resultado pode variar conforme o tráfego na rede, por exemplo, pode ser que o pacote tenha passado por outra rota.

O tráfego pelo qual o pacote passará é dinâmico e depende justamente de quão congestionado alguns ramos da rede podem estar em determinado momento.

Observamos que o comando traceroute demora um certo tempo para obtermos a resposta do rastreamento total. Nesse exemplo, ele foi informando o endereço de IP dos dispositivos e às vezes ele indica umas referências em relação a quem pertence esse dispositivo.

Muitas vezes, essa informação é referente ao provedor de serviço de conexão de internet que está ali no meio do caminho.
Já o comando ping é mais rápido e automático. Ele espera um certo tempo de resposta, se o pacote não foi recebido, ele simplesmente sai e dá o pacote como perdido.

Agora que já conseguimos testar a conectividade de um dispositivo em uma rede, é hora de colocarmos em prática a construção de uma rede. Começaremos com dispositivos mais simples até avançarmos na construção de uma intranet corporativa incluindo o servidor DNS.

Daremos os primeiros passos na próxima aula. Até lá!

@@09
Teste de conectividade

Você está criando uma rede interna com alguns computadores. Todas as conexões físicas entre os dispositivos de rede e computadores foram realizadas e agora, você deseja testar se as interligações estão funcionando corretamente.
Qual comando pode ser utilizado para verificar se dois computadores dessa rede são capazes de trocar dados entre si?

ipconfig
 
Alternativa correta
ping
 
O comando ping é usado justamente para testar a conectividade entre dois dispositivos.
Alternativa correta
hostname

@@10
Análise de redes

O gerenciamento de uma rede de computadores requer o uso de algumas ferramentas que permitam testar e analisar o que está ocorrendo no processo de comunicação. Uma das principais ferramentas é o comando ping que além de permitir o teste de conectividade entre dispositivos, possibilita identificar alguns problemas que podem ocorrer em redes.
Marque problemas que o comando ping nos auxilia a detectar:

Alta latência.
 
O ping estima o tempo necessário para que um pacote seja encaminhado de um computador para outro e retornado. Dessa forma, permite analisarmos a latência da rede, isto é, o tempo que um pacote leva para trafegar entre um computador de origem e um computador de destino.
Alternativa correta
Perda de pacotes.
 
O ping também nos ajuda a detectar a perda de pacotes na rede, indicando problemas como congestionamento ou falhas em dispositivos.
Alternativa correta
Erros de configuração.

@@11
Tráfego em redes

Quando encaminhamos um pacote de dados de um computador para outro, situado em outra rede e localização geográfica, nem sempre ele seguirá pela mesma rota, passando pelos mesmos dispositivos de rede.
Qual ferramenta podemos utilizar para verificar o caminho seguido por um pacote de dados entre um computador e outro?

Ping.
 
Alternativa correta
ipconfig.
 
Alternativa correta
Traceroute.
 
O comando traceroute exibe a rota de tráfego de um pacote de dados entre um computador de origem e um computador de destino.

@@12
Faça como eu fiz: testando ping e traceroute

Vamos agora testar a conectividade de nosso computador com a máquina do Youtube. Para isso, siga os passos referentes ao seu sistema operacional.
Caso esteja usando Windows, vá até o campo pesquisar e digite “cmd”. Na tela que abrir, digite: ping www.youtube.com.
Caso esteja usando Mac, vá até o spotlight (lupa) no canto superior direito e digite “terminal”. Selecione a opção referente a ele e na sequência, ao abrir a tela preta, digite: ping www.youtube.com.
Caso esteja usando o Linux, no campo de pesquisa, digite “terminal” e selecione a opção referente a ele. Posteriormente, digite ping www.youtube.com.
Que tal agora verificarmos a rota de comunicação entre nosso computador e a máquina do Youtube? Para isso digite:

Caso seja Windows: tracert www.youtube.com.
Caso seja Ubuntu: sudo apt-get install traceroute (caso não tenha instalado), e depois traceroute www.youtube.com.
Caso seja Mac: traceroute www.youtube.com.

Você deve ter obtido um resultado bem parecido com esse:
C:\Users\lucas>ping www.youtube.com

Disparando youtube-ui.l.google.com [142.251.129.142] com 32 bytes de dados:
Resposta de 142.251.129.142: bytes=32 tempo=1ms TTL=118
Resposta de 142.251.129.142: bytes=32 tempo=2ms TTL=118
Resposta de 142.251.129.142: bytes=32 tempo=1ms TTL=118
Resposta de 142.251.129.142: bytes=32 tempo=2ms TTL=118

Estatísticas do Ping para 142.251.129.142:
    Pacotes: Enviados = 4, Recebidos = 4, Perdidos = 0 (0% de
             perda),
Aproximar um número redondo de vezes em milissegundos:
    Mínimo = 1ms, Máximo = 2ms, Média = 1ms
C:\Users\lucas>tracert www.youtube.com

Rastreando a rota para youtube-ui.l.google.com [142.251.129.142]
com no máximo 30 saltos:

  1    <1 ms    <1 ms    <1 ms  192.168.1.10
  2     *        *        *     Esgotado o tempo limite do pedido.
  3    <1 ms    <1 ms    <1 ms  143.107.251.193
  4    <1 ms    <1 ms     1 ms  143.107.251.189
  5    <1 ms    <1 ms    <1 ms  border1.uspnet.usp.br [143.107.0.2]
  6     1 ms    <1 ms     1 ms  143.107.0.185
  7     7 ms    21 ms    21 ms  170.79.214.108
  8     2 ms     1 ms     1 ms  google-sp2.bkb.rnp.br [170.79.215.5]
  9     4 ms     2 ms     2 ms  142.251.69.141
 10     1 ms     1 ms     1 ms  142.251.78.21
 11     1 ms     1 ms     1 ms  gru14s31-in-f14.1e100.net [142.251.129.142]

Rastreamento concluído.

@@13
O que aprendemos?

Nessa aula, você aprendeu:
Uma rede de computadores consiste em uma interconexão entre dispositivos computacionais para troca de informações, em geral, no formato de pacotes de dados.
A internet é uma rede de computadores em nível global, possibilitando que dispositivos dispersos ao redor do mundo troquem informações e compartilhem recursos.
A internet está organizada em camadas e protocolos. Cada camada possui uma função bem definida no encaminhamento de mensagens entre um computador e outro, sendo as principais do modelo de pilha de protocolos: aplicação, transporte, rede e física.
Protocolos de comunicação são conjuntos de definições e especificações que orientam o processo de troca de dados entre dispositivos diferentes em uma rede de comunicação.
Utilizar o comando ping para verificar a conectividade entre dispositivos computacionais.
Usar o comando traceroute para verificar a rota na qual um pacote de dados está seguindo na rede.