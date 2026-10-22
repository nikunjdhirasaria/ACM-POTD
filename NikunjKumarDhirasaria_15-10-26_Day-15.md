# ACM POTD - Day 15

## Problem
A. Series of Crimes (181A)

## Date
22 October 2026

## Problem Description
Given an n × m grid containing exactly three asterisks (*), find the position of the fourth point such that all four points form a rectangle whose sides are parallel to the grid boundaries.

## Approach
Store the positions of the three asterisks.

Among their row coordinates, the coordinate that appears only once gives the missing point's row. Similarly, among their column coordinates, the coordinate that appears only once gives the missing point's column.

Print these two coordinates.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    vector<pair<int, int>> stars;
    char c;

    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= m; j++) {
            cin >> c;
            if (c == '*') {
                stars.push_back({i, j});
            }
        }
    }

    int r1 = stars[0].first;
    int r2 = stars[1].first;
    int r3 = stars[2].first;

    int c1 = stars[0].second;
    int c2 = stars[1].second;
    int c3 = stars[2].second;

    int row = (r1 == r2) ? r3 : (r1 == r3 ? r2 : r1);
    int col = (c1 == c2) ? c3 : (c1 == c3 ? c2 : c1);

    cout << row << " " << col << '\n';

    return 0;
}
```

## Example

Input:
```text
3 2
.*
..
**
```

Output:
```text
1 1
```

## Complexity
- Time Complexity: O(n × m)
- Space Complexity: O(1), excluding the stored positions.

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1777" height="952" alt="Screenshot 2026-10-22 231705" src="https://github.com/user-attachments/assets/f296edb9-e6f4-4ba2-b072-aed25751cf65" />
