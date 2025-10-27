# desafio-batalha-naval
Solução para o desafio de Batalha Naval em C.
// batalha_naval.c
#include <stdio.h>

void imprimir_tabuleiro(int linhas, int colunas, int tabuleiro[linhas][colunas]) {
    for (int i = 0; i < linhas; i++) {
        for (int j = 0; j < colunas; j++) {
            printf("%d ", tabuleiro[i][j]);
        }
        printf("\n");
    }
    printf("\n");
}

int main() {
    // =================================================================
    // NÍVEL NOVATO: Posicionamento dos Navios (Tabuleiro 5x5)
    // =================================================================
    printf("### NÍVEL NOVATO: Posicionamento de Navios (5x5) ###\n");
    
    int tabuleiro_novato[5][5] = {0}; 
    
    // Navio Vertical (tamanho 3, começando em [1][1])
    int linha_vertical = 1;
    int coluna_vertical = 1;
    for (int i = 0; i < 3; i++) {
        tabuleiro_novato[linha_vertical + i][coluna_vertical] = 1; 
        printf("Navio Vertical: Coordenada [%d][%d]\n", linha_vertical + i, coluna_vertical);
    }
    
    // Navio Horizontal (tamanho 4, começando em [3][0])
    int linha_horizontal = 3;
    int coluna_horizontal = 0;
    for (int j = 0; j < 4; j++) {
        tabuleiro_novato[linha_horizontal][coluna_horizontal + j] = 1; 
        printf("Navio Horizontal: Coordenada [%d][%d]\n", linha_horizontal, coluna_horizontal + j);
    }
    
    // Opcional: Imprimir o tabuleiro para visualização
    printf("\nVisualização do tabuleiro 5x5 (1=Navio):\n");
    imprimir_tabuleiro(5, 5, tabuleiro_novato);

    return 0;
}
