# ACM POTD - Day 4

## Problem
A. Holidays (670A)

## Date
4 October 2026

## Approach
A week consists of 5 working days and 2 holidays.

First, we calculate the number of complete weeks using n / 7.
Each complete week contributes exactly 2 holidays.

For the remaining days:
- The minimum number of holidays is obtained by placing the remaining days on working days as much as possible.
- The maximum number of holidays is obtained by taking as many of the remaining days as possible from the two holiday days.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int weeks = n / 7;
    int rem = n % 7;

    int minimum = weeks * 2 + max(0, rem - 5);
    int maximum = weeks * 2 + min(rem, 2);

    cout << minimum << " " << maximum << '\n';

    return 0;
}
```

## Complexity

- Time Complexity: O(1)
- Space Complexity: O(1)

## Accepted Submission

Proof of accepted submission:<img width="1682" height="1007" alt="Screenshot 2026-10-04 235339" src="https://github.com/user-attachments/assets/e06e54a6-46ef-4b97-8139-ae14fcaf0b5f" />
