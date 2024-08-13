# C-programs
/*Input format:
The first input is an integer which corresponds to the year.
The second input is a string which corresponds to the fertilizer.
The third input is a string which corresponds to the technique.
Output format:
Refer the sample output.
Sample Input and Output:
Welcome to Organic Farming
Year
1972
Fertilizer
Compost Manure
Technique
Crop Rotation
Organic Farming was introduced in the year 1972. It relies on Compost Manure and many places emphasis Crop Rotation as a technique.*/
#include<stdio.h>
int main()
{
    int Year;
    printf("Welcome to Organic Farming");
    printf("Year");
    scanf("%d",&Year);
    char Fertilizer[20];
    char Technique[20];
    printf("\nFertilizer\n");
    scanf("\n%[^\n]s",Fertilizer);
    printf("Technique");
    scanf("\n%[^\n]s",Technique);
    printf("\nOrganic Farming was introduced in the year %d. It relies on %s and many places emphasis %s as a technique.",Year,Fertilizer,Technique);
    return 0;
}
/*Input Format:
Input is an integer that corresponds to the area of the farm.
Output Format:
The first line of the output is a float value that corresponds to the production area in two field system.
The second line of the output is a float value that corresponds to the production area in three field system.*/

#include<stdio.h>
int main()
{
    int n;
    float two,three,b;
    scanf("%d",&n);
    two=n/2.0;
    b=n/3.0;
    three=b+b;
    printf("%.2f",two);
    printf("\n%.2f",three);
    return 0;
}
/*Input Format:
The first line of the input is an float that corresponds to the ‘x’ value.
Output Format:
Output is a float value that corresponds to the revenue after 3 years, rounded off to 2 decimal places.*/
#include<stdio.h>
int main()
{
    int x,i;
    float y;
    scanf("%d",&x);
    y=x;
    for(i=0;i<3;i++)
    {
        y=y*(1.089);
    }
    printf("%.2f",y);
    return 0;
}
/*Input Format: 
The first line of the input is an integer that corresponds to the total weight of the residue. 
The second line of the input is an integer that corresponds to the total amount of manure needed. 
Output Format: 
An output is a float value that corresponds to the amount of manure needed extra, rounded off to 2 decimal places. */
#include <stdio.h>
 int main()
 {
     int toweight,toamount;
     float manure,a;
     scanf("%d",&toweight);
     scanf("%d",&toamount);
     a=(30.0*(float)toweight)/100.0;
     manure=(float)toamount-a;
     printf("%.2f",manure);
     return 0;
 }
/*Input format:
The first input is an integer which corresponds to the water required.
The second input is an integer which corresponds to the temperature.
Output format:
Output is a string or a list of strings.
If there are multiple strings in the output, the order to be followed is Rice, Wheat, Cotton.*/
 #include<stdio.h>
int main()
{
    int n,n1;
   scanf("%d",&n);
   scanf("%d",&n1);
    if((n>=5&&n<=10) && (n1>=20&&n1<=27))
    {
        printf("Rice");
    }
    if((n>=12 &&n<=15 ) &&(n1>=21 &&n1<=24 ))
    {
        printf("Wheat");
    }
    if((n>=6 &&n<=13 )&&(n1>=18 &&n1<=30 ))
    {
        printf("Cotton");
    }
return 0;
}
/*Input Format:
The first input is an integer corresponds to month number.
The second input is an integer corresponds to field number.*/

Output Format:
The output is the string.

#include<stdio.h>
int main()
{
    int month,field;
    scanf("%d%d",&month,&field);
    switch(month)
    {
        case 1 ... 4:
        if(field==1)printf("Winter Wheat\n");
        if(field==2)printf("Beans\n");
        if(field==3)printf("Left Fallow\n");
        break;
        case 5 ... 8:
        if(field==2)printf("Winter Wheat\n");
        if(field==3)printf("Beans\n");
        if(field==1)printf("Left Fallow\n");
        break;
        case 9 ... 12:
        if(field==3)printf("Winter Wheat\n");
        if(field==1)printf("Beans\n");
        if(field==2)printf("Left Fallow\n");
        break;
        default:
        printf("enter a valid month");
    }

}
/*Input Format:
The first (and the only) input line contains an integer that corresponds to the area of the field.
Note: Assume inputs are positive.
Output Format:
In the first line of the output, print "Yes", if the field can be divided into three parts as per the requirements of Pandu, else print "No".
If the first line of the output is "Yes", the next line of the output consists of 3 integers separated by a space, which corresponds to the areas of the divided field. In case of distinct integers, the smallest number should appear first.*/
#include<stdio.h>
int main()
{
    int a;
    scanf("%d",&a);
    if(a%2==0&&a>5)
    {
    printf("yes\n");
    if(a%3==0)
    {
        printf("%d%d%d",a/3,a/3,a/3);
    }
        if(a%3==2)
    {
      printf("%d%d%d",a/3,a/3,a/3+2);
    }
    if(a%3==1)
    {
    printf("%d%d%d",a/3-1,a/3+1,a/3+1);
     }
     }
     else
     {
         printf("No");
     }
    return 0;
}
/*Input format:
Input is an integer which corresponds to number of willow trees, n.
Output format:
Output is the series that contains 'n' numbers.*/

#include<stdio.h>
int main()
{
    int i,n,a=0,b=6,k=10,p=11;
    scanf("%d",&n);
    for(i=0;i<=n-1;i++)
{
        if(i%2==0)
     {
        printf("%d",a);
        a+=k;
        k+=2;
    }
        else
     {
        printf("%d",b);
        b+=p;
        p+=2;
     }
    printf(" ");
 }
    return 0;
}
/*Input Format:
First input is an integer that corresponds to the initial fertility of the soil.
Next inputs are number of months the land is left free after every cultivation.
Output Format:
Number of times the crops are grown successfully.*/
 #include<stdio.h>
int main()
{
    int a,b,c=0,i;
    scanf("%d",&a);
    while(a>=30)
    {
        a=a-30;
        c++;
        scanf("%d",&b);
        for(i=0;i<b;i++)
        a=a*2;
    }
    printf("%d",c);
    return 0;
}
/*Input Format:
First and only line of the input contains a string S denoting the letter code on the ticket.
Output Format:
Output a single line containing "Yes" (without quotes) based on the conditions given and "No" otherwise.*/
#include<stdio.h>
#include<string.h>
int main(){
    int k=0,I=0;
    char str[100];
    scanf("%s",str);
    int len=strlen(str);
    char ch1=str[0];
    char ch2=str[1];
    if(ch1==ch2)
    {
      printf("No");
    }
    else{
        for(int i=0;i<len;i++){
        if(i%2==0&&str[i]==ch1){
            k++;
        }
      if( i%2==1&&str[i]==ch2){
         I++;
            }
        }
        if(I+k==len) printf("Yes");
         else  printf("No");
        }
    }
    
