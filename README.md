# ADC-converter-Toradex-imx6ull-512MB-colibri-with-aster-carrier-board
This is the ADC converter in that i am using simple project that is ADC converter 


code in c programming


#include<stdio.h>
#include<stdlib.h>
int main()
{
   
    int num;
    float Voltage;                      //initialize float value that is voltage 

    FILE*fptr;                                
    fptr =fopen("/dev/colibri-ain0","r");    //open that file as read the pin of AIN0 
    if(fptr == NULL)
    
    {
        printf("Error!");
        exit(1);

    }
    
    fscanf(fptr,"%d",&num);                    // scan the float value and from fptr 
    Voltage =(num*3.3/4096);
    printf("Voltage Value=%f\n",Voltage);       //convert the digital value in voltage this is the formula 
     
     
    fclose(fptr);
    
    return 0;


}
