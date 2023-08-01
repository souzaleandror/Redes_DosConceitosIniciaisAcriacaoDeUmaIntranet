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

#### 29/07/2023

@02-Conectando computadores

@@01
Instalando o Packet Tracer

Vamos começar instalando uma ferramenta que nos ajudará a construir e simular o funcionamento de redes de computadores.
Instalando o Cisco Packet Tracer
Utilizaremos a ferramenta de simulação Cisco Packet Tracer fornecida pela Cisco (fabricante de dispositivo de rede). Não é open source, porém, o uso é livre para fins educacionais.

Cisco Packet Tracer

No site do Cisco Packet Tracer, vamos entrar em "Cisco Networking Academy", sendo uma acadêmia com alguns cursos para certificação Cisco. Selecionamos o botão "View courses" e na janela exibida selecionamos "Skills For All".

Cisco Packet Tracer
Seremos redirecionamos para a página de criação de login. Para isso, clicamos no ícone de foto no canto superior direito para preenchermos os dados. No caso, usamos a opção "Google" para logarmos com a nossa conta do Google. Na sequência será solicitado o e-mail e senha, vamos preenchê-los e clicar no botão "Avançar".

Após fazermos o login com a conta Google, somos redirecionados para uma página com os seguintes campos a serem preenchidos:

Seu país ou região de residência:
Ano de nascimento
Mês de nascimento
Em "Seu país ou região de residência" escolhemos a opção "Brazil". O nosso ano e data de nascimento.

Preenchimento com a data de nascimento da pessoa instrutora:
Seu país ou região de residência: Brasil
Ano de nascimento: 1993
Mês de nascimento: Agosto
Clicamos no botão verde "Continuar". Será aberto o "Termos e Condições", onde descemos a tela até o final e clicamos no botão verde "Aceitar e continuar".

Na página seguinte, encontramos uma mensagem de boas-vindas e podemos imediatamente explorar os cursos disponíveis na Cisco Networking Academy. A fim de baixar e instalar o Packet Tracer em nossas máquinas, é necessário se inscrever no curso "Começando com o Cisco Packet Tracer" ao clicarmos no botão "Navegar pelo catálogo".

No primeiro item o curso temos o link para efetuar o download. Para isso, clicamos na página do curso, em seguida, em "Comece já". Do lado esquerdo da página do curso, podemos clicar na seção "Baixar o Cisco Packet Trace" onde teremos acesso ao link de download.

Somos redirecionados para uma tela com algumas etapas chamada de "Learning Resources" (em português, "Recursos de aprendizagem"). Clicamos no link "Packet Tracer 8.2.1 Windows 64bit", localizado na etapa 1 (Step 1).

Escolha o sistema operacional de acordo com o que usa na sua máquina
Ao clicarmos, o arquivo será baixado. Após a conclusão do download, procedemos clicando no arquivo executável para realizar a instalação do Packet Tracer em nosso computador.

Após baixar e instalar a ferramenta em nosso computador, ao abrirmos, nos depararemos com uma interface contendo uma mensagem solicitando o login. Durante o processo de download, foi necessário vincular nossa conta Google ao Skills For All. Portanto, para prosseguir, clicamos no botão verde "Skills For All" localizado no lado direito.

Seremos redirecionados para a página do Skills For All da Cisco, e clicamos novamente na opção de logar com a conta Google. Encontraremos a seguinte mensagem em uma página que será aberta no navegador:

You have successfully logged in to Cisco Packet Tracer. You may close this tab.
Informando que estamos logados corretamente na conta do Cisco.

Ao irmos na ferramenta, ela está livre para o uso.

https://www.netacad.com/courses/packet-tracer

https://skillsforall.com/learningcollections/cisco-packet-tracer?courseLang=pt-BR&utm_source=netacad.com&utm_medium=referral&utm_campaign=packet-tracer&userlogin=0

@@02
Criando uma rede com 3 computadores

Agora que já adquirimos conhecimento sobre os protocolos de comunicação e sua organização nas camadas da internet, bem como sobre testar a conectividade entre dispositivos em rede, é hora de iniciarmos a criação de nossa própria rede.
Criando uma rede com Packet Tracer
Vamos considerar um caso simples para começar. Imaginemos uma empresa no setor de manufatura, como por exemplo, no setor têxtil, que possui uma linha de produção composta por três máquinas.

Essas máquinas precisam trocar informações e transmitir dados durante o processo. No entanto, não é necessário nem prático conectar essas máquinas à internet, por questões de segurança e organização da rede interna.

Para implementar esse caso, utilizaremos nossa ferramenta de simulação, o Packet Tracer. Primeiro, abrimos a ferramenta e, em seguida, selecionamos três PCs no canto inferior esquerdo onde fica a caixa de componentes de rede, na seção "End Devices". Clicamos especificamente em PC, arrastamos e soltamos a tela da área de trabalho.

Caso o tamanho do PC esteja pequeno, você pode aumentar o zoom clicando no ícone de lupa com um sinal de mais no menu superior para facilitar a visualização. Como temos três máquinas na linha de produção, vamos repetir esse processo para inserir três computadores diferentes.

Renomeando os computadores
Observamos que os nomes desses computadores estão com um nome padrão, sendo: "PC3", "PC4" e "PC5".

Para facilitar a identificação, vamos renomear os computadores. O primeiro computador será renomeado como "Manufatura", o segundo como "Acabamento" e o terceiro como "Embalagem". Para fazer isso, clicamos no nome existente abaixo de cada computador, apagamos o texto atual e digitamos o novo nome de sua preferência.

Nomes dos três computadores:
Manufatura
Acabamento
Embalagem
Para interligar os três computadores, precisamos de um dispositivo de encaminhamento de pacotes, como um Hub. Vamos usar um Hub mais simples e econômico para começar. No menu inferior esquerdo, na seção de dispositivos de rede (em inglês, "Network Devices") ou podemos usar o atalho "Ctrl + Alt + R", e buscamos por "Hubs" ou usamos o atalho "Ctrl + Alt + U".

Selecionamos o "PT-Hub" e o arrastamos para o projeto. Colocamos o Hub acima dos três computadores, em formato de piramidal.

Simulação de conexão entre diferentes PCs  de uma rede.  A estrutura é organizada em formato piramidal, com um Hub no topo, interligado a três PCs na base por meio de cabos diretos. Da esquerda para a direita, os PCs estão identificados como Manufatura, Acabamento e Embalagem.

Conectando os computadores
Com três computadores e um dispositivo de rede para interligá-los, precisamos fazer a conexão utilizando cabos. Como o dispositivo de rede que estamos utilizando não permite conexão Wi-Fi, faremos a conexão cabeada. Vamos para a opção "Conexões" no ícone de raio no canto inferior esquerdo (atalho "Ctrl + Alt + O") e selecionamos a opção "Copper Straight Through" (em português, "Cobre Direto").

Clicamos no cabo desejado e, em seguida, clicamos no dispositivo que desejamos interligar (no caso, "Manufatura") e selecionamos a porta que será utilizada para a conexão, neste caso, a "Fast Ethernet".

Para isso, clicamos com o botão direito do mouse no PC "Manufatura" e depois na opção "Fast Ethernet0" e, em seguida, clicamos no Hub, escolhendo a porta desejada para a conexão de forma arbitrária. No caso, podemos selecionar "FastEthernet0".

O Hub possui diversas portas porque é utilizado para interligar dispositivos diferentes.
Da mesma forma, faremos a conexão do computador "Acabamento" com o Hub. Utilizando a conexão de cabo direto, selecionaremos a porta "Fast Ethernet" no computador e escolhemos a porta no Hub em que o computador será conectado, por exemplo, "Fast Ethernet 1".

Replicamos esse processo para o computador de "Embalagem". Vamos selecionar a porta "Fast Ethernet 0" no nosso computador e conectá-la na porta "Fast Ethernet 2" do nosso Hub. Agora nós temos todos os dispositivos interligados. Observem que as conexões estão verdes, o que significa que fizemos tudo corretamente até agora.

Lembrando que nos vídeos anteriores mencionamos que cada dispositivo possui um endereço único de identificação em uma rede. Fizemos a conexão física, mas agora, precisamos fazer o endereçamento para nossa rede. Neste primeiro momento, faremos o endereçamento de forma manual.

Então clicamos no PC "Manufatura". Ao clicarmos com o botão esquerdo do mouse, observamos que uma janela é aberta. Nessa janela, encontramos diferentes opções: Physical, Config, Desktop, Programming e Attributes.

Acessamos a aba Desktop e, em seguida, selecionamos a opção "IP Configuration", que está localizada no canto superior esquerdo. Ao clicarmos nesta opção, será exibida uma janela com alguns campos a serem preenchidos e selecionados.

No primeiro campo nomeado "IP Configuration" nos deparamos com duas escolhas? DHCP e Static. Vamos começar com a opção de IP estático, onde digitaremos um endereço IP para esse computador em "IPv4 Adress".

Digitamos arbitrariamente o endereço 193.168.3.1 e pressionamos "Enter". Observe que é um endereço válido e a parte da máscara de sub-rede (Subnet Mask) foi preenchida automaticamente. Realizaremos esse processo para as demais máquinas.

193.168.3.1COPIAR CÓDIGO
Desktop
IP Configuration: Static
IPv4 Address: 193.168.3.1
Agora precisamos atribuir os endereços também para os computadores "Acabamento" e "Embalagem". Iniciamos pelo "Acabamento". Ao clicarmos com o botão esquerdo do mouse, abrirá uma janela, depois selecionamos na parte superior "Programming". Vamos selecionar a opção Desktop na seção Programming.

Vamos acessar a opção IP Configuration para configurar o endereço IP do computador "Acabamento" localizado no canto superior esquerdo. Digitamos um endereço bastante similar ao que foi digitado para o computador "Manufatura".

No caso, vamos utilizar o endereço 192.168.3.2, onde mudamos o último octeto para .2. Lembre-se de que para o computador "Manufatura" foi utilizado o endereço .1". Vamos entender o motivo em breve.

192.168.3.2COPIAR CÓDIGO
Desktop
IP Configuration: Static
IPv4 Address: 193.168.3.2
Pressionamos "Enter". O endereço é válido e a máscara de sub-rede foi preenchida automaticamente. Vamos fechar a janela.

Agora, vamos realizar o mesmo processo para o computador "Embalagem".

Vamos clicar no PC "Embalagem" com o botão direito do mouse e depois em Desktop, em seguida em IP Configuration. Vamos digitar o endereço 192.168.3 e modificar a parte final. Para o computador de "Manufatura", usamos .1, para "Acabamento" usamos .2 e agora para o computador de "Embalagem" vamos utilizar .3.

192.168.3.3COPIAR CÓDIGO
Desktop
IP Configuration: Static
IPv4 Address: 193.168.3.3
Teclamos "Enter", e observamos que colocamos um endereço válido e a máscara de sub-rede é preenchida automaticamente. Está configurado, vamos fechar a janela.

Agora que temos os endereços para todos os computadores, é hora de testar a conectividade entre essas máquinas.

https://cdn1.gnarususercontent.com.br/1/723333/8fd2131d-b79e-4b66-a9ed-05054b738cf0.png

@@03
Teste de conectividade

Como podemos simplificar o teste de conectividade? Podemos utilizar o comando ping, que já conhecemos. Basta executá-lo em nosso ambiente de simulação para verificar se o pacote foi enviado corretamente e recebido pela máquina de destino.
Vamos clicar no computador da manufatura, e abrirá a aba para configurar o endereço de IP que usamos para configurar o endereço de IP. No entanto, nesse momento, desejamos abrir o prompt de comando, onde digitaremos o comando ping, correto?

Então, selecionamos a quarta opção "Command Prompt". Observe que será aberto um prompt de comando semelhante ao utilizado para realizar o teste de conectividade com o ping.

Digitamos o comando ping seguido do endereço de IP da máquina com a qual desejamos fazer o teste de conectividade. Neste caso, será a máquina da embalagem, que foi o último endereço que configuramos.

ping 193.168.3.3
COPIAR CÓDIGO
Agora, pressione a tecla "Enter" para verificar a conectividade entre o computador da manufatura e o computador da embalagem.

Como podemos realizar o teste de conectividade? Em vídeos anteriores, recebemos uma dica: podemos usar o comando ping. Mas será que o ping funciona neste ambiente de simulação? Sim, o comando ping também é funcional nesta simulação e nos permite realizar o teste.

Para isso, vamos alterar o modo de operação de tempo real (RealTime) para o modo de simulação (Simulation) na rede, localizado do lado direito do Packet Tracer. Observe que agora apareceu um painel de simulação do lado direito que mostrará os protocolos que estão sendo executados na nossa rede.

Agora realizaremos um teste de conectividade usando o comando ping entre o computador da manufatura e o computador da embalagem. Antes disso, vamos iniciar a simulação clicando no botão "play" dos controles na parte inferior.

Com a simulação iniciada, clicamos com o botão direito na máquina da manufatura. Isso abrirá uma janela semelhante àquela que já utilizamos anteriormente para configurar o endereço IP.

Para realizar o teste do ping, utilizamos o prompt de comando em nosso computador. Aqui não é diferente, vamos abrir a opção do prompt de comando clicando em "Command Prompt". Nele, digitamos o seguinte comando:

ping 193.168.3.3
COPIAR CÓDIGO
Pressionamos a tecla "Enter" e verificaremos se os pacotes serão enviados com sucesso.

Observamos no prompt a forma como o comando está sendo executado e como as mensagens - os pacotes de informações que estão sendo enviados por meio desse comando - estão sendo transmitidos através da nossa rede em "Event List" em Simulation Painel.

Nesse ponto, podemos observar o funcionamento do hub, como ele opera, e, ao mesmo tempo, os protocolos que estão sendo executados em segundo plano, na coluna "Type" da seção "Event List" do Painel de simulação.

Como retorno no prompt de comando, obtemos:

Pinging 193.168.3.3 with 32 bytes of data:
Reply from 193.168.3.3: bytes=32 time-8ms TTL-128 Reply from 193.168.3.3: bytes=32 time=4ms TTL-128

Reply from 193.168.3.3: bytes-32 time=4ms TTL-128

Reply from 193.168.3.3: bytes=32 time=4ms TTL=128

Ping statistics for 193.168.3.3: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss), Approximate round trip times in milli-seconds: Minimum 4ms, Maximum 8ms, Average = 5ms

Todos os 4 pacotes enviados foram recebidos pelo computador da embalagem. Isso significa que o teste de conectividade foi bem-sucedido, ou seja, o computador da manufatura e o da embalagem estão devidamente conectados. Observamos isso em Sent = 4, Received = 4.

Mas, antes de prosseguir, vamos observar os protocolos que estavam em funcionamento em segundo plano. Se você rolar para cima, na aba do Painel de Simulação (Simulation Painel), localizada no canto intermediário direito da nossa tela, podemos verificar que tínhamos o protocolo ICMP, seguido pelo protocolo ARP e, em seguida, o protocolo ARP várias vezes.

O protocolo ICMP é fundamental para o funcionamento do comando "ping". É esse protocolo que controla o envio dos pacotes de mensagens por meio dos pedidos (request) e das respostas (reply), permitindo a verificação da conectividade entre dispositivos em uma rede.

Por outro lado, temos o protocolo ARP, que desempenha o papel de identificar o endereço físico de uma máquina com base em seu endereço IP.

Por isso ele foi utilizado. Quando o pacote foi recebido pelo Hub, continha o endereço IP da máquina de destino, o que exigiu que o Hub realizasse a correspondência entre o endereço IP e o endereço físico dessa máquina. No entanto, o que observamos?

Ao longo de todo o processo do ping, foram enviados quatro pacotes. Esses pacotes partiram do computador da manufatura, passaram pelo HUB e, ao invés do HUB, através do protocolo ARP, identificar que esses pacotes eram destinados apenas ao computador da embalagem e enviá-los somente para esse destino, o que ocorreu? Eles também foram enviados para o computador do acabamento.

Não apenas o primeiro, mas todos os quatro pacotes. E da mesma forma, quando o computador da embalagem mandava uma resposta de que tinha recebido a mensagem do computador da manufatura e que tudo tinha dado certo, o Hub enviava essa resposta também para o computador do acabamento.

O HUB funciona como um dispositivo que encaminha mensagens para todos os dispositivos conectados a ele, sem identificar o destinatário específico. É semelhante a um carteiro que distribui cartas para todas as casas em um determinado bairro, sem especificar o destinatário de cada carta.

Portanto, ao enviar uma mensagem através de um Hub, essa mensagem será recebida por todos os dispositivos conectados a esse Hub, e não apenas pelo dispositivo pretendido.

Em uma situação em que o computador da manufatura e o computador da embalagem enviam simultaneamente pacotes de informações para o computador do acabamento, ocorrerá um congestionamento no Hub. Como resultado, nenhuma das mensagens será encaminhada.

O Hub funciona segundo o princípio de broadcast, ou seja, ele envia as mensagens para todos os dispositivos conectados a ele. No entanto, esse método pode gerar congestionamento na rede.
O Hub desperdiça tempo de conexão ao enviar mensagens para dispositivos que não estão relacionados àquela mensagem específica. Além disso, existe o risco de mensagens confidenciais, destinadas a um endereço específico, serem acessadas por pessoas nos computadores conectados ao HUB.

Essas situações podem ocorrer devido à natureza do funcionamento do HUB, que realiza o broadcast indiscriminadamente, sem distinguir os destinatários das mensagens ou garantir a privacidade dos dados transmitidos.
Por ser um dispositivo simples e de baixo custo que pode ser utilizado em redes com requisitos mais básicos, onde a comunicação entre os computadores interligados não é tão frequente.

Entretanto, para aplicações que demandam maior eficiência e requisitos mais avançados, é necessário utilizar dispositivos mais sofisticados. Esses dispositivos têm a capacidade de detectar o destino correto de cada mensagem e encaminhá-la apenas para o destinatário específico.

Em breve, estudaremos essas alternativas mais avançadas. Até mais!

@@04
Funcionamento dos hubs

Vimos, na prática, que o hub é um dispositivo de rede que atua no encaminhamento de mensagens entre dispositivos computacionais que estão conectados em suas portas.
Quais são as principais limitações de um hub?

Congestionamento e vulnerabilidade de segurança.
 
Os hubs não memorizam o endereço e localização de cada máquina, sendo assim, ao receberem uma mensagem, a encaminham para todas as demais máquinas conectadas. Caso ocorra um fluxo intenso de tráfego na rede, teremos essa informação sendo encaminhada para todos os demais usuários causando lentidão e congestionamento na rede. Além disso, quando usuários enviam uma mensagem destinada para um usuário específico, os demais usuários da rede também irão recebê-la, causando assim uma vulnerabilidade de segurança.
Alternativa correta
Memória interna com pequeno espaço e alto preço de mercado.
 
Alternativa correta
Potência do sinal wifi.

@@05
DNS e Nslookup

Ao acessar um website, utilizamos, em geral um nome facilmente memorizável. Quando começamos a estudar redes, observamos que cada máquina disponível na rede possui um endereço de IP que permite identificá-la facilmente enviar uma requisição, um pacote ou mesmo receber no dispositivo.
Como é feito o mapeamento entre o nome que digitamos e o endereço da máquina em que esse website está disponível ao público na internet? Para isso, usamos o protocolo DNS (Domain Name System), que funciona semelhante à agenda telefônica que temos no celular, na qual identificamos cada número salvo com um nome facilmente memorizável. Da mesma forma funciona o DNS.

Para analisar o funcionamento do DNS, temos uma ferramenta administrativa, que é o comando nslookup, que podemos usar no prompt de comando do nosso computador. Vejamos como isso funciona.

Vamos abrir o prompt de comando e passar nslookup. Nesse teste, vamos utilizar o site da Alura, então o comando ficará assim:

nslookup www.alura.com.br
COPIAR CÓDIGO
Não é resposta autoritativa: Nome: www.alura.com.br Addresses: 2606:4700:20::ac43:48e8 2606:4700:20::681a:483 2606:4700:20::681a:583 172.67.72.232 104.26.4.131 104.26.5.131
Ao teclar "Enter", obtemos o resultado do nosso comando com algumas respostas. Note que há dois tipos de endereço: o endereço de IP e o endereço maior, então são dois tipos de máquina. Além disso, nos é informado que a resposta não é autoritativa, o que significa que ele não precisou consultar nenhum servidor autoritativo externo à nossa rede para fazer esse mapeamento. Armazenar esse mapeamento em nossa rede representa facilidade porque não precisamos esperar um longo tempo até que essa resposta chegue ao digitarmos, por exemplo, o comando nslookup em um terminal.

Vamos fazer mais um teste, agora com o site do Google:

nslookup www.google.com
COPIAR CÓDIGO
Não é resposta autoritativa: Nome: www.google.com Addresses: 2800:3f0:4001:833::2004 142.250.218.228
Perceba que temos uma resposta semelhante, também não autoritativa, mas com menos endereços.

Agora, façamos um teste com um nome de domínio que sabemos ser inválido, como wyz.

nslookup wyz
COPIAR CÓDIGO
Unknown não encontrou wyz: Non-existent domain
Como retorno, obtemos que não existe esse domínio na rede.

Agora que já sabemos fazer o mapeamento entre o endereço de IP e o nome de domínio, que tal entendermos melhor como funciona a conexão entre dois dispositivos? Por exemplo, entre o computador e o hub: como o cabo de conexão envia e recebe dados?

@@06
Protocolo DNS

Vimos que o protocolo IP é utilizado para endereçamento de dispositivos em redes. Quando acessamos um website em nosso notebook, por exemplo, estamos acessando uma página que está armazenada em alguma máquina.
Qual é o papel dos servidores DNS nesse processo?

Tradução de endereços IP em endereços MAC.
 
Alternativa correta
Tradução de URLs para endereços IP.
 
Essa é a função dos servidores DNS, realizar um mapeamento entre endereços IP e URLs. Sendo assim, quando digitamos www.alura.com.br no navegador, o protocolo DNS atua na tradução entre o nome da URL e o endereço IP.
Alternativa correta
Tradução de endereços em IPv4 para IPv6.

@@07
Consultando servidores DNS

Ao configurar nossa rede, precisamos obter informações sobre o servidor DNS do domínio que estamos utilizando. No terminal, podemos consultar os servidores DNS para obter informações como o nome e o endereço de IP do servidor do domínio consultado.
Qual dos comandos abaixo podemos utilizar no terminal para realizar essa tarefa?

tracert nomedodominio.com.br
 
Alternativa correta
ping nomedodominio.com.br
 
Alternativa correta
nslookup nomedodominio.com.br
 
O Nslookup pode ser usado para descobrirmos o endereço IP de um domínio, assim como saber detalhes mais avançados de DNS, para saber se nosso serviço está sendo direcionado para a máquina de destino, por exemplo.

@@08
Cabos de conexão

Até agora, falamos muito sobre software e pouco sobre hardware, embora tenhamos utilizado bastante hardware quando estávamos montando o caso prático de rede na indústria têxtil.
Fizemos várias conexões usando cabos e percebemos que há diferentes cabos que conectam, por exemplo, um modem com internet ou mesmo o cabo com o qual conectamos nosso desktop ao roteador. Mas como funcionam esses cabos e por que há diferentes cores e fios de um único cabo?

Neste cabo, com o qual você já deve ter familiaridade, temos um conector padronizado chamado RJ45. Dentro desse cabo, há fios com diferentes cores, então vamos entender melhor como funciona e qual o padrão desse tipo de cabo.

Cabo CAT-4 na cor azul com conector RJ45 em ambas as pontas. Popularmente conhecido como cabo de rede. 

O padrão de cores e a forma desse conector são padronizados pela Associação Internacional de Telecomunicações, a TIA. Todos os dispositivos que utilizamos, como celular, smart TV, desktop e laptop, possuem algum elemento de hardware dedicado à conexão em rede. No celular, por exemplo, haverá um elemento que estabelecerá a conexão wireless (sem fio). Já no computador, podemos ter uma placa que faz a conexão Wi-Fi e, ao mesmo tempo, uma placa que podemos plugar em um conector Ethernet, que é o caso do RJ45 que vimos na imagem anterior.

Por que temos diferentes fios dentro desse cabo? Na placa de rede, teremos diferentes canais, alguns dedicados ao envio de mensagens e outros à recepção de mensagens. É comum nos computadores que as entradas 1 e 2 da placa de rede sejam destinadas ao envio de dados, e os canais 3 e 6 sejam destinados à recepção de pacotes enviados por outros dispositivos que estão na rede.

Para facilitar a identificação desses diferentes fios e como conectá-los em uma placa de rede, adotamos um padrão de cores, como vemos nesta imagem.

À esquerda, um cabo azul do qual saem 8 fios nas seguintes cores, respectivamente: verde e branco; verde; laranja e branco; azul; azul e branco; laranja; vermelho e branco; e vermelho. À direita, um quadro intitulado "T568A" com os mesmos 8 fios seguidos por uma numeração, sendo: verde e branco para 1; verde para 2; laranja e branco para 3; azul para 4; azul e branco para 5; laranja para 6; vermelho e branco para 7; e vermelho para 8.

Esse padrão, definido pela TIA, é conhecido como T568A. Neste padrão, temos:

na posição 1, um fio verde com branco;
na 2, um fio inteiramente verde;
na 3, um fio laranja com branco;
na 6, um fio inteiramente laranja.
Esses são os canais que utilizamos para o envio e recepção de dados.

Mas como esse cabo vai se conectar no hub que utilizamos no caso que construímos? A placa de rede do hub fará a recepção e a transmissão de dados em canais diferentes da placa de rede no nosso computador. Ou seja, nos canais 1 e 2 ela receberá as informações, enquanto nos canais 3 e 6 fará o envio das informações, utilizando esses canais para enviar pacotes de dados para os dispositivos conectados no hub. Dessa forma, podemos usar um cabo que conhecemos como cabo direto para fazer a conexão entre um dispositivo, como o computador, e o hub.

Mas e se quisermos, por exemplo, conectar um daqueles computadores utilizados no exemplo da manufatura, diretamente com o computador da embalagem? Neste caso, teremos apenas dois computadores, então podemos fazer uma conexão direta, sem um dispositivo de rede intermediário.

Mas há um problema: essas placas de rede utilizam os mesmos canais para fazer a transmissão e recepção de dados. Sendo assim, será que podemos usar o cabo T568A nos dois casos? A resposta é não, porque teríamos um crash. Ou seja, os pacotes se encontrariam, um no sentido direto e outro no sentido inverso, causando uma colisão. Dessa forma, precisamos de outro padrão, de forma que possamos conectar, utilizando uma conexão cabeada, dois dispositivos que estão atuando no mesmo nível da rede.

A solução para isso é o cabo cruzado ou crossover. Vamos pensar na prática como funciona esse cabo. De um lado, temos a conexão do padrão T568A. Dentro do cabo cruzado, vamos inverter a posição dos fios que o constituem, que ficará da seguinte forma:

Quadro intitulado "T568B". Nele, há 8 fios enumerados da seguinte forma: na posição 1, fio laranja com branco; na 2, fio todo laranja; na 4, fio verde com branco; na 4, fio todo azul; na 5, fio azul com branco; na 6, fio todo verde; na 7, fio vermelho com branco; e na 8, fio todo vermelho.

No computador da manufatura (com padrão T568A), os fios laranja com branco e todo laranja, respectivamente nas posições 3 e 6, serão direcionados para os canais 1 e 2 da placa de rede do computador (com padrão T568B), que pode ser da embalagem ou do transporte, também nas cores laranja com branco e todo laranja, respectivamente.

Os cabos 1 e 2, no computador com padrão T568A, de cor verde com branco e todo verde, respectivamente, são destinados ao envio das mensagens, e serão direcionados para os canais 3 e 6 do computador T568B, também de cor verde com branco e todo verde, respectivamente, que farão a recepção dos dados.

Dessa forma, fazemos com que dois dispositivos, usando padrões diferentes, apenas fazendo o cruzamento dos cabos, consigam trocar informações entre si sem haver qualquer tipo de colisão nos pacotes enviados.

Agora, voltemos ao exemplo que construímos.

Simulação de conexão entre diferentes PCs de uma rede. A estrutura é organizada em formato piramidal, com um Hub no topo, interligado a três PCs na base por meio de cabos diretos. Da esquerda para a direita, os PCs estão identificados como Manufatura, Acabamento e Embalagem.Nas conexões mostradas no canto inferior esquerdo, temos tipos diferentes. A conexão que mais utilizamos foi a Copper Straight Through (cabo direto), usada como padrão para conectar um computador a um hub, por exemplo. Mas temos também a Crossover, que pode ser utilizada para conectar dois PCs, dois computadores iguais.

As placas de rede modernas já conseguem, por exemplo, fazer pequenas correções via software. Ou seja, se utilizarmos o padrão T568A em um computador e o conectarmos a um computador B, usando esse mesmo padrão, a placa de rede, se for moderna, conseguirá fazer essa correção via software, mudando os canais que ela vai receber ou transmitir dados.

Agora, vamos continuar melhorando a nossa rede. Que tal utilizarmos um dispositivo diferente no lugar do hub?

https://cdn1.gnarususercontent.com.br/1/1310269/1ba5e30c-ec13-428c-aade-b6730b61868b.png

https://cdn1.gnarususercontent.com.br/1/1310269/5455e0cd-a76a-42fc-a807-f79ffd712834.png

https://cdn1.gnarususercontent.com.br/1/1310269/615c19b6-fb75-4e7d-a45c-3dbeaaaa9e08.png

@@09
Cabo cruzado

Quando precisamos conectar dois computadores diretamente, sem usarmos um dispositivo de rede como o hub, devemos utilizar um cabo que leve em consideração que os dispositivos conectados possuem uma placa de rede bastante similar.
Por qual motivo usamos o cabo cruzado nesse caso?

Possui fios internos em posições diferentes em cada ponta.
 
Os cabos cruzados possuem um padrão de cores diferente em cada ponta do cabo. Dessa forma, pode ser utilizado para conectar canais de transmissão e recepção em dispositivos com placa de rede similar.
Alternativa correta
Possui a mesma sequência de cor nas mesmas posições nas duas pontas do cabo.
 
Alternativa correta
Possui sequência de cores aleatórias nas duas pontas.

@@10
Cabos diretos e computadores

Em um projeto precisei interconectar dois computadores diretamente, pelo fato de não ter cabo cruzado, resolvi fazer o teste com cabo direto e consegui “pingar” o outro computador.
Qual é a provável razão para isso ter acontecido?

Isso não é possível de nenhuma forma.
 
Alternativa correta
É provável que tenha sido um erro de fábrica que colocou a placa de rede incorreta no computador.
 
Alternativa correta
É provável que as placas de rede possuam um padrão auto-MDIX capaz de detectar quando conectamos um cabo “errado”, realizando a correção das polaridades via software.
 
As placas de rede modernas apresentam o padrão auto-MDIX. Sendo assim, se as duas placas de rede estiverem configuradas, elas serão capazes de corrigir automaticamente a polaridade para estabelecer a comunicação.

@@11
Para saber mais: entendendo os cabos de rede

Para conhecer melhor os tipos de cabos de rede e as velocidades de transmissão, leia o artigo Entendendo os cabos de rede.

https://www.alura.com.br/artigos/entendendo-os-cabos-de-rede?_gl=1*1wquvrz*_ga*MTgwMzIzMjk2Ni4xNjg4ODE5OTcz*_ga_59FP0KYKSM*MTY5MDYzMTA5NC4zNi4xLjE2OTA2MzI2NTcuMC4wLjA.*_fplc*NXhvVSUyQmpaOTdMMmkyWWRKblRHN0UwbDRTZmo1Y0I3VCUyQlFNcklFWVlQNTNDQmpORlIwJTJCMGtsdFo2JTJCSlp6cVJFVDdLVml1V2VUdWVrMTFqcmclMkIzdzdNYVNYNVhEcklYMldkSVJWU0tPY0RCZGVxVlRHYkhrN1VDVnlSdzc1ZyUzRCUzRA..

@@12
Para saber mais: conhecendo algumas topologias de rede

Ao implementar uma rede de computadores, é necessário considerar a conexão física dos computadores, chamada de topologia física, que pode ser realizada com cabos de metal, fibra óptica ou Wi-Fi.
Além disso, é importante estabelecer regras de comunicação para permitir a interação entre os computadores, conhecida como topologia lógica. Para saber mais sobre o assunto, leia o artigo Conhecendo algumas topologias de rede.

https://www.alura.com.br/artigos/conhecendo-algumas-topologias-de-rede?_gl=1*1ye60iv*_ga*MTgwMzIzMjk2Ni4xNjg4ODE5OTcz*_ga_59FP0KYKSM*MTY5MDYzMTA5NC4zNi4xLjE2OTA2MzI2ODYuMC4wLjA.*_fplc*TWRCQmJKU3gyJTJGYVVhbFl0dkJzeHNvSlA5d0JvS0pMYnlVQm9KMUxSNlYlMkZTeSUyRm9waXZZYWVWaUhnU3JHQTM2ZVNFMHM1U2lDSUdFOWx3cWd2QWtySFZFNDhObEJ4T3ljZ2tCJTJCbFYxbHdZc25DNGtZTE1qREVuUnZEcmtya1ElM0QlM0Q.

@@13
Faça como eu fiz: crie sua rede com 5 computadores no Packet Tracer!

Agora é a sua vez de criar uma rede no Packet Tracer. Para fazer isso, siga os seguintes passos:
No canto inferior esquerdo, clique em End Devices e arraste o computador para a área de trabalho. Faça isso 5 vezes;
Posteriormente, clique no ícone Hubs e arraste o objeto para área de trabalho;
Clique no ícone Connections, selecione Copper straight-through (Cabo direto), normalmente a terceira opção, e faça a conexão na porta FastEthernet dos computadores com o Hub;
Clique em cada um dos computadores -> aba Desktop -> IP Configuration. Atribua um IP para cada computador: 192.168.3.1, 192.168.3.2,192.168.3.3, 192.168.3.4 e 192.168.3.5;
Na aba Desktop, selecione Command prompt e escreva ping (#endereço IP de um dos outros dois computadores#). Atenção! Cada computador deverá conseguir realizar o ping dos outros dois!
Então, clique na opção de simulação, abra o Command prompt e digite novamente ping (#endereço IP de um dos outros dois computadores#) e depois vá clicando no botão Capture/Forward para verificar como a informação vai passando.

Opinião do instrutor

Você deve ter obtido um resultado bem similar ao da imagem abaixo:
alt text: Rede formada por cinco computadores e um hub representada no programa Cisco Packet Tracer. Todas as cinco conexões estão em verde.

https://caelum-online-public.s3.amazonaws.com/3092-redes-conceitos-iniciais-criacao-intranet/image1.png

@@14
O que aprendemos?

Nessa aula, você aprendeu como:
Criar e simular redes no ambiente didático do Cisco Packet Tracer;
Implementar e testar o funcionamento de uma rede de computadores com um hub como dispositivo de rede;
Usar o comando nslookup para consultar servidores DNS;
Conectar dispositivos computacionais e de rede usando cabos de conexão.

@03-Switches e monitoramento de tráfego de redes

@@01
Construindo redes com switches

No exemplo que construímos, utilizamos um dispositivo de rede bem simples, o HUB. Será que conseguimos replicar esse exemplo utilizando outro dispositivo para fazer a interconexão entre os computadores que utilizamos? Vejamos!
Vamos abrir então o nosso software de simulação, Cisco Packet Tracer.

No exemplo anterior, em que estávamos numa linha de produção, tínhamos três máquinas e para cada máquina tínhamos um computador dedicado. Vamos novamente inserir as três máquinas, ou três PCs.

O primeiro, renomeamos como "Manufatura"; o segundo, como "Acabamento"; e o terceiro como "Máquina de Embalagem", no contexto da indústria têxtil.

Anteriormente nós utilizamos o Hub. Agora, optaremos por um dispositivo de rede conhecido como Switch. Então, no canto inferior esquerdo clicamos em "Network Devices" para acessar os dispositivos de rede. Na segunda opção, "Switch", selecionamos o "2950-24", arrastamos e soltamos na tela.

Já temos o dispositivo de rede. Agora vamos fazer as conexões. Neste caso, quando vamos ligar um dispositivo de rede a um computador, como um PC, utilizamos uma conexão de cabo direto. Então vamos selecionar a conexão de cabo direto, clicar no dispositivo que queremos ligar, selecionar a porta "FastEthernet0", arrastar até o Switch e clicar. Observe que 0 Switch nos dá diferentes portas. Podemos selecionar qualquer uma delas, então vamos optar por "FastEthernet0/1".

Em seguida, repetimos o mesmo processo para a segunda e terceira máquina. Feito isso, o Switch está ligado, conectado nas três máquinas e, ao que parece, está tudo em ordem. Observe que todas as conexões ficaram verdes, ou seja, estão funcionando e os computadores estão conectados no Switch.

Mas falta uma coisa: assim como fizemos no exemplo anterior, precisamos configurar o endereço de IP de cada um desses computadores. Então, clicamos com o botão direito do mouse na máquina da manufatura e uma janela abrirá. Nela, vamos na aba "Desktop" e, depois, na opção "IP Configuration".

Observe que ele preencheu automaticamente a máscara de sub-rede. Vamos, então, arbitrariamente definir um endereço de IP. Digitaremos "193.168.3.1" e teclamos "Enter".

Agora, repetimos o mesmo processo para "Acabamento", definindo o IP como "193.168.3.2". Perceba que estamos mudando apenas o último octeto. Vamos entender melhor por que estamos fazendo isso mais adiante.

Por fim, fazemos o mesmo processo para o computador de embalagem, definindo o IP como "193.168.3.3". Pronto! Todas as nossas máquinas já possuem um endereço de IP.

Vamos testar o funcionamento da nossa rede utilizando novamente o comando Ping para enviar um pacote de dados de um computador para o outro. Vamos enviar um pacote de dados do computador da embalagem para o computador manufatura. Assim, vamos entender, na prática, como funciona o switch.

Antes, vamos mudar aqui o nosso modo de funcionamento do Real-Time para Simulation. Observe que a simulação continua pausada, quando clicarmos na opção de Play, no menu acima dos dispositivos, a simulação será iniciada. À direita, temos um painel de simulação onde podemos verificar todos os protocolos que estão rodando em segundo plano com o funcionamento da nossa rede. Então, vamos dar o ping do computador da embalagem para o computador da manufatura.

Para isso, clicamos com o botão direito do mouse sobre o computador da embalagem e vamos em "Command Prompt", e digitamos ping para o computador que está na nossa rede, 193.168.3.1 - esse foi o endereço de IP que atribuímos manualmente para esse computador.

ping 193.168.3.1
COPIAR CÓDIGO
Vamos pressionar Enter, minimizar o Prompt de Comando e dar o Play.

Observem o seguinte aspecto: no primeiro momento, o switch recebeu o pacote de dados, encaminhou para o computador da manufatura e do acabamento. Mas nós sabemos que esse pacote não era destinado para o acabamento. Na sequência, o computador da manufatura respondeu, e o switch encaminhou apenas para o computador da embalagem. Quando o segundo pacote do ping foi enviado pelo computador da embalagem, o switch encaminhou apenas para o computador da manufatura. A partir de agora, ele só vai encaminhar o pacote para o computador da manufatura.

Aqui nós já temos um primeiro dado do comportamento do switch: ele utiliza o protocolo ARP para entender quais dispositivos e quais endereços estão plugados em cada uma das suas portas. Nessa primeira experiência de conexão, ele verifica quem é quem na rede, por isso que ele encaminha a mensagem para os dois computadores que estão plugados nas suas portas. A partir desse primeiro contato, dessa primeira interação, ele armazena na memória interna para qual endereço MAC (que é o endereço físico da placa de rede de cada dispositivo) está associado o endereço de IP.

Cabe ressaltar a diferença entre o endereço MAC e o endereço IP. O endereço MAC é como se fosse uma espécie de RG desse dispositivo, que é utilizado apenas nessa rede interna. Quando esse dispositivo precisa encaminhar um pacote de dados para um computador que está externo a essa rede, ele precisa de um documento, ou seja, de uma identificação universalmente aceita que é o endereço IP.

Neste momento da execução, vemos na nossa tela o último pacote do comando PING ser enviado para o computador da manufatura que está respondendo. Novamente observamos que o switch vai encaminhar essa resposta apenas para o computador da embalagem.

Se olharmos nosso Simulation Panel, vamos observar os protocolos que estavam funcionando durante o comando PING. Nós sabemos que o protocolo ICMP é o protocolo padrão do comando PING. Mas temos, também, o protocolo ARP, que mostra uma série de endereços com os quais não estamos muito acostumados. Esses são os endereços MAC, utilizados na rede interna para localização dos dispositivos, com os quais nós estamos nos comunicando e transferindo dados e outros tipos de arquivos.

Agora que sabemos que cada dispositivo possui um endereço MAC atribuído pelo fabricante da placa de rede que inserimos, seja num desktop ou laptop, podemos conferir se o nosso computador tem acesso a esse endereço MAC. Para isso, vamos clicar no menu "Iniciar" e buscar o Prompt de Comando para abri-lo. Nele, digitamos o comando ipconfig /all.

ipconfig /all
COPIAR CÓDIGO
Ao executar, observe que aparece uma série de informações. Para identificarmos o endereço MAC da nossa placa de rede, que está no desktop utilizado para fazer essa aula, por exemplo, vemos a opção "Endereço Físico". Esse é o endereço MAC da nossa placa e é a identificação que é utilizada na rede interna na qual ela está conectada.

Agora, ao conectar-se externamente (na internet), é necessário outro endereço para que outros dispositivos consigam se comunicar, ou seja, consigam enxergar o dispositivo no qual estamos conectados. Esse endereço, como já sabemos, é o endereço IP, atribuído pelo servidor DHCP. Mais adiante, estudaremos o que é esse servidor DHCP.

Já sabemos que o comando ipconfig /all nos retorna uma série de informações e que, para localizar o endereço MAC, que é o endereço da nossa placa de rede, vemos a opção "Endereço Físico".

Já o endereço usado para se conectar à internet, ou seja, aquele em que as pessoas podem enviar informações e a partir do qual também podemos enviar informações para outros dispositivos, é o endereço IPv4. Observe que é um endereço IP com o qual já estamos um pouco mais familiarizados e inclusive inserimos nos computadores da nossa simulação.

Vimos como funciona o switch e o hub. O switch possui uma memória interna para armazenar o mapeamento dos endereços MAC dos diferentes dispositivos que estão plugados nas portas e os seus respectivos endereços IP.

Já o hub não possui esse tipo de memória interna. Portanto, sempre que recebe um pacote de dados, encaminha para todos os dispositivos conectados em suas portas, de modo que esse pacote chegue ao dispositivo de destino.

Outra informação a ser considerada é o congestionamento da rede quando usamos o hub. Porém, vamos analisar sob a ótica da segurança. Imagine que você está compartilhando dados sensíveis em uma rede e não quer que outras pessoas visualizem, por exemplo, quais sites está acessando ou que tipo de informação está transmitindo. Se estiver usando um dispositivo de rede como o hub, algumas pessoas podem utilizar um software de monitoramento de tráfego na rede para identificar os pacotes que estão chegando na máquina delas, monitorando as informações que você está recebendo, os sites que está acessando e, se em alguns desses sites você inseriu alguma informação como senha não criptografada, isso também fica visível para outros usuários que estão na rede, já que o hub envia todos os pacotes para todas as máquinas.

No caso do switch, isso não ocorre porque ele identifica, utilizando o protocolo ARP, quais dispositivos estão conectados em suas portas e quais são os respectivos endereços. Então armazena isso na memória interna e, a partir daí, encaminha os pacotes de dados apenas para os dispositivos aos quais esses pacotes se destinam.

Mas usar o switch não impede todos os riscos de ataques. É possível que algumas pessoas queiram atacar um switch de forma a lotar a memória de endereços MAC desse switch. Uma forma de evitar esse tipo de ataque é limitando dois ou três endereços MAC por cada porta, assim não lota a memória.

Inclusive, após esgotar a memória interna do switch, ele passa a funcionar como hub. Isso significa que ele encaminha todos os pacotes que ele recebe para todos os dispositivos conectados nas portas, pois não é mais capaz de identificar quais dispositivos estão conectados. Então, para assegurar que o dispositivo recebeu o pacote destinado a ele, ele envia para todos os que estão conectados nas portas. Por isso, é importante limitar o número de endereços MAC que podem ser armazenados para cada uma das portas do switch.

Conforme mencionado anteriormente, podemos utilizar o monitoramento de tráfego para analisar pacotes que estão trafegando na nossa rede, inclusive pacotes que não deveriam estar sendo destinados ao nosso computador, se estivermos plugados em um dispositivo de rede como um hub.

No entanto, o monitoramento de tráfego é muito útil para que possamos analisar o que está acontecendo na nossa rede, e é o que veremos na sequência.

@@02
Hubs ou switches

Hub e switch são dispositivos utilizados para interligar computadores e formar uma rede local Ambos desempenham a função de concentrar e distribuir o tráfego de rede e experimentamos utilizar ambos. Mas existem diferenças significativas entre eles em termos de eficiência e capacidade de gerenciamento.
Qual a principal diferença a se destacar entre os dispositivos?

O hub não consegue memorizar onde um equipamento está localizado, o Switch sim.
 
Os hubs não conseguem aprender o endereço MAC dos equipamentos de uma rede, já os Switches possuem essa função.
Alternativa correta
O hub possui capacidade de conexão sem fio.
 
Alternativa correta
O switch possui memória RAM.

@@03
Vulnerabilidade dos switches

Você precisa montar uma rede com switch em um laboratório de informática, quando é indagado sobre as possíveis vulnerabilidades de segurança que esse switch pode apresentar. Então, você indica que há uma forma de ataque usada para conseguir informações passadas no Switch destinadas a outro usuário.
Selecione a alternativa que corresponde a este ataque.

Inserir vários endereços MAC falsos para “encher” a memória do Switch e fazer com que ele atue como um Hub.
 
Exatamente, esse é um dos principais métodos usados por usuários maliciosos. Ao inserir vários endereços MAC falsos para preencher a memória do Switch, o dispositivo não vai conseguir definir onde cada um realmente está, passando a atuar como um Hub.
Alternativa correta
Resetar a memória interna do switch.
 
Alternativa correta
Resetar a memória não-volátil, pois assim podemos facilmente configurá-lo para redirecionar a informação para nós.

@@04
Prevenção de ataques

Após explicar a principal vulnerabilidade de segurança dos switches ao coordenador do laboratório de informática, você começa a refletir a respeito de possíveis estratégias de configuração do dispositivo que possam evitar tais ataques.
Neste contexto, qual modo de prevenção de ataques você poderia sugerir?


Alternativa correta
Construir camadas de segurança na rede.
 
Alternativa correta
Configurar a opção de segurança na porta, para que fique limitada a receber uma quantidade máxima de endereços MAC.
 
Podemos configurar a porta do Switch para aceitar um número máximo de endereços MAC. Ao ultrapassar esse limite, a porta é desligada e o ataque não ocorre com êxito.
Alternativa correta
Inserir um dispositivo de hardware adicional que seja capaz de criar barreiras de segurança na rede.

@@05
Monitorando o tráfego na rede

Falamos um pouco sobre monitoramento do tráfego de uma rede. Como será que isso é possível? Vamos analisar na prática como usar uma ferramenta aberta que nos permite fazer essa tarefa.
No Google, vamos digitar Wireshark que é um monitorador de tráfego de rede ethernet. Vamos clicar no primeiro resultado da pesquisa que é o site do wireshark.org.

Ao descer a página, vamos encontrar a opção de fazer o download do Wireshark. Podemos baixar o instalador conforme as especificações da nossa máquina. No nosso caso, vamos baixar o pacote do Windows de 64 bits. Depois é só instalar e vai estar pronto para uso na nossa máquina.

Monitorar o tráfego de redes
Como já temos o Wireshark instalado no computador, vamos abrir o programa para começar a nossa atividade de monitoramento do tráfego de redes.

A interface inicial consiste em uma barra de menu, barra de ferramentas, barra de filtros e a página de boas-vindas.
O que vamos fazer nessa página? Selecionar uma interface de rede dentre as diferentes interfaces listadas.

Quando utilizamos o comando ipconfig no terminal do computador, percebemos que haviam várias interfaces. A maior parte delas estava com mídia desconectada. No nosso caso, só estávamos utilizando uma interface, a Ethernet.

Por isso, vamos selecionar essa interface Ethernet onde temos algum tráfego de dados, protocolos sendo executados, pois estamos utilizando de conexão à rede. Damos dois cliques nessa interface e agora vamos ver uma sequência de pacotes de protocolos de comunicação sendo executados.

Nessa janela, temos três painéis. No topo, o painel de lista de pacotes. Abaixo, lado a lado, o painel de detalhes do pacote e o painel de bytes do pacote. Na parte inferior, temos uma barra de status.
Interface do Wireshark como descrita anteriormente.

Esses protocolos estão de fato acontecendo, é o que está acontecendo por trás da nossa rede. Tem protocolo UDP, TCP e outros que ainda nem conhecemos ainda ao longo do curso. O TCP já aprendemos que atua na camada de aplicação.

Se selecionamos aleatoriamente um desses protocolos, vamos observar uma série de informações no painel de detalhes. Essas informações são relativas às diferentes camadas que constituem a nossa rede.

Por exemplo, temos a opção do Internet Protocol Version 4, que é a camada de rede. Isto é, temos o protocolo IP versão 4 atuando.

Temos outra que é o protocolo UDP (User Datagram Protocol), que está atuando na camada de transporte. Também temos um pacote de dados (data) de 25 bytes que estava trafegando e passando através dessas camadas.

Dessa forma, com o monitorador de tráfego de redes, Wireshark, conseguimos visualizar os protocolos que estão rolando por trás da rede, o pacote de dados que estão mandando e por onde esse pacote passa, ou seja, quais protocolos utilizam em cada uma das camadas.

Não conseguimos identificar o que tem dentro desse pacote, mas observam o tráfego dele na rede e os protocolos que são usados para isso.

Além disso, também é possível observar os cabeçalhos que cada uma dessas camadas adicionam a esse pacote. Como explicamos anteriormente, cada camada adiciona um cabeçalho que é relevante para ela.

Assim, quando esse pacote chegar no endereço de destino, as camadas vão atuar no sentido de retirar esses cabeçalhos de tal forma que a informação fique disponível no aplicativo de quem estiver recebendo uma mensagem, por exemplo. É isso que observamos por trás dos panos (internamente) com o Wireshark.

Teste de monitoramento
Vamos fazer um teste?

Vamos acessar o navegador e abrir aleatoriamente uma página na internet para verificar se conseguimos identificar o uso do protocolo HTTP, que é presente na camada de aplicação.

No navegador, vamos digitar algum website. Por exemplo, vamos acessar o site da Alura e clicar na opção da "Escola de programação" onde temos várias informações.

Também podemos visitar outros sites. Vamos digitar no Google "programação C", por exemplo. São retornados vários conteúdos de programação C de diferentes universidades, blogs e livros.

Por fim, em outra aba, vamos navegar em mais uma página como o Google. Realizamos uma pesquisa pela "Wikipédia" e encontramos vários resultados.

Desse modo, fizemos algumas pesquisas e usamos bastante o protocolo HTTP no navegador. Agora, vamos verificar se elas aparecem no monitorador de tráfego.

A ferramenta nos possibilita filtrar alguns pacotes por meio dos protocolos que queremos observar melhor.

Agora, conseguimos dar um zoom ao clicar no ícone de lupa da barra de ferramentas, o que nos permite visualizar melhor o que está acontecendo na tela. Dá inclusive pra alterar o tamanho dos painéis.

Antes de selecionar pacotes e observarar o que está ocorrendo, podemos digitar na barra de filtros "HTTP" que é o protocolo que queremos analisar. Selecionamos HTTP e pressionamos "Enter".

O processo de filtro pode ser um pouco lento. Após fazer o filtro, obtivemos alguns resultados. Por exemplo, vamos analisar o primeiro resultado no painel de lista de pacotes.

Com isso, surge no painel de detalhes:

Frame 248101;
Ethernet II;
Internet Protocol Version;
Transmission Control Protocol;
Hypertext Transfer Protocol.
Observe que temos o uso do protocolo HTTP (Hypertext Transfer Protocol) na nossa camada de aplicação. Na sequência, temos o uso do protocolo TCP (Transmission Control Protocol) na camada de transporte. Ou seja, prepara um pacote para seguir para a camada de rede, representada pelo protocolo IP (Internet Protocol Version).

Mais à frente, temos o protocolo Ethernet. Nesse ponto, o pacote já está se encaminhando para a transmissão, através da rede física.

O que fizemos?
Inicialmente, clicamos em algum pacote que queríamos analisar com protocolo HTTP na parte superior da ferramenta que é o painel de lista de pacotes. Na parte inferior esquerda da ferramenta, onde temos o painel de detalhes de pacotes, vamos observar os protocolos que estão rodando nesse pacote selecionado.

Nele, temos o HyperText Transfer Protocol (HTTP) na camada de aplicação. Também temos o Transmission Control Protocol (TCP). Quando selecionamos esse protocolo, abrem informações sobre o protocolo TCP rodando na camada de transporte e preparando o nosso pacote para se encaminhar à camada de rede.

É o que temos na sequência, com o Internet Protocol (IP) versão 4. Em seguida, o pacote vai para a camada Ethernet, onde se prepara para transmissão por meios físicos até atingir o endereço de destino.

Agora que já sabemos como monitorar o tráfego em uma rede, que tal aprimorarmos o projeto que estamos construindo para a fábrica? Vamos pensar em inserir outro dispositivo de rede? É isso que faremos na sequência.

https://www.wireshark.org/

@@06
Wireshark

Uma amiga estava em dúvida sobre qual ferramenta utilizar para monitorar o tráfego de rede em seu computador. Nesse momento, você lembra do Wireshark e o recomenda.
Qual principal função do Wireshark você citaria para justificar a utilização dele neste caso?

Analisar protocolos utilizados na troca de pacotes pelo computador, facilitando a solução de problemas na rede.
 
O Wireshark tem como principal utilização analisar protocolos que trafegam na rede com o intuito de verificar problemas que possam existir.
Alternativa correta
Analisar o tráfego de rede, fornecendo uma visão detalhada do que está ocorrendo nas diferentes camadas.
 
O Wireshark fornece uma visão detalhada do tráfego baseada nos protocolos que estão atuando na rede.
Alternativa correta
Analisar usuários que estão conectados em sua rede.

@@07
Protocolo TCP

Ao analisar o tráfego em sua rede usando o Wireshark, você observa o uso frequente do protocolo TCP. O Transmission Control Protocol (TCP) é um dos principais protocolos da Internet e fornece um serviço confiável, garantindo a integridade e a ordem dos pacotes.
Qual seria a principal função deste protocolo?


Transportar informações.
 
O protocolo TCP encontra-se acima da camada onde o IP está localizado e ele é responsável por realizar o transporte das informações. Além disso, a camada de transporte possui também outro protocolo bastante conhecido, o UDP.
Alternativa correta
Criptografar informações.
 
Alternativa correta
Endereçamento de pacotes.

@@08
Máscara de rede

Falamos sobre construção de redes e utilizamos o switch. Vamos voltar ao caso que estamos analisando para a construção da nossa rede. Temos uma empresa do setor de manufatura, uma empresa têxtil. Temos três setores e cada setor tem uma máquina dedicada.
Porém, vale notar que em muitas empresas temos diferentes setores que possuem diferentes demandas de conexão e velocidade de rede. Nesses casos, é muito prático a configuração de diferentes redes.

Para simplificar, exemplificamos com apenas um PC no setor de manufatura, mas poderíamos ter alguns dispositivos trocando informação entre si e, eventualmente, trocando informações com máquinas em outros setores da empresa.

Por isso, seria mais prudente que tivéssemos uma rede dedicada à manufatura, outra ao acabamento e até outra para o setor da embalagem. Assim como outros setores, como marketing ou vendas.

Dessa forma, você teria a troca eventual de algumas informações entre esses setores, mas cada setor sendo respeitado de acordo com a sua demanda e requisitos de acesso à rede. Alguns com acesso à rede externa, outros apenas à rede interna, como no exemplo da linha de produção.

Estávamos utilizando um switch nessa rede. Havíamos começado com um equipamento mais simples, o hub. Mas, com o switch notamos que tínhamos mais segurança, os pacotes eram caminhados de forma mais eficiente, ele armazenava os endereços dos dispositivos com os quais estava conectado.

No entanto, será que o switch permite configurar diferentes redes e conectar essas redes em suas portas? Podemos testar agora e vamos aprender como configurar uma rede diferente da outra.

Máscara de sub-rede
Voltamos ao Cisco Packet Tracer. Lembre-se que quando estávamos fazendo o endereçamento, ou seja, configurando o endereço de IP de cada uma das máquinas que conectamos ao switch, clicávamos com o botão direito em cima do PC e abria uma janela. Por exemplo, clicamos no "PC-PT Manufatura".

Nela, selecionávamos a aba "Desktop" e a opção "IP Configuration", onde digitávamos um endereço de IP de forma arbitrária. Afinal, ainda não aprendemos como nomear o endereço de IP, ou seja, as diferentes classes de IP.

Com isso, o endereço em "Subnet Mask" (máscara de sub-rede) era preenchido de forma automática.

IP Configuration: Static
IPv4 Address: 193.168.3.1
Subnet Mask: 255.255.255.0
O que é a máscara de sub-rede? Por que foi automaticamente preenchida? Isso tem relação com a classe de IP que usamos.

Mas, no que isso se reflete na prática? No tópico de construção de diferentes redes?

Esses endereços que são formados por quatro octetos. Assim, temos 32 bits de informação em cada um desses endereços.
O que a máscara de sub-rede faz é dividir o endereço de IP em dois grupos.

Os grupos de octetos do endereço de IP que estão ordenados com esses octetos na máscara de sub-rede, 255, são um endereço que identifica a rede na qual estamos conectados.

Lembra que quando estávamos configurando cada um desses PCs, estávamos mudando apenas o último octeto. Isso tem exatamente a ver com essa máscara de sub-rede.

É porque apenas esse último octeto era variável. Tínhamos que manter esses três primeiros octetos 193.168.3 para que os três computadores estivessem conectados na mesma rede.

Se modificamos esse primeiro octeto para o PC da manufatura, para o PC do acabamento e também para o PC da embalagem, o que vai acontecer? Eles estarão em três redes diferentes.

A máscara de subrede tem como função identificar qual parte do endereço de IP se refere ao endereço da rede e qual parte podemos usar para modificar e atribuir um endereço diferente dentro dessa rede para cada dispositivo que queremos nos conectar.
Configuração de diferentes redes
Vamos modificar o endereço de rede de cada um desses computadores. Em seguida, vamos testar se o switch nos permite conectar essas diferentes redes.

Só vamos modificar o primeiro octeto de cada um. No "PC-PT Manufatura", vamos manter com esse padrão de IP 193.168.3.1.

IPv4 Address: 193.168.3.1
Clicamos com o botão direito no "PC-PT Acabamento", selecionamos a aba "Desktop" e a opção "IP Configuration". Continuamos com o IP estático. Ao invés de 193, vamos colocar 192. Observe que apertamos "Enter", mas nada modificou.

IPv4 Address: 192.168.3.1
Por fim, fazemos o mesmo para "PC-PT Embalagem". Modificamos para o primeiro octeto para 191.

IPv4 Address: 191.168.3.1
As interligações dos PCs continuam verdes, mas agora temos computadores em redes diferentes. A máscara de sub-rede se mantém, porque estamos usando a mesma classe.

Os três primeiros octetos se referem a nova rede que estamos usando para aquele setor. Enquanto o último permite identificar o PC de forma específica.
Agora que já fizemos a configuração das três diferentes redes, uma para cada setor da nossa linha de produção. Vamos testar a conectividade do computador da manufatura com o computador da embalagem, utilizando o novo endereço de IP que atribuímos ao computador da embalagem.

Vamos clicar com o botão direito em "PC-PT Manufatura", aba "Desktop" e opção "Command Prompt" (Prompt de comando).

Digitamos aquele comando que já conhecemos:

ping 192.168.3.1
COPIAR CÓDIGO
No vídeo, o instrutor se equivoca e pinga o endereço 192.168.3.3, quando, na verdade deveria ter pingado o 192.168.3.1, conforme alterado nesta transcrição. O ping não ia dar certo de qualquer forma, pois estávamos usando um switch, tentando conectar PCs em redes diferentes, problema motivador para passarmos a utilizar o roteador.
Vamos digitar o "Enter" e aguardar para verificar se o pacote vai ser enviado e vai ser recebido.

Request timed out.
Request timed out.
Request timed out.
Request timed out.
Ping statistics for 192.168.3.3:

Packets: Sent = 4, Received = 0, Lost = 4 (100% loss)
Os quatro pacotes deram Request timed out, ou seja, não foram entregues. A estatística do nosso ping foi: quatro pacotes foram enviados, quatro pacotes foram perdidos.

Isso significa que, não conseguimos conectar duas ou mais redes diferentes utilizando um switch. Vamos precisar de outro dispositivo: o roteador.

Agora você talvez se pergunte: mas por que usamos o switch?

O switch nos permite conectar múltiplos computadores e máquinas em um mesmo ambiente.
Por exemplo, seja no escritório, laboratório de uma escola ou em outros setores que haja demanda para conectar diferentes dispositivos em uma única rede.

Apesar do símbolo gráfico do switch no simulador, como é o switch de fato no mundo real? Podemos fechar aqui o prompt de comando e clicar em cima do switch com o botão direito para abrir uma janela com a aparência do switch.

Representação gráfica de um switch de rede. Hardware retangular com 24 portas de conexão enfileiradas lado a lado. Abaixo, 1 porta de console e 1 conexão do cabo de alimentação.

Observe que temos várias portas nas quais podemos conectar múltiplos dispositivos. Então, chega um endereço de rede, criamos uma rede única e conectamos esses múltiplos dispositivos nessa rede.

Roteador
Já aprendemos que com o switch não vamos conseguir resolver esse problema de conectar redes diferentes em um mesmo ambiente. Vamos ter que usar os roteadores.

Podemos começar já selecionando o roteador. Para isso, clicamos no ícone de "Router" no canto inferior esquerdo na caixa de componentes de rede. Selecionamos especificamente o roteador "1841" e o arrastamos até a tela da área de trabalho.

Observe que todos esses equipamentos que utilizamos são de especificação da Cisco. A Cisco é a empresa que mantém esse software para fins educacionais. No entanto, temos outras fabricantes de dispositivos de rede que podemos eventualmente utilizar em nossos projetos.

Na sequência, vamos aprender como inserir e configurar esse roteador na nossa rede.

https://cdn1.gnarususercontent.com.br/1/1319058/95c69824-a8fe-479e-8ab6-b859998aaa14.png

@@09
Função da máscara de rede

Você comentou com um amigo que estava estudando redes, então ele perguntou sobre alguns termos diferentes que costuma ouvir quando alguém está falando sobre o tema. Um destes termos é o de máscara.
Qual explicação você utilizaria para indicar a função da máscara de rede de modo simples?

Estabelecer uma conexão com a internet, informando aos demais dispositivos que seu computador está conectado em uma rede.
 
Alternativa correta
Como o próprio nome sugere, criar uma máscara para esconder nosso endereço IP na rede.
 
Alternativa correta
Dividir o endereço IP em dois grupos (rede e máquina) para que seja possível definir quando outro dispositivo estará na mesma rede que a dele.
 
Exatamente! A máscara de rede é usada como forma de comparação para determinar se dois equipamentos estão na mesma rede. Para isso ela vai dividir o endereço IP em dois grupos, de rede e hosts (máquinas).

@@10
Para saber mais: diferenças entre hubs e switches

Hubs e switches são ambos equipamentos de rede utilizados para interligar computadores e formar uma rede local (LAN - Local Area Network). Eles desempenham a função de concentrar e distribuir o tráfego de rede, mas há diferenças entre eles.
Comparando os dois, podemos dizer que os switches são mais eficientes e oferecem melhor desempenho em comparação com os hubs. Os hubs são mais adequados para redes pequenas ou para fins de teste, enquanto os switches são mais indicados para redes maiores, onde a velocidade e a capacidade de gerenciamento são importantes.

Caso queira entender mais sobre o assunto, , acesse o artigo Diferenças Entre Hubs e Switches!

https://www.alura.com.br/artigos/diferencas-entre-hubs-e-switches?_gl=1*1d7hj7y*_ga*MTgwMzIzMjk2Ni4xNjg4ODE5OTcz*_ga_59FP0KYKSM*MTY5MDczOTA3OC40MC4xLjE2OTA3NDAxMDkuMC4wLjA.*_fplc*d2s3ZFVrT01PcnF5JTJCRmZPZ1NDUE02YzYwWHVOQ3BWUkFZdFUwZ0pLOXAzS05EMXBtcU9GWTBxVHZZJTJGbDIlMkJGRGxvNlBBeWREYiUyRjJ5RWV0cmhDQms3Y00xUnFlNWZWQUFXVUx5bEtyRmZmM24lMkZzTUVvM1NxS1ZFbTh3WlhqUSUzRCUzRA..

@@11
Faça como eu fiz: analise o tráfego em sua rede!

Faça o download e instalação do Wireshark em seu computador. Para baixar, acesse o site do Wireshark e selecione a versão compatível com a sua máquina;
Abra o Wireshark e como fizemos no vídeo, selecione uma interface de rede;
Para iniciar a captura de pacotes, você precisa clicar na opção “Iniciar captura” no canto esquerdo do menu superior do Wireshark;
Agora, realize alguma operação de rede, tal como acessar um site no navegador do seu computador;
Pare a captura de pacotes, clicando na opção “Parar captura” no menu superior do Wireshark;
Crie algum filtro para facilitar o seu processo de análise, tal como um protocolo específico (HTTP, por exemplo). O filtro também pode ser feito durante a captura de pacotes;
Analise os pacotes coletados. Lembrando que a inspeção também pode ser realizada durante a captura.

https://www.wireshark.org/

Opinião do instrutor

Você deve ter obtido um resultado bem similar ao da imagem abaixo:
alt text: Tela do Wireshark com destaque para primeira linha de resultado da captura utilizando o protocolo HTTP como filtro. A tela de resultados é dividida em três partes. A parte superior indica os resultados da busca. A parte intermediária descreve os protocolos envolvidos na operação selecionada (requisição HTTP). A parte inferior detalha os protocolos selecionados na tela intermediária.

Observe que podemos analisar detalhadamente os diferentes protocolos utilizados em uma operação de rede. Para uma visão mais detalhada, basta clicarmos em cada protocolo listado e obtermos mais informações.

https://caelum-online-public.s3.amazonaws.com/3092-redes-conceitos-iniciais-criacao-intranet/image2.png

@@12
O que aprendemos?

Nessa aula, você aprendeu como:
Interligar computadores em rede de modo mais seguro utilizando switches;
Monitorar tráfegos de rede, analisando os diferentes protocolos usados nas operações de rede;
Observar a atuação dos protocolos nas diferentes camadas de rede;
Verificar quais dispositivos estão em uma mesma rede, analisando seus endereços IP e suas respectivas máscaras de rede.

#### 01/07/2023

@04-Roteadores e endereçamento IP

@@01
Construindo redes com roteadores

Aprendemos que podemos configurar diferentes redes para atender às demandas dos diferentes setores da linha de produção. Para isso, teremos que utilizar outro dispositivo de rede. Neste caso, teremos que usar o roteador.
Surge a pergunta: será que basta colocar o roteador, fazer as conexões com os computadores que já temos na linha de produção e tudo vai funcionar? Podemos testar.

Conectar PC e roteador
Vamos abrir o projeto no Cisco Packet Tracer. Temos os três PCs, um de cada setor da linha de produção. Já havíamos inserido um roteador, selecionamos o 1841 e vamos ter que substituir o switch pelo roteador.

Antes, o que teremos que fazer? Vamos ter que excluir as conexões existentes entre cada PC e o switch. Para isso, clicamos na tecla "Delete" para aparecer uma ferramenta de seleção no cursor do mouse. Assim, podemos clicar nas conexões que queremos deletar. Ao final desse processo, vamos clicar na tecla "ESC", para desativar essa ferramenta de exclusão de conexões e equipamentos.

Vamos posicionar o roteador no topo da estrutura e afastar o switch.

Qual conexão que vamos utilizar para conectar o PC no roteador?

Temos duas questões para refletir nesse processo de seleção. A primeira, eles são equipamentos iguais?

Se são equipamentos iguais, possuem a mesma placa de rede. Já aprendemos que teríamos que usar, via de regra, um cabo de conexão cruzada. Mas, não são iguais.

Ainda assim tem uma segunda reflexão que temos que fazer. Será que essa conexão permite que aproveitemos o máximo que esse dispositivo tem para nos oferecer em termos de conexão?

No caso do roteador, ele permite conectar diferentes redes. Enquanto, um PC permite se conectar a múltiplos dispositivos. Neste caso, teremos que usar a conexão de cabo cruzado.
Na caixa de componentes de rede, selecionamos "Connections" (conexões) e especificamos o "Copper Cross-Over" que é o cabo cruzado.

Em seguida, clicamos o PC de manufatura, e escolhemos a porta "FastEthernet 0" para ser utilizada. Depois, clicamos no roteador para conectá-los e selecionamos a porta "FastEthernet 0/0".

Na sequência, vamos fazer o mesmo processo para o PC do acabamento. Pegamos outro cabo de conexão cruzado e selecionamos a porta "FastEthernet 0" no PC e "FastEthernet 0/1" no roteador.

Por fim, conectamos o pc de embalagem na porta "FastEthernet 0" com o roteador. Ops! Não temos mais portas para conectar nesse roteador.

O que vamos fazer? Vamos apertar a tecla "ESC" para cancelar essa conexão.

Ao clicar com o botão direito em cima do roteador, se abre uma janela. Na aba "Physical", podemos visualizar uma representação de como é um roteador fisicamente. Claro, todos os dispositivos de rede nessa ferramenta são da Cisco, mas, na prática, podemos usar de diferentes fabricantes.

Representação gráfico de um roteador. Hardware retangular com dois slots, 4 portas, 1 chave de força e 1 conexão do cabo de alimentação.

O que teremos que fazer? Temos alguns slots no equipamento onde podemos adicionar módulos, de tal forma que ganhemos novas portas de conexão. Por exemplo, como a porta Ethernet que precisamos para conectar o PC da embalagem.

Vamos navegar pelo menu lateral esquerdo da aba "Physical" e verificar quais portas que cada módulo nos permite adicionar. Por exemplo, o módulo "WIC-1AM" tem dois RJ-11 conectores. Não é o que queremos.

Se clicamos no módulo "WIC-1ENET", podemos ler na descrição que temos aqui uma porta Ethernet.

Primeiro, é necessário certificar se a chave de força do roteador está desligada.
Porque ao fazer a conexão de uma nova porta Ethernet, é importante que o equipamento esteja desligado. Quando ligado, uma luz verde aparece abaixo da chave de força, basta clicar na desligá-la.

Após desligada, é possível adicionar o módulo desejado, arrastando e soltando no slot do equipamento. Com isso, temos uma nova porta de conexão Ethernet.

Depois de ligar novamente o dispositivo, é possível fazer a conexão com o cabo de conexão cruzada entre o PC da embalagem na porta "FastEthernet 0" e o roteador na porta "Ethernet 0/1/0".

Simulação de conexão entre diferentes PCs em diferentes redes. A estrutura é organizada em formato piramidal, com um roteador no topo, interligado a três PCs na base por meio de cabos cruzados. Da esquerda para a direita, os PCs estão identificados como Manufatura, Acabamento e Embalagem. A conexão entre os dispositivos está vermelha.

No entanto, todas as conexões estão com indicação vermelha, o que significa que é necessário fazer um passo extra de configuração - diferente do que acontece com switches e hubs, cujas conexões ficam verdes automaticamente.

Conexão com cabo console
Na prática, se tivéssemos que configurar um roteador em uma linha de produção para dar acesso a PCs de diferentes setores, seria preciso usar um cabo chamado cabo console. Iríamos plugar o PC no roteador usando esse cabo console.

No navegador, vamos procurar uma imagem de cabo console.

Cabo console na cor azul-clara com conector RJ45 em uma ponta e conector DB9 de entrada na outra. O conector DB9 também é conhecido como conexão serial.

Esse cabo tem uma conexão serial (DB9) em uma extremidade e uma conexão do conector RJ45 na outra. A conexão serial é conectada na porta serial de um computador, enquanto o conector RJ45 é plugado no roteador. Caso o computador não tenha uma porta serial, é possível utilizar um conversor USB serial.

Essa comunicação serial transmite 1bit por vez.
Não basta apenas conectar o cabo console no PC e no roteador. Além disso, é necessário baixar um software de emulação para configuração de dispositivos. Também muito utilizado para configuração remota de servidores, chamado PuTTY.

Tem uma interface simples, onde você pode adicionar um endereço IP do dispositivo que você quer configurar. Usando uma conexão SSH, você pode configurá-la a distância.

Captura de tela de janela de configuração do software Putty. À esquerda, possui um painel com uma lista de categorias e a direita as opções específicas de cada categoria.

Esse software é muito utilizado tanto por profissionais de TI quanto de redes na configuração de dispositivos.

Vamos aprender como seria esse processo na prática usando nosso simulador?

No Cisco Packet Tracer, é possível realizar esse processo adicionando um novo PC ao lado do roteador. Dentre as conexões, vamos escolher o "Console" que é o cabo console.

Nesse novo PC chamado "PC-PT PC1" vamos conectar esse cabo na saída "RS 232" (conector da porta serial) e na porta "Console" do roteador.

Ao clicar com o botão direito para abrir o "PC-PT PC1", acessamos a aba "Desktop" e a opção "Terminal", onde temos a configuração do terminal. Vamos manter no deafult (padrão) ao clicar no botão "OK".

Agora, é possível observar a interface de configuração do roteador. Mas, podemos fechar essa janela.

Se clicamos com o botão direito no roteador na área de trabalho e acessamos a aba "CLI", vamos encontrar a mesma a interface de configuração.

O que isso significa? No caso do simulador, é possível usar a interface adaptada clicando no roteador. Mas, na prática, é necessário fazer toda a conexão usando o cabo console entre o computador e o roteador.

Portanto, ao contrário do switch, é preciso usar um computador para configurar um roteador de modo que as conexões sejam realizadas com sucesso.

Modo de Configuração
Já que não vamos usar o PC no caso do simulador, podemos excluí-lo. Para isso, apertamos a tecla "Delete", clicamos no "PC-PT PC1" e automaticamente vamos excluir a conexão com o cabo console. Lembre-se de apertar "ESC" para desativar a ferramenta de exclusão.

Se passamos o cursor do mouse sobre o roteador, podemos observar a lista das portas. Todas as portas estão com o estado de Down, ou seja, não estão ativas.

Device Name: Router2
Device Model: 1841
Hostname: Router
Port	Link	VLAN	IP Address	IPv6 Address	MAC Address
FastEthernet0/0	Down	--	not set	not set	0001.439C.8801
FastEthernet0/1	Down	--	not set	not set	0001.439c.8802
Ethernet0/1/0	Down	--	not set	not set	000B.BE4B.53E6
Vlan1	Down	1	not set	not set	0006.2A22.C285
Physical Location: Intercity> Home City > Corporate office > Main Wiring Closet > Rack > Router2

Da mesma forma, há um campo para "IP address" (endereço IP), e não há nenhum endereço IP definido para nenhuma das portas.

O que vamos ter que fazer? Vamos ter que mudar o status de cada uma das portas que estamos utilizando: "FastEthernet0/0", "FastEthernet 0/1" e "Ethernet 0/1/0". Em seguida, vamos atribuir um endereço de IP para cada uma dessas portas.

Para isso, vamos configurar o roteador usando a aba "CLI", como havíamos mencionado.

Caso necessário, você pode mudar a fonte do terminal CLI. Na barra de menu superior, selecione "Options > Preferences" (ou "Ctrl + R"). Na nova janela, clique na aba "Font" e aumentar para tamanho 16 a fonte da opção CLI. Na sequência, clique em "Apply".
Observe que aparece uma pergunta em inglês: "Você gostaria de entrar na configuração de modo diálogo?". Esse é um modo de configuração bem detalhado, passo a passo.

No nosso caso, vamos fazer de forma mais simples e rápida. Por isso, vamos digitar a opção "no" e apertar "Enter".

Would you like to enter the initial configuration dialog? [yes/no]:
no
COPIAR CÓDIGO
Agora, estamos no modo usuário. Mas, para conseguir configurar porta e atribuir endereço de IP, vamos ter que entrar no modo especial. Isto é, vamos ter que escalar um pouco em termos de privilégios. Para isso, vamos usar o comando enable.

enable
COPIAR CÓDIGO
Toda vez que digitamos um comando e entramos num modo diferente de uso desse terminal de configuração, podemos inserir o comando ? e para abrir uma lista de comandos executáveis a partir daquele modo.
Se apertamos "Enter", vão ser exibidos mais comandos. Se apertamos um "Espaço", vai ser exibida a lista completa de comandos que podemos executar naquele modo.

O que queremos é entrar no modo de configuração. Portanto, vamos ter que digitar o seguinte comando:

configure
COPIAR CÓDIGO
Após apertar "Enter", nos perguntam se queremos configurar a partir de um terminal, de uma memória, de uma rede. Vamos querer configurar a partir de um terminal.

Configuring from terminal, memory, or network [terminal]?
terminal
COPIAR CÓDIGO
Após digitar "terminal" e apertar "Enter", entramos no modo de configuração. Agora vamos digitar novamente o ponto de interrogação para exibir a lista de comandos que podemos utilizar nesse modo. Vamos dar "Espaço" para visualizar a lista completa.

O que queremos configurar? É uma interface, pois queremos habilitar uma daquelas portas. Por isso, digitamos interface e um ponto de interrogação para mostrar as diferentes interfaces que podemos configurar.

interface ?
COPIAR CÓDIGO
O que queremos configurar são essas interfaces Ethernet e FastEthernet. Vamos começar pela FastEthernet.

interface FastEthernet 0/0
COPIAR CÓDIGO
Ao dar "Enter", entramos nessa interface. O que podemos fazer? Analisar quais comandos podemos utilizar para configurá-la de modo ativo. Por isso, digitamos novamente o ponto de interrogação e, em seguida, apertamos em "Espaço" para exibir a lista completa.

Existe o comando shutdown que basicamente desliga essa interface. Mas, não há nenhum outro comando que possamos usar diretamente para ligá-la.

Então, qual comando utilizamos? Usamos dois comandos: o comando no, que nega um comando, e o comando shutdown. Ou seja, não desligue a interface "FastEthernet 0/0". Em seguida, damos "Enter".

no shutdown
COPIAR CÓDIGO
% LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0, changed state to up

Assim, já mudamos a configuração da porta. Se observamos a tela da área de trabalho, a conexão entre roteador e o PC de manufatura já ficou verde. Isto é, já habilitamos a interface "FastEthernet 0/0". Contudo, essa interface ainda não tem endereço de IP atribuído.

Vamos clicar em "Enter" e digitar interrogação. Agora, queremos atribuir o endereço de IP para essa porta. Podemos utilizar o comando ip e adicionar uma interrogação.

ip ?
COPIAR CÓDIGO
O que podemos usar? Existe o comando ip address para definir o endereço de IP de uma interface. Digitamos ip address seguido de uma interrogação:

ip address ?
COPIAR CÓDIGO
O que podemos inserir junto com esse comando? O endereço de IP que queremos atribuir a essa porta, se estivermos utilizando o modo estático de atribuição de endereço IP. Ou se esse modo for o automático, podemos usar, por exemplo: ip address dhcp.

No nosso caso, vamos começar de modo estático. Portanto, vamos ter que inserir o endereço de IP que desejamos atribuir para essa porta. Vamos atribuir então 193.168.3.1 e clicar em "Enter".

ip address 193.168.3.1
COPIAR CÓDIGO
% Incomplete command.
Falta alguma informação. Vamos digitar novamente. Se clicamos com a seta direcional para cima, vamos copiar o comando que usamos anteriormente. No final, vamos incluir uma interrogação para saber o que falta.

ip address 193.168.3.1 ?
COPIAR CÓDIGO
Precisamos identificar qual é a máscara de sub-rede que vamos usar para esse endereço de IP.

No caso, estamos usando o endereço IP da classe C, pois é iniciado pelo primeiro octeto 193.

Essa máscara de sub-rede tem quantos octetos 255? Os três primeiros. Vamos completar o comando com 255.255.255.0 e clicar em "Enter".

ip address 193.168.3.1 255.255.255.0
COPIAR CÓDIGO
Dessa vez, conseguimos ativar a porta "FastEthernet 0/0" e atribuir o endereço IP para essa porta.

Vamos repetir o mesmo processo para os dois PCs de acabamento e embalagem. Mas, lembre-se que o PC da embalagem não está numa porta "FastEthernet", mas, sim, em uma porta "Ethernet 0/1/0". É só passar o mouse sobre o roteador para conferir o nome da interface que vamos inserir no CLI.

Vamos maxizar o CLI novamente. Ainda estamos no modo de configuração da interface "FastEthernet 0/0". Temos que sair dessa interface para entrar nas demais, não é verdade? Por isso, vamos colocar o comando exit.

exit
COPIAR CÓDIGO
Agora, estamos novamente no modo de configuração. Vamos selecionar a próxima interface, no caso "FastEthernet 0/1".

interface fastEthernet 0/1
COPIAR CÓDIGO
Agora, replicamos todo o processo com o comando no shutdown.

% LINK-5-CHANGED: Interface FastEthernet0/1, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1, changed state to up

Agora vamos atribuir o endereço de IP dessa porta e adicionar a máscara de rede:

ip address 193.168.2.1 255.255.255.0
COPIAR CÓDIGO
Tudo configurado, Vamos digitar exit para poder configurar a próxima porta.

interface Ethernet0/1/0
COPIAR CÓDIGO
Digitamos a interface de Ethernet e depois o no shutdown.

% LINK-5-CHANGED: Interface Ethernet0/1/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1/0, changed state to up

Vamos atribuir o endereço de IP e a máscara de rede:

ip address 193.168.4.1 255.255.255.0
COPIAR CÓDIGO
Por fim, damos exit novamente.

Depois de configurar todas as portas como ativas e atribuir os seus respectivos endereços de IP, podemos passar o mouse sobre o roteador para verificar que todas as portas estão com status Up e possuem endereços de IP.

Port	Link	VLAN	IP Address	IPv6 Address	MAC Address
FastEthernet0/0	Up	--	193.168.3.1/24	not set	0001.439C.8801
FastEthernet0/1	Up	--	193.168.2.1/24	not set	0001.439c.8802
Ethernet0/1/0	Up	--	193.168.4.1/24	not set	000B.BE4B.53E6
Vlan1	Down	1	not set	not set	0006.2A22.C285
Observe que os endereços de IP são diferentes. Têm os dois primeiros octetos iguais, porém o terceiro octeto é diferente. O que isso significa?

Estamos na classe C e acabamos de configurar três redes diferentes, uma para cada setor da linha de produção. Agora, precisamos configurar os IPs dos nossos computadores.

Caso esqueçamos o endereço de IP dessa rede, basta passar o mouse sobre o roteador para lembrar que a FastEthernet 0/0 tem endereço de IP da rede 193.168.3, e o último octeto é dedicado ao host, ou seja, o dispositivo que queremos conectar. No caso, já estamos usando 1 para o roteador. Para os PCs, podemos usar o 2.

Vamos então fazer esse processo para cada um dos computadores. Clicamos com o botão direito em cada computador e selecionamos "Desktop > IP Configuration" para mudar o "IPv4 Address":

PC da manufatura: 193.168.3.2;
PC da acabamento: 193.168.2.2;
PC da embalagem: 193.168.4.2.
Após configurar os IPs, vamos verificar se adicionamos corretamente todos os endereços de rede ao passar o mouse em cima do roteador.

Simulação de conexão entre diferentes PCs em diferentes redes como descrita anteriormente. Agora, a conexão entre os dispositivos está verde.

Podemos fazer um ping para testar se a nossa rede está funcionando de fato.

Clicamos no PC da manufatura e vá na opção "Command Prompt". Vamos dar um ping para o computador da embalagem.

ping 193.168.4.2
COPIAR CÓDIGO
Request timed out.
Request timed out.
Request timed out.
Request timed out.
Ping statistics for 192.168.3.3:

Packets: Sent = 4, Received = 0, Lost = 4 (100% loss)
As quatro requisições falharam. Ou seja, dos quatro pacotes enviados no comando ping, nenhum foi recebido e não houve qualquer tipo de retorno.

O que aconteceu? Quando damos um comando ping, o PC procura primeiro qual dispositivo naquela rede pode receber aquele pacote de dados. Como esse pacote está sendo enviado para outra rede, precisamos informar ao PC para onde mandar esse pacote.

Até o momento, não configuramos essa informação. Não dissemos ao PC "quando você tem que mandar uma informação para outra rede, envie essa informação para esse endereço". Na sequência, vamos aprender como resolver esse problema.

https://cdn1.gnarususercontent.com.br/1/1319058/2804eeb8-b9ac-4408-b030-e9e8516803a2.png

https://cdn1.gnarususercontent.com.br/1/1319058/6ae4b613-76f2-4ac0-abf0-2d38c41139a4.png

https://cdn1.gnarususercontent.com.br/1/1319058/d3ee1ec5-725e-47be-8507-38c0c096913c.png

https://cdn1.gnarususercontent.com.br/1/1319058/8e665169-d5c0-4513-bdeb-429602616a04.png

https://cdn1.gnarususercontent.com.br/1/1319058/b73c15a9-5826-4502-95a1-06c362409f60.png

@@02
Comunicação externa

Você criou uma rede com endereço IP: 193.167.2.0 e máscara: 255.255.255.0 interconectando alguns computadores e vai precisar conectar esses dispositivos com redes externas.
Qual dispositivo de rede você deve adotar para exercer essa função?

Alternativa correta
Roteador.
 
Exatamente, a principal função dos roteadores é interconectar redes, encaminhando seus pacotes de dados.
Alternativa correta
Switch.
 
Alternativa correta
Hub.

@@03
Endereços de rede

Ao verificar as conexões de um roteador, você constata que um dos dispositivos conectados possui endereço IP: 33.44.55.66 e máscara de rede: 255.0.0.0.
Qual dos equipamentos listados abaixo está conectado na mesma rede desse dispositivo?

Alternativa correta
Equipamento A - IP: 34.44.55.67 e Máscara 255.0.0.0
 
Alternativa correta
Equipamento B - IP: 33.255.4.3 e Máscara: 255.0.0.0
 
O primeiro octeto do endereço IP é 33, logo só ele me importa para analisar se outro dispositivo está na mesma rede que eu. Os demais são números da máquina. As outras opções começam com número diferente de 33, o que caracteriza que a máquina está em outra rede.
Alternativa correta
Equipamento A - IP: 39.44.55.66 e Máscara 255.0.0.0

@@04
Portão de saída

Nossos pings não conseguiam alcançar do computador da manufatura até o computador da embalagem, correto? Precisamos configurar nosso computador para enviar mensagens para dispositivos externos à nossa rede. Como podemos fazer isso?
Se acessarmos o menu de contexto do nosso PC Manufatura clicando com o botão direito, abrirá a janela familiar a nós. Vamos selecionar a opção "desktop" e, em seguida, "IP Configuration". Observe que temos um campo chamado "default gateway" (em português, "gateway padrão"), que é o portão de saída para o qual devemos encaminhar mensagens ao sair da nossa rede.

Neste campo, devemos inserir o endereço da porta do roteador à qual nosso computador está conectado.

Dessa forma, configuramos a porta de saída da rede, permitindo que nosso computador envie mensagens, dados e outras informações para computadores e dispositivos externos à nossa rede. Isso possibilita a transmissão de informações além dos limites da nossa rede local.

Para recuperar o endereço IP que atribuímos a uma porta do roteador, o processo é simples: basta clicarmos com o botão direito no roteador do nosso projeto do Packet Tracer, selecionar "enter". Na janela exibida, digitamos o comando enable para entrar no modo de configuração.

enable
COPIAR CÓDIGO
Em seguida, digitamos o comando show ip interface e inserimos o nome da interface para a qual desejamos descobrir o endereço IP atribuído. Por exemplo, para a interface FastEthernet0/0, onde o PC da manufatura está conectado, digitamos o comando e pressionamos "Enter".

show ip interface FastEthernet0/0
COPIAR CÓDIGO
Como retorno, obtemos:

A tabela abaixo foi parcialmente transcrita. Para conferi-la na íntegra, execute o código na sua máquina.
FastEthernet0/0 is up, line protocol is up (connected)
Internet address is 193.168.3.1/24

Broadcast address is 255.255.255.255

Address determined by setup command

Observe que ele mostrou para nós o endereço, que é 193.168.3.1.

Podemos utilizar o atalho "Ctrl+C" para copiar o IP. Em seguida, abrimos a aba de configuração de IP no PC da manufatura e inserimos o endereço IP copiado no campo "default gateway". Dessa forma, estamos configurando essa porta do roteador como o portão de saída para essa rede.

Pressionamos "Enter" para salvar as configurações. Agora vamos testar o ping para verificar se está funcionando corretamente. Acessamos novamente o prompt de comando do PC da manufatura e digitamos o comando ping 193.168.4.2, 0.3 é o endereço da nossa rede, enquanto o endereço da rede do PC da embalagem é 0.4. Vamos enviar o ping agora.

ping 193.168.3.4
COPIAR CÓDIGO
Como retorno, obtemos:

Pinging 193.168.4.2 with 32 bytes of data:
Request timed out.

Request timed out.

Request timed out.

Request timed out.

Ping statistics for 193.168.4.2:

Packets: Sent = 4, Received = 0, Lost = …

O primeiro, segundo, terceiro e possivelmente o quarto pings não obtiveram resposta. Você deve estar se perguntando: "O que está acontecendo?". Nosso PC está enviando o ping para o portão de saída do roteador, que por sua vez está encaminhando-o para o PC da embalagem.

No entanto, não configuramos no PC da embalagem qual é a porta de saída daquela rede. Isso significa que o ping está chegando lá, mas não está sendo reencaminhado porque o computador da embalagem não possui essa informação sobre a porta de saída da sua rede.

Agora, vamos repetir esse mesmo processo para todos os PCs. No entanto, há uma maneira mais simples de descobrir o endereço IP das portas do roteador. Como mencionei anteriormente, basta passarmos o mouse sobre o roteador da nossa rede no Packet Tracer e ele mostrará os IPs atribuídos para cada uma das portas.

Apenas queria demonstrar que nós também podemos utilizar esse comando para obter o endereço IP de forma mais rápida e também para copiar e colar.

Vamos clicar no PC de Acabamento e acessar "IP Configuration". A rede nesse computador é 193.168.2.1, que é o portão de saída dessa rede. Portanto, preenchemos o campo "Default Gateway" com esse IP. Agora, no PC de Embalagem, faremos o mesmo procedimento de "IP Configuration" e o endereço será 193.168.4.1.

PC Acabamento
Default Gateway: 193.168.2.1
PC Embalagem:
Default Gateway: 193.168.4.1.
Pressionamos "Enter".

Agora, vamos realizar o teste de ping novamente do PC da Manufatura para o PC da Embalagem. Para isso, clicamos no PC da Manufatura, e na aba "Desktop" selecionamos "Command Prompt". Vamos verificar se agora funciona digitando o comando ping 193.168.4.2.

ping 193.168.4.2
COPIAR CÓDIGO
Como retorno, obtemos:

Pinging 193.168.4.2 with 32 bytes of data:
Reply from 193.168.4.2: bytes=32 time-6ms TTL-127

Reply from 193.168.4.2: bytes=32 time<lms TTL-127

Reply from 193.168.4.2: bytes=32 time<lms TTL=127

Reply from 193.168.4.2: bytes=32 time<lms TTL-127

Ping statistics for 193.168.4.2:

Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),

Approximate round trip times in milli-seconds:

Minimum Oms, Maximum = 6ms, Average = 1ms

Observe que agora recebemos uma resposta. Isso significa que os quatro pacotes foram enviados e recebidos corretamente.

Agora que identificamos e corrigimos o problema, surge a pergunta: será que é possível realizar todo esse processo de atribuição de endereço IP de forma automática?

Vamos ver sobre isso na sequência. Até mais!

@@05
Default gateway

Uma amiga estava testando a criação de quatro sub-redes usando um roteador em um ambiente de simulação, tal como o Cisco Packet Tracer. Ao testar a conectividade entre computadores em redes diferentes utilizando o ping, ela percebe um erro. Os pacotes encaminhados não alcançam o destino. Nesse momento, você aponta que talvez ela não tenha configurado o default gateway das redes.
Qual argumento você utilizaria para explicar esse apontamento?

 você utilizaria para explicar esse apontamento?

Alternativa correta
O default gateway garante o acesso remoto dos equipamentos conectados em uma rede.
 
Alternativa correta
O default gateway é utilizado no encaminhamento de pacotes entre a rede local e redes externas, sendo o “portão de saída” de uma rede.
 
O default gateway é o endereço IP responsável por encaminhar pacotes para redes externas.
Alternativa correta
O default gateway é usado para bloquear acessos maliciosos na rede.

@@06
IPv4, IPv6 e classes de IP

Até o momento, utilizamos uma série de endereços IP para a configuração das nossas máquinas e o endereçamento delas nas redes, mas não fizemos nenhuma reflexão. Será que podemos usar qualquer sequência de 4 octetos? Podemos, por exemplo, fazer uma sequência como 999.0.0.0? Essa é uma sequência válida? Nesse vídeo, descobriremos que não!
Nós temos 4 octetos e utilizamos 32 bits para fazer o endereçamento de IP. Com esses 32 bits, conseguimos fazer a identificação única de 4,3 bilhões de dispositivos ao redor do mundo. Porém, existem muito mais que 4,3 bilhões de computadores hoje em dia.

Logo, a versão 4 do protocolo IP precisou ser modificada, evoluindo para uma nova versão conhecida como IPv6 (versão 6 do protocolo IP), que utiliza 128 bits para endereçamento dos dispositivos. Assim, é possível endereçar até 1 decilhão de dispositivos.

Você deve estar se perguntando: por que estamos usando o IPv4 se precisamos usar IPv6, dado o volume de máquinas que temos? Algumas redes e dispositivos ainda foram criados utilizando o padrão IPv4, então usamos uma técnica chamada tunelamento para fazer o encapsulamento de um endereço IPv6 e encaminhar isso através de uma rede IPv4. Chegando ao destino, esse pacote é desencapsulado e então temos o endereçamento IPv6 da máquina de destino.

Não entraremos em muitos detalhes técnicos sobre o protocolo IPv6, no entanto, basta saber que ele utiliza uma abordagem hierárquica para a atribuição dos endereços.

O protocolo IPv4, que estamos utilizando na construção de redes, é dividido em algumas classes, ou seja, conjuntos de endereços. Surge a primeira pergunta: há um limite inferior ou superior de endereços, isto é, de sequências numéricas que podemos utilizar nos octetos?

Descobriremos que sim! Mas quais são esses limites?

Limites de endereço no IPv4
Quanto ao limite inferior, não existem endereços de IP negativos, logo, os endereços devem ser superiores à sequência de zero nos quatro octetos (0.0.0.0). Da mesma forma, temos um limite superior: os endereços devem ser inferiores à sequência de 255 em todos os quatro octetos (255.255.255.255).

Classe A
No IPv4, os endereços estão distribuídos em cinco classes diferentes. Vamos começar pela primeira: a classe A. Na classe A, temos endereços de IP que começam o primeiro octeto com sequências que vão de 1 a 126.

Nessa classe, temos como máscara de rede padrão o formato 255.0.0.0. A máscara de rede nos permite identificar, a partir de um endereço de IP da classe, qual é o endereço da rede na qual o dispositivo se encontra.

Vamos analisar um exemplo prático: temos o endereço de IP 123.145.3.3, que pertence à classe A, visto que o primeiro octeto é iniciado com a sequência 123. Qual seria o endereço de rede desse dispositivo?

Basta observar na máscara de rede padrão quais octetos estão ocupados pela sequência de 255. Fazendo a subtração e preenchendo os demais octetos com zero, nós obtemos o endereço de rede na qual esse dispositivo está conectado, ou seja, 123.0.0.0.

O endereço de rede acima não pode ser atribuído a nenhum dispositivo da nossa rede, logo, ele é dedicado à identificação dessa rede específica.
Além do endereço de rede, dedicado à identificação da rede, temos outro endereço: o de broadcast, para o qual o dispositivo envia um pacote de mensagem que quer encaminhar para os demais da mesma rede em que ele está conectado. Inclusive, ao enviar para esse endereço, o próprio dispositivo recebe o pacote de mensagem enviado.

Para obter o endereço de broadcast, basta pensarmos de forma oposta a como obtemos o endereço de rede. Ao invés de preencher os demais octetos com 0, vamos preencher com 255, ou seja, 123.255.255.255.

Assim, conseguimos estabelecer um limite inferior e um limite superior da nossa rede, que são os endereços dedicados primeiro à rede e depois ao broadcast.

Classe B
Temos também a classe B, onde temos os endereços IP que possuem como primeiro octeto uma sequência de 128 até 191. Já a máscara padrão dessa classe é 255.255.0.0. Essa máscara é importante para identificar o endereço da rede de um dispositivo conectado com o endereço IP da classe B e também o endereço de broadcast dessa rede.

Agora, vamos usar como exemplo o seguinte endereço IP da classe B: 135.145.3.3. Qual seria o endereço da rede na qual o dispositivo está conectado?

O exercício é o mesmo, mas agora os dois primeiros octetos são dedicados à identificação da rede e os demais são preenchidos com 0, obtendo 135.145.0.0.

Para encontrar o endereço de broadcast, preenchemos os demais octetos com 255, então obtemos 135.145.255.255.

Dessa forma, identificamos o endereço da rede e de broadcast de um endereço de IP na classe B.

Classe C
Agora, vamos à classe C. Ela é formada por dispositivos que apresentam no seu primeiro octeto uma sequência de 192 até 223. Como máscara de rede padrão, ela possui uma sequência de 255 nos três primeiros octetos, sendo apenas o último octeto utilizado para identificar os dispositivos conectados na rede, então temos 255.255.255.0.

A máscara de rede nos permite analisar quantos dispositivos nós podemos conectar nessa rede específica. No caso da classe C, podemos ter várias redes diferentes e poucos dispositivos conectados em cada uma delas.

Observando a máscara de rede padrão da classe A, temos um único octeto para a identificação da rede, e os demais podem ser utilizados para identificar os dispositivos. Portanto, na classe A, podemos agregar o maior número possível de dispositivos em uma rede.

Então, como descobrir o endereço de rede e o endereço broadcast de um dispositivo conectado com o endereço IP da classe C? Vamos usar o exemplo do endereço 193.168.3.3.

Para encontrar o endereço dessa rede, basta modificar o último octeto para 0, obtendo 193.168.3.0. De modo similar, para encontrar o endereço broadcast da rede, substituímos o último octeto pela sequência 255, ou seja, 193.168.3.255.

Classes D e E
Além das anteriores, temos duas outras classes que são especiais, as quais não utilizamos na identificação dos dispositivos computacionais no dia a dia. São a classes D e E.

A classe D é formada por endereços de IP que apresentam o seu primeiro octeto no intervalo de 224 a 239. Ela é muito utilizada, por exemplo, para multicast, ou seja, para encaminhar mensagens a grupos de dispositivos específicos em uma rede.

Já a classe E é formada por endereços que apresentam o seu primeiro octeto no intervalo de 240 até 255. Essa classe é utilizada para fins de pesquisa e desenvolvimento em redes.

Conclusão
Agora sabemos como usar um endereço de IP, os seus limites e as classes, sendo algumas delas inclusive reservadas, conforme abordado anteriormente.

Em relação ao endereço de IP, ainda há mais um detalhe: a questão de IP público e IP privado. Será que o endereço que usamos na rede é de fato o endereço da nossa máquina? Vamos analisar isso na sequência!

@@07
Limitações IPv4

Apesar da simplicidade do endereçamento IPv4, representado por uma sequência de quatro octetos (por exemplo: 193.186.6.1), o processo de alocação e atribuição de endereços tem se tornado cada vez mais complexo devido a uma limitação de versão do protocolo.
Assinale a alternativa que indica tal limitação:

Diferentes padrões de máscara de rede adotados em cada classe.
 
A diferença entre os padrões de máscara de rede adotados em cada classe não constitui uma limitação do IPv4. Como vimos, é uma facilidade que permite a criação de redes com diferentes perfis.
Alternativa correta
Número de bits adotado no endereçamento.
 
O IPv4 usa endereços de 32 bits, possibilitando um total aproximado de 4,3 bilhões de endereços únicos. Com a evolução do número de dispositivos conectados em rede, esse limite é insuficiente, tornando o processo de atribuição de endereços mais complexo. Com isso, surgiu uma nova versão do protocolo IP - conhecida como IPv6 - com capacidade de atribuir endereços únicos a undecilhões de dispositivos.
Alternativa correta
Alocação do endereço de rede e broadcast, indisponibilizando seu uso por equipamentos conectados na rede.

08
Classes IP

Os endereços IP (Internet Protocol) são usados para identificar e localizar dispositivos em uma rede IP. Existem diferentes formas de criar endereços IP para computadores. Imagine que você está criando uma rede de um laboratório de informática e precisa definir como será o endereçamento IP das máquinas.
Quais são as classes de endereços IP que podem ser usadas neste caso?

Classe A, B e D.
 
Alternativa correta
Classe A, B e C.
 
A IETF (Internet Engineering Task Force) determinou que existiriam ao todo 5 classes de endereços IP, indo de ordem alfabética da classe A até a classe E. Porém as duas últimas classes não são usadas para endereçar as máquinas conectadas em um ambiente como laboratório de informática ou escritório, apenas em usos mais reservados (multicast e experimentos).
Alternativa correta
Classe A, B e E.
 
Parabéns, você acertou!


09
Identificando classes

Ao verificar o endereço IP do seu computador na rede usando o comando ipconfig /all no prompt de comando do Windows, você obtém o IP 190.145.49.3 e máscara de rede 255.255.0.0.
Esse endereço pertence a qual classe?

Classe C.
 
Alternativa correta
Classe A.
 
Alternativa correta
Classe B.
 
A classe "B" possui o primeiro octeto variando de 128 a 191. Dessa forma, pelo fato do número 190 se encontrar dentro de 128 a 191, sabemos que é um endereço da classe "B".

10
Endereço de Rede e Broadcast

Você tem a informação de que uma máquina possui endereço IP 9.8.9.8, com máscara de rede 255.0.0.0.
Qual seria o endereço da rede na qual essa máquina está conectada e seu respectivo endereço de broadcast?

Rede: 9.0.0.0 e Broadcast: 9.255.0.255
 
Alternativa correta
Rede: 9.0.0.0 e Broadcast: 9.255.255.255
 
Como fazemos para descobrir o endereço de rede que esse endereço IP está inserido?
Basta substituirmos o 255 da máscara de rede pelo o octeto correspondente do endereço IP. Neste caso, teremos: 9.0.0.0 :)
E para descobrir o endereço de broadcast da rede?
Pegamos o endereço de rede e substituímos os octetos com 0’s (originais da máscara) pelo octeto 255. Sendo assim, obteremos: 9.255.255.255
Alternativa correta
Rede: 9.8.0.0 e Broadcast: 9.8.0.255

@@11
IP público e privado

Como conseguimos nos conectar à internet?
Para estabelecer uma conexão com a internet, é necessário que nosso provedor de serviços de internet atribua um endereço à nossa rede, permitindo a troca de informações e a visualização de nossa rede por outros computadores, possibilitando que respondam às nossas solicitações. Nesse sentido, há uma distinção entre os endereços de IP público e privado, dentro de cada classe de endereços IP.

IP público e IP privado
IP público = conexão externa na internet
IP privado = identificação de dispositivos em rede interna

Os endereços IP públicos são usados para estabelecer a conexão externa com a internet, enquanto os endereços IP privados são empregados para identificar dispositivos em redes internas. Dentro de cada classe de endereço IP, existem conjuntos específicos de endereços designados como endereços IP privados.

Conforme vimos, não há nada extremamente confidencial. A única distinção é que esse conjunto de endereços é exclusivamente utilizado para identificar dispositivos em uma rede privada, ou seja, destinado somente para comunicação interna dentro dessa rede.

IP privado
Classe A: 10.0.0.0
Classe B: 172.16.0.0 a 172.31.0.0

Classe C: 192.68.0.0

Dentro da classe A de endereços IP, os endereços IP privados são aqueles em que o primeiro octeto começa com 10. Na classe B, o conjunto de endereços IP privados varia do primeiro octeto 172.16 até a sequência dos dois primeiros octetos 172.31. Já na classe C, temos um conjunto de endereços IP privados em que os dois primeiros octetos começam com 192.68.

Entendemos a distinção entre endereço IP privado e endereço IP público em todas as classes. Podemos, agora, realizar um teste prático para verificar qual é o endereço IP atribuído ao nosso computador e qual endereço IP é visível para dispositivos externos à nossa rede.

Testando o IP da nossa máquina
Para realizar o teste, vamos abrir o prompt de comando digitando "prompt" ao clicarmos no botão do Windows (ou do sistema operacional que você esteja usando). Em seguida, digitaremos o comando ipconfig /all.

ipconfig /all
COPIAR CÓDIGO
Esse comando nos fornecerá uma série de informações, incluindo o endereço IP que estamos usando para identificar nossa máquina na rede interna. Dentre as informações temos o endereço IP que foi identificado: 192.168.1.117. Também foi exibida a máscara de rede.

O retorno abaixo foi parcialmente transcrito. Para conferi-lo na íntegra, execute o código na sua máquina.
Adaptador Ethernet Ethernet
Sufixo DNS específico de conexão.

Descrição: Intel(R) Ethernet Controller (3) 1225-V

Endereço Físico: D8-5E-D3-85-95-4B

DHCP Habilitado : Sim

Configuração Automática Habilitada : Sim

Endereço IPv6 de link local : fe80::4db5:f496: 8b0a:6f77% 3 (Preferencial)

Endereço IPv4 : 192.168.1.117(Preferencial)

Máscara de Sub-rede : 255.255.252.0

Concessão Obtida : quarta-feira, 26 de abril de 2023 15:42:2

Assim, identificamos que estamos usando a classe C.

Agora, vamos verificar na internet, utilizando um dos sites que utilizamos para testar a velocidade de conexão, qual endereço IP está sendo identificado para o nosso dispositivo a partir da rede externa. Vamos lá.

Vamos prosseguir abrindo o navegador, no caso, o Google Chrome, e acessando o endereço meuip.com.br. Neste site, podemos identificar o endereço IP associado ao nosso dispositivo. Observem que ao entrarmos no site já é identificado o IP.

Meu ip é 177.8.171.44
É importante observar que esse endereço IP, obtido no site, pode ser bastante diferente daquele que obtivemos ao executar o comando ipconfig.

Isso ocorre porque o endereço IP que obtivemos no site é o endereço IP público que estamos utilizando para nos conectarmos à internet. Por outro lado, na nossa rede privada, temos um endereço IP diferente que é utilizado para identificar nossa máquina internamente.

Essa distinção entre endereços IP público e privado é comum e necessária para o correto funcionamento das redes.

Agora que compreendemos a distinção entre endereço IP público e endereço IP privado, vamos prosseguir com o nosso projeto? Até mais!

@@12
IP privado e internet

Um colega de trabalho questiona sobre a diferença entre o IP identificado por um site que exibe endereços IP de computadores e o endereço IP exibido pelo comando ipconfig no prompt de comando do Windows desse mesmo computador.
Qual seria a explicação que você utilizaria para justificar essa diferença?

O comando ipconfig está exibindo o IP público do computador, enquanto o site está exibindo o IP privado.
 
Alternativa correta
O comando ipconfig está exibindo o IP privado usado apenas para comunicação na rede local, enquanto o site está exibindo o IP público.
 
Os endereços IP privados são usados para comunicação somente em redes locais, de acordo com a especificação, eles não podem ser usados para comunicação na internet por exemplo. Os IPs privados são convertidos em IPs públicos pelo método de tradução NAT. Os IPs públicos são fornecidos pelos provedores de serviços de rede.
Alternativa correta
O site está gerando IPs aleatórios para exibir.

@@13
Faça como eu fiz: crie e teste outros casos de rede!

Explore o que já aprendemos até aqui e crie outros casos de rede no simulador Cisco Packet Tracer.
Você pode também utilizar outros roteadores e switches para conectar diferentes dispositivos.

Aproveite o simulador para aprender explorando diferentes possibilidades, analise a operação das redes no modo de simulação. Verifique os protocolos que estão sendo executados no painel lateral direito que surge quando estamos no modo de simulação.

Opinião do instrutor

O melhor jeito de desenvolver habilidades no mundo tech é pondo a mão na massa, fazendo experiências e testando possibilidades.

@@14
Para saber mais: entendendo o IPv6

Durante nosso aprendizado, falamos brevemente a respeito dessa nova versão do protocolo IP, o IPv6. Caso queira se aprofundar neste tema, você pode acessar o artigo Entendendo o IPv6, disponível na plataforma da Alura!
Leia aqui o trecho inicial do artigo:

“Uma empresa de hospedagem está enfrentando um problema: o número de endereços IPs disponíveis está acabando. Sem endereços IPs, a empresa não pode ter novos clientes. Essa empresa possui cerca de 5000 servidores dedicados para os clientes. Cada servidor tem um IP público, por isso ela tem uma faixa de IPs para comportá-los. Por exemplo, uma faixa de 250.127.1.x a 250.127.20.x endereços disponíveis.[...]”

https://www.alura.com.br/artigos/entendendo-o-ipv6?_gl=1*z3aa6q*_ga*MTgwMzIzMjk2Ni4xNjg4ODE5OTcz*_ga_59FP0KYKSM*MTY5MDg3ODgwNS40NC4xLjE2OTA4ODE2ODEuMC4wLjA.*_fplc*b0p4aUhKQ1YwR2VzOXV0WTN1JTJGeHhGOHFjTEpIVVRjbDglMkJEZHhVbVozS3BFJTJCbTlIYVZxNzZKNlAlMkJwN0w1ZUk0a3pITkdzY2h2Z252V3V0JTJGMnRLeUdqMnZCOGNOQ3MlMkZvdW53RkVlZ2FIelRyWUZhNSUyRldEbllWTTlTNkRwMEElM0QlM0Q.

@@15
O que aprendemos?

Nessa aula, você aprendeu como:
Construir e operar redes usando roteadores como dispositivo de interligação, permitindo a comunicação de redes locais com redes externas;
Criar sub redes usando roteadores;
Configurar o default gateway de uma rede;
Observar as regras do protocolo IP na atribuição de endereços aos equipamentos interligados em uma rede.