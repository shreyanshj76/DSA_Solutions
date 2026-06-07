# Armstrong No.

Solution:

```c++
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    int org = n;
    int sum = 0;
    
    while (n > 0){
        int digit = n % 10;
        sum += digit * digit * digit;
        n /= 10;
    }
    
    if (sum == org) {
        cout << "It is armstrong no.";
    }
    else {
        cout << "It is not armstrong no.";
    }
    
    return 0;
}
```