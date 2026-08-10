---
title: Aula Introdutória (04/08)
---
Professor: Denise Bandeira
Local: Prédio 32, sala 516
Horário: JK (17:30 -> 19:00)
## Descrição da Aula:
Mesmo sendo uma aula introdutória, ela foi densa em conteúdo. Fomos introduzidos ao funcionamento de bancos de dados, e suas vantagens acima de quando programando sem eles. O SGBD (Sistema de Gerência de Banco de Dados) parece ser um foco da disciplina, pois é o sistema pelo qual interagimos com o banco de dados. Alguns conceitos futuros foram mencionados, como a linguagem SQL (Structured Query Language) que utilizaremos pelo fim do semestre ou a partição de um armazenamento para diferentes funções.
O foco da aula, porém, foi o funcionamentos do SGBD, e os papeis do banco de dados (*BD*) e do dicionário de dados (*DD*) que o compõem. O *BD* seria a informação pura, enquanto o *DD* seria o guia para que essa informação seja extraída corretamente. Além disso, o *DD* também serve para verificar a integridade dos dados inseridos no sistema; por exemplo, uma data de nascimento não pode ser após a data de hoje, ou um CPF não pode ser repetido para mais de uma pessoa. "Verificar a integridade", nesse sentido, seria impedir que o *BD* fique incorreto, principalmente servindo para evitar equívocos de digitação ou tentativas de burlar um sistema.
- Diagrama 1 - Um sistema que não utiliza um *BD*:
![diagramaBD1.dark](Excalidraw/diagramaBD1.dark.svg)
- Diagrama 2 - Um sistema que utiliza um *BD*:
![diagramaBD2.dark](Excalidraw/diagramaBD2.dark.svg)
- Diagrama 3 - O fucnionamento de um SGBD:
![diagramaSGBD1.dark](Excalidraw/diagramaSGBD1.dark.svg)
## Aspectos Importantes:
- Cargos que envolvem essa disciplina incluem Projetista de BD e Administrador de BD;
- SGBD funciona como um tipo de "middleman" entre o usuário e o banco de dados;
- Dicionário de dados protege o banco de dados de se tornar inválido, e forma uma barreira entre o input e o *BD*.