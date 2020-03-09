### Algorithm

1. Create a map that store the the value and its' index.
2. When we iterate and insert elments into the map, also check if current element's complement already exists in the map. If it exists, return the index.

### Solutions

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    const map ={};
    for(let i=0;i<nums.length-1;i++){
        map[target-nums[i]] = i;
        if(nums[i+1] in map){
            return [map[nums[i+1]],i+1];
        }
    }
};
```