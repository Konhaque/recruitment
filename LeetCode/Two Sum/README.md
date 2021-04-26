# 1. Two Sum

Given an array of integers, return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.

## Example:

```
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```
function sumNumbers(numbers,value){
  for(var i = 0; i<numbers.length;i++){
     for(var j = i+1; j<numbers.length;j++){     
        var sum = numbers[i]+numbers[j];
        if(sum == value) return [i,j];
    }  
}

}

sumNumbers([2,7,11,15],18);
 
