## EXPERIMENT-41-REVERSE ARRAY ELEMENTS

### AIM:
To develop a program that prints the elements of an array in reverse order.

### ALGORITHM:
1. Begin the program.
2. Declare integer variables `n` and `i` to store the size of the array and loop counters respectively.
3. Declare an integer array `arr` with a maximum size of 100 to store the elements.
4. Read the value of `n` representing the size of the array.
5. Declare an integer pointer `p` and point it to the last element of the array (`&arr[n-1]`).
6. Use a loop to read the elements of the array from the user and store them in the array `arr`.
7. Declare an integer variable `m` and assign it the value of `n`.
8. Use a loop to iterate through the array in reverse order:
   - Print the current element along with its index in the format: "element - [index] : [element_value] ".
   - Decrement the pointer `p` to point to the previous element.
   - Decrement the value of `m`.
9. End the program.
## PROGRAM:
``` 
#include<stdio.h>
int main()
{
    int n,i;
    int arr[100];
    scanf("%d",&n);
    int *p;
    p=&arr[n-1];
    
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    int m;
    m=n;
    for(i=0;i<n;i++)
    {
       printf("element - %d : %d  ",m,*p--); 
       m--;
    }
}
```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/d412ea86-805c-42f8-8283-54676bc18794)


## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/68597d67-fbdc-4fec-ba3b-7cf38240f803)




## RESULT:
Thus the required program is written and executed successfully.



## EXPERIMENT-42-PRINT ARRAY ELEMENTS USING POINTER

### AIM:
To write a program that prints the elements of an array using pointer arithmetic.

### ALGORITHM:
1. Begin the program.
2. Declare an integer variable `n` to store the size of the array.
3. Read the value of `n` representing the size of the array.
4. Declare an integer array `array` of size `n` to store the elements.
5. Declare an integer pointer `ptr`.
6. Use a loop to read the elements of the array from the user and store them in the array `array`.
7. Initialize the pointer `ptr` to point to the first element of the array (`array`).
8. Use a loop to iterate through the array elements using pointer arithmetic:
   - Print the current element pointed to by `ptr`.
   - Increment the pointer `ptr` to point to the next element.
9. End the program.

## PROGRAM:
``` 
#include <stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int array[n];
    int *ptr;
    for(int i=0;i<n;i++)
    scanf("%d",&array[i]);
    for(ptr=array;ptr<array+n;ptr++)
    printf("the elements are %d\n",*ptr);
}   

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/d71ada7c-d0d8-423c-a1ec-0e2876abc129)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/a8f75da5-1954-4093-a48e-6ea01f1a7993)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-43-DYNAMIC MEMORY ALLOCATION FOR AN INTEGER ARRAY

### AIM:
To demonstrate dynamic memory allocation for an integer array using malloc() function.

### ALGORITHM:
1. Begin the program.
2. Declare an integer pointer `arr`.
3. Allocate memory for the array dynamically using `malloc()` to store 3 integers.
4. Check if memory allocation is successful:
   - If memory allocation fails, print an error message and exit the program.
5. Assign values to the elements of the array:
   - Assign `101` to the first element.
   - Assign `201` to the second element.
   - Assign `301` to the third element.
6. Print the elements of the array.
7. Free the allocated memory using `free()`.
8. End the program.

## PROGRAM:
``` 
#include <stdio.h>
#include <stdlib.h>

int main() {

    int *arr = (int *)malloc(3 * sizeof(int));
    
    
    if (arr == NULL) {
        printf("Memory allocation failed. Exiting program.\n");
        return 1; 
    }
    
   
    arr[0] = 101;
    arr[1] = 201;
    arr[2] = 301;
    
    
    printf("%d\n%d\n%d\n", arr[0], arr[1], arr[2]);

    free(arr);
    
    return 0; 
}

```




## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/3710b747-811b-4a11-b1c2-20e4eef380eb)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-44-MULTIPLY FOUR FLOATING POINT NUMBERS

### AIM:
To multiply four floating-point numbers entered by the user and print the result.

### ALGORITHM:
1. Begin the program.
2. Declare four floating-point variables `n1`, `n2`, `n3`, and `n4` to store the input numbers.
3. Declare a floating-point variable `sum` to store the result of the multiplication.
4. Prompt the user to enter four floating-point numbers `n1`, `n2`, `n3`, and `n4`.
5. Read the four floating-point numbers entered by the user.
6. Calculate the product of the four numbers and store it in the variable `sum` using the formula:
   ```
   sum = n1 * n2 * n3 * n4;
   ```
7. Print the result with an appropriate message.
8. End the program.
## PROGRAM:
``` 
#include <stdio.h>
int main()
{
    float n1,n2,n3,n4,sum=0;
    scanf("%f%f%f%f",&n1,&n2,&n3,&n4);
    sum=n1*n2*n3*n4;
    printf("The result is %f",sum);
    return 0;
    
}
```
## SAMPLE OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/bacbfa09-3dae-431e-950e-9d384e3312e4)

## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/799114d4-291a-46eb-ad3c-54feee290b9c)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-45-BOOK DETAILS USING STRUCTURE

### AIM:
To store and display details of multiple books using a structure in C.

### ALGORITHM:
1. Begin the program.
2. Define a structure named `Book` with the following members:
   - `title`: to store the title of the book (array of characters)
   - `author`: to store the author of the book (array of characters)
   - `publication`: to store the publication of the book (array of characters)
   - `price`: to store the price of the book (floating-point number)
3. Declare an array of structures `books` of size 3 to store details of 3 books.
4. Use a loop to input details of each book from the user:
   - Prompt the user to enter the title, author, publication, and price of the book.
   - Read these details and store them in the respective members of the current structure in the array.
5. Use another loop to display details of each book:
   - Print the title, author, publication, and price of each book stored in the array.
6. End the program.

## PROGRAM:
``` 
#include <stdio.h>

// Define structure for book
struct Book {
    char title[100];
    char author[100];
    char publication[100];
    float price;
};

int main() {
    // Declare an array of structures to hold details of 3 books
    struct Book books[3];
    for (int i = 0; i < 3; i++) {
        scanf("%s", books[i].title);
        scanf("%s", books[i].author);
        scanf("%s", books[i].publication);
        scanf("%f", &books[i].price);
    }
    for (int i = 0; i < 3; i++) {
        printf("Title: %s\n", books[i].title);
        printf("Author: %s\n", books[i].author);
        printf("Publication: %s\n", books[i].publication);
        printf("Price: %.2f", books[i].price);
    }
    
    return 0;
}

```



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/d7cb9e7f-d378-4476-a6b4-8e0941eb9f4f)


## RESULT:
Thus the required program is written and executed successfully.



## EXPERIMENT-46-EMPLOYEE DETAILS USING STRUCTURE

### AIM:
To read and display details of an employee using a structure and functions in C.

### ALGORITHM:
1. Begin the program.
2. Define a structure named `Employee` with the following members:
   - `id`: to store the employee ID (integer)
   - `name`: to store the name of the employee (array of characters)
   - `salary`: to store the salary of the employee (floating-point number)
3. Define a function named `readEmployeeDetails` that takes a pointer to `struct Employee` as an argument:
   - Inside the function, prompt the user to enter employee details such as ID, name, and salary.
   - Read these details and store them in the respective members of the employee structure.
4. Define a function named `displayEmployeeDetails` that takes a `struct Employee` as an argument:
   - Inside the function, print the employee details such as ID, name, and salary.
5. In the `main` function:
   - Declare a variable of type `struct Employee` named `emp`.
   - Call the `readEmployeeDetails` function, passing the address of the `emp` variable.
   - Call the `displayEmployeeDetails` function, passing the `emp` variable.
6. End the program.

## PROGRAM:
``` 
#include <stdio.h>

// Define structure for employee
struct Employee {
    int id;
    char name[100];
    float salary;
};

// Function to read employee details
void readEmployeeDetails(struct Employee *emp) {
    //printf("Enter employee ID: ");
    scanf("%d", &emp->id);
    //printf("Enter employee name: ");
    scanf("%s", emp->name);
    scanf("%f", &emp->salary);
}

// Function to display employee details
void displayEmployeeDetails(struct Employee emp) {
    printf("Id is: %d\n", emp.id);
    printf("Name is: %s\n", emp.name);
    printf("salary is: %.2f\n", emp.salary);
}

int main() {
    struct Employee emp; // Declare an employee structure
    
    // Read details of employee
    readEmployeeDetails(&emp);
    displayEmployeeDetails(emp);
    
    return 0;
}
```



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/57ada994-9798-4a50-bcd7-1d8b1835b830)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-47-STUDENT DETAILS SORTING

### AIM:
To read details of students including their names and addresses, sort them based on their names, and display the sorted list.

### ALGORITHM:
1. Begin the program.
2. Define a constant `MAX_LENGTH` to represent the maximum length of strings (e.g., names and addresses).
3. Define a structure named `Student` with the following members:
   - `stud_name`: to store the name of the student (array of characters)
   - `address`: to store the address of the student (array of characters)
4. Define a function named `swap` that takes two pointers to `struct Student` as arguments:
   - Inside the function, swap the contents of the two structures.
5. Define a function named `sortStudents` that takes an array of `struct Student` and an integer `n` as arguments:
   - Implement the bubble sort algorithm to sort the student structures based on their names.
6. In the `main` function:
   - Read the number of students `n`.
   - Declare an array of `struct Student` named `students` with size `n`.
   - Use a loop to read details of each student (name and address) and store them in the array.
   - Call the `sortStudents` function to sort the array of students based on their names.
   - Use another loop to display the sorted list of student details (name and address).
7. End the program.

## PROGRAM:
``` 
#include <stdio.h>
#include <string.h>

#define MAX_LENGTH 100

// Define structure for student
struct Student {
    char stud_name[MAX_LENGTH];
    char address[MAX_LENGTH];
};

// Function to swap two student structures
void swap(struct Student *a, struct Student *b) {
    struct Student temp = *a;
    *a = *b;
    *b = temp;
}

// Function to perform bubble sort on student structures based on stud_name
void sortStudents(struct Student students[], int n) {
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (strcmp(students[j].stud_name, students[j + 1].stud_name) > 0) {
                swap(&students[j], &students[j + 1]);
            }
        }
    }
}

int main() {
    int n;
    
    scanf("%d", &n);

    struct Student students[n];

  
    for (int i = 0; i < n; i++) {
        scanf("%s %[^\n]", students[i].stud_name, students[i].address);
    }

   
    sortStudents(students, n);

   
    for (int i = 0; i < n; i++) {
        printf("%s      %s\n", students[i].stud_name, students[i].address);
    }

    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/471f8b80-be62-418b-a7ea-a266ab397551)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/bbfbcf0f-fb8b-44d3-8aa3-801bbc086201)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-48-ELECTRICITY BILL CALCULATION

### AIM:
To calculate the electricity bill based on the previous and current meter readings, considering different tariff rates for various units consumed.

### ALGORITHM:
1. Begin the program.
2. Define a structure named `ElectricityBill` with the following members:
   - `serviceNo`: to store the service number of the customer (integer)
   - `name`: to store the name of the customer (array of characters)
   - `prevReading`: to store the previous meter reading (integer)
   - `currReading`: to store the current meter reading (integer)
   - `unitsConsumed`: to store the units of electricity consumed (integer)
   - `amount`: to store the calculated electricity bill amount (float)
3. Define a function named `calculateElectricityBill` that takes a pointer to `struct ElectricityBill` as an argument:
   - Calculate the units consumed by subtracting the current reading from the previous reading.
   - Based on the units consumed, calculate the electricity bill amount using the following tariff rates:
     - For the first 100 units: Rs. 2.00 per unit
     - For the next 200 units (101 to 300): Rs. 3.00 per unit
     - For units above 300: Rs. 5.00 per unit
   - Update the `amount` and `unitsConsumed` members of the structure.
4. In the `main` function:
   - Declare a variable `bill` of type `struct ElectricityBill`.
   - Read the service number, name, previous reading, and current reading of the customer.
   - Call the `calculateElectricityBill` function, passing the address of `bill`.
   - Print the service number, name, units consumed, and amount to be paid.
5. End the program.
## PROGRAM:
``` 
#include <stdio.h>

// Structure definition for Electricity Bill
struct ElectricityBill {
    int serviceNo;
    char name[100];
    int prevReading;
    int currReading;
    int unitsConsumed;
    float amount;
};

// Function to calculate electricity bill
void calculateElectricityBill(struct ElectricityBill *bill) {
    int units = - bill->currReading + bill->prevReading;

    if (units <= 100) {
        bill->amount = units * 2.00;
    } else if (units > 100 && units <= 300) {
        bill->amount = 100 * 2.00 + (units - 100) * 3.00;
    } else {
        bill->amount = 100 * 2.00 + 200 * 3.00 + (units - 300) * 5.00;
    }

    bill->unitsConsumed = units;
}

int main() {
    struct ElectricityBill bill;

    
    scanf("%d", &bill.serviceNo);
    scanf("%s", bill.name);
    scanf("%d", &bill.prevReading);
    scanf("%d", &bill.currReading);

    // Calculating electricity bill
    calculateElectricityBill(&bill);

    printf("service number:%d\n", bill.serviceNo);
    printf("service name:%s\n", bill.name);
    printf("unit consumption:%d\n", bill.unitsConsumed);
    printf("amount:%.2f\n", bill.amount);

    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/e75ff252-6dc2-4487-90e6-a5c9550dcc1a)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-6/assets/144870412/3c351738-e276-4884-bfd0-fc1c974f5241)





## RESULT:
Thus the required program is written and executed successfully.



















