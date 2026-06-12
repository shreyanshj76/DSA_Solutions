# 121. Best Time to Buy and Sell Stock

Solution:

```c++
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int minPrice = INT_MAX;
        int maxProfit = 0;

        for (int price : prices){
            if (price < minPrice){
                minPrice = price;
            }
            else if (price - minPrice > maxProfit){
                maxProfit = price - minPrice;
            }
        }

        return maxProfit;
    }
};
```