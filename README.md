#include <stdio.h>

int main() {
    int matriz[4][4];
    int i, j;
    int maior, linha, coluna;

    printf("Digite os valores da matriz 4x4:\n");

    for(i = 0; i < 4; i++) {
        for(j = 0; j < 4; j++) {
            printf("M[%d][%d] = ", i, j);
            scanf("%d", &matriz[i][j]);
        }
    }

    maior = matriz[0][0];
    linha = 0;
    coluna = 0;

    for(i = 0; i < 4; i++) {
        for(j = 0; j < 4; j++) {
            if(matriz[i][j] > maior) {
                maior = matriz[i][j];
                linha = i;
                coluna = j;
            }
        }
    }

    printf("\nMatriz informada:\n");
    for(i = 0; i < 4; i++) {
        for(j = 0; j < 4; j++) {
            printf("%4d", matriz[i][j]);
        }
        printf("\n");
    }

    printf("\nMaior valor encontrado: %d\n", maior);
    printf("Posicao: Linha %d, Coluna %d\n", linha, coluna);

    return 0;
}
