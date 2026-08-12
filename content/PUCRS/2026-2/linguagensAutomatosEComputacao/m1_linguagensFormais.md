---
title: Conceitos Básicos sobre Linguagens Formais (M1)
---
## Descrição do Módulo:
O foco do módulo é na criação e descrição de linguagens formais, essas sendo importantes por construírem os compiladores usados pelas principais linguagens de programação. Existe quase um prefácio, que explica o nome da disciplina, com "linguagens" representando as linguagens formais estudadas, e "autômatos" destacando as estruturas matemáticas que permitem a programação.
Iniciamos o módulo destacando as diferenças entre as linguagens naturais (como o português) e as artificiais (como o Java), um processo muito similar ao feito na disciplina de lógica. Como naquela aula, diferenciamos a noção sintática da língua de sua semântica, e focamos na primeira. Usado de exemplo é a linguagem Java, que serve para traduzir a lógica algorítmica que desejamos executar com a máquina de uma maneira que seja legível para o computador. Para fazer isso, a linguagem estabelece certas regras a serem seguidas, que determinam a forma da programação com a qual estamos familiares.
Vimos também uma linha do tempo, que destaca duas figuras como marcantes no desenvolvimento das máquinas como às conhecemos hoje: Turing, criador da Máquina de Turing, que estabeleceu uma base para os computadores antes mesmo deles existirem; e Chomsky, que, em seu livro "Estruturas Sintáticas", cria a teoria das linguagens formais, permitindo que a programação exista de uma maneira acessível ao humano. Seguindo a lógica de Chomsky, é possível parsar a principal diferença entre as linguagens de programação das demais: a falta de ambiguidade, uma necessidade para máquinas puramente lógicas.
Finalmente, seguimos para um entendimento concreto do funcionamento das linguagens formais, observando diversas características da sua composição. Abaixo estão as principais:
- Alfabeto: Representado pelo símbolo $\Sigma$, o alfabeto é um conjunto finito e não vazio que contém todos os símbolos disponíveis para a utilização em um contexto. Por exemplo, a representação do alfabeto binário seria:
$$
\Sigma = \{0, 1\}
$$
- Palavra: A palavra consiste numa sequência finita e não vazia de símbolos que se encaixa a um determinado alfabeto. Por exemplo, no binário, $10010$ seria uma palavra válida, enquanto "olá" não seria.
- Palavra vazia: Representada pelo símbolo $\varepsilon$, uma palavra vazia é como uma palavra que não é constituida de nenhum símbolo. Essa palavra é especial pois ela pode ser construída em qualquer alfabeto.
- Comprimento da palavra: representado por |palavra|, o comprimento é um valor numérico dado a uma palavra, determinado pelo número de símbolos (tamanho) dela. Uma operação possível com essa propriedade acontece quando um símbolo subscrito aparece ao final da representação. Nesse caso, o valor do comprimento será a quantidade de símbolos equivalentes ao valor subscrito:
$$
|1000101|_0 = 4
$$
- Potências de Alfabeto: Aparecem como um número superscrito no topo do símbolo $\Sigma$  e determinam um conjunto com todas as palavras possíveis com o número de símbolos especificado. O item superscrito também pode aparecer como um * (todas as palavras possíveis) ou ⁺ (todas as palavras menos a vazia). Abaixo, um exemplo utilizando o alfabeto binário:
$$
\Sigma² = \{00, 01,10,11\}
$$
- Concactenação de Palavras: Aparecem como um número superscrito em uma palavra ou símbolo, determinando quantas vezes aquele componente é imediatamente repetido:
$$
(0101)² = 01010101
$$
- Prefixos e Sufixos: São, respectivamente, todos os símbolos que aparecem posicionalmente "antes" ou "depois". Os prefixos e sufixos são expressos em conjuntos, sempre contendo a palavra vazia e a palavra original:
$$
\text{Prefixos de } abcd = \{\varepsilon, a,ab,abc,abcd\}
$$
$$
\text{Sufixos de }abcd = \{\varepsilon, d,cd,bcd,abcd\}
$$
- Linguagem: um conjunto específico de palavras, compostas por um alfabeto, que seguem uma determinada regra. Usando a linguagem, podemos criar uma regra para um conjunto, de maneira similar à Matemática Discreta. Uma linguagem é expressa da seguinte maneira:
 $$
L =\{\omega \space |\text{ Propriedade sobre }\omega\}
$$

## Aspectos Importantes:
- Linguagens artificias podem ser divididas novamente entre linguagens de programação (Java, C#, etc.), e linguagens de modelagem (UML, OCL, etc.);
- Documentações existem especificando a maneira de escrever argumentos em Java, ou qualquer outra linguagem artificial. O módulo indica [esse](https://docs.oracle.com/javase/specs/) link para a documentação do Java;
- A ambiguidade das linguagens naturais surge de existirem diversas maneiras de dizer a mesma coisa, ou uma coisa podendo significar diversas outras;
- Três atividades foram passadas junto ao módulo, mas duas são programas de quiz. O questionário passado está disponível [aqui](PUCRS/2026-2/linguagensAutomatosEComputacao/lista_linguagensFormais.md) (gabarito no final).
