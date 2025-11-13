# EX3 Write a program to count the number of digits in an integer.
## DATE: 13/11/2025
## AIM:
To write a program to count the number of digits in an integer.

## Algorithm
```text
1. Start
2. Read an integer n
3. Define a recursive function countDigits(n)
   If n == 0, return 0
   Else, return 1 + countDigits(n / 10)
4. If the number is 0, print 1 (since it has one digit)
5. Otherwise, call countDigits(n) and display the result
6. End
```

## Program:
Program to to count the number of digits in an integer
```java
import java.util.Scanner;

public class Main {
    static int countDigits(int n) {
        if (n == 0)
            return 0;
        return 1 + countDigits(n / 10);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        if (n == 0)
            System.out.println(1);
        else
            System.out.println(countDigits(Math.abs(n)));
        sc.close();
    }
}
```
Developed by: Thilak Raj . P

RegisterNumber:  212224040353

## Output:
<img width="402" height="364" alt="image" src="https://github.com/user-attachments/assets/abe54e89-2f14-404d-b659-50e39fe58684" />



## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
