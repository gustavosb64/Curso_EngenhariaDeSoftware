# Engenharia de Software Moderna -> Capítulo 1: Introdução

## 1.1 Definições, Contexto e História
* **Engenharia de Software**: área que trata da aplicação de abordagens sitemáticas, disciplinadas e quantificáveis para desenvolver, operar, manter e evoluir software. Ou seja, propor e aplicar princípios de engenharia na construção de software.
* No início, softwares eram mais simples, com caráter mais científico e usado por poucos. Conforme a computação foi evoluindo surgiu o desafio de que novas aplicações passavam a ser mais demandadas.
* **Conferência da OTAN (1968)**:
    * Conferência com cerca de 50 cientistas da computação para chamar atenção para um "problema crucial do uso de computadores, o chamado software". Foi produzido um relatório com mais de 130 páginas acerca do problema.
    * Esta conferência é considerada o marco histórico de criação da Engenharia de Software.
* Software não deve ser construído em fases sequenciais.
* Já existem padrões que podem ser usados de maneira genérica para diferentes tipos de problemas.
* Software também envelhece: precisa de manutenção.
### Não existe bala de prata
* O desenvolvimento de software é diferente de qualuqer outro produto de Engenharia.
* Frederick Brooks: **não existe bala de prata**. 
    * Existem dois tipos de dificuldades em desenvolvimento de software: dificuldades **essenciais** e **acidentais**
* **Dificuldades essenciais**
    * _Complexidade_: software é uma das construções mais desafiadoras e complexas que existe.
    * _Conformidade_: software tem que se adaptar ao seu ambiente, que muda a todo momento no mundo moderno.
    * _Facilidade de mudanças_: software deve evoluir sempre, inforporando novas funcionalidades. O quão mais bem sucedido é um software, mais mudanças.
    * _Invisiblidade_: software é abstrato, portanto é difício visualizar e estimar o esforço de construir um sistema.
* **Dificuldades acidentais**
    * Normalmente associadas a questões técnicas. Exemplo: problemas de compilação, IDE com muitos bugs, etc.
    * Não são uma característica inerente dos sistemas mencionados.

## 1.2 O que se estuda em Engenharia de Software?
* **12 áreas de conhecimento em Engenharia de Software** (SWEBOK):
    * Engenharia de Requisitos
    * Projeto de Software
    * Construção de Software
    * Testes de Software
    * Manutenção de Software
    * Gerência de Configuração
    * Gerência de Projetos
    * Processos de Software
    * Modelos de Software
    * Qualidade de Software
    * Prática Profissional
    * Aspectos Econômicos
    * Qualidade de Software
    * _Áreas de fronteira_: Fundamentos da computação, Fundamentos da Matemática e Fundamentos da Engenharia
### 1.2.1 Engenharia de Requisitos
* **Requisitos funcionais**: definem o que um sistema deve fazer
* **Requisitos não-funcionais**: definem como um sistema deve operar. Exemplos: desempenho, disponibilidade, segurança, etc.

### 1.2.2 Projeto de Software
* **Interfaces providas** 
    * Serviços que uma unidade de código torna público para uso pelo resto do sistema.
* **Interfaces requeridas** 
    * Interfaces das quais uma unidade de código depende para funcionar.
    * Chamadas de **dependências**
* **Projeto Arquitetal** 
    * Quando possuem um nível mais alto e apresentam maior granulidade (um pacote, por exemplo).
    * **Arquitetura de Software** lida com a organização de um sistema em um nível de abstração mais alto do que aquele qeu envolve classes ou construções semelhantes
### 1.2.3 Construção de Software
* Se trata da implementação. 
### 1.2.4 Testes de Software
* Tipos:
    * **Testes de unidade**: quando se testa uma parcela pequena do código
    * **Testes de integração**: quando se testa uma unidade com maior granulidade, como um conjunto de classes
    * **Testes de usabilidade**: quando se testa a usabilidade da interface do sistema.
* Testes podem ser usados tanto para verificação como para validação de sistemas.
    * _Verificação_: tem como objetivo garantir que um sistema atende à sua especificação
        * "Estamos implementando o sistema corretamente?" (De acordo com os requisitos)
    * _Validação_: tem como objetivo garantir que um sistema atende às necessidades de seus clientes
        * "Estamos implementando o sistema correto?" (Aquele que o cliente realmente quer)
    * Pode ocorrer de a especificação de um sistema não expressar as necessidades de sesu clientes.
* Código **defeituoso** é aquele que não está de acordo com a sua especificação. Se o código for executado e de fato levar o programa a apresentar um resultado incorreto, dizemos que ocorreu uma **falha**.
### 1.2.5 Manutenção e Evolução de Software
* **Tipos de Manutenção**:
    * **Manutenção corretiva**:
        * Tem como objetivo corrigir os bugs reportados.
    * **Manutenção preventiva**:
        * Tem como objetivo corrigir os bugs _latentes_ no código, que ainda não causaram falhas juntos aos usuários do sistema.
    * **Manutenção adaptativa**:
        * Tem como objetivo adaptar um sistema a uma mudança em seu ambiente, como novas tecnologias, legislação, etc.
        * _Refactorings_.
    * **Manutenção evolutiva**:
        * Tem como objetivo incluir nova funcionalidade ou introduzir um aperfeiçoamento importante em funcionalidades existentes.
* **Sistemas legados**
    * Sistemas antigos, baseados em linguagens, SOs e bancos de dados tecnologicamente ultrapassados.
    * Manutenção mais custosa e trabalhosa.
### 1.2.6 Gerência de Configuração
* Uso de controle de versões é algo fundamental.
* Gerência de configuração é mais do que usar controle de versões: trata-se de um conjunto de políticas para gerenciar as diversas versões de um sistema. Exemplo: identificar as releases de um software.
### 1.2.7 Gerência de Projetos
* **Stakeholder**: todas as partes interessadas no desenvolvimento de um software. Podem ser, além dos desenvolvedores e dos clientes, empresas subcontratadas, fornecesdores de qualquer natureza, etc.
* **Lei de Brooks**: "A inclusão de novos desenvolvedores em um projeto que está atrasado contribui para torná-lo ainda mais atrasado" 
* _Design vs Project_
### 1.2.8 Processos de Desenvolvimento de Software
* Dois grandes tipos de processos: **Cascata** e **Ágeis**
* **Cascata** (_Waterfall_)
    * Também chamados por **processos dirigidos por planejamento**
    * Foram os primeiros a serem propostos.
    * Inspirados nos procesos de desenvolvimento de outras Engenharias no geral.
    * Foram muito usados até a década de 90.
    * Propõem que a construção de um sistema deve ser feita em etapas **sequenciais**.
    * Seque o seguinte pipeline:
        * Levantamento de requisitos
        * Análise
        * Projeto
        * Codificação
        * Testes
        * Implantantação
    * Muito criticados:
        * Sistema muito enrigecido, atrasa com frequência, problemas recorrentes. 
        * Difícil lidar com falhas
* **Ágeis** (ou _Iterativos_ ou _Incrementais_)
    * Um sistema deve ser construído de maneira incremental e iterativa.
    * Pequenos incrementos de funcionalidades são produzidos, em intervalos de cerca de um mês e, logo em seguida, validados pelos usuários.
    * Vários métodos: _XP_, _Scrum_, _Kanban_, e _Lean Development_.
### 1.2.9 Modelos de Software
* Um modelo oferece uma representação mais alto nível de um sistema.
* Podem ser escritos:
    * antes do código: **Engenharia Avante** (_Forward Engineering_).
    * depois do código: **Engenharia Reversa** (_Reverse Engineering_).
* Normalmente baseados em notações gráficas, como o **UML**.
### 1.2.10 Qualidade de Software
* Bertrand Meyer: qualidade de software pode ser:
    * **Qualidade externa**: considera fatores que podem ser aferidos sem analisar o código, como, por exemplo:
        * Correção: o software atende à sua especificação?
        * Robustez: o software continua funcionando mesmo quando ocorrem eventos anormais?
        * Eficiência: o software faz bom uso de recursos computacionais?
    * **Qualidade interna**: considera propriedades e características relacionadas com a implementação de um sistema. Só pode ser avaliada por um eespecialista em Engenharia de Software.
### 1.2.11 Prática Profissional
* **Responsabilidade ética** dos profissionais de software.
* [sem muita informação relevante]
### 1.2.12 Aspectos Econômicos
* [sem muita informação relevante]

## 1.3 Classificação de Sistemas de Software
* Três tipos de software:
    * **Sistemas A** (_Acute_):
        * Qualquer falha pode causar um imenso prejuízo.
        * Sistemas críticos.
    * **Sistemas B** (_Business_):
        * Variadas aplicações corporativas, sistemas Web, redes sociais, sistemas de busca.
    * **Sistemas C** (_Casuais_):
        * Não sofrem pressão para terem níveis altos de qualidade. Podem ter alguns bugs, que não comprometem seu fundamentalmente seu funcionamento.
        * Maior risco é **over-engineering**, ou seja, o uso de recursos mais sofisticados do que o necessário.
