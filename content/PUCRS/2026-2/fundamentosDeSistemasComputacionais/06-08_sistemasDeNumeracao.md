---
title: Sistemas de Numeração (06/08)
---
Professor: Iaçanã Ianiski Weber
Local: Prédio 32, sala 508
Horário: LM (19:15 -> 20:45)
## Descrição da Aula:
Essa aula foi uma revisão direta do conteúdo já visto na disciplina de Introdução a Computação. Começamos a aula relembrando de conceitos básicos, como as bases, que definem quantos numerais estão presentes em cada sistema de numeração. Nesse tópico, revimos também sistemas de numeração posicionais (Arábico) e não posicionais (Romano), os modelos de caracteres aceitos pelo computador, como ASCII, composto por 1 byte (8 bits), ou Unicode, composto por 32 bits.
O foco da aula foi na estrutura dos diferentes sistemas de numeração. Primeiramente, entendemos que os principais meios alternativos de numeração são o Binário e o Hexadecimal. Vimos também como transformar números de um sistema a outro, como a utilização de quatro dígitos do binário para passar para hexadecimal. Encerramos a aula revisando os três meios de representar números negativos no sistema binário: Sinal-magnitude, complemento e complemento de dois.
- Sinal-magnitude: O primeiro dígito de um número binário determina seu sinal, 0 sendo positivo e 1 negativo. Apesar de parecer intuitivo, a desvantagem desse sistema é a existência de dois zeros, 1000 e 0000, e a soma e subtração tradicionais não funcionando;
- Complemento: O inverso de um número binário é o seu equivalente negativo (0001 vira 1110). Esse modo resolve a soma que não funcionava anteriormente e mantém a ideia do sinal magnitude, mas ainda existem dois zeros, 1111 e 0000;
- Complemento de dois: Igual ao complemento, exceto que 1111 equivale a -1 ao invés de 0 (e todos os negativos viram o seu anterior depois disso). Isso resolve a maioria dos problemas existentes com os soutros sistemas, além de permitir um número a mais no lado negativo, e, por isso, é o modo preferido na modernidade.
## Aspectos Importantes: 
- 0x10 = Base 16 (Hexadecimal);
- 0b10 = Base 2 (Binário);
- Quando transformando números no sistema do complemento de dois ao decimal, a lógica é a mesma, mas, se presente, o primeiro dígito é subtraído ao invés de adicionado.