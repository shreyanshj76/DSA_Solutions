# 231. Power of Two

[Link](https://leetcode.com/problems/power-of-two/description/)

Solution:

```c++
class Solution {
public:
    bool isPowerOfTwo(int n) {
        bool flag = true;

        if (n <= 0) {
            return false;
        }

        for (long i = 1; i <= n; i = i * 2) {
            if (n % i != 0) {
                flag = false;
                break;
            }
        }

        return flag;
    }
};
```