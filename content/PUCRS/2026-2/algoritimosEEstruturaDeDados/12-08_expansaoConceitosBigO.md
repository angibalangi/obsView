---
title: Expanção de Conceitos sobre Big-O (12/08)
---
Professor: Daniela Amaral
Local: Prédio 32, sala 403
Horário: LM (19:15 -> 20:45)
## Descrição da aula:
Extremamente similar a aula passada, ela repetiu quase tudo pois haviam novos alunos na turma. O principal conteúdo novo foi um entendimento básico de como calcular o Big-O apenas olhando para o código, embora a professora não tenha completado o pensamento.
Abaixo está um exemplo de um código, e os polinômios que compôem a fórmula da sua complexidade:
```
public static int somavetor(int[] v){
	int soma = 0; -> 1
	for(int i=0; i<v.length; i++){ -> 1 n+1 n
		soma = soma + v[i]; -> n
	}
	return soma; -> 1
}
```

- ```int soma = 0;``` é executado uma vez, inicializando o atributo, logo tem o custo de '1';
- ```int i=0;``` também é executado apenas uma única vez, custo '1';
- ```i<v.length;``` é uma verificação que ocorre uma vez para cada repetição do for, e mais uma adicional. Logo, seu custo é 'n+1';
- ```i++``` executa uma vez cada repetição do for, custo 'n';
- ```soma = soma + v[i];``` executa uma vez para cada item no vetor, logo, custo 'n';
- ```return soma;``` executa só uma vez, custo '1'.

Entendendo isso, nós somamos então todos os valores obtidos, conseguindo a seguinte equação:
$$
1+1+(1+n)+n+n+1 = 3n+4
$$
Depois disso, identificamos o maior polinômio (nesse caso, o 'n'), e ignoramos todas as outras constantes. Utilizamos esse polinômio para identificar o nível de Big-O, nesse caso, O(n) (linear).