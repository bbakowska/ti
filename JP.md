# JP

```c
int main() {
  printf("witaj świecie\n");
}
Zamiana z Farenthajda na Celsjusza ale zmiennoprzecinkowe wyniki

#include<stdio.h>
 int main(){
      double fahr, celsius;
      int lower, upper, step;
      lower=0;
      upper=300;
      step=20;
      fahr=lower;
      while(fahr<=upper){
      celsius=(5.0/9.0)*(fahr-32.0);
      printf("%lf\t %lf\n", fahr, celsius);
      fahr=fahr+step;
      }
      getchar();
return 0;
}           


Zamiana z Farenthajda na Celsjusza ale zmiennoprzecinkowe wyniki i liczby są wypisane przecinek po przecinku

#include<stdio.h>
 int main(){
      double fahr, celsius;
      int lower, upper, step;
      lower=0;
      upper=300;
      step=20;
      fahr=lower;
      while(fahr<=upper){
      celsius=(5.0/9.0)*(fahr-32.0);
      printf("%5.1lf\t %7.2lf\n", fahr, celsius);
      fahr=fahr+step;
      }
      getchar();
return 0;
}
   _______________________________________________
Zamiana z Farenthajda na Celsjusza ale na pętla
#include<stdio.h>
#define LOWER 0
#define UPPER 300
#define STEP 20
int main (){
    int fahr;
    for (fahr=LOWER; fahr<=UPPER; fahr=fahr+STEP)
    printf("%3d %6.1lf\n", fahr,(5.0/9.0)*(fahr-32));
      getchar();
return 0;
}
