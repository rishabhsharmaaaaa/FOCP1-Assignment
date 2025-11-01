# FOCP1-Assignment
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
