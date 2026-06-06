# Palindrome Digit Sum

[Link](https://www.geeksforgeeks.org/problems/sum-of-digit-is-pallindrome-or-not2751/%E2%81%A0%EF%BF%BD)

Solution:

```c++
class Solution {
	public:
	bool isDigitSumPalindrome(int n) {
		// code here
		
		if (n<0) {
			return false;
		}
		
		int sum = 0;
		
		while (n>0) {
			int digit = n%10;
			sum += digit;
			n /= 10;
		}
		
		int org = sum;
		long rev = 0;
		
		while (sum>0) {
			int digit = sum % 10;
			rev = rev * 10 + digit;
			sum /= 10;
		}
		
		if (rev == org) {
			return true;
		}
		else {
			return false;
		}
	}
};
```