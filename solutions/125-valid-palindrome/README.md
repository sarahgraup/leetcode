# [125]. valid palindrome

## Problem Link
[LeetCode 125 - valid palindrome](https://leetcode.com/problems/valid-palindrome/?envType=study-plan-v2&envId=top-interview-150)

## Difficulty
Easy

## Related Topics/Tags
- two pointers

## Problem Description
A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

Given a string s, return true if it is a palindrome, or false otherwise.

## Examples from Problem
```
Example 1:

Input: s = "A man, a plan, a canal: Panama"
Output: true
Explanation: "amanaplanacanalpanama" is a palindrome.
Example 2:

Input: s = "race a car"
Output: false
Explanation: "raceacar" is not a palindrome.
Example 3:

Input: s = " "
Output: true
Explanation: s is an empty string "" after removing non-alphanumeric characters.
Since an empty string reads the same forward and backward, it is a palindrome.
```

## Pattern Recognition
### Signals
- What in the problem hints at certain patterns?
    - palindrome- two pointers
- What keywords suggest this approach?
    - palindrome
- Similar problems this reminds you of?

### Pattern Category
- Which pattern category does this fall under?
- Why this pattern?

## Initial Setup
### Key Variables
- `start`: start of palindrome
- `end`: end of string (two pointers)

### Data Structures
- What data structures are needed?
- Why these specific ones?

## Solution Approaches

### Approach 1: [Approach Name]
```javascript
function isPalindrome(s: string): boolean {
    
    
let sArr = s.toLowerCase().split('').filter(char=>char.match(/[0-9A-Za-z]/));
let start=0;
let end = sArr.length-1;

    while(start<=end){
        if(sArr[start]!==sArr[end]){
            return false;
        }
        start++;
        end--;
    }
    return true;
    
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
- only numbers and letters
- space ('') is valid palindrome

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