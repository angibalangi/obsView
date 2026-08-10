---
title: Revisão de Conceitos (05/08)
---
Professor: Daniela Amaral
Local: Prédio 32, sala 403
Horário: LM (19:15 -> 20:45)
## Descrição da Aula:
No início da aula, focamos em entender alguns conceitos ensinados no semestre passado de fundamentos, como algorítimos. Algorítimos, como descrito pela professora, são as regras que escrevemos em código usando as linguagens de programação e que depois são rodadas como um programa. Revemos os básicos termos da linguagem java, como as diferentes variáveis básicas (int, String, etc..), e estruturas de controle (repetição, seleção, vetores). Fizemos um exercício onde tinhamos que identificar o tipo de informação armazenada, e discutimos se um CPF deveria ser registrado como int ou String.
A segunda parte da aula foi focada em uma lista de exercícios de revisão. Abaixo estão os meus códigos após os respectivos enunciados:

a) Uma concessionária está oferecendo descontos nos preços dos seus veículos de acordo com o tipo de combustível. Os descontos estão estruturados da seguinte forma: para veículos com álcool são 25% , com gasolina são 21% e com diesel são 14%. Crie uma função que receba o valor do veículo e o tipo de combustível e retorne o resultado do cálculo do valor de desconto. Crie também uma função que calcule e retorne o valor a ser pago pelo cliente com o desconto. Exiba o valor do carro sem desconto, o desconto concedido, o valor do desconto e o valor do carro com desconto.
```
import java.util.Scanner;
public class a_concessionaria
{
    public static void main (String[] args){
        Scanner in = new Scanner(System.in);
        System.out.println("Informe o valor do veículo: ");
        double valorOriginal = in.nextDouble();
        System.out.println("Informe o tipo de combustível: ");
        in.nextLine();
        String combustivel = in.nextLine().toLowerCase();
        int desconto = qualDesconto(combustivel);
        double valorDesconto = calcDesconto(valorOriginal, desconto);
        double valorFinal = novoValor(valorOriginal, valorDesconto);
        System.out.printf("Valor sem desconto: R$%.2f", valorOriginal);
        System.out.printf("Desconto concedido: %d", desconto);
        System.out.printf("Valor do desconto: R$%.2f", valorDesconto);
        System.out.printf("Novo valor: R$%.2f", valorFinal);
    }

    public static int qualDesconto (String c){
        switch (c){
            case "álcool": return 25;
            case "gasolina": return 21;
            case "diesel": return 14;
            default: return 1;
        }
    }

    public static double calcDesconto (double v, int d){
        return v*d/100;
    }
    public static double novoValor (double v, double vd){
        return v-vd;
    }
}
```

b) Construa um vetor que recebe 10 valores inteiros lidos através do teclado. Exiba o vetor resultante na ordem inversa da qual os dados estão inseridos. Após, leia um número inteiro e procure por este valor no vetor respeitando a ordem na qual os dados foram inseridos. Se encontrar, exiba o número lido e o índice da primeira ocorrência deste valor. Se não encontrar, exiba a mensagem "Valor X não encontrado" onde o X é o número lido.
```
import java.util.Scanner;
public class b_vetorInverso {
    public static void main (String[] args){
        Scanner in = new Scanner(System.in);
        int[] v = new int[10];
        for (int i = 9; i >= 0; i--){
            System.out.println("Insira um valor: ");
            v[i]= in.nextInt();
        }
        System.out.print("Vetor: ");
        for (int i = 0; i < v.length; i++){
            System.out.printf("%d ", v[i]);
        }
        System.out.println("\nInforme um número para achar o índice: ");
        int n = in.nextInt();
        for (int i = 0; i < v.length; i++){
            if (n == v[i]){
                System.out.printf("Valor %d encontrado no índice %d", n, i);
                return;
            }
        }
        System.out.printf("Valor %d não encontrado", n);
    }
}
```

c) Construa uma matriz de 5x4 que em cada posição receba um número randômico entre 0 e 99. Exiba a matriz gerada de maneira adequada na tela. Depois, crie um vetor que armazene os valores de todos os números pares da matriz e exiba o resultado do vetor. Use a classe Random para geração de valores aleatórios.
```
import java.util.Random;
public class c_matrizPar {
    public static void main (String[] args){
        Random rnd = new Random();
        int[][] m = new int[4][5];
        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 5; j++){
                m[i][j] = rnd.nextInt(100);
            }
        }
        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 5; j++) {
                System.out.printf("%d ", m[i][j]);
            }
            System.out.println();
        }
        int n = 0;
        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 5; j++) {
                if (m[i][j]%2==0){
                    n++;
                }
            }
        }
        int[] p = new int[n];
        n = 0;
        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 5; j++) {
                if (m[i][j]%2==0){
                    p[n] = m[i][j];
                    n++;
                }
            }
        }
        System.out.print("Pares: ");
        for(int i = 0; i < p.length; i++){
            System.out.printf("%d ",p[i]);
        }
    }
}
```

d) Crie pequeno jogo de adivinhação onde inicialmente deve-se gerar um número aleatório inteiro entre 0 e 50 que será o "número secreto". Em seguida solicite que o usuário digite um número inteiro. Se o número digitado for menor que o número secreto, imprima “O número secreto é MAIOR”, se o número digitado for maior que o número secreto, imprima “O número secreto é MENOR”. O usuário deve ter 10 tentativas de digitação de um número. Caso em algum momento ele acerte, o sistema deve apresentar a mensagem "Parabéns, você acertou em X tentativas!" onde X é o número de tentativas que ele levou para acertar e encerrar a execução. Caso o usuário não consiga acertar nas 10 tentativas, apresente uma mensagem desejando "Boa sorte na próxima!".
```
import java.util.Random;
import java.util.Scanner;
public class d_adivinhacao {
    public static void main (String[] args){
        Random rnd = new Random();
        Scanner in = new Scanner(System.in);
        int num = rnd.nextInt(51);
        System.out.println("Adivinhe o número secreto (0 - 50): ");
        for (int i = 0; i < 10; i++){
            int n = in.nextInt();
            if (n == num){
                System.out.printf("Parabéns, você acertou em %d tentativas!", i+1);
                return;
            } else if (n > num){
                System.out.println("O número secreto é MENOR!");
            } else {
                System.out.println("O número secreto é MAIOR!");
            }
        }
        System.out.print("Boa sorte na próxima!");
    }
}
```
## Aspectos Importantes:
- As atividades não vão ser cobradas no futuro;
- ```printf```,```%d```, e ```%.2f``` podem ser usados para mais facilmente inserir dados em um System.out.print. 