Quick Left Rotation
BasicAccuracy: 34.84%Submissions: 33K+Points: 1
Lamp
Stand out from the crowd. Prepare with Complete Interview Preparation  

Given an array arr[] of size N and an integer K, the task is to left rotate the array K indexes

Example 1:

Input: N = 7, K = 2
arr[] = {1, 2, 3, 4, 5, 6, 7}
Output: 3 4 5 6 7 1 2
Explanation: Rotation of the above 
array by 2 will make the output array .

Example 2:

Input: N = 6, K = 12
arr[] = {1, 2, 3, 4, 5, 6}
Output: 1 2 3 4 5 6

Your Task:
This is a function problem. You don't need to take any input, as it is already accomplished by the driver code. You just need to complete the function leftRotate() that takes array arr, integer K and integer N as parameters and rotate the given array by d value.

 

Expected Time Complexity: O(N).
Expected Auxiliary Space: O(1).


Quick Left Rotation
BasicAccuracy: 34.84%Submissions: 33K+Points: 1
Lamp
Stand out from the crowd. Prepare with Complete Interview Preparation  

Given an array arr[] of size N and an integer K, the task is to left rotate the array K indexes

Example 1:

Input: N = 7, K = 2
arr[] = {1, 2, 3, 4, 5, 6, 7}
Output: 3 4 5 6 7 1 2
Explanation: Rotation of the above 
array by 2 will make the output array .

Example 2:

Input: N = 6, K = 12
arr[] = {1, 2, 3, 4, 5, 6}
Output: 1 2 3 4 5 6

Your Task:
This is a function problem. You don't need to take any input, as it is already accomplished by the driver code. You just need to complete the function leftRotate() that takes array arr, integer K and integer N as parameters and rotate the given array by d value.

 

Expected Time Complexity: O(N).
Expected Auxiliary Space: O(1).





class Solution {
    void leftRotate(int[] arr, int n, int d) {
        // code here
        int[] nums = new int[n];
        for(int i =0;i<n;i++){
            nums[i]=arr[i];
            
            
            
        }
        for(int i=0;i<n;i++){
            arr[i]=nums[(i+d)%n];
        }
        
        
        
    }
}
