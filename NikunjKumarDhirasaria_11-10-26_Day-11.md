# ACM POTD - Day 11

## Problem
A. Domino Piling (50A)

## Date
11 October 2026

## Problem Description
Given a rectangular board of size M × N and an unlimited number of dominoes of size 2 × 1, find the maximum number of dominoes that can be placed on the board without overlapping.

Each domino covers exactly two squares.

## Approach
Calculate the total number of squares on the board by multiplying M and N.

Since each domino covers two squares, the maximum number of dominoes is the integer division of M × N by 2.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int M, N;
    cin >> M >> N;

    cout << (M * N) / 2 << '\n';

    return 0;
}
```

## Example

Input:
```text
2 4
```

Output:
```text
4
```

## Complexity
- Time Complexity: O(1)
- Space Complexity: O(1)

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1727" height="996" alt="Screenshot 2026-10-11 220449" src="https://github.com/user-attachments/assets/5de1a8c1-cdd5-4514-9dec-4ca8bfce06e2" />
