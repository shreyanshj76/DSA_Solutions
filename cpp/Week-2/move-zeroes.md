# 283. Move Zeroes

Solution:

```c++
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        //0,1,0,3,12
        //1,0,0,3,12

        int j=0;
        for (int i=0; i<nums.size(); i++){
            if (nums[i] != 0){
                nums[j] = nums[i];
                j++;
            }
        }
        for (; j<nums.size(); j++){
            nums[j] = 0;
        }
    }
};
```