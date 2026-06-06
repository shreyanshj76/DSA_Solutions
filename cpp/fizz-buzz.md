# 412. Fizz Buzz

[Link](https://leetcode.com/problems/fizz-buzz/description/)

Solution:

```c++
class Solution {
public:
    vector<string> fizzBuzz(int n) {
        vector<string> arr(n);

        for (int i = 1; i <= n; i++) {
            if (i % 3 == 0 && i % 5 == 0) {
                arr[i - 1] = "FizzBuzz";
            }

            else if (i % 3 == 0) {
                arr[i - 1] = "Fizz";
            }

            else if (i % 5 == 0) {
                arr[i - 1] = "Buzz";
            }

            else {
                arr[i - 1] = to_string(i);
            }
        }

        return arr;
    }
};
```