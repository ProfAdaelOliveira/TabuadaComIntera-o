# TabuadaComIntera-o
Nesse projeto o usuário poderá escolher um número para a verificação da tabuada. Após aprensentado o resultado da tabuada o sistema dá a opção ao usuário para Reiniciar ou Finalizar o sistema.

Recomendação de site para compilar o código: https://www.programiz.com/

// Segue projeto em C: 

#include <stdio.h>
#include <unistd.h> // Biblioteca para usar a função sleep

int main() {
    int num, i;
    char decisao;

    do {
        // Entrada de um número para a tabuada
        printf("Digite um número para ver a tabuada: ");
        scanf("%d", &num);

        // Loop para mostrar a tabuada de 1 a 10
        for (i = 1; i <= 10; i++) {
            printf("%d x %d = %d\n", num, i, num * i);
           // sleep(1); // Pausa de 1 segundo
        }
        
        printf("\n");
        
        // Pergunta ao usuário se deseja ver outra tabuada
        printf("Deseja ver outra tabuada?\n");
        printf("Digite 1 para SIM e 2 para NÃO:\n");
        scanf(" %c", &decisao); // Lê a escolha do usuário

        // Switch para a decisão do usuário
        switch (decisao) {
            case '1':
                printf("Você escolheu ver outra tabuada.\n");
                break;
            case '2':
                printf("Você escolheu sair. Até a próxima!\n");
                break;
            default:
                printf("Opção inválida. Tente novamente.\n");
                break;
        }
    } while (decisao == '1'); // Repete se o usuário escolher '1'

    return 0;
}


