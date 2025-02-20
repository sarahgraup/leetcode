# 1768. Merge Strings Alternately

## Problem Link
[LeetCode 1786 - Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/description/?envType=study-plan-v2&envId=leetcode-75)

## Difficulty
Easy

## Related Topics/Tags
- Array
- two pointers

## Problem Description
You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.

## Examples from Problem
```
Example 1:

Input: word1 = "abc", word2 = "pqr"
Output: "apbqcr"
Explanation: The merged string will be merged as so:
word1:  a   b   c
word2:    p   q   r
merged: a p b q c r
Example 2:

Input: word1 = "ab", word2 = "pqrs"
Output: "apbqrs"
Explanation: Notice that as word2 is longer, "rs" is appended to the end.
word1:  a   b 
word2:    p   q   r   s
merged: a p b q   r   s
Example 3:

Input: word1 = "abcd", word2 = "pq"
Output: "apbqcd"
Explanation: Notice that as word1 is longer, "cd" is appended to the end.
word1:  a   b   c   d
word2:    p   q 
merged: a p b q c   d
```

## Pattern Recognition
### Signals
- Need to process two strings simultaneously
- Alternating elements from each string
- Handling remaining characters from longer string
- Sequential access to string characters

### Pattern Category
- Two Pointers / String Manipulation
- Reason: We need to track position in two different strings simultaneously

## Initial Setup
### Key Variables
- `result`: string to store merged result
- `i`: index pointer for iterating through both strings
- `maxLength`: length of longest string to ensure we process all characters

### Data Structures
- Just strings - no complex data structures needed
- Built-in string methods for concatenation

## Solution Approaches

### Approach 1: [Approach Name]
```javascript
var mergeAlternately = function(word1, word2) {
   let result = '';
   let i=0; 
   const maxLength = Math.max(word1.length, word2.length);
   while(i<maxLength){
    if(i<word1.length){
        result+=word1[i];
    }
    if(i<word2.length){
        result+=word2[i];
    }
    i++;
   }
   return result;
    


    
};
```

#### Step-by-Step
1. Initialize empty result string and pointer i
2. Find maxLength to know how long to iterate
3. In each iteration:
    - Add character from word1 if available
    - Add character from word2 if available
    - Increment pointer
4. Return merged result

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
1. Equal Length:
  - Input: word1 = "abc", word2 = "pqr"
  - Expected: "apbqcr"
  - Tests basic alternating merge

2. Different Lengths:
  - Input: word1 = "ab", word2 = "pqrs"
  - Expected: "apbqrs"
  - Tests handling of remaining characters

3. Empty String:
  - Input: word1 = "", word2 = "pqr"
  - Expected: "pqr"
  - Tests edge case with empty string

## Related Problems
- [Problem 1](link) - How it's similar/different
- [Problem 2](link) - How it's similar/different

## Personal Notes
- Key insights: Single pointer can track both strings
- Don't overcomplicate - simple while loop works well
- Array.join() approach might be more readable but less space efficient
- Good starter problem for string manipulation



## Review & Follow-up
- [ ] Understand the solution completely
- [ ] Time/space complexity analysis clear
- [ ] Can explain to others
- [ ] Solved edge cases
- [ ] Considered alternative approaches
- [ ] Review again in X days

## Tags for Future Reference
#string #two-pointers #easy