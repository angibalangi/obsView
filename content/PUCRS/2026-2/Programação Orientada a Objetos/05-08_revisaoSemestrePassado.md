---
title: Revisão de Conceitos (05/08)
---
Professor: Daniel Callegari
Local: Prédio 32, sala 403
Horário: JK (17:30 -> 19:00)
## Descrição da Aula:
Foi uma aula densa, onde revisamos alguns conceitos explorados no semestre passado, e explorando mais dos comandos de Shell com o Java.
Primeiramente, observamos a estrutura de arquivos de código, com .java representado o código e .class sendo o que é lido pela máquina (.class é gerado na compilação). O comando básico de início de Main também foi mais explorado:
```
public static void main (String[] args)
```
Questionando um pouco a frase, percebemos que ```args``` é, na realidade, um vetor de Strings. A maneira pela qual interagimos com esse vetor é pelos argumentos disponíveis quando iniciando um programa de Shell
```
$ java App 1 2 3
```
Nesse caso, ```java App``` seria o comando de inicialização, enquanto ```1 2 3``` seriam três diferentes Strings no vetor ```args```. Podemos utilizar esse vetor em códigos como usariamos qualquer outro. Abaixo está um exemplo de um código que soma os argumentos, escrito em conjunto durante a aula.
```
public class Somador{
	public static void main (String[] args){
		int qntos = args.length;
		int total = 0;
		for (int i = 0; i<args.length; i++){
			int num = Integer.parseInt(args[i]);
			total += num;
		}
		System.out.println(total);
	}
}
```
Após isso, exploramos um pouco mais algumas palavras chave da disciplina, como classificação (juntar características em objetos, ou seja, criar uma classe), e instanciar (criar exemplares de objetos). Também aprendemos que existem diversos jeitos de escrever código, chamados paradigmas de linguagens de programação; Alguns dos mais relevantes são: Procedural, declarativo, imperativo, lógico, funcional, orientado a objetos, etc..
Finalizamos a aula utilizando o BlueJ com algumas funções novas, nos permitindo ter uma visão mais intuitiva de objetos criados, até mesmo podendo os criar sem uma classe ```Main```.
Entendemos um pouco mais sobre objetos, o principal sendo a diferença entre eles e as variáveis bases. Enquanto uma variável int realmente contém a informação destinada, um objeto serve apenas para apontar ao endereço de memória. Crucialmente, criar dois objetos diferentes com o mesmo conteúdo cria dos endereços de memória diferentes, isso devido o "nome de nascença" de cada objeto, visível ao dar um print() quando não existe um toString (normalmente, vai parecer algo como objeto@6ba1ab1). Para conseguir um objeto diferente que aponta para o mesmo endereço, usamos o sinal de =.
## Aspectos Importantes:
- Objetos podem ser elementos concretos (coisas que podemos encostar, uma escola) ou conceituais (coisas que não podemos encostar, uma marca);
- Muitas vezes, fazer essa separação não é fácil. A abstração é uma habilidade valiosa no curso por causa disso;
- O sinal de = não significa, no contexto da programação, "igual" (este seria = =). Ele representa mais uma idéia de transferência e receber uma informação;
- Instâncias de objetos tem três características: Estado (seus valores), comportamento (seus métodos) e identidade (o "nome de nascença" mencionado).