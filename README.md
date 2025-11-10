# class-10-nov

#include<stdio.h>
#include<string.h>

int main(){
	char name[]="hafsa";
	char lastName[]="mukarram";
	
	printf("%s length is %d",name,strlen(name));
	
	printf("%s\n",strcat(name,lastName));
	
	printf("%s\n",strncat(name,lastName,3));
 
	char myName[]="sara";
	char yourName[]="amna";
	
	srtcpy(myName,yourName);
	printf("%s\n",myName);	
	
	strncpy(myName,yourName,2);
	printf("%s\n",myName);
	
	char dbpassword[]="sara124";
	char password[]="sara";
    printf("%d\n",strcmp(dbPassword,password));
    
    if(strcmpi("Apple","apple")==0){
    	printf("equal\n");
	}
	
	char data[]="hello this is my friend ali,ali is bright student";
	if(strstr(data,"ali")==0){
		printf("found\n");
	}
	
	
}
