# Matriz 2x2 virando dois vetores e ordenando eles
#
#include <stdio.h>
#include <stdlib.h>
#include <locale.h> 
				
int main() 
{
	setlocale(LC_ALL, "Portuguese");
    int mat[2][2],volta[2],volta2[2];
	int i,j;
	int k,copia=0;
	
    for(i=0;i<=1;i++)
	{
        for(j=0;j<=1;j++)
		{
			printf("Digite valor para mat[%d][%d]: ", i+1, j+1); //solicitacao ao usuario
			scanf("%d",&mat[i][j]);	
        }
    }
    
    for(j=0;j<=1;j++)
	{
        for(i=0;i<=1;i++)
		{
			printf("%d ",mat[i][j]); // mostra a matriz
		}
		printf("\n");
	}
		printf("\n");
		
		
for (k=0;k<=1;k++)
{
	 	 for(j=0;j<=1;j++)
		{
			volta[i] = mat[k][j]; // o vetor pega uma coluna da matriz
            	if(volta[i] > volta[i+1]) // se o elemento i for maior que o i+1, troca
				{
	                copia = volta[i];
	                volta[i] = volta[i+1]; // faz a troca de posicões caso for maior que o outro
	                volta[i+1] = copia;
	                copia=0;
				}
	 		
			printf("%d ", volta[i]); // mostra uma coluna da matriz
			
			printf("\n");
	  	}
	  	printf("\n");
}
		
	return 0;
}
