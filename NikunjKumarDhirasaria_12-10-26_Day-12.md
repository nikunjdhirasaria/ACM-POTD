# ACM POTD - Day 12

## Problem
A. Word (59A)

## Date
12 October 2026

## Problem Description
Given a word containing uppercase and lowercase English letters, convert it entirely to uppercase or lowercase.

If uppercase letters are more frequent, convert the word to uppercase. Otherwise, convert it to lowercase.

## Approach
Count the uppercase and lowercase letters in the word.

- If uppercase letters are more numerous, convert the entire word to uppercase.
- Otherwise, convert the entire word to lowercase.
- If both counts are equal, choose lowercase.

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    cin >> s;

    int upper = 0, lower = 0;

    for (char c : s) {
        if (isupper(c)) {
            upper++;
        } else {
            lower++;
        }
    }

    if (upper > lower) {
        transform(s.begin(), s.end(), s.begin(), ::toupper);
    } else {
        transform(s.begin(), s.end(), s.begin(), ::tolower);
    }

    cout << s << '\n';

    return 0;
}
```

## Example

Input:
```text
HoUse
```

Output:
```text
house
```

## Complexity
- Time Complexity: O(n)
- Space Complexity: O(n)

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1731" height="885" alt="Screenshot 2026-10-12 235932" src="https://github.com/user-attachments/assets/d9119b92-007b-448d-bcf8-5d30038dfec7" />
