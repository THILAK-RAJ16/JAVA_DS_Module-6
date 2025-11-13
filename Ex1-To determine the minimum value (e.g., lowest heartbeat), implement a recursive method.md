# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE: 13/11/2025
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
```text
Step 1: Start
Step 2: Read the number of heartbeats (n) and store them in an array arr.
Step 3: Define a recursive method findMin(arr, n) that returns the minimum value among the first n elements.
Step 4: If n == 1, return arr[0] (base case).
        Otherwise, recursively find the minimum of the first n-1 elements and compare it with arr[n-1].
        Return the smaller value.
Step 5: Display the result as the lowest heartbeat.
Step 6: End
```
## Program:

Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
```java
import java.util.Scanner;

public class Main {
    static int findMin(int arr[], int n) {
        if (n == 1)
            return arr[0];
        int min = findMin(arr, n - 1);
        return Math.min(min, arr[n - 1]);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] heartbeat = new int[n];
        for (int i = 0; i < n; i++) {
            heartbeat[i] = sc.nextInt();
        }
        int minValue = findMin(heartbeat, n);
        System.out.println("The lowest heartbeat value is: " + minValue);
        sc.close();
    }
}

```
Developed by: Thilak Raj . P

RegisterNumber:  212224040353


## Output:

<img width="708" height="429" alt="image" src="https://github.com/user-attachments/assets/9d2429e2-a166-42cb-a4e8-cdcf4e2f0cdf" />

## Result:
Thus,the JAVA program find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully.
