# MY PROCESS

We are given a `message.txt` file. When you open it up, it looks like this:

![image](https://github.com/user-attachments/assets/f64f0b8a-ea0f-4cb0-b2ba-5fca39cd99d6)

We are tasked to take this numbers and `modulo` it to 37 and translate it to:
- 0-25: Alphabet (uppercase)
- 26-35: Decimal Digits
- 37: Underscore

## SOLVING

This time I did it differently since my language for now is C <sub>I WILL LEARN PYTHON SOON OR SMTH</sub>, I made a C program that can map the modulos into those specifications.

The Code:
```
#include <stdio.h>
#include <stdlib.h>

char map(int modulo){
    if(modulo >= 0 && modulo <= 25){
        return 'A' + modulo;
    } else if(modulo >= 26 && modulo <= 35){
        return '0' + (modulo - 26);
    } else if(modulo == 36){
        return '_';
    } else{
        return -1;
    }
}

int main(){
    
    FILE *file;

    char filename[] = "message.txt";
    file = fopen(filename, "r");

    if(file == NULL){
        printf("Cannot open the file.\n", filename);
        return 1;
    }

    int number;

    printf("picoCTF{");
    while(fscanf(file, "%d", &number) != EOF){
        int modulo = number % 37;
        char mapped = map(modulo);
        printf("%c", mapped);
    }
    printf("}");
    fclose(file);
    return 0;
}
```

After running the program, The numbers will turn into characters and that will be the flag of the challenge.
