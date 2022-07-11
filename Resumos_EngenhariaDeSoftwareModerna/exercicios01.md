# Engenharia de Software Moderna
# Capítulo 1: Introdução

## Exercícios

#### 1. Segundo Frederick Brooks, desenvolvimento de software enfrenta dificuldades essenciais (para as quais não há bala de prata. e acidentais (para as quais existe uma solução melhor). Dê um exemplo de dificuldade acidental que já tenha experimentado ao desenvolver programas, mesmo que pequenos. Sugestão: elas podem estar relacionadas a ferramentas que tenha usado, como compiladores, IDEs, bancos de dados, sistemas operacionais, etc.
* Dificuldades acidentais se referem a problemas objetivos associados a problemas com tecnologias, por exemplo. Já enfrentei diversas dificuldas já enquanto desenvolvia programas. 
 
#### 2. Diferencie requisitos funcionais de requisitos não-funcionais.
* **Requisitos funcionais** são requisitos objetivos mais palpáveis referentes à funcionalidades do sistema, como funcionalidades de cadastro, características de uma página principal, etc. Já **requisitos não-funcionais** se referem a requisitos mais abstratos e intangíveis, como a disponibilidade do sistema e latência mínima.
 
#### 3. Explique por que testes podem ser considerados tanto uma atividade de verificação como de validação de software. Qual tipo de teste é mais adequado se o objetivo for verificação? Qual tipo de teste é mais adequado se o objetivo for validar um sistema de software?
* Para testarmos a _verificação_ de um sistema, devemos responder à seguinte pergunta: "_O sistema está sendo implementado corretamente?_" Os testes de verificação testam métodos de maneira mais direta, sem o envolvimento do cliente, para que os desenvolvedores chequem se estão de acordo com os requisitos.
* Já a _validação_, respondemos: "_O sistema que está sendo implementado é o sistema correto?_" Para isso, precisamos que o cliente valide o sistema criado, então os testes precisam avaliar as funcionalidades e precisam ser mais acessíveis do ponto de vista do cliente, 
 
#### 4. Por que testes não conseguem provar a _ausência_ de bugs?
* Bugs são defeitos que ocorrem durante a implementação do programa, onde determinados métodos e funcionalidades possuem resultados inesperados não previsto pelos desenvolvedores. Embora testes possam detectar e previnir diversos bugs, não é possível provar que algum bug que não foi pensado e que não tenha se manifestado até o momento possa estar presente no sistema.

#### 6. Se considerarmos o contexto histórico, por que foi natural que os primeiros processos de desenvolvimento de software tivessem características sequenciais e fossem baseados em planejamento e documentação detalhados?
* Na época, o processo de desenvolvimento de software foi encarado como o desenvolvimento de outros produtos da Engenharia, que possuem características mais imutáveis. Logo, era natural que as primeiras tentativas de sistematização de desenvolvimento lançassem mão de abordagens convenientes a esse tipo de produto.
 
#### 8. _Refactoring_ é uma transformação de código que preserva comportamento. Qual o significado da expressão preservar comportamento? Na prática, qual restrição ela impõe a uma operação de refactoring?
* Refactoring (ou refatoração) significa reestruturar o código sem mudar suas funcionalidades. Normalmente, se reescreve o código para deixá-lo mais claro ou limpo, por exemplo, ou adequar a novas tecnologias mais convenientes que surgiram, mas sem alterar suas funcionalidades, de maneira que o cliente não perceba nenhuma diferença funcional no programa.
