# JĘZYKI PROGRAMOWANIA


<blockquote>
<p> <i> Zamiana z Farenthajda na Celsjusza ale zmiennoprzecinkowe wyniki </i>
</blockquote>

```html

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
```

<blockquote>

<p> <i> Zamiana z Farenthajda na Celsjusza ale zmiennoprzecinkowe wyniki i liczby są wypisane przecinek po przecinku </i>
</blockquote>

```html

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
```

<blocquote>
<p> <i>Zamiana z Farenthajda na Celsjusza ale na pętla </i>
</blockquote>

```html
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
```

<blockquote>
<p> <i>Mnożenie, dzielenie, dodawanie, odejmowanie. Wszystko razem.</i>
</blockquote>

```html
#include <stdio.h>

int main(){
  int a,b;
  a=10;
  b=5;
  printf("%d - %d = %d\n", a,b, a-b);  	/*  nowa linia \n  */    <- nie pezeszkadza kompilatorowi
  printf("%d + %d = %d\n", a,b, a+b);
  printf("%d x %d = %d\n", a,b, a*b);
  printf("%d / %d = %d\n", a,b, a/b);
  getchar();
  return 0;
  
```

Wynik:
10-5=5
10+5=15
10x5=50
10/5=2


<blockquote>
<p> <i>Dzielenie, aby dobrze policzył trzeba zamienić na typ zmiennoprzecinkowy. Program wyświetli 6 cyfr po przecinku. </i>
</blocquote>


```html
#include <stdio.h>

int main(){
    double a=3.0, b=7.0;
    printf ("%lf : %lf = %lf \n", a,b, a/b);

  getchar();
  return 0;
       
}
```

<blockquote>
<p> <i>Dodawanie, aby wyświetlił brak licz po przecinku: </i>
</blockquote>

```html
#include <stdio.h>

int main(){
    double a=3.0, b=7.0;
    printf ("%.0lf + %.0lf = %.0lf \n", a,b, a+b);

  getchar();
  return 0;
    
}
```

<blockquote>
<p> <i>Obliczanie długości okręgu
</blockquote>

```html
#include <stdio.h>
#include <math.h>

int main(){
    double r=5;
    printf ("Długość okręgu to %lf", 2*M_PI*r);

  getchar();
  return 0;
   
}
```

<blockquote>
<p> <i> Oblicza na raz pole powierzchni o obwód : </i>
</blockquote>


#include <stdio.h>
#include <math.h>

int main(){
    double r=5;
    printf ("Pole powierzchni koła to %lf", r*r*M_PI);
    printf ("Długość okręgu to %lf", 2*M_PI*r);

  getchar();
    
}

--------------------------------------------------------------------------------------------------------------------------------------------------------

Przeliczanie temperatury Farenhaita na Celsiusza

#include <stdio.h>
int main () {
         int fahr, celsius;
         int lower, upper, step;
         lower=0;
         upper=300;
         step=20;
         fahr=lower;
         while (fahr<=upper) {
               celsius=5*(fahr-32)/9;
               printf ("%d\t %d\n", fahr, celsius);
               fahr=fahr+step;
               }
         getchar ();
         return 0;
         }


Większa dokładność, zmiana na zmiennoprzecinkowe

#include <stdio.h>
int main () {
         double fahr, celsius;
         int lower, upper, step;
         lower=0;
         upper=300;
         step=20;
         fahr=lower;
         while (fahr<=upper) {
               celsius=5*(fahr-32)/9;
               printf ("%lf\t %lf\n", fahr, celsius);                  -> zmienić na %lf
               fahr=fahr+step;
               }
         getchar ();
         return 0;
         }


Żeby się równo wypisywało

#include <stdio.h>
int main () {
         double fahr, celsius;
         int lower, upper, step;
         lower=0;
         upper=300;
         step=20;
         fahr=lower;
         while (fahr<=upper) {
               celsius=5*(fahr-32)/9;
               printf ("%5.1lf\t %7.2lf\n", fahr, celsius);
               fahr=fahr+step;
               }
         getchar ();
         return 0;
         }

------------------------------------------------------------------------------------------------------------------------------------

Wpisywanie stałych dla preprocesora

#include <stdio.h>
# define LOWER 0
# define UPPER 300
# define STEP 20
int main () {
         int fahr;
         for (fahr=LOWER; fahr<=UPPER; fahr=fahr+STEP)
             printf ("%3d %6.1lf\n", fahr, (5.0/9.0)*(fahr-32));
         getchar ();
         return 0;
}
