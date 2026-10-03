# ACM POTD - Day 3

## Problem
A. Second Order Statistics (22A)

## Date
3 October 2026

## Approach
First, sort the given sequence in ascending order. The first element
is the minimum. Then, find the first element after it that is different
from the minimum. This is the second smallest distinct element.

If no different element exists, print `NO`.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> a(n);

    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    sort(a.begin(), a.end());

    int minimum = a[0];

    for (int i = 1; i < n; i++) {
        if (a[i] != minimum) {
            cout << a[i] << '\n';
            return 0;
        }
    }

    cout << "NO\n";

    return 0;
}
```

## Complexity

- Time Complexity: O(n log n)
- Space Complexity: O(n)

## Accepted Submission

Proof of accepted submission:<img width="1731" height="937" alt="Screenshot 2026-10-03 234700" src="https://github.com/user-attachments/assets/d1e8ff8b-fce3-43f5-85de-bc27138121aa" />
