---
title: Conceitos Básicos sobre Objetos (10/08)
---
## Descrição da aula:
Iniciamos a aula relembrando dos componentes básicos de um objeto, estes sendo o nome, atributos e operações dele. Entendemos um pouco mais do funcionamento básico de classes, como a função do ```private``` colocado no início dos atributos de um objeto. Esse termo impede que os valores armazenados naquela variável sejam interagidos por classes exteriores, necessitando de métodos como ```getAtributo``` e ```setAtributo``` para poder fazer essas alterações. Quando vazios, porém, esses métodos anulam a necessidade do private, por isso, eles são usados quando precisamos filtrar as informações que entram no sistema.
Fizemos um exemplo disso em aula, simulando uma classe chamada Funcionario onde, para definir um salário, esse deve ser maior do que o salário mínimo e não ser menor do que o anterior:
```
public static void setSalario (double novoSalario){
	if(this.salaro > novoSalario){
	return;
	}
	if(novoSalario < 1621.0){
	return;
	}
	this.salario = novoSalario;
} 
```
Dois pontos relevantes aparecem nesse código, o primeiro sendo o ```this.``` utilizado. Essa é uma de muitas convenções que são consideradas boas práticas de programação, facilitando a leitura do código quando sendo analisado. Outra dessas boas práticas aparece nesse código também; apesar de desnecessário, o ```.0``` no fim de valores é uma boa indicação de que o valor é um double. O segundo ponto é o termo ```static```, que representa uma ação que afeta toda a classe, e não uma única instância do objeto. Um exemplo disso foi outra ideia explorada na aula, a de um valor fixo na classe determina o salário mínimo, entendendo que esse pode mudar. Nesse sentido, adicionar um ```private double salarioMinimo;```, apesar de funcionar, é extremamente ineficiente, pois o valor do salário mínimo estaria presente em todas as futuras instâncias desse objeto. Ao invés disso, podemos estabelecer o atributo como ```static```, permitindo que seja interagido quando necessário e que ele esteja disponível para as operações do objeto, mas removendo a necessidade de adicioná-lo a cada instância.
Um tópico interessante que ajuda na construção de um objeto é a classe construtora. Esta é uma classe especial que impede a criação de um objeto sem passar certos atributos, evitando os valores nulos que acontecem quando esses não são especificados. Apesar disso, ainda ocorreram bugs no programa construído em aula (eu tinha ele escrito, mas meu computador apagou por alguma razão :/), e identificá-los é um processo essencial no ciclo de vida de um projeto
Finalizamos a aula utilizando o Astah, um programa que facilita a criação de classes, criando bases que podem ser preenchidas seguindo as especificações do usuário. Um aspecto interessante disso é a documentação de um código, que é gerada automaticamente ao escrever, mas que muitas vezes acaba desorganizada sem a ajuda de um programa como o Astah.
Uma lista de exercícios foi passada, a resposta dela está disponível [aqui](https://github.com/angibalangi/POO_10-08).
## Aspectos Importantes:
- Quando não declarado de outra forma, um novo atributo sempre vai ser ```public```;
- Estruturas de dados podem ser homogêneas, como vetores, ou heterogêneas, como classes;
- Quando construindo excessões, podemos utilizar uma função ```if``` grande, ou podemos utilizar vários ```if```s pequenos. A segunda opção tende a ser preferida, especialmente em códigos grande e frequentemente atualizados;
- Existem vários valores vazios, que são utilizados quando um valor não é especificado em um atributo ou objeto. Exemplos disso são o "null" para String e 0.0 para double;
- Para escrever corretamente na documentação de um código, um comentário deve seguir algumas regras. É possível identificar esses comentários pois eles começam sempre com ```/***```.