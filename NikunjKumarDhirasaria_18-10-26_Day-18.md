# ACM POTD - Day 18

## Problem
A. Stones on the Table (266A)

## Date
18 October 2026

## Problem Description
Given `n` stones arranged in a row, each colored red (`R`), green (`G`), or blue (`B`), find the minimum number of stones to remove so that no two adjacent stones have the same color.

## Approach
Traverse the string from the second character to the end. If the current stone has the same color as the previous stone, increment the removal count. Print the total number of removals.

## Solution

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    int n;
    string s;
    cin >> n >> s;

    int removals = 0;

    for (int i = 1; i < n; i++) {
        if (s[i] == s[i - 1]) {
            removals++;
        }
    }

    cout << removals << '\n';
    return 0;
}
```

## Example

**Input:**
```text
3
RRG
```

**Output:**
```text
1
```

## Complexity
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)

## Accepted Submission
Attach a screenshot of the accepted Codeforces submission here.
<img width="1686" height="1025" alt="Screenshot 2026-10-23 225444" src="https://github.com/user-attachments/assets/8d5fd6e0-7fba-4d46-8ebb-eb5298d8fe17" />
