# ACM POTD - Day 8

## Problem
A. Greed (892A)

## Date
8 October 2026

## Problem Description
Jafar has several cans containing some amount of cola. Each can also
has a maximum capacity. We need to determine whether all the remaining
cola can be poured into only two cans.

## Approach
First, calculate the total amount of remaining cola in all cans.

Then, find the two cans with the largest capacities. These two cans
provide the maximum possible combined capacity.

If their combined capacity is at least the total amount of cola,
then all the cola can fit into two cans and the answer is "YES".
Otherwise, the answer is "NO".

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<long long> a(n), b(n);

    long long total = 0;

    for (int i = 0; i < n; i++) {
        cin >> a[i];
        total += a[i];
    }

    for (int i = 0; i < n; i++) {
        cin >> b[i];
    }

    sort(b.rbegin(), b.rend());

    if (b[0] + b[1] >= total) {
        cout << "YES\n";
    } else {
        cout << "NO\n";
    }

    return 0;
}
```

## Complexity

- Time Complexity: O(n log n)
- Space Complexity: O(n)

## Accepted Submission

Proof of accepted submission:<img width="1666" height="956" alt="Screenshot 2026-10-08 235553" src="https://github.com/user-attachments/assets/6b084b69-1cce-49cc-ad75-8bd77b6dceaa" />
