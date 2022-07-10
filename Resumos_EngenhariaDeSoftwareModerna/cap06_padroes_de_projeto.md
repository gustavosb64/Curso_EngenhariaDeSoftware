# Engenharia de Software Moderna
# Capítulo 6: Padrões de Projeto

## 6.1 Introdução
* Padrões de projeto visam a criação de projetos de software flexíveis e extensíveis.
* Devemos projetar um sistema pensando em mudanças que inevitavelmente vão ocorrer: **design for change**.
* 23 padrões de projeto, separados em três categorias:
    * **Criacionais**: padrões que propõem soluções flexíveis para **criação de objetos**. 
        * Abstract Factory (6.2), Factory Method, Singleton (6.3), Builder (6.12) e Prototype.
    * **Estruturais**: padrões que propõem soluções flexíveis para **composição de classes e objetos**. 
        * Proxy (6.4), Adapter (6.5), Facade (6.6), Decorator (6.7), Bridge, Composite e Flyweight.
    * **Comportamentais**: padrões que propõem soluções flexíveis para **interação e divisão de responsabilidades** entre classes e objetos. 
        * Strategy (6.8), Observer (6.9), Template Method (6.10), Visitor (6.11), Chain of Responsibility, Command, Interpreter, Iterator (6.12), Mediator, Memento e State.

## 6.2 Fábrica
* **Oferece um método para centralizar a criação de um tipo de objeto.**
* Possui algumas variações, porém, usaremos um método estático (**Método Fábrica Estático**) que:
    * apenas cria e retorna objetos de uma determinada classe;
    * também oculta o tipo desses objetos por trás de uma interface
* **Princípio: Prefira interfaces a Classes**.
* Funciona como "aspirador" de métodos ```new```: todas as chamadas ```new``` migram para uma única chamada.
* **Fábrica Abstrata**:
    * Oferece uma interface ou classe abstrata para criação de uma família de objetos relacionados.

## 6.3 Singleton
* **Garante que uma classe possui, no máximo, uma instância e oferece um ponto único de acesso a ela.**
* Deve ser usado para modelar recursos que, conceitualmente, devem possuir no máximo uma instância durante a execução do programa.
* Críticas:
    * Pode ser usado para camuflar a criação de variáveis e estruturas de dados globais.
    * Um uso abusivo do padrão ocorre quando ele é adotado como um artifício para criação de variáveis globais.
    * Eles tornam o teste automático de métodos mais complicado devido ao "estado global" da instância utilizada.

## 6.4 Proxy
* **Funciona como um intermediário que controla o acesso a um objeto base.**
* Defende a inserção de um objeto intermediário, chamado _proxy_, entre um objeto base e seus clientes, de forma qeu os clientes não terão mais uam referência direta para o objeto base, mas sim para o proxy.
* O proxy deve implementar as mesmas interfaces do objeto base.
* O objetivo é mediar o acesso a um objeto base, agregando-lhe funcionalidades, sem qeu ele tome conhecimento disso.
* Além de ajudar na implementação de caches, proxies podem ser usados para implementar outros requisitos não-funcionais:
    * Comunicação com um cliente remoto, para encapsular protocolos e detalhse de compunicação (**stubs**)
    * Alocação de memória por demanda para objetos que consomem muita memória.
    * Controlar o acesso de diversos clientes a um objeto base (por exemplo, exigindo autenticação).
     
## 6.5 Adaptador (Wrapper)
* **Converte a interface de uma classe para outra interface esperada pelos clientes. Permite que classes trabalhem juntas, o que não seria possível devido à incompatibilidade de suas interfaces.**
* É recomendado seu uso quando temos que converter a interface de uma classe para outra interface, esperada pelos seus clientes.
 
## 6.6 Fachada 
* **Oferece uma interface unificada e de alto nível que torna mais fácil o uso de um sistema.**
* Uma classe que oferece uma interface mais simples para um sistema.
* O objetivo é evitar que os usuários tenham que conhecer classes internas desse sistema; em vez disso, eles precisam interagir apenas com a classe de Fachada, tendo as classes internas encapsuladas por trás da Fachada.
 
## 6.7 Decorador 
* **Permite adicionar dinamicamente novas funcionalidades a uma classe.**
* Alternativa à herança quando se precisa adicionar novas funcionalidades em uma classe base.
* Em vez de herança, usa-se composição para adicionar tais funcionalidades dinamicamente nas classes base.
* **Princípio: "Prefira Composição a Herança"**.
 
## 6.8 Strategy 
* **Permite parametrizar os algoritmos usados por uma classe.**
* Parametriza os algoritmos usados por uma classe, preescrevendo como encapsular uma família de algoritmos e como torná-los intercambiáveis.
* Seu uso é recomendado quando uma classe é usuária de um certo algoritmo (de ordenação, no nosso exemplo). 
 
## 6.9 Observador 
* **Permite que um objeto avise outros objetos de que seu estado mudou.**
* Define como implementar uma relação do tipo um-para-muitos entre objetos sujetio e observadores. Quando o estado de um sujeito muda, seus observadores devem ser notificados.
* Vantagens:
    * Não acopla os sujeitos a seus observadores.
    * Uma vez implementado, disponibiliza um mecanismo de notificação qeu pode ser reusado por diferentes pares de sujeito-observador.
 
## 6.10 Template method 
* **Define o esqueleto de um algoritmo em uma classe base e delega a implementação de alguns passos para subclasses.**
* Permite que subclasses customizem um algoritmo, mas sem mudar sua estrutura geral implementada na base
* Permitem que "código antigo" chame "código novo": **inversão de controle**, fundamental para a implementação de **frameworks** (aplicações semi-prontas para serem customizadas por seus clientes).
 
## 6.11 Visitor
* **Torna uma estrutura de dados aberta a extensões, isto é, permite adicionar uma função em cada elemento de uma estrutura de dados, mas sem alterar o código de tais elementos.**
* Define como "adicionar" uma operação em uma família de objetos, sem que seja preciso modificar as classes dos mesmos.
* Visitors facilitam a adição de um método em uma hierarquia de classes, congregando operações relacionadas.
* Desvantagem:
    * podem forçar uma quebra no encapsulamento das classes que serão visitadas.
     
## 6.12 Outros Padrões de Projeto
* **Iterador**:
    * Oferece uma interface padronizada para caminhar em estruturas de dados.
* **Builder**:
    * Facilita a construção de objetos complexos com vários atributos, sendo alguns deles opcionais.

## 6.13 Quando não se utilizar padrões de projeto?
* O uso de padrões tem um custo. Exemplos:
    * Fábrica demanda a implementação de pelo menos mais uma classe no sistema
    * Strategy requer a criação de uam classe abstrata e mais uam classe para cada algoritmo
* Deve-se atentar para a quando os padrões irão fornecer ganhos em **flexibilidade** e **extensibilidade**.
* Uso exagerado de padrões de projeto: **paternite**.
