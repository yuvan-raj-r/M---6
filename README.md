# EX-26-AREA-OF-RECTANGLE-USING- POINTER

## AIM

To write a C Program to find area of rectangle using pointer.

## ALGORITHM

1. Start the program.
2. Read two numbers.
3. Calculate the area of rectangle using the formula area=(x)(\*y)
4. Display the result.
5. Stop the program.

## PROGRAM

```
#include <stdio.h>
int main() {
    float x, y, area;
    float *ptrY = &y;
    scanf("%f", &x);
    scanf("%f", ptrY);
    area = x * (*ptrY);
    printf("Area of rectangle = %.2f\n", area);
    return 0;
}

```

## OUTPUT

<img width="1917" height="1141" alt="C-26" src="https://github.com/user-attachments/assets/1f1e5c82-023e-40a6-a5a8-4c981a5ca043" />


## RESULT

Thus the program to find area of rectangle using pointer has been executed successfully

# EX-27-DYNAMIC-MEMORY-ALLOCATION

## AIM

To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM

1. Start the program.
2. Read a string variable.
3. Allocate memory using malloc().
4. Display the string.
5. Remove the allocated memory using free().
6. Stop the program.

## PROGRAM

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char));
    if(str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}

```

## OUTPUT
<img width="1918" height="1142" alt="C-27" src="https://github.com/user-attachments/assets/68227478-b62f-48f2-be16-87854a28fd47" />



## RESULT

Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully.

# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1. Start the program.
2. Create a student structure with name, roll number and marks as members.
3. Using structure variable read the structure members and print them.
4. Stop the program.

## PROGRAM

```
#include <stdio.h>
struct Student {
    char name[50];
    int roll;
    float marks;
};
int main() {
    struct Student s;
    scanf("%[^\n]", s.name);
    scanf("%d", &s.roll);
    scanf("%f", &s.marks);
    printf("%s\n", s.name);
    printf("%d\n", s.roll);
    printf("%.2f\n", s.marks);
    return 0;
}

```

## OUTPUT
<img width="1917" height="1140" alt="C-28" src="https://github.com/user-attachments/assets/aec05776-0db5-4856-8377-fcfaecfaf545" />




## RESULT

Thus the program to store the student information and display it using structure has been executed successfully.

# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1. Start the program.
2. Create an employee structure with name, id and salary details as members.
3. Using structure variable read the structure members.
4. Calculate the gross salary and print the details.
5. Stop the program.

## PROGRAM

```
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basic, hra, da, gross;
};
int main() {
    struct Employee emp[3];
    int i;
    for(i = 0; i < 3; i++) {
        scanf("%[^\n]", emp[i].name);
        scanf("%d", &emp[i].id);
        scanf("%f %f %f", &emp[i].basic, &emp[i].hra, &emp[i].da);
        getchar();
        emp[i].gross = emp[i].basic + emp[i].hra + emp[i].da;
    }
    for(i = 0; i < 3; i++) {
        printf("%s\n", emp[i].name);
        printf("%d\n", emp[i].id);
        printf("%.2f\n", emp[i].gross);
    }
    return 0;
}

```

## OUTPUT
<img width="1918" height="1142" alt="C-29" src="https://github.com/user-attachments/assets/20dee601-5f7d-429c-be31-3a67cd75422b" />




## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM

Create a C program to calculate the total and average of student using structure.

## ALGORITHM

Step 1: Start the program.
Step 2: Define a struct student with:
• name: a character array (size 10) for the student's name (not used in the logic).
• rollno: an integer for the student's roll number (also unused).
• subject[5]: an array to store marks of 5 subjects.
• total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input
and iteration.
Step 4: Input Loop (i = 0 to 1):
• Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
• Loop j = 0 to 4:
o Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
• Initialize s[i].total to 0.
• Loop j = 0 to 4:
o Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
• Set s[0].total = 374;
• Set s[1].total = 383;
This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re
already calculating them.
Step 7: Output Loop (i = 0 to 1):
• Print s[i].total for each student.
Step 8: End the program.

## PROGRAM

```
#include <stdio.h>
struct Student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};
int main() {
    struct Student s[2];
    int i, j;
    for(i = 0; i < 2; i++) {
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for(i = 0; i < 2; i++) {
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    for(i = 0; i < 2; i++) {
        printf("%d %.2f\n", s[i].total, s[i].average);
    }
    return 0;
}

```

## OUTPUT
<img width="1918" height="1141" alt="C-30" src="https://github.com/user-attachments/assets/b1d70dcb-bf91-486d-8194-62802013490b" />



## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
