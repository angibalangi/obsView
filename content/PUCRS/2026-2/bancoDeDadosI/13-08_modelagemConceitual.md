---
title: Modelagem Conceitual (13/08)
---

Professor: Denise Bandeira
Local: Prédio 32, sala 516
Horário: JK (17:30 -> 19:00)
## Descrição da Aula:
Iniciamos a aula entendendo o porquê precisamos de uma estrutura de banco de dados, e como ela seria planejada. Nesse sentido, a modelagem conceitual é a maneira pela qual conseguimos construir um banco de dados visível e legível, antes de transformá-lo em algo concreto. Para construir um diagrama de modelagem conceitual, porém, existem algumas regras a serem seguidas para melhorar a legibilidade:
- Diagrama 1: Estrutura básica da modelagem conceitual:
![modelagemBancoDeDadosGlobal.dark](Excalidraw/modelagemBancoDeDadosGlobal.dark.svg)

Entendemos que a modelagem conceitual é construída por entidades compostas por atributos, que são conectadas por relacionamentos. As entidades, nesse sentido, seriam as tabelas nas quais as tuplas e os atributos são estruturados. Os relacionamentos, no contexto da modelagem conceitual, aparecem como verbos que informam o tipo de relação entre duas tabelas, e eles são acompanhados de valores (0, 1, N) que aparecem próximos às entidades conectadas. Finalmente, os atributos são os valores presentes nas tabelas que não se conectam com outras, esses podendo ser pintados (Atributo Identificador/Chave primária) ou não.
Os valores mencionados determinam quantos de uma entidade existem em relação a outra; por exemplo, no diagrama apresentado, uma (1) disciplina possui várias (N) turmas. Essas podem também aparecer de forma mais complexa, como (0,1), onde o primeiro valor determina o mínimo e o segundo, o máximo.
Finalmente, as relações podem também ser entidades. Nesse caso, elas deixariam de aparecer como verbos, e poderíam conter seus próprios atributos. Esse tipo de representação é util quando existem conexões mais complexas.
## Aspectos Importantes:
- Os termos explorados na aula anterior somente se aplicam quando falando dos modelos relacionais. Seria incorreto, por exemplo, chamar um atributo identificador de chave primária na modelagem conceitual;
- Ainda na aula passada, o processo de construção de tabelas é chamado de modelagem lógica;
- A modelagem conceitual aparece quando fazendo a análise de requisitos de dados, e seu final acaba sendo o modelo físico do SQL. No contexto da análise de requisitos de sistema, utilizamos modelagens UML;