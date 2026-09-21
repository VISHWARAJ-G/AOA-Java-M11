
# EX 1A Print All Numbers 
## DATE: 16/07/2026
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

### Algorithm

1. Start
2. Read the value of `N`.
3. Check whether `N` is less than or equal to `0`.
4. If `N <= 0`, display `"Invalid input. N must be greater than 0."` and terminate.
5. Initialize a loop variable `i = 1`.
6. Repeat while `i <= N`, and print `i`.
7. Increment `i` by 1 after each iteration.
8. End 

## Program:
```java
/*
Program to implement Reverse a String
Developed by: Vishwaraj G
Register Number: 212223220125
*/
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        int N;
        Scanner sc = new Scanner(System.in);
        N = sc.nextInt();
        if(N<=0){
            System.out.println("Invalid input. N must be greater than 0.");
            return ;
        }
        for(int i=1;i<=N;i++){
            System.out.print(i+" ");
        }
    }
}
```

## Output:
<img width="394" height="99" alt="image" src="https://github.com/user-attachments/assets/063a6a1a-e9d1-48fe-aae7-064e4fbf159e" />


## Result:
The program successfully print all the numbers from 1 to N. 
