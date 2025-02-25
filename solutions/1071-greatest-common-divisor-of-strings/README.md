# [1071]. greatest common divisor of strings

## Problem Link
[LeetCode 1071 - greatest common divisor of strings](https://leetcode.com/problems/greatest-common-divisor-of-strings/description/?envType=study-plan-v2&envId=leetcode-75)

## Difficulty
Easy

## Related Topics/Tags
- Array
- String
- etc.

## Problem Description
For two strings s and t, we say "t divides s" if and only if s = t + t + t + ... + t + t (i.e., t is concatenated with itself one or more times).

Given two strings str1 and str2, return the largest string x such that x divides both str1 and str2.

## Examples from Problem
```
Example 1:

Input: str1 = "ABCABC", str2 = "ABC"
Output: "ABC"
Example 2:

Input: str1 = "ABABAB", str2 = "ABAB"
Output: "AB"
Example 3:

Input: str1 = "LEET", str2 = "CODE"
Output: ""
```

## Pattern Recognition
### Signals
- What in the problem hints at certain patterns?
    - strings
    -prefixes 
    - common divisor string for both inputs
    - looking for longest string
- What keywords suggest this approach?
- Similar problems this reminds you of?

### Pattern Category
- Which pattern category does this fall under?
    - string manipulation
    - need to find common substring patterns that divide both strings evenly (greatest common divisor)
- Why this pattern?

## Initial Setup
### Key Variables
- `str1` and `str2`: input strings


### Data Structures
- strings

## Solution Approaches

### Approach 1: [Approach Name]
```javascript
{if(str1+str2 !==str2+str1){
    return '';
}

//get greatest common divisor length
const gcdLength = gcd(str1.length, str2.length);
    // Return the substring of that length (from either string)
    return str1.substring(0, gcdLength);
    }
//helper function 
function gcd(a, b) {
    while (b) {
        let temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}
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
function gcdOfStrings(str1, str2) {
    // Ensure str1 is longer
    if (str1.length < str2.length) {
        return gcdOfStrings(str2, str1);
    }
    
    // Base case (equivalent to b === 0)
    if (str2 === "") {
        return str1;
    }
    
    // Check if str2 is a prefix
    if (str1.substring(0, str2.length) !== str2) {
        return "";
    }
    
    // This is equivalent to a % b in the number version
    return gcdOfStrings(str1.substring(str2.length), str2);
}
```

## Edge Cases & Constraints
- Empty input handling
- Invalid input handling
- Boundary cases
- Size limits
- Other constraints from problem

## Test Cases
1. Basic Case:

Input: str1 = "ABCABC", str2 = "ABC"
Expected: "ABC"
Tests simple divisor case where one string is divisor of other


Common Divisor:

Input: str1 = "ABABAB", str2 = "ABAB"
Expected: "AB"
Tests finding common divisor that's not one of original strings


No Common Divisor:

Input: str1 = "LEET", str2 = "CODE"
Expected: ""
Tests case with no common divisor


Same Strings:

Input: str1 = "ABCD", str2 = "ABCD"
Expected: "ABCD"
Tests case where strings are identical


One Empty String:

Input: str1 = "", str2 = "ABC"
Expected: ""
Tests edge case with empty string

## Related Problems
- [Problem 1](link) - How it's similar/different
- [Problem 2](link) - How it's similar/different

## Personal Notes
- Key insights
- if two strings have common divisor, their concatenation in either order will be identical
- mathematical gcd of lengths give us the length of largest common divisor
- remember to check if a common divisor exists before calculating


## Review & Follow-up
- [ ] Understand the solution completely
- [ ] Time/space complexity analysis clear
- [ ] Can explain to others
- [ ] Solved edge cases
- [ ] Considered alternative approaches
- [ ] Review again in X days

## Tags for Future Reference
#string #math #gcd #pattern-matching #string-manipulation