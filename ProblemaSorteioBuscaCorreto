import java.util.Random;
import java.util.Scanner;

public class ProblemaSorteioBuscaCorreto {
    public static void main(String[] args) {
        Random random = new Random();
        Scanner scanner = new Scanner(System.in);

        int[] numeros = new int[100];

        // Sorteando 100 números inteiros e armazenando no vetor
        for (int i = 0; i < 100; i++) {  // Corrigido: índice começa em 0
            numeros[i] = random.nextInt(1000);  // Gera números de 0 a 999
            System.out.println("Número sorteado: " + numeros[i]);
        }

        // Ordenando o vetor (Bubble sort)
        for (int i = 0; i < numeros.length - 1; i++) {
            for (int j = 0; j < numeros.length - 1 - i; j++) {  // Corrigido: ajustado limite do loop interno
                if (numeros[j] > numeros[j + 1]) {
                    int temp = numeros[j];
                    numeros[j] = numeros[j + 1];
                    numeros[j + 1] = temp;
                }
            }
        }

        // Exibindo o vetor ordenado
        System.out.println("Vetor ordenado: ");
        for (int i = 0; i < numeros.length; i++) {  // Corrigido: `i < numeros.length`
            System.out.print(numeros[i] + " ");
        }
        System.out.println();

        // Solicita o número a ser buscado
        System.out.print("Digite um número para buscar no vetor: ");
        int valorBusca = scanner.nextInt();

        // Busca binária no vetor ordenado
        int resultadoBusca = buscaBinaria(numeros, valorBusca);

        if (resultadoBusca == -1) {
            System.out.println("O número " + valorBusca + " não foi encontrado.");
        } else {
            System.out.println("O número " + valorBusca + " foi encontrado na posição " + resultadoBusca + ".");
        }
    }

    // Função de busca binária
    public static int buscaBinaria(int[] arr, int valor) {
        int inicio = 0;
        int fim = arr.length - 1;  // Corrigido: `fim` deve ser `arr.length - 1`

        while (inicio <= fim) {
            int meio = (inicio + fim) / 2;

            if (arr[meio] == valor) {
                return meio;
            }

            if (arr[meio] < valor) {
                inicio = meio + 1;
            } else {
                fim = meio - 1;
            }
        }

        return -1;  // Retorna -1 se não encontrar o valor
    }
}
