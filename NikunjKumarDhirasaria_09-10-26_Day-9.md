# ACM POTD - Day 9

## Problem
A. Triangular Numbers (47A)

## Date
9 October 2026

## Problem Description
Given an integer n, determine whether it is a triangular number.

A triangular number can be represented as k * (k + 1) / 2 for some positive integer k.

## Approach
We check triangular numbers using the formula k * (k + 1) / 2.

If any calculated triangular number equals n, we print "YES". If it exceeds n without finding a match, we print "NO".

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    for (int k = 1; k <= n; k++) {
        int triangular = k * (k + 1) / 2;

        if (triangular == n) {
            cout << "YES\n";
            return 0;
        }

        if (triangular > n) {
            break;
        }
    }

    cout << "NO\n";
    return 0;
}
```

## Complexity
- Time Complexity: O(√n)
- Space Complexity: O(1)

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1735" height="925" alt="Screenshot 2026-10-09 235556" src="https://github.com/user-attachments/assets/699695b5-15d9-476d-b8dd-0fb9392d20ab" />
