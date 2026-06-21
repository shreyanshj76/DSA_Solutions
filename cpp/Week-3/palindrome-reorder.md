# Palindrome Reorder

Solution:

```c++
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main(){
    string s;
    cin >> s;

    vector<int> freq(26, 0);

    for (char c : s){
        freq[c - 'A']++;
    }
    int oddCount = 0;
    char oddChar = '\0';

    for (int i=0; i<26; i++){
        if (freq[i] % 2){
            oddCount++;
            oddChar = 'A' + i;
        }
    }

    if (oddCount > 1){
        cout << "NO SOLUTION\n";
        return 0;
    }

    string firstHalf = "";
    string middle = "";

    for (int i=0; i<26; i++){
        firstHalf.append(freq[i]/2, 'A'+i);

        if (freq[i] % 2){
            middle.append(freq[i], 'A'+i);
        }
    }

    string secondHalf = firstHalf;
    reverse(secondHalf.begin(), secondHalf.end());

    cout << firstHalf + middle + secondHalf << '\n';
    return 0;
}
```