# ACM POTD - Day 13

## Problem
A. Petya and Strings (112A)

## Date
13 October 2026

## Problem Description
Given two strings of equal length, compare them lexicographically without considering the case of their letters.

Print -1 if the first string is smaller, 1 if it is greater, and 0 if both strings are equal.

## Approach
Convert both strings to lowercase and compare them lexicographically.

- If the first string is smaller, print -1.
- If the first string is greater, print 1.
- If both strings are equal, print 0.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string a, b;
    cin >> a >> b;

    for (char &c : a) {
        c = tolower(c);
    }

    for (char &c : b) {
        c = tolower(c);
    }

    if (a < b) {
        cout << -1 << '\n';
    } else if (a > b) {
        cout << 1 << '\n';
    } else {
        cout << 0 << '\n';
    }

    return 0;
}
```

## Example

Input:
```text
abs
Abz
```

Output:
```text
-1
```

## Complexity
- Time Complexity: O(n)
- Space Complexity: O(1) auxiliary space

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1777" height="945" alt="Screenshot 2026-10-13 235124" src="https://github.com/user-attachments/assets/dd93f116-c169-4c7d-835c-3a6910844ba5" />
