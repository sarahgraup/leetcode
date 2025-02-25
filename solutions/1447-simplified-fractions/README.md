# [1447]. simplified fractions

## Problem Link
[LeetCode 1447 - simplified fractions](https://leetcode.com/problems/simplified-fractions/)

## Difficulty
Medium

## Related Topics/Tags
- Array
- String
- etc.

## Problem Description
Given an integer n, return a list of all simplified fractions between 0 and 1 (exclusive) such that the denominator is less-than-or-equal-to n. You can return the answer in any order.

## Examples from Problem
```
Example 1:

Input: n = 2
Output: ["1/2"]
Explanation: "1/2" is the only unique fraction with a denominator less-than-or-equal-to 2.
Example 2:

Input: n = 3
Output: ["1/2","1/3","2/3"]
Example 3:

Input: n = 4
Output: ["1/2","1/3","1/4","2/3","3/4"]
Explanation: "2/4" is not a simplified fraction because it can be simplified to "1/2".
```

## Pattern Recognition
### Signals
- need to generate all fractions with specific constraints
- need to check if fractions are simplified
- need to identify numbers with greatest common divisor of 1
- Similar problems this reminds you of?

### Pattern Category
- greatest common divisor
- need to determine if fractions are simplified which requires checking if numerator and denominator have no common factors

## Initial Setup
### Key Variables
- `result`: array to store simplified fraction strings
- `n`: upper limit for denominators
- `gcd`: helper functino to find greates common divisor

### Data Structures
- What data structures are needed?
- Why these specific ones?

## Solution Approaches

### Approach 1: [Approach Name]
```javascript
var simplifiedFractions = function(n){
    const result = [];

    function gcd(a,b){
        return b===0 ? a: gcd(b, a%b);
    }

    //for loop
    for(let denominator=2; denominator<=n; denominator++){
        for(let numerator=1; numerator<denominator; numerator++){
            if(gcd(numerator, denominator)===1){
                result.push(`${numerator}/${denominator}`);
            }
        }
    }

    return result;

}
```

#### Step-by-Step
(n=4)
1. denominator = 2; 
    - numerator=1
        - gcd(1,2)
            - gcd(2, 1%2->1)
            - gcd(2,1)=> gcd(1,0) ->1
        - gcd is 1 so add '1/2'
2. denominator = 3
    - numerator=1
        - gcd(1,3):
            - gcd(3,1)=> gcd(1,0)->1
        - GCD is 1, so add "1/3"
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