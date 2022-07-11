# Engenharia de Software Moderna
# Capítulo 7: Arquitetura

## 7.1 Introdução
* Mais de uma definição para arquitetura de software:
    * Definição 1: Arquitetura preocupa-se com "projeto em mais alto nível", ou seja, o foco deixa de ser a organização e interfaces de classes individuais e passa a ser unidades de maior tamanho.
        * Os componentes arquiteturais devem ser relevantes para que um sistema atenda a seus objetivos.
    * Definição 2: Arquitetura de software inclui as decisões de projeto mais importantes em um sistema; decisões tão importantes que, uma vez tomadas, dificilmente poderão ser revertidas.
        * **conjunto de decisões**.
* **Padrões arquiteturais** propõem uam organização mais alto nível para sistemas de software, incluindo seus principais módulos e as relações entre eles.
### 7.1.1 Debate Tanenbaum-Torvalds
* Tanenbaum argumentou que "Linux estava obsoleto" por seguir uma **arquitetura monolítica**, e defendia que sistemas operacionais deveriam seguir uma **arquitetura microkernel**, onde o kernel fica responsável apenas pelas funções mais básicas do sistema.
 
## 7.2 Arquitetura em Camadas
* É um dos padrões arquiteturais mais usados.
* **Camadas:** classes são organizadas em módulos de maior tamanho, que estão dispostas de forma hierárquica.
* **Uma camada somente pode usar servições da camada imediatamente inferior.**
* São muito usadas na implementação de protocolos de rede.
* Particiona a complexidade envolvida no desenvolvimento de um sistema em componentes menores.
### 7.2.1 Arquitetura em Três Camadas
* Tipo de arquitetura comum na cosntrução de sistemas de informação corporativos. As três camadas são:
    * **Camada de apresentação** (ou _interface com o Usuário_)
    * **Camada de aplicação** (ou _Lógica de Negócio_): implementa as regras de negócio do sistema.
    * **Banco de dados**: armazena os dados manipulados pelo sistema.
* Normalmente é uma arquitetura distribuída:
    * A camada de apresentação roda na máquina dos clientes;
    * A camada de aplicação em um servidor (servidor de aplicação);
* A camada de aplicação pode ter diversos módulos, incluindo:
    * _Fachada_, para facilitar o acesso ao sistema pelos clientes
    * Módulo de _persistência_, para isolar o banco de dados.
* Também existem arquiteturas em **duas camadas**, com a camada de interface e de aplicação unidas em uma única camada.
    * Desvantagem: todas as operações ocorre nos clientes, que devem possuir um maior poder computacional.
  
## 7.3 Arquitetura MVC
* _Model-View-Controller_.
* Define que as classes de um sistema deve mser organizadas em três grupos:
    * **Visão**: responsáveis pela interface gráfica.
    * **Controladoras**: tratam e interpretam eventos gerados por dispositivos de entrada e saída.
    * **Modelo**: classes qeu armazenam os dados manipulados pela aplicação e que têm a ver com o domínio do sistema em construção. Não tem nenhum conhecimento das classes Visão ou Controller.
* Interface gráfica: formada por objetos de visão e controladores.
    * MVC = (Visão + Controladores) + Modelo = Interface Gráfica + Modelo
* **Vantagens**:
    * Favorece a especialização do trabalho de desenvolvimento (front-end não precisa mexer no back-end)
    * Permite que classes de Modelo sejam usadas por diferentes Visões.
    * Favorece testabilidade. Como é mais fácil testar objetos não visuais, a separação entre eles favorece os testes.
* **Diferença entre MVC e três camadas**?
    * Existem duas vertentes do MVC: a clássica, que surgiu com Smalltalk-80, e a versão Web, que se assemelha bastante sistema de três camadas.
### 7.3.1 Single Page Applications
* SPAs seguem uma arquitetura parecida com MVC. A interface da SPA, contendo visão e controle, é implementada em HTML. O modelo é implementado em JavaScript.

## 7.4 Microsserviços
* Alternativa às estruturas monolíticas.
* Aplicações baseadas em microsserviços tornam-se possíveis devido à **computação em nuvem**.
* Possui uma boa compatibilidade com métodos ágeis.
* Certos grupos de módulos são executados em processos independentes, sem compartilhamento de memória, ou seja, o sistema é decomposto em mulos não apenas em tempo de desenvolvimento, mas também em tempo de execução.
* Quando os módulso são separados em processos distintos, não há mais possibilidade de que um módulo acesse um recurso interno de outro módulo.
* Em vez disso, por construção, toda comunicação tem que ocorrer via interfaces públicas dos módulos.
* **Vantagens**:
    * Evolução mais rápida e independente, com melhor separação em times. 
    * **Escalabilidade**: bem mais fácil lidar com problemas de performance, por exemplo, com microsserviços.
    * Permitem que diferentes partes do sistema sejam implementadas em diferentes tecnologias, como diferentes linguagens.
    * **Falhas parciais**: quando há uma falha, ela ocorrem em apenas um microsserviço.
### 7.4.1 Gerenciamento de Dados
* Microsserviços devem ser autômatos também do ponto de vista de dados.
* O ideal é que cada microsserviço utilize sua própria base de dados.
### 7.4.2 Quando não usar microsserviços?
* **Complexidade**: esta arquitetura é mais complexa do que a monolítica, e deve ser implementada em sistemas distribuídos.
* **Latência**: a comunicação entre microsserviços também envolve um atraso maior.
* **Transações distribuídas**: dificultade de lidar com bancos de dados atômicos.
 
## 7.5 Arquiteturas Orientadas a Mensagens
* A comunicação entre clientes e servidores é mediada por um terceiro serviço que têm a única função de prover uma **fila de mensagens** (ou **brokers**).
* Cliente -> (msg_n ... msg_3; msg_2; msg_1) -> Servidor
* Os clientes atuam como **produtores** de informações (inserem mensagens na fila)
* Os servidores atuam como **consumidores** de mensagens.
* A comunicação do lado do cliente torna-se **assíncrona**, por isso o serviço de mensagens deve ser instalado em uma máquina estável com alto poder de processamento.
* Viabilizam duas formas de **desacoplamento** entre componentes de uma aplicação distribuída:
    * **Desacoplamento no espaço**: clientes não precisam conhecer os servidores e vice-versa.
    * **Desacoplamento no tempo**: clientes e servidores não precisam estar simultaneamente disponíveis para se comunicarem.
* Desacoplamento no espaço torna filas de mensagens bem flexíveis, onde times de desenvolvimento podem evoluir seus sistemas com autonomia.
* Desacoplamento no tempo torna a solução robusta a falhas (quedas no servidor não tem impacto nos clientes).
 
## 7.6 Arquiteturas Publish/Subscribe
* Também chamadas de **Arquiteturas Orientadas a Eventos**.
* As mensagens são chamadas de **eventos**, os componentes são chamados de **publicadores** e **assinantes** de eventos.
* Publicadores produzem eventos e os publicam no serviço de publish/subscribe, normalmente em uma máquina separada.
* Assinantes devem previamente assinar eventos de sesu interesse. Quando um evento é publicado, seus assinantes são notificados.
* Oferecem desacoplamento no tempo e no espaço.
* **Diferenças com filas de mensagens**:
    * Um evento gera notificações em todos os seus assinantes, enquanto em filas de mensagens, as mensagens são sempre consumidas por um único servidor.
    * Os assinantes são notificados assincronamente, enquanto que, em fila de mensagens, os servidores têm que "puxar" as mensagens da fila.
* Em alguns sistemas publish/subscribe, eventos são organizados em **tópicos**, que funcionam como categorias de eventos.

## 7.7 Outros padrões arquiteturais
#### Pipes e filtros
* É um tipo de arquitetura orientada a dados, na qual os programas — chamados de **filtros** — têm como função processar os dados recebidos na entrada e gerar uma nova saída. 
* Os filtros são conectados por meio de pipes, que agem como buffers. Isto é, pipes são usados para armazenar a saída de um filtro, enquanto ela não é lida pelo próximo filtro da sequência. 
* Com isso, os filtros não precisam conhecer seus antecessores e sucessores, o que torna esse tipo de arquitetura bastante flexível, permitindo as mais variadas combinações de programas. Além disso, por construção, filtros podem ser executados em paralelo
#### Cliente/Servidor
* Muito usada na implementação de serviços básicos de rede. 
* Clientes e servidores são os dois únicos módulos desse tipo de arquitetura e eles se comunicam por meio de uma rede. Os clientes solicitam serviços ao módulo servidor e aguardam o processamento. São usadas para implementar serviços como os seguintes: 
    * serviço de impressão, que possibilita que clientes imprimam em uma impressora remota, que não está fisicamente conectada à máquina deles; 
    * serviço de arquivos, que possibilita que clientes acessem o sistema de arquivos (isto é, o disco) de uma máquina servidora; 
    * serviço de bancos de dados, que permite que clientes acessem um banco de dados instalado em uma outra máquina; 
    * serviço Web, que permite que clientes (no caso, navegadores) acessem recursos (no caso, páginas HTML) armazenadas e providas por um servidor Web.

## 7.8 Anti-Padrões Arquiteturais
* **Não** é recomendado.
* Explosão no número de dependências, que dá origem a um espaguete de código. Consequentemente, a manutenção do sistema torna-se muito difícil e arriscada.
* **Big ball of mud**: sistemas nos quais qualquer módulo comunica-se com praticamente qualquer outro módulo.
