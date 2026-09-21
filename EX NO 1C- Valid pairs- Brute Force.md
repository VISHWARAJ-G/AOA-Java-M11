
# EX 1C Valid Pairs using Brute Force Approach
## DATE: 18/07/2026
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

### Algorithm

1. **Start**
2. Read the array size `n`, the array elements, and the value `k`.
3. Initialize `count = 0`.
4. Traverse each element `nums[i]` using an outer loop.
5. For each `i`, traverse the elements after it using an inner loop with `j = i + 1`.
6. Check whether `|nums[i] - nums[j]| == k`.
7. If the condition is true, increment `count` by 1.
8. Display the final value of `count`.
9. **End**

## Program:
```
/*
Program to implement Reverse a String
Developed by: Vishwaraj G
Register Number: 212223220125
*/
import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        //Type your code here
        int count = 0;
        for (int i=0;i<nums.length;i++){
            for(int j=i+1;j<nums.length;j++){
                if(Math.abs(nums[i]-nums[j])==k){
                    count++;
                }
            }
        }
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}
```

## Output:
<img width="285" height="175" alt="image" src="https://github.com/user-attachments/assets/50feb1de-dbb4-4063-9d92-9c146cb9d4a1" />



## Result:
The program successfully implemented and the expected output is verified.
