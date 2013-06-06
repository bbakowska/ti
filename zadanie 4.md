```html
#include <stdio.h>
#include <math.h>

double pierwiastek (double a) {
       double x=1, ep=1e-12;
       do {
           x=(x+a/x)/2;
           } while (fabs (x-a/x)>ep*x);
           return x;
           }
main () {
     double z;
     for (z=1e-5; z<=1e15; z=z*10){
         printf ("pierw (%lf)=%.15lf\n", z, pierwiastek (z));
         printf ("_sqrt (%lf)=%.15lf\t", z, sqrt (z));
         printf ("blad wzgledny=%e\n",(pierwiastek(z)-sqrt(z))/sqrt(z));
         }
    getchar ();
    getchar ();
    }
```
