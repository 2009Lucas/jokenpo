# jokenpo
```java
package ppt;

import java.util.Scanner;

/**
 *
 * @author aluno.saolucas
 */
public class PPT {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
       int escolhaIA, escolhaJog, opcao, vitorias, derrotas, empates;
        Scanner ler = new Scanner(System.in);
        opcao = 1;
        escolhaJog = 0;
        vitorias = 0;
        derrotas = 0;
        empates = 0;

        while (opcao != 0) {

            System.out.println("0 - Sair");
            System.out.println("1 - Continuar");
            System.out.println("ESCOLHA UMA OPÇÃO:");
            opcao = ler.nextInt();

            if (opcao != 0) {
                System.out.println("Bem-vindo ao jogo Pedra, Papel ou Tesoura!");
                System.out.println("OPÇÕES:");
                System.out.println("0 - Pedra");
                System.out.println("1 - Papel");
                System.out.println("2 - Tesoura");
                System.out.println("Digite sua jogada:");
                escolhaJog = ler.nextInt();

                escolhaIA = (int) (0 + Math.random() * 2);
                System.out.println("Jogada da IA:" + escolhaIA);

                switch (escolhaIA) {
                    case 0:
                        System.out.println("Pedra");
                        break;
                    case 1:
                        System.out.println("Papel");
                        break;
                    case 2:
                        System.out.println("Tesoura");
                        break;
                    default:
                        System.out.println("Opção invalida!!");
                }

                if (escolhaJog == escolhaIA) {
                    System.out.println("Resultado: Empate!");
                    empates++;
                } else if ((escolhaJog == 0 && escolhaIA == 2)
                        || (escolhaJog == 1 && escolhaIA == 0)
                        || (escolhaJog == 2 && escolhaIA == 1)) {
                    System.out.println("Resultado: Você venceu!");
                    vitorias++;
                } else {
                    System.out.println("Resultado: Você perdeu!");
                    derrotas++;
                }
                } else {
                    System.out.println("Obrigado por jogar!");
                }

                System.out.println("Escolha do Jogador:" + escolhaJog);
        }

                System.out.println("===== Placar Final =====");
                System.out.println("Vitórias: " + vitorias);
                System.out.println("Derrotas: " + derrotas);
                System.out.println("Empates: " + empates);
    }
    }
    


```
