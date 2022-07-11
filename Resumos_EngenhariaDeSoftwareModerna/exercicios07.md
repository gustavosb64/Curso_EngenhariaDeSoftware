# Engenharia de Software Moderna
# Capítulo 7: Arquitetura

## Exercícios

#### 1. Dada a sua complexidade, sistemas de bancos de dados são componentes relevantes na arquitetura de qualquer tipo de sistema. Verdadeiro ou falso? Justifique a sua resposta.

#### 2. Descreva três vantagens de arquiteturas MVC.
* Por separar a componente View das outras componentes do sistema, favorece a especialização do time que desenvolve o sistema.
* A componente Model se torna independente das outras, o que evita inconvenientes que poderiam ser causados ao se mexer nas sessões que trabalham diretamente com a base de dados.
* Permite que as classes Model sejam utilizadas por diferentes classes View.
* Favorece a testabilidade, já que os métodos funcionais não estão totalmente atrelados ao desenvolvimento das classes visuais.

#### 3. Qual a diferença entre classes Controladoras em uma Arquitetura MVC tradicional e classes Controladoras de um sistema Web implementado usando um framework MVC como Ruby on Rails?
* 

#### 4. Descreva resumidamente quatro vantagens de microsserviços.
* Possui falhas parciais, devido à modularização do sistema em componentes menores.
* Desenvolvimento e evolução de diferentes serviços de maneira independente.
* Diferentes partes do sistema podem ser implementada com diferentes tecnologias.
* Escalabilidade: como os sistemas estão mais modularizados, é mais fácil lidar com problemas de performance, por exemplo, em microsserviços.
 
#### 5. Por que microsserviços não são uma bala de prata? Isto é, descreva pelo menos três desvantagens do uso de microsserviços.
* São sistemas mais complexos de se implementar.
* Possuem maior latência de comunicação entre as partes.
* O acesso aos bancos de dados deve ser realizado com maior cautela para evitar problemas.

#### 6. Explique a relação entre a Lei de Conway e microsserviços.
* Lei de Conway: empresas tendem a adotar arquiteturas de software que são cópias de suas estruturas organizacionais. É comum sistemas Web utilizarem microsserviços, o que não é uma surpresa, já que estamos falando de sistemas que se conectam ao redor do mundo e são desenvolvidos por equipes espalhadas em partes diversas.

#### 7. Explique o que significa desacoplamento no espaço e desacoplamento no tempo. Por que arquiteturas baseadas em filas de mensagens e arquiteturas Publish/Subscribe oferecem essas formas de desacoplamento?
* **Desacoplamento no espaço**: clientes não precisam conhecer os servidores e vice-versa.
* **Desacoplamento no tempo**: clientes e servidores não precisam estar simultaneamente disponíveis para se comunicarem.
* As arquiteturas de mensagems enfileram diversas mensagens antes de serem enviadas aos servidores, que gera o desacoplamento acima. De maneira similiar, Publish/Subscribe publicam os chamados eventos em um serviço separado (de publish/subscribe), de onde os chamados assinantes requisitam o acesso. Além disso, os assinantes são notificados assincronamente.

#### 8. Quando uma empresa deve considerar o uso de uma arquitetura baseada em filas de mensagens ou uma arquitetura publish/subscribe?
* Quando a empresa está lidando com um sistema que pode ser dividido em outros subsistemas (de vendas e engenharia, por exemplo), em que é necessário haver uma comunicação entre as duas partes sem que seja de maneira imediata. Neste contexto, é conveniente se utilizar uma fila de mensagens ou um serviço de publish/subscribe para que as partes que precisam acessar o que foi enviado o façam quando possível.

#### 9. Explique o objetivo do conceito de tópicos em uma arquitetura publish/subscribe.
* Tópicos são categorias de eventos, que servem para que apenas os assinantes interessados no tópico acessem os eventos.

#### 10. (POSCOMP, 2019, adaptado) Marque V ou F.
    * (F?) O padrão MVC é uma adaptação do padrão arquitetural Camadas. A Camada Visão lida com a apresentação e a manipulação da interface, a Camada Modelo organiza os objetos específicos da aplicação, e a Camada Controle posiciona-se entre estas duas com as regras do negócio.
    * (V) O padrão Broker é voltado a problemas de ambientes distribuídos. Sugere uma arquitetura na qual um componente (broker) estabelece uma mediação que permite um desacoplamento entre clientes e servidores.
    * (V) Mesmo que um dado padrão arquitetural ofereça uma solução para o problema sendo resolvido, nem sempre ele é adequado. Fatores como contexto e o sistema de forças que afeta a solução fazem também parte do processo de avaliação e da escolha de padrões adequados.
