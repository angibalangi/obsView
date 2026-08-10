---
title: Sistemas de Armazenamento de Dados (06/08)
---
Professor: Denise Bandeira
Local: Prédio 32, sala 516
Horário: JK (17:30 -> 19:00)
## Descrição da Aula:
Foi uma aula relativamente leve, onde observamos diferentes modelos de armazenamento de dados, além de finalizar os pensamentos iniciados na aula passada. Começamos falando um pouco sobre os testes de integridade anteriormente explorados, e focamos no ramo do controle de concorrência. Basicamente, quando dois usuários tentam utilizar e mudar valores de um BD ao mesmo tempo, aquele que inicia a interação primeiro que faz as alterações desejadas, enquanto o outro é mantido em espera. Quando o processo do primeiro usuário é concluído, os dados são atualizados para o segundo, e este então faz a ação desejada. Isso impede que os sistemas estabelecidos sejam burlados, e mantém os dados armazenados coerentes com a realidade.
Depois disso, exploramos um pouco os diferentes jeitos de escrever código. Os dois meios relevantes a essa disciplina são o procedural, utilizado por linguagens como Java, e declarativo, utilizado pelo SQL. 
Mais importante que isso, porém, é a organização de um banco de dados. Na maioria dos casos, essa é relacional, mas existem outras diversas maneiras de armazenar dados.
- Relacional: dados armazenados em listas e tabelas. Crucialmente, não são permitidos vetores nessa estrutura;
- Hierárquico: também chamado de árvore (mesmo que pareça mais uma árvore invertida), informações são armazenadas em cadeia;
- Rede: parecido com o modelo hierárquico, sua principal diferença é a possibilidade de uma informação ter mais de um "parente", ou seja, dado de que este é dependente;
- Não relacional: parecido com o relacional, com a diferença de que vetores, nesse caso, são permitidos. Normalmente, só substitui o relacional quando é necessária uma flexibiliade dos dados;
- XMC: brevemente mencionado, não parece ser muito relevante.
## Aspectos Importantes:
- Modelos procedurais essencialmente perguntam ao programador "como?", enquanto os declarativos focam no "o que?".