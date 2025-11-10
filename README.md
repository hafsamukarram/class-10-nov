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
	
	
}#include <stdio.h>

int main() {
    int grades[5][4];
    float avg[5];
    int count = 0;

    printf("Enter grades for 5 students (4 subjects each):\n");
    for (int i = 0; i < 5; i++) {
        printf("Student %d:\n", i + 1);
        for (int j = 0; j < 4; j++)
            scanf("%d", &grades[i][j]);
    }

    printf("\nGrades Table:\n");
    printf("Student\tSub1\tSub2\tSub3\tMath\n");

    for (int i = 0; i < 5; i++) {
        float sum = 0;
        printf("%d\t", i + 1);
        for (int j = 0; j < 4; j++) {
            printf("%d\t", grades[i][j]);
            sum += grades[i][j];
        }
        avg[i] = sum / 4;
        printf("\n");
        if (grades[i][3] > 80)
            count++;
    }

    printf("\nAverage per student:\n");
    for (int i = 0; i < 5; i++)
        printf("Student %d: %.2f\n", i + 1, avg[i]);

    printf("\nStudents scoring above 80 in Math: %d\n", count);
    return 0;
}
#include <stdio.h>

#define SIZE1 5
#define ROW 3
#define COL 3

void displayReverse(int *arr) {
    printf("1D Array in reverse: ");
    for (int i = SIZE1 - 1; i >= 0; i--)
        printf("%d ", *(arr + i));
    printf("\n");
}

int sum1D(int *arr) {
    int sum = 0;
    for (int i = 0; i < SIZE1; i++)
        sum += *(arr + i);
    return sum;
}

int max2D(int (*arr)[COL]) {
    int max = arr[0][0];
    for (int i = 0; i < ROW; i++)
        for (int j = 0; j < COL; j++)
            if (arr[i][j] > max)
                max = arr[i][j];
    return max;
}

void display2D(int (*arr)[COL]) {
    printf("2D Array:\n");
    for (int i = 0; i < ROW; i++) {
        for (int j = 0; j < COL; j++)
            printf("%d ", arr[i][j]);
        printf("\n");
    }
}

int main() {
    int arr1D[SIZE1];
    int arr2D[ROW][COL];

    printf("Enter 5 integers for 1D array:\n");
    for (int i = 0; i < SIZE1; i++)
        scanf("%d", arr1D + i);

    printf("Enter 9 integers for 3x3 2D array:\n");
    for (int i = 0; i < ROW; i++)
        for (int j = 0; j < COL; j++)
            scanf("%d", &arr2D[i][j]);

    displayReverse(arr1D);
    display2D(arr2D);

    printf("Sum of 1D array = %d\n", sum1D(arr1D));
    printf("Maximum value in 2D array = %d\n", max2D(arr2D));

    return 0;
}

