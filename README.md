//# Linumiz
//C programming - task

#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
    char *str = (char *)malloc(sizeof(char)*20);
    gets(str);
    int n1=0,n2,flag=0;
    for(int i=0;i<=strlen(str);i++)
    {
        if(str[i]==' ' || str[i]=='\0')
        {
            n2 = i;
            flag=1;
        }

        if(flag==1)
        {
            for(int j=n2-1;j>=n1;j--)
            {
                printf("%c",str[j]);
            }
            printf(" ");

            n1 = n2+1;
            flag=0;
        }

    }
}
