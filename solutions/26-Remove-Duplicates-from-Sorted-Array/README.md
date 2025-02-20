# 26. Remove Duplicates from Sorted Array

## Problem Link
[LeetCode 26 - Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)

## Pattern Recognition
### Signals
- Array is sorted (non-decreasing)
- In-place modification
- Need to track unique elements
- Need to maintain relative order

### Pattern Category
- Two Pointers (slow and fast pointer)
- Array In-place Modification

## Initial Setup
### Key Variables
- `slow`: Points to position where next unique element should go
- `fast`: Scans through array to find unique elements

## Solution
```javascript
var removeDuplicates = function(nums) {
    if (nums.length === 0) return 0;
    
    let slow = 0; // position for next unique element
    
    // Start fast pointer from 1 since first element is always in place
    for (let fast = 1; fast < nums.length; fast++) {
        // If we find a number different from what's at slow pointer
        if (nums[fast] !== nums[slow]) {
            slow++; // move slow pointer forward
            nums[slow] = nums[fast]; // place the new number
        }
    }
    
    return slow + 1; // length is one more than last index
};
```

## Step-by-Step Walkthrough
Using example: [1,1,2]

1. Initial state:
   - nums = [1,1,2]
   - slow = 0 (pointing to first 1)
   - fast = 1

2. First iteration:
   - fast points to second 1
   - nums[fast] === nums[slow], so skip

3. Second iteration:
   - fast points to 2
   - nums[fast] !== nums[slow]
   - increment slow (now 1)
   - place nums[fast] at slow position
   - nums becomes [1,2,2]

4. Return slow + 1 = 2 (length of unique elements)

## Edge Cases
- Empty array: return 0
- Single element: return 1
- No duplicates: everything gets copied
- All duplicates: only first element kept

## Time & Space Complexity
- Time: O(n) - single pass through array
- Space: O(1) - in-place modification, no extra space

## Test Cases
```javascript
console.log(removeDuplicates([1,1,2])) // 2, nums becomes [1,2,_]
console.log(removeDuplicates([0,0,1,1,1,2,2,3,3,4])) // 5, nums becomes [0,1,2,3,4,_,_,_,_,_]
console.log(removeDuplicates([1])) // 1, nums stays [1]
console.log(removeDuplicates([1,2,3])) // 3, nums stays [1,2,3]
```

## Common Mistakes
1. Not handling empty array case
2. Incorrect pointer manipulation
3. Not returning correct length
4. Moving slow pointer incorrectly

## Solution Pattern Tips
- Use slow pointer for placement position
- Use fast pointer for scanning
- Only move slow pointer when finding unique element
- Remember to return slow + 1 for length