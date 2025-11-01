# FOCP1-Assignment
// -----------------------ASSIGNMENT -1-------------------------

Q1>
#include<stdio.h>
int main(){
    int n,c,r,arm=0;
    printf("Enter your number : \n");
    scanf("%d",&n);
    c = n;
    while(n>0)
    {
        r = n % 10;
        arm = (r*r*r) + arm;
        n = n / 10;
    }
    if(c == arm){
        printf("Armstrong");
    } else {
        printf("Not armstrong");
    }

   return 0;
}
-------------------------------------------------------------------------------------------------------------------------
Q2>


#include<stdio.h>
int main(){
  int a,b,greater,smaller,c;
  printf("Enter two numbers :  ");
  scanf("%d%d",&a,&b);
  if(a>b){
    greater = a;
    smaller = b;

  }else {greater = b;
smaller = a;}
while (1)
{
    c=greater%smaller;
    if (c==0){
        printf("the hcf of %d and %d is %d",a,b,smaller);
        break;

  }
  greater=smaller;
  smaller=c;
}

   return 0;
}
------------------------------------------------------------------------------------------------------------
Q3>
#include<stdio.h>
int main(){

int a,b,sub;
printf("Enter Two integers");
scanf("%d%d",&a,&b);

// sub=b;
// sub=~b;
sub=a+~b+1; //-b=~b+1
printf("subtraction of %d and %d is %d",a,b,sub);
return 0;
}
------------------------------------------------------------------------------------------------------------
Q4>
#include <stdio.h>

void swap(int*x, int*y)
{ 
    int temp;
    temp = *x;
    *x = *y;
    *y = temp;
}

int main()
{
    int a, b;

 printf("Enter values for a and b\n");
    scanf("%d%d", &a, &b);

  swap(&a, &b);

   printf("a = %d and b = %d\n", a, b);

return 0;
}
------------------------------------------------------------------------------------------------------------
Q5>
#include <stdio.h>

int main() {
   
   float x, y;

   
  printf("Enter the x-coordinate: ");
    scanf("%f", &x);
    printf("Enter the y-coordinate: ");
    scanf("%f", &y);
        if (x == 0 && y == 0) {
      printf("\nPoint (%.2f, %.2f) lies at the Origin.\n", x, y);
  }
        else if (y == 0) {
        if (x > 0)
            printf("\nPoint (%.2f, %.2f) lies on the Positive X-axis.\n", x, y);
        else // x < 0
            printf("\nPoint (%.2f, %.2f) lies on the Negative X-axis.\n", x, y);
    }
    else if (x == 0) {
        if (y > 0)
            printf("\nPoint (%.2f, %.2f) lies on the Positive Y-axis.\n", x, y);
        else // y < 0
            printf("\nPoint (%.2f, %.2f) lies on the Negative Y-axis.\n", x, y);
    }
   
  else if (x > 0 && y > 0) {
        printf("\nPoint (%.2f, %.2f) lies in the First Quadrant (I).\n", x, y);
    }
    else if (x < 0 && y > 0) {
        printf("\nPoint (%.2f, %.2f) lies in the Second Quadrant (II).\n", x, y);
    }
    else if (x < 0 && y < 0) {
        printf("\nPoint (%.2f, %.2f) lies in the Third Quadrant (III).\n", x, y);
    }
    else { // The only remaining possibility is x > 0 and y < 0
        printf("\nPoint (%.2f, %.2f) lies in the Fourth Quadrant (IV).\n", x, y);
    }

  return 0;
}
------------------------------------------------------------------------------------------------------------
Q7>
#include <stdio.h>

void print_binary_pyramid(int rows) {
    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            printf("%d", (i + j) % 2);
        }
        printf("\n");
    }
}

int main() {
    int num_rows = 5;

   printf("Binary Pyramid Pattern:\n");
    print_binary_pyramid(num_rows);
    return 0;
}
------------------------------------------------------------------------------------------------------------
Q8>
#include <stdio.h>

int main() {
    int n, i;
    int t1 = 0, t2 = 1;
    int nextTerm = t1 + t2;

   printf("Enter the number of terms (n) for the Fibonacci series: ");
   scanf("%d", &n);

   printf("\nFibonacci Series up to %d terms:\n", n);
    
  if (n >= 1) {
  printf("%d", t1);
  }
  if (n >= 2) {
   printf(", %d", t2);
   }
   for (i = 3; i <= n; ++i) {
  printf(", %d", nextTerm);
  t1 = t2;
  t2 = nextTerm;
      nextTerm = t1 + t2;
  }
    printf("\n");
   return 0;
}
