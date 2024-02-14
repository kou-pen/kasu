# kasu
```c
#include <stdio.h>
#include <math.h>
#include <stdlib.h>
#include <string.h>

#define MAKURO(x) (x*x)
#define def 10000

int gaibu;

int main(void){
    int hutuu;
    static int seiteki;


    enum animal{
        animaru_a,
        animaru_b,
        animaru_c
    };

    enum animal animaru;
    animaru = animaru_a;


    struct person
    {
        int data;
    };

    struct person name;
    printf("%d",name.data);

    struct person *ptr;
    printf("%d",ptr->data);
    
}

void num_lib(void){
    double data;
    data = sqrt(2);


    int rands;
    srand(123456);
    rands = rand();


    int sz;
    printf(sizeof sz);
    printf(sizeof(int));


    int a, b;
    printf((a>b)?a:b);

}

void str_lib(void){
    char a[20], b[10];

    strcpy(a, "a");
    strcpy(b, "b");
    strcat(a, b);

    if(strcmp(a ,b) == 0){  /*a>bとかa<bなら0以外が帰ってくる*/
        printf("True");
    }

    printf("%d", strlen(a));

}

void read_file(void){
    FILE *file_ptr;
    char buffer[256];
    int buf;
    
    file_ptr = fopen("address", "mode");
    if(file_ptr == NULL){
        printf("err");
    }

    buf = fgetc(file_ptr);
    fgets(buffer, 256, file_ptr);

    fclose(file_ptr);
}

void format_io(void){
    FILE *file_ptr;
    int logger;

    file_ptr = fopen("address", "mode");

    fprintf(file_ptr, "%d", "nanka");
    fscanf(file_ptr, "%d", &logger);
    fclose(file_ptr);
}

void rec_call(void){
    rec_call();
}
```
