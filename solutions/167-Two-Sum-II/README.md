# [167]. two sum
## Problem Link
[LeetCode 167 - two sum II](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/description/?envType=study-plan-v2&envId=top-interview-150)

## Difficulty
Medium

## Related Topics/Tags
- Array
- two pointer
- etc.

## Problem Description
Given a 1-indexed array of integers numbers that is already sorted in non-decreasing order, find two numbers such that they add up to a specific target number. Let these two numbers be numbers[index1] and numbers[index2] where 1 <= index1 < index2 <= numbers.length.

Return the indices of the two numbers, index1 and index2, added by one as an integer array [index1, index2] of length 2.

The tests are generated such that there is exactly one solution. You may not use the same element twice.

Your solution must use only constant extra space.

## Examples from Problem
```
Example 1:

Input: numbers = [2,7,11,15], target = 9
Output: [1,2]
Explanation: The sum of 2 and 7 is 9. Therefore, index1 = 1, index2 = 2. We return [1, 2].
Example 2:

Input: numbers = [2,3,4], target = 6
Output: [1,3]
Explanation: The sum of 2 and 4 is 6. Therefore index1 = 1, index2 = 3. We return [1, 3].
Example 3:

Input: numbers = [-1,0], target = -1
Output: [1,2]
Explanation: The sum of -1 and 0 is -1. Therefore index1 = 1, index2 = 2. We return [1, 2].
```

## Pattern Recognition
### Signals
- What in the problem hints at certain patterns?
- What keywords suggest this approach?
- Similar problems this reminds you of?

### Pattern Category
- Which pattern category does this fall under?
- Why this pattern?

## Initial Setup
### Key Variables
- `index1`: number in numbers
- `index2`: greater number in numbers

### Data Structures
- What data structures are needed?
- Why these specific ones?

## Solution Approaches

### Approach 1: [Approach Name]
```javascript
function twoSum(numbers: number[], target: number): number[] {
    let indexOne = 0;
    let indexTwo = numbers.length-1;

    while(indexOne<indexTwo){
        let sum = numbers[indexOne]+numbers[indexTwo];
        if(sum>target){
            indexTwo--;
        }
        else if(sum<target){
            indexOne++;
        }
        else{
            return [indexOne+1, indexTwo+1];
        }
    }
    
};
```

#### Step-by-Step
1. First step...
2. Second step...
3. Third step...

#### Time & Space Complexity
- Time: O(X)
  * Explanation of time complexity
- Space: O(Y)
  * Explanation of space complexity

### Approach 2: [Alternative Approach] (if applicable)
```javascript
// Alternative implementation
```

## Edge Cases & Constraints
- Empty input handling
- Invalid input handling
- Boundary cases
- Size limits
- Other constraints from problem

## Test Cases
1. Basic Case: 
   - Input: xxx
   - Expected: xxx
   - Why this tests core logic

2. Edge Case:
   - Input: xxx
   - Expected: xxx
   - Why this is important

## Related Problems
- [Problem 1](link) - How it's similar/different
- [Problem 2](link) - How it's similar/different

## Personal Notes
- Key insights
- Common mistakes to avoid
- What made this problem tricky
- What to remember for similar problems

## Review & Follow-up
- [ ] Understand the solution completely
- [ ] Time/space complexity analysis clear
- [ ] Can explain to others
- [ ] Solved edge cases
- [ ] Considered alternative approaches
- [ ] Review again in X days

## Tags for Future Reference
#array #two-pointers #etc