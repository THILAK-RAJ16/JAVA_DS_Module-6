# Ex5 Count Inversions in an Array
## DATE: 13/11/2025
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
```text
1. Start
2. Read the number of elements n
3. Read n elements into array arr
4. Initialize count = 0
5. For each pair (i, j) such that i < j
    If arr[i] > arr[j], increment count by 1
6. Display count as the total number of inversions
7. End
```
## Program:
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
```java
import java.util.Scanner;

public class Main {
    static int countInversions(int[] arr, int n) {
        int count = 0;
        for (int i = 0; i < n - 1; i++)
            for (int j = i + 1; j < n; j++)
                if (arr[i] > arr[j])
                    count++;
        return count;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        System.out.println(countInversions(arr, n));
        sc.close();
    }
}
```
Developed by: Thilak Raj . P

RegisterNumber:  212224040353

## Output:

<img width="413" height="249" alt="image" src="https://github.com/user-attachments/assets/828dc6ce-0b5c-4bdb-8597-9f90d9d10ec6" />


## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
