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
------------------------------------------------------------------------------------------------------------
// -----------------------ASSIGNMENT -2-------------------------
Q9>
#include <stdio.h>

int main() {
    int n, i, found = -1;

   printf("Enter the number of scores: ");
    scanf("%d", &n);

printf("Enter %d scores:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &scores[i]);
    }


for(i = 0; i < n; i++) {
        if(scores[i] == 99) {
        found = i; 
break;      
     }
 }

   
if(found != -1)
printf("The first occurrence of 99 is at position %d.\n", found + 1);
 else   
  printf("Score 99 not found in the array.\n");
   return 0;
}

------------------------------------------------------------------------------------------------------------
Q10>
#include <stdio.h>

int main() {
    int n, i, count = 0;
    printf("Enter number of students: ");
    scanf("%d", &n);

int marks[n];
    char names[n][50];

 printf("\nEnter names and marks of each student:\n");
    for (i = 0; i < n; i++) {
        printf("Student %d name: ", i + 1);
        scanf("%s", names[i]);
        printf("Marks: ");
        scanf("%d", &marks[i]);
    }

printf("\nStudents who scored 99:\n");
    for (i = 0; i < n; i++) {
        if (marks[i] == 99) {
            printf("%s\n", names[i]);
            count++;
  }
    }

 printf("\nTotal number of students who scored 99: %d\n", count);
    return 0;
}
------------------------------------------------------------------------------------------------------------
Q11>
#include <stdio.h>

int main()
{
    int scores[100], even_array[100], odd_array[100];
    int n, i, even_count = 0, odd_count = 0;

printf("Enter number of scores: ");
    scanf("%d", &n);

 printf("Enter %d scores:\n", n);
    for (i = 0; i < n; i++)
        scanf("%d", &scores[i]);

 for (i = 0; i < n; i++)
    {
if (scores[i] % 2 == 0)
            even_array[even_count++] = scores[i];
        else
            odd_array[odd_count++] = scores[i];
    }

printf("\nEven scores: ");
    for (i = 0; i < even_count; i++)
        printf("%d ", even_array[i]);

 printf("\nOdd scores: ");
    for (i = 0; i < odd_count; i++)
        printf("%d ", odd_array[i]);

 return 0;
}
------------------------------------------------------------------------------------------------------------
Q12>
#include <stdio.h>

int main()
{
    int scores[100], n;
    int max, min;
    int i;

   
   printf("Enter number of scores: ");
    scanf("%d", &n);

 
    printf("Enter %d scores:\n", n);
    for (i = 0; i < n; i++)
 {
    scanf("%d", &scores[i]);
   }

 
 max = min = scores[0];


   for (i = 1; i < n; i++)
 {
 if (scores[i] > max)
            max = scores[i];
        if (scores[i] < min)
            min = scores[i];
    }

 printf("\nMaximum score = %d", max);
    printf("\nMinimum score = %d\n", min);

return 0;
}
------------------------------------------------------------------------------------------------------------
Q13>
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

 int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

 int peakIndex = -1;

   if (n == 1)
        peakIndex = 0;
else {
        for (int i = 0; i < n; i++) {
            if (i == 0 && arr[i] >= arr[i + 1]) {
                peakIndex = i;
                break;
            }
 else if (i == n - 1 && arr[i] >= arr[i - 1]) {
                peakIndex = i;
                break;
            }
 else if (arr[i] >= arr[i - 1] && arr[i] >= arr[i + 1]) {
                peakIndex = i;
                break;
            }
        }
    }

 if (peakIndex != -1)
        printf("Peak element is %d at index %d\n", arr[peakIndex], peakIndex);
    else
        printf("No peak element found.\n");

 return 0;
}
------------------------------------------------------------------------------------------------------------
Q14>
#include <stdio.h>

int main() {
    int n, count = 0;
    printf("Enter number of elements: ");
    scanf("%d", &n);

 int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

for (int i = 0; i < n; i++) {
        int num = arr[i];
        int isPrime = 1;

if (num <= 1)
            isPrime = 0;
else {
 for (int j = 2; j * j <= num; j++) {
                if (num % j == 0) {
                    isPrime = 0;
                    break;
                }
            }
        }

 if (isPrime)
            count++;
    }

printf("Number of prime numbers in the array: %d\n", count);
    return 0;
}
------------------------------------------------------------------------------------------------------------
Q15>
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

int last = arr[n - 1];
    for (int i = n - 1; i > 0; i--)
        arr[i] = arr[i - 1];
    arr[0] = last;

 printf("Array after cyclic rotation: ");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

 printf("\n");
    return 0;
}
------------------------------------------------------------------------------------------------------------
Q16>
#include <stdio.h>

int main() {
    int n, pos, val;
    printf("Enter number of elements: ");
    scanf("%d", &n);

int arr[100];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

printf("Array before insertion:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");

printf("Enter value to insert: ");
    scanf("%d", &val);

 printf("Enter position (1 for front, %d for end, or any between for middle): ", n + 1);
    scanf("%d", &pos);

if (pos < 1 || pos > n + 1) {
        printf("Invalid position!\n");
        return 0;
    }

for (int i = n; i >= pos; i--)
        arr[i] = arr[i - 1];

arr[pos - 1] = val;
    n++;

 printf("Array after insertion:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");

 return 0;
}
------------------------------------------------------------------------------------------------------------
Q17>
#include <stdio.h>

int main() {
    int n, pos;
    printf("Enter number of elements: ");
    scanf("%d", &n);

 int arr[100];
 printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

 printf("Array before deletion:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");

 printf("Enter position to delete (1 for front, %d for end, or any between for middle): ", n);
    scanf("%d", &pos);

 if (pos < 1 || pos > n) {
        printf("Invalid position!\n");
        return 0;
    }

for (int i = pos - 1; i < n - 1; i++)
        arr[i] = arr[i + 1];
    n--;

printf("Array after deletion:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);
   printf("\n");

 return 0;
}
------------------------------------------------------------------------------------------------------------
Q18>
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

 int arr[n];
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

int found = 0;
 printf("Duplicate elements: ");
    for (int i = 0; i < n; i++) {
        int count = 0;
        for (int j = 0; j < n; j++) {
            if (arr[i] == arr[j])
                count++;
        }
 if (count > 1) {
            int alreadyPrinted = 0;
            for (int k = 0; k < i; k++) {
                if (arr[k] == arr[i]) {
                    alreadyPrinted = 1;
                    break;
                }
            }
 if (!alreadyPrinted) {
                printf("%d ", arr[i]);
                found = 1;
 }

