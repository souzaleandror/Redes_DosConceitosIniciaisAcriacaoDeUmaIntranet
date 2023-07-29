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

