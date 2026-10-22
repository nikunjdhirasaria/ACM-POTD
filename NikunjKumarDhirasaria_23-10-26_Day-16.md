# ACM POTD - Day 16

## Problem
A. System of Equations (214A)

## Date
16 October 2026

## Problem Description
Given two integers `n` and `m`, count the pairs of non-negative integers `(a, b)` satisfying both equations:

- \(a^2 + b = n\)
- \(a + b^2 = m\)

## Approach
Iterate through all possible values of `a` and `b` from `0` to `100`. For each pair, check whether both equations are satisfied. If both conditions hold, increment the answer. Finally, print the total number of valid pairs.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    int ans = 0;

    for (int a = 0; a <= 100; a++) {
        for (int b = 0; b <= 100; b++) {
            if (a * a + b == n && a + b * b == m) {
                ans++;
            }
        }
    }

    cout << ans << '\n';
    return 0;
}
```

## Example

**Input:**
```text
9 3
```

**Output:**
```text
1
```

## Complexity
- **Time Complexity:** O(100²)
- **Space Complexity:** O(1)

## Accepted Submission
Attach a screenshot of the accepted Codeforces submission here.
<img width="1780" height="889" alt="Screenshot 2026-10-22 233002" src="https://github.com/user-attachments/assets/b2dc7b91-b1c8-48b0-aed7-604712dd9248" />
