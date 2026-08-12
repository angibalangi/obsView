---
title: Modelos Relacionais (11/08)
---
Professor: Denise Bandeira
Local: Prédio 32, sala 516
Horário: JK (17:30 -> 19:00)
## Descrição da Aula:
Começamos a aula discutindo a característica revolucionária do modelo relacional dos bancos de dados. Isso vem devido a simplicidade desse modelo e a capacidade de manipulação dele, tudo em cima de algo que só exige do programador um conhecimento de matemática básica. A base desse modelo é a teoria dos conjuntos, e a lógica proposta pela matemática discreta. Para começar a entender esse modelo, definimos alguns conceitos:
- Produto Cartesiano: todas as combinações possíveis entre os elementos disponibilizados;
- Relação como Subconjunto: determina um subconjunto do produto cartesiano que contém apenas as combinações semânticamente válidas a uma determinada regra.
A representação dos modelor relacionais acontece em tabela, na qual as linhas representam o tupla (valor), enquanto as colunas determinam os atributos. Abaixo, um exemplo de uma tabela do modelo relacional:

| ID  | Nome  | Email           | Cidade         |
| --- | ----- | --------------- | -------------- |
| 101 | João  | joao@email.com  | São Paulo      |
| 102 | Maria | maria@email.com | Rio de Janeiro |
| 103 | Pedro | pedro@email.com | Belo Horizonte |

Além dos tuplas e atributos, também são relevantes a cardinalidade, determinada pelo número de linhas, e o grau, determinado pelo número de colunas. Nesse sentido, é importante, quando entendendo a lógica do modelo relacional, estabelecer a diferença entre o domínio e o atributo:
- Domínio: um conceito universal, que determina o "tipo" dos atributos em uma coluna. O que classifica um domínio é subjetivo, mas podemos utilizar como exemplo os números reais;
- Atributos: normalmente, são apenas um atributo dos diversos disponíveis em um domínio. Seguindo a lógica dos numeros reais, podemos dizer que valores como um salário mínimo são atributos desse domínio.
O foco da aula foi nas chaves, um novo conceito que é importante quando buscando entender esse modelo. As chaves se dividem em quatro tipos:
- Chaves Candidatas: todos aqueles atributos que são únicos em cada linha podem ser considerados chaves candidatas. Enquanto coisas como nomes podem eventualmente repetir, um CPF ou email é único por linha, então seriam possíveis chaves candidatas;
- Chave primária: é escolhida uma das chaves candidatas para se tornar a chave primária, ou seja, aquela que identifica cada linha quando procurando informações. Em casos onde não existem chaves candidatas, pode existir uma chave primária composta, em que mais de um atributo é usado como identificação;
- Chaves Alternativas: todas as chaves candidatas que não são escolhidas como chave primária. No caso de não existir chaves candidatas, ou de existir apenas uma, podem não existir chaves alternativas;
- Chaves Estrangeiras: as chaves estrangeiras são aquelas que são "importadas" de outra tabela. Obrigatóriamente, as chaves estrangeiras são primárias em outra tabela do modelo relacional, que são então usadas como atributos em outra tabela.
## Aspectos Importantes:
- Chaves compostas, embora possam existir, dificultam o processo. Por conta disso, muitas vezes é criado o ID, que define um número único a cada linha; mesmo que eficiente em alguns cenários, quando em uma escala maior, o ID pode trazer prejuízos.