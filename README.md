# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER


## PROGRAM:

```
#include <stdio.h>  
#include <string.h>  
#include <ctype.h>  
void main()  
{  
    char plain[10],cipher[10];  
    int key,i,length;      
    int result;      
    printf("\n Enter the plain text:");      
    scanf("%s", plain);      
    printf("\n Enter the key value:");      
    scanf("%d", &key);      
    printf("\n \n \t PLAIN TEXt: %s", plain);      
    printf("\n \n \t ENCRYPTED TEXT:");      
    for(i=0, length = strlen(plain); i<length; i++)  
    {  
        cipher[i]=plain[i] + key;          
        if (isupper(plain[i]) && (cipher[i] > 'Z'))
            cipher[i] = cipher[i] - 26;          
        if (islower(plain[i]) && (cipher[i] > 'z'))
            cipher[i] = cipher[i] - 26;          
        printf("%c", cipher[i]);  
    }  
    printf("\n \n \t AFTER DECRYPTION : ");      
    for(i=0;i<length;i++)  
    {  
        plain[i]=cipher[i]-key;          
        if(isupper(cipher[i])&&(plain[i]<'A'))          
        plain[i]=plain[i]+26;          
        if(islower(cipher[i])&&(plain[i]<'a'))          
        plain[i]=plain[i]+26;          
        printf("%c",plain[i]);  
    }  
} 

```

## OUTPUT:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c1c5a325-a58e-48f8-be2b-17609fcf415a" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
