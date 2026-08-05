---
title: Aula Introdutória (04/07)
---
Professor: Iaçanã Ianiski Weber
Local: Prédio 32, sala 508
Horário: LM (19:15 -> 20:45)
## Descrição da Aula:
Foi uma aula extensa, mesmo ainda sendo introdutória. Foram introduzidos diversos conceitos novos que não foram muito explorados, mas imagino que eles sejam no futuro.
Primeiro, vimos uma pirâmide que mostrava os níveis de abstração que temos quando utilizamos um programa/aplicação, e exploramos um pouco aspectos como a ISA (Instruction Set Architecture), que define certos aspectos de como um programa é desenvolvido. Passamos rapidamente por modos de desenvolvimento, e suas diferenças quando o tempo passava, mas o maior foco da aula foi no hardware de chips, e os desafios que ele traz.
A Lei de Moore propõe que, a cada dois anos, a quantidade de transistores em um processador duplicaria. Embora tenha sido verdadeira por muitos anos, atualmente essa ideia se torna estagnada. Exploramos um pouco o porquê disso, com fenômenos quânticos acontecendo quando transistores se tornam cada vez menores, mas tambem entendemos que a duplicação de transistores não equivaleria, quando em escalas maiores, ao dobro do poder computacional, uma ideia proposta por Dennard. Isso resulta na criação de processadores de *dual core*, que aumentam a quantidade de processadores ao invés de tentar maximizar o potencial de um.
Com avanços tecnológicos, a ideia de múltiplos cores resolvendo o problema proposto por Dennard também se torna obsoleta, pois muitos processamentos sequenciais não podem ser dividos entre os diferentes núcleos (Lei de Amdahl). Exploramos, nesse tópico, um pouco sobre o paralelismo e a microarquitetura, que dividem ações em diferentes passos para conseguir concluí-las com eficiência.
- Diagrama 1 - Níveis de abstração na computação:
[[Excalidraw/niveisDeAbstracaoSWHW.dark.svg]]
- Diagrama 2 - Funcionamento de processador Multi Thread:
![multiThreadArquitetura.dark](Excalidraw/multiThreadArquitetura.dark.svg)
## Aspectos Importantes: 
- Pouquíssimas são as companhias que conseguem fabricar processadores modernos devido ao desafio trazido pelo tamanho quântico dos transistores. Um exemplo de uma dessas fábricas é a TSMC;
- Além do desafio intrínsico da prática, a fabricação desses processadores é dificultada por embargos econômicos e coisas do gênero;
- Diferentes tipos de memória no computador tem diferentes tempos de resposta. Por exemplo, a memória Cache poderia ser comparada ao tempo de cruzar a PUCRS, enquanto a memória do Disco, ao tempo de viajar a Plutão;
- Chamamos o funcionamento em cores trazido pela microarquitetura de pipeline, se assemelhando a uma linha de produção;
- Em computadores antigos, fenômenos físicos como raios cósmicos poderiam causar alterações em máquinas. Atualmente, a grande maioria dos processadores vêm com sistemas de correção no caso de um desses eventos.