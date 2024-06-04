Sort the array with elements 0, 1 and 2 in Java
Here, in this page we will discuss the program to sort the array with elements 0, 1 and 2 in Java . We use the concept of counting the frequency of 0, 1 and 2 . We are giving with the size of the array along with array elements .We have to print sorted array

Sort the array with elements
Algorithm :
Declare three variable count_0, count_1 and count_2

Using count function, count the number of zero in array and store in count_0

Using count function, count the number of one in array and store in count_1

Using count function, count the number of two in array and store in count_2

Declare an array name new_arr

Append all the 0 to new_arr

Append all the 1 to new_arr

Append all the 2 to new_arr

Print new_arr

Sort the array consisting of 0,1 and 2 using java
Related Pages
Find the “Kth” max and min element of an array 

Move all the negative elements to one side of the array

Find the Union and Intersection of the two sorted arrays

Find Largest sum contiguous Subarray

Minimize the maximum difference between heights 

Java code
Run

import java.util.*;
public
class Main {
    public
    static void arrange012(int[] arr) {  // we arrange 0 1 2 iteratively
        int i = 0, j = 0, k = arr.length - 1;
        // 0 to j-1  ==> All Zeroes

        while (i <= k) {
            if (arr[i] == 0) {
                swap(arr, i, j);
                i++;
                j++;
            } else if (arr[i] == 1) {
                i++;
            } else {
                swap(arr, i, k);
                k--;
            }
        }
    }
    // used for swapping ith and jth elements of array
    public
    static void swap(int[] arr, int i, int j) {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
    // main function
    public
    static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        
        int n = 4;
        int[] arr = new int[]{ 1,0,0,1}; 
    
        arrange012(arr);
        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
    }
}
Output
0
0
1
1
