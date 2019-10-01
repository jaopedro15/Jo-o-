#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
//int main(int argc, char **argv)
{
    char frase[60], vog[10];
    int palavra=1,vogais,i,e;
    bool estado;
    estado = true;
    vog[0] = 'a';
    vog[1] = 'e';
    vog[2] = 'i';
    vog[3] = 'o';
    vog[4] = 'u';
    vog[5] = 'A';
    vog[6] = 'E';
    vog[7] = 'I';
    vog[8] = 'O';
    vog[9] = 'U';
    printf( "Escreva uma frase: \n");
    gets(frase);
    for ( i = 0; i < strlen(frase);i++)
    {
    // Verifica se o caracter atual é diferente de espaço, so for, seta estado como true, para que o proximo espaço que existir, ele conte uma palavra.
    if ( frase[i] != 32)
        estado = true;
        if ( frase[i] == 32 && estado == true)
    {
            palavra++;
        estado = false;
        }
    else
    {
            for ( e = 0; e <= 9; e++ )
        {
                if ( frase[i]==vog[e] )
                    vogais++;
            }
        }
    }
    if ( vogais = 1) {
        printf("A frase %s contém %i palavra(s) e %i vogal \n",frase,palavra,vogais);
    }
    else {
       printf("A frase %s contém %i palavra(s) e %i vogais \n",frase,palavra,vogais);
    }

    return 0;

}
