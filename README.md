# Caculadora-C



 // Progama usado foi o Dev C++ 
 //Um Calculadora de um codigo que peguei para estudar algums codigos c / c++
 
 
 
 
 
	#include <stdio.h> 
	#include <conio.h>
	#include <math.h>
	#include <stdlib.h> 

	int main(){

	float num1, num2; //flutuante real
	char oper;  //caractere (nesse caso o resultado da operação e a operação)
	
		do{
	printf("Operacoes disponiveis\n");  //Demostra uma ideia ou argumento
	
			//printf mostrando que quero escrever o argumento de mais, \n pular para linha abaixo
            printf("'+' : soma\n");  //(Soma)
            printf("'-' : subtracao\n"); //(Sub)
            printf("'*' : multiplicao\n"); //(Multi)
            printf("'/' : divisao\n"); //(Div)
            printf("'%%' : resto da divisao\n"); //(Porcentagem)

            printf("\nDigite a expressao na forma: numero1 operador numero2\n"); 
            printf("Exemplos: 1 + 1 , 2.3 * 2.3, 66 - 105, 205 * 3.5, dentre outros... \n");
            printf("Para sair digite: 0 0 0\n");
            
            scanf("%f", &num1); //%f lê float
            scanf("%c", &oper); //%c lê o character
            scanf("%f", &num2); //%f lê o Float

            system("cls || clear"); // "||" quebrando a linha do codigo tendo system cls e clear na mesma linha com funções distintas
            //system executa outro progama no caso o CMD (Shell), fazendo o looping de volta assim que conta for feita
			//

            printf("Calculando: %.2f %c %.2f = ", num1,oper,num2);
	

            switch( oper ) // switch com a variavel "Oper", assim que o codigo fizer a operação ele voltara ("while").
            {
                case '+': //Caso o usuario escolha "+"
                        printf("%.2f\n\n", num1 + num2); //diz que float(%f) pode conter 2 cacteres alem do principal ex: 1.00, 2.99 ,3.12 
                        break; //para o resto do codigo apos realizar o "case"

                case '-':
                        printf("%.2f\n\n", num1 - num2);
                        break;

                case '*':
                        printf("%.2f\n\n", num1 * num2);
                        break;

                case '/':
                        if(num2 != 0)
                            printf("%.2f\n\n", num1 / num2);
                        else // SE O USUARIO COLOCAR 0
                            printf("Nao existe divisao por 0\n\n"); // Printf mostrando que não podera ser dividido por 0
                        break;

                case '%':
                        printf("%d\n\n", (int)num1 % (int)num2);
                        break;

                default:
                        if(num1 != 0 && oper != '0' && num2 != 0)
                            printf(" Operador invalido\n\n ");
                        else
                            printf(" Fechando calculadora!\n ");
            }

        }while(num1 != 0 && oper != '0' && num2 != 0);

}
