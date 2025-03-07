# [392]. is subsequence

## Problem Link
[LeetCode 392 - is subsequence](https://leetcode.com/problems/is-subsequence/description/?envType=study-plan-v2&envId=top-interview-150)

## Difficulty
Easy

## Related Topics/Tags
- two pointer

## Problem Description
Given two strings s and t, return true if s is a subsequence of t, or false otherwise.

A subsequence of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. (i.e., "ace" is a subsequence of "abcde" while "aec" is not).

## Examples from Problem
```
Example 1:

Input: s = "abc", t = "ahbgdc"
Output: true
Example 2:

Input: s = "axc", t = "ahbgdc"
Output: false
```

## Pattern Recognition
### Signals
- What in the problem hints at certain patterns?
    - subsequece and two strings
- What keywords suggest this approach?
- Similar problems this reminds you of?

### Pattern Category
- Which pattern category does this fall under?
    - two pointers
- Why this pattern?

## Initial Setup
### Key Variables
- `variable1`: purpose/what it tracks
- `variable2`: purpose/what it tracks

### Data Structures
- What data structures are needed?
- Why these specific ones?

## Solution Approaches

### Approach 1: [Approach Name]
```javascript
function isSubsequence(s: string, t: string): boolean {
    if(s.length>t.length){
    return false;
   }
   
    let sPointer = 0;
    let tPointer = 0;
    while(sPointer<s.length && tPointer<t.length){

        if(s[sPointer]!==t[tPointer]){
            tPointer++;
        }else{
            sPointer++;
        tPointer++;

        }
        
    }
    if(sPointer===s.length){
        return true;
    }
    return false;

    
};
```

#### Step-by-Step
1. if we think about it we can do an example of juyst if abc is subsequence of abc
2. so we loop through both and go through each character and compare
3. so then in the example abc and ahbgdc we loop through both start at each string [0]
4. if they are not equal we need to go to the next index of t and check if the character of s equals the character of t. if they do then increase both pointers. 

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