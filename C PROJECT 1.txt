#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main(){
        int number,guess,nguesses = 1;
        srand(time(0));
        number = rand()%100 + 1;
        do{
            printf("Guess the number between 1 to 100 : \n");
            scanf("%d" ,&guess);
            if(guess>number){
                printf("Enter lower number :\n" );
            }
            else if(guess<number){
                printf("Enter higher number :\n" );
            }
            else{
                printf("You Guessed it right nigga!! in %d attempts\n",nguesses );
            }
            nguesses++;
        }while(guess!=number);
        return 0;
}