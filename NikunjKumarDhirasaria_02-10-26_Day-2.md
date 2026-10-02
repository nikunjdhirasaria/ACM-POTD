# ACM POTD - Day 2

## Problem
A. Flag (16A)

## Date
2 October 2026

## Problem Description
We need to check whether the given grid represents a valid flag.
Each row must contain the same colour, and two adjacent rows must
have different colours.

## Approach
For every row, we check that all characters are the same.

Then, we compare each row with the previous row. Since every row
contains only one colour, checking the first character of adjacent
rows is sufficient.

If any row contains different characters or two adjacent rows have
the same colour, we print NO. Otherwise, we print YES.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    vector<string> flag(n);

    for (int i = 0; i < n; i++) {
        cin >> flag[i];
    }

    for (int i = 0; i < n; i++) {
        for (int j = 1; j < m; j++) {
            if (flag[i][j] != flag[i][j - 1]) {
                cout << "NO\n";
                return 0;
            }
        }

        if (i > 0 && flag[i][0] == flag[i - 1][0]) {
            cout << "NO\n";
            return 0;
        }
    }

    cout << "YES\n";

    return 0;
}
```

## Complexity

- Time Complexity: O(n × m)
- Space Complexity: O(n × m)

## Accepted Submission

Proof of accepted submission:<img width="1602" height="907" alt="Screenshot 2026-10-02 234718" src="https://github.com/user-attachments/assets/a298fdb3-d686-42cc-ae1f-2402a2792d8d" />
