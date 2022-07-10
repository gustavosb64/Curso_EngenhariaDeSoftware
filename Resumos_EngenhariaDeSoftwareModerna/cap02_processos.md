# Engenharia de Software Moderna
# Capítulo 2: Processos

## 2.1 Importância de Processos
* Um processo de desenvolvimento de software define um conjunto de passos, tarefas, eventos e práticas que devem ser seguidos por desenvolvedores de software na produção de um sistema.
* Quando lidamos com equipes, sem um processos (mesmo que simples e leve) existe o risco de qeu os times de desenvolvimento passem a trabalhar de forma descoordenada.

## 2.2 Manifesto Ágil
* 2001: um grupo de profissionais se reuniu na cidade de Snowbird, em Utah, para discutir e propor uma alternativa aos processos Waterfall.
* Software é diferente de outros produtos da Engenharia:
    * Requisitos mudam com frequência
* **MANIFESTO ÁGIL**:
    * **Indivíduos e interações**, mais do que processos e ferramentas.
    * **Software em funcionamento**, mais do que documentação abrangente.
    * **Colaboração com o cliente**, mais do que negociação de contratos.
    * **Respostas a mudanças**, mais do que seguir um plano.
* **Característica principal**: 
    * Ciclos curtos e iterativos de desenvolvimento.
    * Começando pelo o que é mais urgente ao cliente.
* Passos:
    * Primeiramente, se implementa uma primeira versão do sistema, com as funcionalidades mais essenciais.
    * Depois de validade pelo cliente, começa-se um novo ciclo (iteração), adicionando mais funcionalidades.
* As iterações em métodos ágeis **não** são um pipeline de tarefas.
* Outras características dos processos ágeis:
    * **Menor ênfase em documentação**;
    * **Menor ênfase em planos detalhados**;
    * **Inexistência de uma fase dedicada a design** (_big design front_);
    * **Desenvolvimento em times pequenos**;
    * **Ênfase em novas práticas de desenvolvimento**, como _pair programming_ testes autômatos e integração contínua.
* Pelas características mais versáteis, processos ágeis são chamados de processos **leves**.
* **Alguns métodos ágeis**:
    * _Extreme Programming_ (XP);
    * _Scrum_;
    * _Kanban_;
* Processos vs métodos:
    * _Processos_ são conjunto de passos, etapas e tarefas qeu se usa pra construir um software.
    * _Métodos_ são conjunto de recomendações de como organizar um processo.

## 2.3 Extreme Programming (XP)
* Método leve e recomendado para desenvolver software com requisitos vagos ou sujeitos a mudanças (basicamente, sistemas comerciais).
* **Não** é um método prescritivo:
    * É definido por um conjunto de valores, princípios e práticas de desenvolvimento.
* Frequentemente, quando decidem adotar XP, desenvolvedores concentram-se em _práticas_.
* **Valores**:
    * Comunicação, simplicidade, feedback, coragem, respeito e qualidade de vida.
* **Princípios**:
    * Humanidade, economicidade, benefícios mútuos, melhorias contínuas, falhas acontecem, baby steps e responsabilidade pessoal
* **Práticas**:
    * **Prática sobre o Processo de Desenvolvimento**:
        * representante dos clientes, histórias dos usuários, iterações, releases, planejamento de releases, planejamento de iteraçẽos, planning poker, slack.
    * **Práticas de Programação**:
        * Design incremental, programação pareada, desenvolvimento dirigido por testes (TDD), build automatizado, integração contínua.
    * **Práticas de Gerencimaneto de Projetos**:
        * Métricas, ambiente de trabalho, contratos com escopo aberto.
### 2.3.1 Valores
* XP defende que o desenvolvimento de software seja norteado por três valores principais:
    * **Comunicação**:
        * Importante para qualquer projeto, para evitar e aprender com os erros
    * **Simplicidade**:
        * Todo sistema complexo e desafiador possui subsistemas mais simples.
    * **Feedback**:
        * Importante para que correções de rota, como mudanças em requisitos e mudanças de tecnologia, são implementadas o quanto antes.
        * "_Planeje-se para jogar fora partes de seu sistema, pois você fará isso._" (Frederick Brooks)
        * Por isso, feedbacks são importantes: ajudam a detectar o que deve ser jogado fora mais rapidamente.
### 2.3.2 Princípios
* **Humanidade**: software é uma atividade intensiva de uso de capital humano; portanto, gestão de pessoas é fundamental para o sucesso de projetos de software.
* **Economicidade**: software é uma atividade cara; portanto, software não é uma obra de arte, mas algo que deve gerar resultados econômicos.
* **Benefícios Mútuos**: "todo negócio deve ser bom para os dois lados".
* **Melhorias contínuas**: nenhum processo de desenvolvimento de software é perfeito; portanto, é mais seguro trabalhar com um sistema que vai sendo constantemente aprimorado.
* **Falhas acontecem**: falhas são esperadas no desenvolvimento de software, e **não** devem ser usadas para punir membros de um time.
* **Baby steps**: é importante é garantir melhorias contínuas, não importando que sejam pequenas, desde que na direção correta. 
* **Responsabilidade pessoal**: responsabilidade não pode ser transferida, sem que a outra parte a aceite. Desenvolvedores devem ter uma ideia clara de seu papel na equipe, e o XP defente que o engenheiro de software desenvolva uma _história_ (requisitos), e também deve ser responsável por testá-la e mantê-la.
### 2.3.3 Práticas sobre o Processo de Desenvolvimento
* Os times incluem pelo menos um **representante dos clientes**. Uma de suas responsabilidades é escrever **histórias de usuário**, que são requisitos escritas de maneira resumida, com duas ou três sentenças.
* As histórias normalmente possuem um título e uma breve descrição.
* Depois de escritas pelo representante, as histórias são estimadas pelos desenvolvedores.
* Frequentemente, são estimadas em **story points**, para dar uma ordem relativa entre as histórias. É comum utilizar uma escala de Fibonacci para definir a escala de possíveis story points.
* A implementação de histórias ocorre por **iterações**, as quais têm uma duração fixa e bem definida, que compõem os chamados **releases**, que são ciclos mais longos, com alguns meses de duração.
* A **velocidade** de um time é o número de story points que ele consegue implementar em uma iteração.
* Em resumo, para começar a usar XP, precisamos de:
    * Definir a duração de uma iteração.
    * Definir o número de iterações de uma release.
    * Um conjunto de histórias, escritas pelo representante dos clientes.
    * Estimativas para cada história, feitas pelos desenvolvedores.
    * Definir a velocidade do time, isto é, o número de story points que ele consegue implementar por iteração.
* Uma vez definido tudo acima, o cliente prioriza as histórias. Os desenvolvedores não opinam na ordem escolhida para as histórias.
* Deve-se respeitar a velocidade do time de desenvolvimento.  A tarefa de alocar histórias a iterações e releases é chamada de **planejamento de releases**. 
#### Perguntas frequentes
_(A seguinte sessão foi copiada diretamente do livro texto)_

* **Qual a duração ideal de uma iteração?** 
    * Difícil precisar, pois depende das características do time, da empresa contratante, da complexidade do sistema a ser desenvolvido, etc. Iterações curtas — por exemplo, de uma semana — propiciam feedback mais rápido. Porém, requerem um maior comprometimento dos clientes, pois toda semana um novo incremento de produto deve ser validado. Além disso, requerem que as histórias sejam mais simples. Por outro lado, iterações mais longas — por exemplo, de um mês — permitem que o time planeje e conclua as tarefas com mais tranquilidade. Porém, demora-se um pouco mais para receber feedback dos clientes. Esse feedback pode ser importante quando os requisitos são pouco claros. Por isso, uma escolha de compromisso seria algo como 2 ou 3 semanas. Outra alternativa recomendada consiste em experimentar, isto é, testar e avaliar diferentes durações, antes de decidir.

* **O que o representante dos clientes faz durante as iterações?** 
    * No início de uma release, cabe ao representante dos clientes escrever as histórias das iterações que farão parte dessa release. Depois, no final de cada iteração, cabe a ele validar e aprovar a implementação das histórias. Porém, durante as iterações, ele deve estar fisicamente disponível para tirar dúvidas do time. Veja que uma história é um documento muito resumido, logo é natural que surjam dúvidas durante a sua implementação. Por isso, o representante dos clientes deve estar sempre disponível para se reunir com os desenvolvedores, para tirar dúvidas e explicar detalhes relativos à implementação de histórias.

* **Como escolher o representante dos clientes?** 
    * Antes de mais nada, deve ser alguém que conheça o domínio do sistema e que tenha autoridade para priorizar histórias. Conforme detalhado a seguir, existem pelo menos três perfis de representante dos clientes:
        * Suponha o desenvolvimento interno de um sistema, isto é, o departamento de sistemas da empresa X está desenvolvendo um sistema para um outro departamento Y, da mesma empresa. Nesse caso, o representante dos clientes deve ser um funcionário do departamento Y.
        * Suponha que o time de desenvolvimento foi contratado para desenvolver um sistema para a empresa X. Ou seja, trata-se de um desenvolvimento terceirizado. Nesse caso, o representante do cliente deve ser um funcionário da empresa X, com pleno domínio da área do sistema e que vai ser um dos seus principais usuários, quando ele ficar pronto.
        * Suponha que o time de desenvolvimento de uma empresa X foi designado para fazer um sistema para um público externo à empresa. Por exemplo, um sistema como aquele usado neste capítulo, similar ao Stack Overflow. Logo, os clientes do sistema não são funcionários de X, mas sim clientes externos. Nesse caso, o representante dos clientes deve ser alguém da área de marketing, vendas ou negócios da empresa X. Em última instância, pode ser o dono da empresa. Em qualquer caso, a sugestão é que seja uma pessoa próxima do problema e o mais distante possível da solução. Por isso mesmo, deve-se evitar que ele seja um desenvolvedor ou um gerente de projeto. O tipo de representante dos clientes que mencionamos neste item é, às vezes, chamado de um user proxy.

* **Como definir a velocidade do time?** 
    * Não existe bala de prata para essa questão. Essa definição depende da experiência do time e de seus membros. Se eles já participaram de projetos semelhantes àquele que estão iniciando, certamente essa deve ser uma questão menos difícil. Caso contrário, tem-se que experimentar e ir calibrando a velocidade nas iterações seguintes.

* **Histórias podem incluir tarefas de instalação de infraestrutura de software?** 
    * Não, histórias são especificadas pelo representante dos clientes, que é um profissional leigo em Engenharia de Software. Portanto, ele não costuma ter conhecimento de infraestrutura de software. No entanto, uma história pode dar origem a uma tarefa como instalar e testar o banco de dados. Resumindo, histórias estão associadas a requisitos funcionais; para implementá-las criam-se tarefas, que podem estar associadas a requisitos funcionais, não-funcionais ou tarefas técnicas, como instalação de bancos de dados, servidores, frameworks, etc.

* **A história X depende da história Y, mas o representante dos clientes priorizou X antes de Y. O que devo fazer?** 
    * Por exemplo, suponha que no sistema de exemplo o representante dos clientes tenha alocado a história Postar Pergunta para a iteração 2 e a história Postar Resposta para a iteração 1. A pergunta então é a seguinte: o time deve respeitar essa alocação? Sim, pois a regra é clara: o representante dos clientes é a autoridade final quando se trata de definir a ordem de implementação das histórias. Logo, pode-se perguntar em seguida: como que vamos postar respostas, sem ter as perguntas? Para isso, basta implementar algumas perguntas fixas, que não possam ser modificadas pelos usuários. Na iteração 1, quando o cliente abrir o sistema, essas perguntas vão aparecer por default, talvez com um leiaute bem simples, e então o cliente vai poder usar o sistema apenas para responder essas perguntas fixas.

* **Quando um projeto XP termina?** 
    * Quando o representante dos clientes decide que as histórias já implementadas são suficientes e que não há mais nada de relevante que deva ser implementado.

### 2.3.4 Práticas de Programação
* O nome _Extreme Programming_ foi escolhido porque propõe um conjunto de práticas de programação inovadoras, que dá grande importância para tarefas de programação de produção de código.
* O método propôs um novo conjunto de práticas de programação que foram adotadas por outros métodos posteriormente:
* **Design Incremental**:
    * Deve se reservar tempo para definir o design do sistema qeu estã osendo desenvolvido, porém, com uma atividade contínua e incremental.
    * Momento ideal para pensar em _design_ é quando ele se revelar importante:
        * "Faça a coisa mais simples que possa funcionar"
        * "Você não vai precisar disso" (YAGNI: "_you aren't gonna need it_")
    * Somente é possível caso seja adotado em conjunto com as demais práticas XP, principalmente **refactoring**.
* **Pair Programming**:
    * Uma das práticas mais polêmicas: toda codificação deve ser realizada por dois desenvolvedores, sendo que um é o **líder** (_driver_), ou seja, quem de fato coda. O segundo é chamado de **navegador**, e o cabe a função de revisor e questionador do trabalho do líder.
* **Propriedade coletiva do código**:
    * Qualquer desenvolvedor pode codificar qualquer parte do código, seja para adicionar uma feature ou corrigir algum bug.
* **Testes Automatizados**:
    * Uma das práticas de maior sucesso: testes manuais é um processo custoso; portanto, XP propõe a implementação de programas (chamados de testes) para executar peqeunas unidades de um sistema, como métodos, e verificar se as saídas produzidas são aquelas esperadas.
* **Desenvolvimento Dirigido por Testes (TDD)**:
    * Implementa-se os testes de um método antes do código. Motivações:
        * Evitar que a escrita de testes nunca seja feita
        * Ao escrever um teste, o desenvolvedor se coloca no papel do cliente
* **Build Automatizado**:
    * Geração de uma versão de um sistema que seja executável e que possa ser colocada em produção.
* **Integração contínua**:
    * Desenvolvedores devem integrar seu código sempre, se possível, todos os dias.
### 2.3.5 Práticas de Gerenciamento de Projetos
* **Ambiente de Trabalho**:
    * Projeto deve ser desenvolvido com um time pequeno e deve-se evitar times fracionados, em que alguns devs trabalham apenas alguns dias da semana.
    * Desenvolvedores devem trabalhar em uma mesma sala, para facilitar comunicação e feedback.
    * Deve garantir jornadas de trabalho sustentáveis.
* **Contratos com Escopo Aberto**:
    * Ao contrário de um contrato de escopo fechado, o de escopo aberto possui o pagamento por hora trabalhada.
    * Contratos de escopo aberto são mais compatíveis com os métodos ágeis de uma maneira geral.
* **Métricas de processo**:
    * Recomenda-se o uso de duas métricas principais:
        * Número de bugs em produção (idealmente, poucos por ano)
        * Interfalo de tempo entre início do desenvolvimento e o momento em que o projeto começa a gerar seus primeiros resultados financeiros (que também deve ser pequeno, aproximadamente um ano).

## 2.4 Scrum
* Método ágil, iterativo e incremental para gerenciamento de projetos.
* Principais diferenças com XP:
    * XP é voltado exclusivamente para projetos de desenvolvimento de software.
    * Scrum é um método ágil para gerenciamento de projetos, que não necessariamente precisam ser projetos de software.
* Definições:
    * **Papéis**: Dono do produto (PO), Scrum Master, Desenvolvedor.
    * **Artefatos**: Backlog do Produto, Backlog do Sprint, Quadro Scrum, Gráfico de Burndown.
    * **Eventos:** Planejamento do Sprint, Sprint, Reuniões diárias, Revisão do Sprint, Retrospectiva.
### 2.4.1 Papéis
* Time scrum são formados por um PO, um Scrum Master e de 3 a 9 desenvolvedores
* **Product Owner**: representante dos clientes. Escreve histórias dos usuários.
* **Scrum Master**: especialista em Scrum do time, responsável por garantir que as regras do método estão sendo seguidas. Também é um facilitador dos trabalhos e removedor de impedimentos.
* Times **cross-funcionais**: multidisciplinares, e não deve depender de membros externos.
### 2.4.2 Principais Artefatos e Eventos
* **Backlog do Produto**:
    * lista de histórias, ordenada por prioridades. É dinâmico, sendo constantemente atualizado.
* **Sprint**:
    * Nome de uma iteração. Ao final de uma sprint, deve-se entregar ao cliente um produto com valor tangível para ocliente.
* **Planejamento do Sprint**:
    * Reunião na qual todo time se reúne para decidir as histórias que serão implementadas.
    * Dividida em duas partes:
        * 1ª: com o PO, onde sugere as histórias a serem implementadas.
        * 2ª: comandada pelos desenvolvedores, onde estimam e analisam as histórias.
* **Backlog do Sprint**:
    * Artefato gerado ao final do Planejamento do Sprint.
    * Lista de tarefas do sprint, bem como a duração das mesmas.
* Times de Scrum são **auto-organizáveis**.
* Para que uma história seja marcada como concluída, pode-se exigir a implementação de testes de unidade, bem como a revisão do código.
* **Gráfico de Burndown**:
    * A cada dia do sprint, esse gráfico mostra quantas horas são necessárias para se implementar as tarefas qeu ainda não estão concluídas.
### 2.4.3 Outros Eventos
* **Reuniões diárias** de 15 minutos, de pé.
* **Revisão do Sprint**:
    * Reunião param mostrar os resultados de um sprint. Todos os membros participam.
    * Todas as histórias devem ser aprovadas pelo PO.
* **Retrospectiva do Sprint**:
    * Última atividade de um Sprint.
    * Trata-se de uma reunião do time Scrum, com o objetivo de refletir sobre o sprint que está terminando, vendo o que pode ser melhorado no processo.
* Todos os evetnos do Scrum têm uma duração bem definida, chamada de **time-box**.
#### Perguntas frequentes
_(A seguinte sessão foi copiada diretamente do livro texto)_
 
* **O que significa a palavra Scrum?** 
    * O nome não é uma sigla, mas uma referência à reunião de jogadores realizada em uma partida de rugby para decidir quem vai ficar com a bola após uma infração involuntária.

* **O que é um squad?** 
    * Esse termo é um sinônimo para time ágil ou time Scrum. O nome foi popularizado pela Spotify. Assim como times Scrum, squads são pequenos, cross-funcionais e auto-organizáveis. É comum ainda usar o nome tribo para denotar um conjunto de squads.

* **O Dono do Produto pode ser um comitê?** 
    * Em outras palavras, pode existir mais de um Dono de Produto em um time Scrum? A resposta é não. Apenas um membro do time exerce essa função. O objetivo é evitar decisões por comitê, que tendem a gerar produtos lotados de funcionalidades, mas que foram implementadas apenas para atender a determinados membros do comitê. Porém, nada impede que o Dono do Produto faça a ponte entre o time e outros usuários com amplo domínio da área do produto que está sendo construído. Na verdade, essa é uma tarefa esperada de Donos de Produto, pois às vezes existem requisitos que são do domínio de apenas alguns colaboradores da organização. Cabe então ao Dono do Produto intermediar as conversas entre os desenvolvedores e tais usuários.

* **O Scrum Master deve exercer seu papel em tempo integral?** 
    * Idealmente, sim. Porém, em times maduros, que conhecem e praticam Scrum há bastante tempo, às vezes não é necessário ter um Scrum Master em tempo integral. Nesses casos, existem duas possibilidades: (1) permitir que o Scrum Master desempenhe esse papel em mais de um time Scrum; (2) alocar a responsabilidade de Scrum Master a um dos membros do time. No entanto, caso a segunda alternativa seja adotada, o Scrum Master não deve ser também o Dono do Produto. A razão é que uma das responsabilidades do Scrum Master é exatamente acompanhar e auxiliar o Dono do Produto em suas tarefas de escrever e priorizar histórias do usuário.

* **O Scrum Master precisa ter um diploma de nível superior em um curso da área de Computação?** 
    * Não, pois sua função envolve remover impedimentos e assegurar que o time esteja seguindo os princípios de Scrum. Portanto, ele não é um resolvedor de problemas técnicos, tais como bugs, uso correto de frameworks, implementação de funcionalidades, etc. Por outro lado, isso não impede que um desenvolvedor técnico, com um curso superior na área de Computação, assuma as funções de Scrum Master, como vimos na resposta anterior. Existem também certificações para Scrum Master, as quais podem ser requeridas por empresas que decidem adotar Scrum.

* **Além de histórias, quais outros itens podem fazer parte do Backlog do Produto?** 
    * Também podem ser cadastrados no Backlog do Produto itens como bugs — principalmente aqueles mais complexos e que demandam dias para serem resolvidos — e também melhorias em histórias já implementadas.

* **Existem gerentes quando se usa Scrum?** 
    * A resposta é sim! De fato, times Scrum são autônomos para implementar as histórias priorizadas pelo Dono do Produto. Porém, um projeto demanda diversas outras decisões que devem ser tomadas em um nível gerencial. Dentre essas decisões, podemos citar as seguintes:

        * Contratar e alocar membros para os times Scrum; ou seja, os desenvolvedores não têm autonomia para escolher em quais times eles vão trabalhar. Essa é uma decisão de mais alto nível e, portanto, tomada por gerentes.

        * Decidir os objetivos e responsabilidades de cada time, incluindo o sistema — ou parte de um sistema — que o time irá desenvolver usando Scrum. Por exemplo, um time não decide, por conta própria, que a organização precisa de um novo sistema de contabilidade e então começa a desenvolvê-lo. Essa é uma decisão estratégica, que cabe aos gerentes e executivos da organização.

        * Gerenciar e administrar questões de recursos humanos, incluindo contratações de novos funcionários, desligamentos de funcionários, promoções, transferências, treinamentos, etc.

        * Avaliar se os resultados produzidos pelos times Scrum estão, de fato, gerando benefícios e valor para a organização.

## 2.5 Kanban

## 2.6 Quando não usar métodos ágeis?





