
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 21/07/2026
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## ALGORITHM
1. **Start**
2. Read the sizes and elements of the two sorted arrays `nums1` and `nums2`.
3. Calculate the total number of elements `total = m + n` and initialize pointers `p1` and `p2` to `0`.
4. Compare the elements at `p1` and `p2`, select the smaller element, and move its corresponding pointer forward.
5. If one array is exhausted, select elements from the remaining array.
6. If `total` is even, move to the middle two elements and calculate their average as the median.
7. If `total` is odd, move to the middle element and use it as the median.
8. Display the calculated median.
9. **End** 

## Program:
```
/*
Program to implement Reverse a String
Developed by: Vishwaraj G
Register Number: 212223220125
*/
import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
       //Type code here...
       int m = nums1.length;
       int n = nums2.length;
       int total = (m+n);
       if(total%2==0){
           for(int i=0;i<total/2-1;i++){
               getMin(nums1,nums2);
           }
           return (double)(getMin(nums1,nums2)+getMin(nums1,nums2))/2;
       }else{
           for(int i=0;i<total/2;i++){
               getMin(nums1,nums2);
           }
           return (double)getMin(nums1,nums2);
       }
    }

    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        //System.out.print("Enter size of first sorted array: ");
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        //System.out.println("Enter " + m + " sorted integers for first array:");
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        //System.out.print("Enter size of second sorted array: ");
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        //System.out.println("Enter " + n + " sorted integers for second array:");
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}
```

## Output:
<img width="624" height="195" alt="image" src="https://github.com/user-attachments/assets/673af301-470b-4dd1-9ebc-6c42ce2039b8" />


## Result:
The program successfully implemented and the expected output is verified.
