# Super-agenda
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <string.h>

#define tam 5
typedef struct agenda {
 char nome[30], rua[30], complemento[15], telefone[20], num[5];
 int cod;
}cadastro;

int main(int argc, char *argv[]) {
 setlocale(LC_ALL,"Potuguese");
 int codigo, op, i, cont;
 cadastro dados[tam];
    
    
 op = 3;
 i = 0;
 while(op != 0){
  
  printf("\tMENU");
  printf("\n[1]Novo cadastro:\n[2]Ver contatos:\n[0]Fechar agenda:\n");
  scanf("\n%d", &op);
  fflush(stdin);
     system("cls");
  
  if (op == 1){
      if(i <= 4){
   
    codigo= i+1;
    dados[i].cod = codigo ;
    printf("CODIGO %d\n", codigo);
    printf("NOME: "); 
       gets(dados[i].nome);
       printf("TELEFONE: ");
       gets(dados[i].telefone);
       printf("RUA: ");
       gets(dados[i].rua);
       printf("COMPLEMENTO: ");
       gets(dados[i].complemento);
    printf("NUMERO: ");
       gets(dados[i].num);
          fflush(stdin);
    system("cls");
    i++;
     }
   else{
    printf("AGENDA CHEIA\n");
    system("pause");
    system("cls");
   }
   }
   
   else {
    if((op == 2)&&(i > 0)){
     for(cont = 0; cont < codigo;cont++){
      printf("Cod %d\n", dados[cont].cod);
      printf("NOME: %s\n", dados[cont].nome);
      printf("TEL: %s\n", dados[cont].telefone );
      printf("RUA: %s\n", dados[cont].rua );
      printf("COMPLEMENTO: %s\n", dados[cont].complemento);
      printf("NUMERO: %s\n", dados[cont].num);
      system("pause");
      system("cls");
   
     }
     
    }
   else{
   	if (i==0){
	   
   	printf("AGENDA VAZIA\n");
   	system("pause");
   	system("cls");
   }
   }
   }
     
  if (op > 2){
      printf("Opção invalida\n");
      system("pause");
   system("cls");
      
  }
 }
 
 return 0;
}
