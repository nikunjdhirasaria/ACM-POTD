# ACM POTD - Day 7

## Problem
A. Army (38A)

## Date
7 October 2026

## Problem Description
We need to find the number of years Vasya needs to rise from rank a
to rank b. The input gives the number of years required to move
between consecutive ranks.

## Approach
To move from rank a to rank b, we add the required years for every
rank transition from a to b - 1.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> d(n);

    for (int i = 1; i < n; i++) {
        cin >> d[i];
    }

    int a, b;
    cin >> a >> b;

    int ans = 0;

    for (int i = a; i < b; i++) {
        ans += d[i];
    }

    cout << ans << '\n';

    return 0;
}
```

## Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)

## Accepted Submission

Proof of accepted submission:<img width="1662" height="895" alt="Screenshot 2026-10-07 235350" src="https://github.com/user-attachments/assets/ae914f23-eb5a-4e05-8e71-75e68283a7d0" />
