# Number of 1 Bits
Given a positive integer N, print count of set bits in it. 

Example 1:
Input:
N = 6
Output:
2

Explanation:
Binary representation is '110' 
So the count of the set bit is 2.

Example 2:

Input:
8
Output:
1

Explanation:
Binary representation is '1000' 
So the count of the set bit is 1.

## Best Explanation in Java🚀🚀

### Brute Force:

#### Code:

class Solution {
    static int setBits(int N) {
        // code here
        int count =0;
        while(N>0){
            int r=N%2;
            if(r==1)
                count++;
            N/=2;
        }
        return count;
    }
}

#### Explanation:

Here is a step-by-step explanation of the code:

Declare a variable "count" and initialize it to 0. This variable will be used to keep track of the count of set bits.

Enter a while loop with the condition "N > 0". This loop will continue until N becomes 0.

Inside the loop, calculate the remainder (r) when N is divided by 2. This will give the least significant bit of N.

Check if the remainder (r) is equal to 1. If it is, increment the count variable by 1. This means that a set bit (1) is found in the binary representation of N.

Divide N by 2 to remove the least significant bit. This is done by performing an integer division N/=2.

Repeat steps 3-5 until N becomes 0. This will process all the bits in the binary representation of N.

After the while loop ends, return the final value of the count variable. This will be the count of set bits in the binary representation of N.

### Optimized Approach:

#### Code:

class Solution {
    static int setBits(int N) {
        int c = 0;
        while(N > 0) {
            c += N & 1;
            N >>= 1;
        }
        return c;
    }
}

#### Explanation:

1. The "setBits" method takes an integer "N" as input and returns the count of set bits (i.e., the number of 1s) in the binary representation of "N".

2. Inside the method, an integer variable "c" is initialized to 0. This variable will be used to keep track of the count of set bits.

3. The method then enters a while loop that continues as long as "N" is greater than 0. 

4. Inside the loop, the current value of "N" is bitwise ANDed with 1 (i.e., N & 1). This operation extracts the least significant bit of "N". If the result is 1, it means that the least significant bit is set (i.e., it is a 1), so the count "c" is incremented by 1. 

5. After that, the value of "N" is right-shifted by 1 bit (i.e., N >>= 1). This operation effectively shifts all the bits of "N" to the right by one position, discarding the least significant bit. 

6. The loop continues until all the bits of "N" have been processed. 

Finally, the count "c" is returned as the result of the method.

Hope this helps😎!!
