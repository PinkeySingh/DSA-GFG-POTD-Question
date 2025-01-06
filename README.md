Given an array arr[] and a number target, find a pair of elements (a, b) in arr[], where a<=b whose sum is closest to target.
Note: Return the pair in sorted order and if there are multiple such pairs return the pair with maximum absolute difference. If no such pair exists return an empty array.

Examples:

Input: arr[] = [10, 30, 20, 5], target = 25
Output: [5, 20]
Explanation: As 5 + 20 = 25 is closest to 25.
Input: arr[] = [5, 2, 7, 1, 4], target = 10
Output: [2, 7]
Explanation: As (4, 7) and (2, 7) both are closest to 10, but absolute difference of (2, 7) is 5 and (4, 7) is 3. Hence, [2, 7] has maximum absolute difference and closest to target. 
Input: arr[] = [10], target = 10
Output: []
Explanation: As the input array has only 1 element, return an empty array.
Constraints:
1 <= arr.size() <= 2*105
0 <= target<= 2*105
0 <= arr[i] <= 105

Logic:
We start by sorting the array to make it easier to find pairs. Then, we use two pointers: one at the beginning (left) and one at the end (right). We calculate the sum of the numbers at these pointers and check how close it is to the target. If it's the closest sum so far, we store the pair. If there are multiple pairs with the same sum, we choose the one with the larger difference between the numbers. Depending on whether the sum is less than or greater than the target, we move the pointers accordingly to explore other potential pairs. This process continues until we've checked all possible pairs.

