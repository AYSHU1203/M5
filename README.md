EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
#include <stdio.h>

int main() {
    float num = 23.65;
    float *ptr = &num;
    *ptr = 25.0;
    
    printf("Converted value: %.0f\n", *ptr);

    return 0;
}
```

## OUTPUT:

 	
![439875798-ec5009d6-ccc9-456b-83e1-39b60a02101a](https://github.com/user-attachments/assets/430fddc0-3e57-4a8d-b6d1-a83b6abcd62f)











## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>

long long int factorial(int n) {
    if (n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    int num = 12;
    long long int result = factorial(num);

    printf("Product of first 12 natural numbers (12!) = %lld\n", result);

    return 0;
}
```

## OUTPUT:
![439876435-388936de-3bc1-4b5a-a7b3-50faeb1f54da](https://github.com/user-attachments/assets/f0dffe64-d776-4484-af67-2ad2f52f9f89)

         		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int matrix[2][3];
    int i, j;
    printf("Enter elements of the 2x3 matrix:\n");
    for (i = 0; i < 2; i++) {
        for (j = 0; j < 3; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }
    printf("\nSum of each row:\n");
    for (i = 0; i < 2; i++) {
        int rowSum = 0;
        for (j = 0; j < 3; j++) {
            rowSum += matrix[i][j];
        }
        printf("Row %d sum = %d\n", i + 1, rowSum);
    }

    return 0;
}
```



## OUTPUT

![439880476-2e6820b9-ce4e-4cdf-8b80-23620703df2e](https://github.com/user-attachments/assets/6c936b08-605a-4fd9-9f18-1e6c07f259de)


 
 

 ## RESULT
 Thus the program has been executed successfully.
 


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows, i, j;

    printf("Enter a string: ");
    scanf("%s", str);

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    for (i = 0; i < rows; i++) {
        for (j = 0; j < strlen(str); j++) {
            printf("%c ", str[j]);
        }
        printf("\n");
    }

    return 0;
}
```


 ## OUTPUT
 
![439881799-82a5e63a-e2ec-4867-8678-4be47ae7c520](https://github.com/user-attachments/assets/c40b51ca-bfae-4227-b7c2-6375e16c3f57)

 

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int arr[6];
    int *ptr;
    int i;
    ptr = arr;

    printf("Enter 6 integer elements:\n");
    for (i = 0; i < 6; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", ptr + i); 
    }

    printf("\nThe elements entered are:\n");
    for (i = 0; i < 6; i++) {
        printf("Element %d = %d\n", i + 1, *(ptr + i));
    }

    return 0;
}
```

## OUTPUT
![439883142-3794c57a-c5f6-43d5-a251-dbb8d9c6f1c4](https://github.com/user-attachments/assets/54854f28-62b3-4387-b836-81cd89268290)


 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


