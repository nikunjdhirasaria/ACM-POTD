# ACM POTD - Day 17

## Problem
A. Is your horseshoe on the other hoof? (228A)

## Date
17 October 2026

## Problem Description
Valera has four horseshoes, each with a particular color. He wants to wear four horseshoes of different colors. Given the colors of his four horseshoes, determine the minimum number of horseshoes he needs to buy.

## Approach
Store the four horseshoe colors in a set. Since a set stores only unique colors, subtract the number of unique colors from four to find how many additional horseshoes Valera needs to buy.

## Solution

```cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    int s1, s2, s3, s4;
    cin >> s1 >> s2 >> s3 >> s4;

    set<int> colors;
    colors.insert(s1);
    colors.insert(s2);
    colors.insert(s3);
    colors.insert(s4);

    cout << 4 - colors.size() << '\n';

    return 0;
}
```

## Example

**Input:**
```text
1 7 3 3
```

**Output:**
```text
1
```

## Complexity
- **Time Complexity:** O(1), as there are always four horseshoes.
- **Space Complexity:** O(1)

## Accepted Submission
Attach a screenshot of the accepted Codeforces submission here.
<img width="1686" height="1025" alt="Screenshot 2026-10-23 225444" src="https://github.com/user-attachments/assets/09a4012b-2292-4b5e-9479-10ea309797a4" />
