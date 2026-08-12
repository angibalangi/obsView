---
title: Representação Fracionária dos Números Binários (11/08)
---
Professor: Iaçanã Ianiski Weber
Local: Prédio 32, sala 508
Horário: LM (19:15 -> 20:45)
## Descrição da Aula:
A aula começou com uma revisão da aula passada, mas logo seguimos para a idéia do ponto binário, esse dividindo o número binário entre sua representação tradicional e a fracionária. Importante notar que a representação fracionária não muda, de maneira alguma, aquela proposta pelo complemento de dois; as duas podem ser usadas simultâneamente sem problemas.
A fração binária funciona com a mesma lógica da fração decimal, embora não seja tão intuitiva. Cada posição depois da vírgula representa 2⁻ⁿ, com n sendo o número de casas após a vírgula. Por exemplo, para representar o número 2,75:
$$
0010.1100
$$
$$
2¹ + 2⁻¹+2⁻²
$$
$$
2+0,5+0,25
$$
Embora isso funcione bem em códigos mais simples, já é possível observar que isso pode gerar ineficiência nos bits quando pensando em números muito grandes ou muito pequenos. Por conta disso, é criado um sistema muito utilizado na representação de números atual, conhecido como Floating Point. Basicamente, bits são utilizados para determinar a posição do ponto, a seguinte fórmula é utilizada para obter o resultado final:
$$
(-1)^s \times (1+\text{Significado })\times2^{(Expoente-127)}
$$
Quando observando uma sequência de 32 bits, o primeiro determina o sinal (s), os próximos 8 determinam o expoente e os outros 23 representam o expoente. Abaixo está um exemplo dessa lógica funcionando, representando o número -7,5:
$$
1\space10000001\space11100000000000000000000
$$
$$
(-1)^1\times(1+0.111)\times2^{(129-127)}
$$
$$
-1 \times 1.111 \times 2^2
$$
$$
-111.1
$$
(Se o final do cálculo parece estranho, lembre que a base é dois, logo, multiplicar por 2 funciona como multiplicar por 10 no sistema decimal.)
## Aspectos Importantes:
- Quando negativo, o expoente de 2 diminui o número, colocando-o mais casas abaixo da vírgula;
- Apesar de ter sido brevemente explorado na disciplina de Introdução da Computação, o Floating Point, e especialmente a maneira de como calcular ele, é um conceito novo.