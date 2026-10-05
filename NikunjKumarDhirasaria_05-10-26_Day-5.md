# ACM POTD - Day 5

## Problem
B. Borze (32B)

## Date
5 October 2026

## Approach
The Borze code represents ternary digits using '.', '-.' and '--'.

- '.' represents 0
- '-.' represents 1
- '--' represents 2

We traverse the string from left to right. If the current character is '.', we output 0. If it is '-', we check the next character to determine whether the digit is 1 or 2.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    cin >> s;

    for (int i = 0; i < s.size(); i++) {
        if (s[i] == '.') {
            cout << 0;
        } else {
            if (s[i + 1] == '.') {
                cout << 1;
            } else {
                cout << 2;
            }
            i++;
        }
    }

    cout << '\n';

    return 0;
}
```

## Complexity

- Time Complexity: O(n)
- Space Complexity: O(1)

## Accepted Submission

Proof of accepted submission:<img width="1726" height="970" alt="Screenshot 2026-10-05 235350" src="https://github.com/user-attachments/assets/17f1eb3b-f595-4919-a6f2-cfa03d15aa2b" />
