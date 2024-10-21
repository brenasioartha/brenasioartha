#include<stdio.h>

void generateImage(int width, int height) {
    for (int i = 0; i < height; i++) {
        for (int j = 0; j < width; j++) {
           
            if (i == 0 || i == height - 1 || j == 0 || j == width - 1) {
                printf("*");
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }
}

int main() {
    int width, height;

    while (1) {
        printf("Masukkan lebar (10-100): ");
        scanf("%d", &width);
        printf("Masukkan tinggi (5-75): ");
        scanf("%d", &height);

        if (width >= 10 && width <= 100 && height >= 5 && height <= 75) {
            generateImage(width, height);
        } else {
            printf("Input tidak valid! Lebar harus antara 10-100 dan tinggi antara 5-75.\n");
        }

        char lagi;
        printf("Ingin mencoba lagi? (y/n): ");
        scanf(" %c ", &lagi);
        if (lagi == 'n' || lagi == 'N') {
            break;
        }
    }

    return 0;
}
