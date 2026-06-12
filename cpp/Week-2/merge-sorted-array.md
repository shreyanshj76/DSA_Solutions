# 88. Merge Sorted Array

Solution:

```c++
class Solution {
public:
    void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
        for (int i=m, j=0; i<m+n, j<n; i++, j++){
            nums1[i] = nums2[j];
        }
        int size = n+m;

        for (int i=0; i<size; i++){
            int minIdx = i;
            for (int j=i+1; j<size; j++){
                if (nums1[j]<nums1[minIdx]){
                    minIdx = j;
                }
                swap(nums1[i], nums1[minIdx]);
            }
        }
    }
};
```