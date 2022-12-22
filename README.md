# estudoemC
estudo em linguagem C
#include <stdio.h>

int login();
int menu();

 



int main()
{
    printf("argentina campeã \n\n\n");
    login();
    menu();
    
    
  

    return 0;
}


#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <locale.h>

int login()
{
    setlocale (LC_ALL, "");
    char nome[50];
    char login[15] = "silva"; 
    char login1[15]; 
    char senha[100] = "silva";
    char senha1[15]; 
    
    printf("LOGIN: ");
    scanf("%s",login1); 
    printf("SENHA: ");
    scanf("%s", senha1);
    
    if (strcmp(login, login1) == 0) 
    {
    	printf("\nSeja bem vindo Silva!\n\n");
    }
    else
    {
    	printf("Login Inválido\n");
    }
}

int menu()
{
   char c;     
   int sair;
    int num, num1, num2 ;
    int primo, resultado, i;
    int soma;
    int n;
    
    int x=1;
    int *ponteiro;
    ponteiro= &x;
    do{
        
    
    
     printf("MENU: \n \n");
    printf("1.soma de dois números \n\n");
    printf("2.verificar se um número é primo \n\n");
    printf("3.sequencia de numero primo \n\n");
    printf("4.utilização de poteiros\n\n");
    printf("5.utilização de struct\n\n");
    printf("escolha a opção desejada:");
    scanf("%d", &num);
    
    switch(num)
    {
        case 1:
        printf("digite um numero: \n");
        scanf("%d", &num1);
        printf("digite outro numero: \n");
        scanf("%d", &num2);
        soma = num1 + num2;
        
        printf("a soma entre eles é: %d \n", soma);
        
        break;
        case 2:
        printf("digite um número:");
    scanf("%d", &n);
    
    if(n<=1){
        printf("esse número não é primo");
        
    }
    else{
        for(i=2; i<n; i++){
            if(n%i==0){
                printf("Esse número não é primo\n");
                break;
            }
        }
        if(i==n){
            printf("Esse número é primo\n");
        }
        break;
    }
        case 3: 
        printf("digite um numero:");
    scanf("%d", &num1);
    
    while( x < num1){
        printf("%d \n ",x);
        x= x + 2;
        
    }
    
    break;
        case 4:
        
        printf("%d \n", x);
        printf("%d \n", ponteiro);
        printf("%d \n",*ponteiro);
        break;
        
	}
	printf("DESEJA FILANIZAR O PROGRAMA (S)(N)? ");
	scanf("%d",&sair);
	scanf("%c",&c);
} while(c=='N' || c=='n');
}

//===================================================================================

#include <stdio.h>
int marmita();

int main(){
    marmita();
    
}
int marmita()
{
    struct marmita{
    int arroz;
    int feijao;
    int macarrao;
    int carne;
    };

    struct marmita pdr ;

    pdr.arroz=2;
    pdr.feijao=1;
    pdr.macarrao=3;
    pdr.carne=3;

    printf(" o Peso da marmita do pedreiro e: %ikg %ikg %ikg %ikg = 9kg\n", pdr.arroz, pdr.feijao, pdr.macarrao, pdr.carne);
    

    return 0;
}
