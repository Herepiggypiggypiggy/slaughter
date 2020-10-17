/*
* Student: T. Velzel
* Number: 5229642
* Assignment: 4.3
*/


#include<stdio.h>
#include<stdlib.h>
int main()
{
    /* this program has two main variables n and m. N represents the number of products and m the amount of customers                   *
     * the program asks for n, then the price per product, then m and then for every m the amount of products that the customer bought  *
     * it then calculates for every m the amount of money spent */

    /*declare variables*/
    int n, m, i, j;
    char tmp;
    /*string and pointers for strtod*/
    char* endptr;

    double pricesarray[100];
    /*number 1100 for 100 10-digit floats with 100 spaces inbetween*/
    char pricesstring[1100];
    char productsstring[1100];

    int productsbought[100][100];
    float moneyspent[100];
    /* I MISS C99 MIXED DECLARATIONS AND CODE*/

    /*array of doubles with size n*/
    scanf("%d",&n);

    /*scan for string with product prices*/

    /* temp statement to clear buffer*/
    scanf("%c",&tmp);
    scanf("%[^\n]",pricesstring);

    /*method for turning pricesstring into array of prices*/
    /*insert first n into array to get initial value for pEnd*/
    pricesarray[0]= strtod(pricesstring, &endptr);
    /*loop for remaining prices until end of string*/
    for(i=1; i<n; i++)
    {
        pricesarray[i]= strtod(endptr, &endptr);
    }

    /* ask for m*/
    scanf("%d", &m);


    /*apply string to array method with integer values */
    for (i=0; i<m; i++)
    {
        scanf("%c",&tmp);
        scanf("%[^\n]",productsstring);

        productsbought[i][0]= strtod(productsstring, &endptr);
        /*loop for remaining prices until end of string*/
        for(j=1; j<n; j++)
        {
            productsbought[i][j]= strtod(endptr, &endptr);
        }
    }
    
    /*multiply productsbought with pricesarray*/
    for (i=0; i<m; i++)
    {
        moneyspent[i]=0;
        for(j=0; j<n; j++)
        {
            moneyspent[i]= moneyspent[i] + productsbought[i][j] * pricesarray[j];
        }

    }
    
    /*print amount spent*/
    for (i=0; i<m; i++)
    {
        printf("%.2f\n", moneyspent[i]);
    }
    return 0;
}
