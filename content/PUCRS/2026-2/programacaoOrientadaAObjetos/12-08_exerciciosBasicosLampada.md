---
title: Exercício Básico da Lâmpada (12/08)
---
Professor: Daniel Callegari
Local: Prédio 32, sala 403
Horário: JK (17:30 -> 19:00)
## Descrição da Aula:
Passamos a aula revisando e construíndo as atividades passadas na aula passada, mas o foco foi na atividade de criar uma classe para uma lâmpada imaginária. Abaixo está o código construído em aula:
```
public class LampadaAula {
    private int estado; //0=desligada, 1=ligada, -1=queimada

    public LampadaAula() {
        this.estado = 0; //ligada
    }

    public void ligar(){

        // se já está queimada, manter assim
        if (estado == -1) return;

        double sorteio = Math.random();
        if (sorteio < 0.3) this.estado = -1; //queimada
        else this.estado = 1; //ligada
    }

    public void desligar(){
        // se já está queimada, manter assim
        if (estado == -1) return;

        this.estado = 0; //desligada
    }

    public String getEstado(){
        switch (estado){
            case -1: return "QUEIMADA";
            case 0: return "DESLIGADA";
            case 1: return "LIGADA";
            default: return "**BUG**";
        }
    }
}
```
Discutimos um pouco outras maneiras que esse código poderia ser construído para resolver o mesmo problema. Nesse caso, utilizamos um valor int para determinar o estado da lâmpada, mas esse poderia ser quase qualquer tipo de atributo. Refizemos o código, substituindo a lógica do int por dois atributos boolean:
```
public class Lampada2Aula {
        private boolean ligada;
        private boolean queimada;

        public Lampada2Aula() {
            this.ligada = false;
            this.queimada = false;
        }

        public void ligar(){
            if(queimada) return;

            if(Math.random() < 0.3){
                queimada = true;
                ligada = false;
            } else {
                ligada = true;
            }
        }

        public void desligar(){
            if(queimada) return;
            ligada = false;
        }

        public String getEstado(){
            if (queimada) return "QUEIMADA";
            if (ligada) return "LIGADA";
            else return "DESLIGADA";
        }
    }
```
Enquanto construíamos esses códigos, exploramos algumas outras técnicas de programação úteis, como a função for destinada exclusivamente para objetos, ou um if simplificado quando lidando com valores booleanos. Abaixo estão exemplos de como utilizar esses conceitos:
- For para objetos: declaramos o objeto, damos um nome e associamos ele a todos os objetos de um vetor do mesmo tipo. Assim, a função se repete até que todos os objetos do vetor tenham executado a função especificada
```
for(Lampada lamp:minhasLampadas)
{
	lamp.ligar
	lamp.desligar
}
```
- If simplificado: quando lidando com valores booleanos em que ambas as opções fazem uma ação simples da mesma maneira, mas com valores diferentes (ex.: return 0 se falso, 1 se verdadeiro), podemos simplificar sua escrita da seguinte forma:
```
return(vouf)?15:5;
// O primeiro valor é o return se verdadeiro, o segundo, se falso
```
## Aspectos importantes:
- Outra variação do código da lâmpada pode ser uma onde só existe um método para ligar e desligar. Apesar de considerada, a proposta de reescrever o código era que isso fosse feito de uma maneira que manteria qualquer código externo funcionando; Mudar a estrutura dos métodos quebraria isso.