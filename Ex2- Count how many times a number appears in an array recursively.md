# Ex2 Count how many times a number appears in an array recursively.
## DATE: 13/11/2025
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
```text
1. Start
2. Read the number of elements n
3. Read n elements into the array arr
4. Read the number target whose occurrences need to be counted
5. Define a recursive function countOccurrences(arr, n, target)
  If n == 0, return 0
  If arr[n-1] == target, return 1 + countOccurrences(arr, n-1, target)
  Otherwise, return countOccurrences(arr, n-1, target)
6. Call the function with arguments (arr, n, target)
7. Display the returned value as the total count of occurrences
8. End
```

## Program:
Program Count how many times a number appears in an array recursively.
```java
import java.util.Scanner;

public class Main {
    static int countOccurrences(int arr[], int n, int target) {
        if (n == 0)
            return 0;
        if (arr[n - 1] == target)
            return 1 + countOccurrences(arr, n - 1, target);
        else
            return countOccurrences(arr, n - 1, target);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();
        int target = sc.nextInt();
        System.out.println(countOccurrences(arr, n, target));
        sc.close();
    }
}

```
Developed by: Thilak Raj . P

RegisterNumber:  212224040353

## Output:

<img width="549" height="438" alt="image" src="https://github.com/user-attachments/assets/be034c9c-e18b-4b15-b0e6-a6525f16e188" />


## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
