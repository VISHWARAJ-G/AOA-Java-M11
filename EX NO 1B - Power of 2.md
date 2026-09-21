
# EX 1B Power of 2
## DATE: 17/07/2026
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

### Algorithm

1. **Start**
2. Read the integer `n`.
3. Check whether `n > 0`.
4. Perform the bitwise operation `n & (n - 1)`.
5. If the result is `0`, return `true`, since `n` is a power of two.
6. Otherwise, return `false`.
7. Display the returned boolean result.
8. **End**

## Program:
```
/*
Program to implement Reverse a String
Developed by: Vishwaraj G
Register Number: 212223220125
*/
import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
        //Type your code here
        if((n>0) && ((n&(n-1))==0))
            return true;
        return false;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}
```

## Output:

<img width="306" height="120" alt="image" src="https://github.com/user-attachments/assets/28715bf7-9b4d-4587-9f6d-a04b6d79ddc1" />


## Result:
The program successfully implemented and the expected output is verified.
