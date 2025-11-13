# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 13/11/2025
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrix.

## Algorithm
```text
1. Start
2. Read the number of rows and columns
3. Read Matrix A and Matrix B
4. Check whether all elements of Matrix A are odd
5. Check whether all elements of Matrix B are even
6. If both conditions are true, add both matrices element-wise
7. For each element of the resultant matrix:
   If all elements are odd → Result is ODD
   If all elements are even → Result is EVEN
   Otherwise → Result is MIXED
8. Display the nature of the resultant matrix
9. End
```
## Program:
Program to ind the nature of resultant matrrix.
```java
import java.util.Scanner;

public class Main {
    static boolean isAllOdd(int[][] A, int rows, int cols) {
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                if (A[i][j] % 2 == 0)
                    return false;
        return true;
    }

    static boolean isAllEven(int[][] B, int rows, int cols) {
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                if (B[i][j] % 2 != 0)
                    return false;
        return true;
    }

    static String findMatrixNature(int[][] A, int[][] B, int rows, int cols) {
        int[][] C = new int[rows][cols];
        boolean allEven = true, allOdd = true;
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                C[i][j] = A[i][j] + B[i][j];
                if (C[i][j] % 2 == 0)
                    allOdd = false;
                else
                    allEven = false;
            }
        }
        if (allOdd)
            return "Resultant matrix is ODD";
        else if (allEven)
            return "Resultant matrix is EVEN";
        else
            return "Resultant matrix is MIXED";
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int rows = sc.nextInt();
        int cols = sc.nextInt();
        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                A[i][j] = sc.nextInt();
        for (int i = 0; i < rows; i++)
            for (int j = 0; j < cols; j++)
                B[i][j] = sc.nextInt();
        if (isAllOdd(A, rows, cols) && isAllEven(B, rows, cols))
            System.out.println(findMatrixNature(A, B, rows, cols));
        else
            System.out.println("Matrix A or B does not meet the condition");
        sc.close();
    }
}
```
Developed by: Thilak Raj . P

RegisterNumber:  212224040353

## Output:

<img width="448" height="392" alt="image" src="https://github.com/user-attachments/assets/f38a15f8-44e8-4017-b34e-1dc65767a82f" />

## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
