# ACM POTD - Day 14

## Problem
A. Next Round (158A)

## Date
14 October 2026

## Problem Description
Given the scores of n participants and an integer k, determine how many participants advance to the next round.

A participant advances if their score is at least the score of the participant ranked kth and their score is positive.

## Approach
1. Read the number of participants n and the position k.
2. Store all participants' scores in an array.
3. Find the score of the participant at position k using a[k - 1].
4. Count participants whose scores are greater than or equal to the kth score and greater than zero.
5. Print the final count.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, k;
    cin >> n >> k;

    vector<int> a(n);

    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    int count = 0;

    for (int i = 0; i < n; i++) {
        if (a[i] >= a[k - 1] && a[i] > 0) {
            count++;
        }
    }

    cout << count << '\n';

    return 0;
}
```

## Example

Input:
```text
8 5
10 9 8 7 7 7 5 5
```

Output:
```text
6
```

## Complexity
- Time Complexity: O(n)
- Space Complexity: O(n)

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1780" height="952" alt="Screenshot 2026-10-14 213728" src="https://github.com/user-attachments/assets/9dd98a62-6f7d-401f-9949-2b092516a233" />
