# 268. Missing Number

Solution:

```c++
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int result=0, i=0;
        for (i=0; i<nums.size(); i++){
            result = result^i^nums[i];
        }
        return result^i;
    }
};
```