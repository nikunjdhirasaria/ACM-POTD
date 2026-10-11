# ACM POTD - Day 10

## Problem
A. Sleuth (49A)

## Date
10 October 2026

## Problem Description
Given a question represented by a line of text, determine whether its answer is "YES" or "NO".

The answer depends on the last letter of the question, ignoring spaces and the question mark. If the last letter is a vowel, including Y, print "YES". Otherwise, print "NO".

## Approach
Read the entire line and traverse it from right to left. Ignore spaces and the question mark. Check whether the first letter encountered is a vowel (A, E, I, O, U, Y). If it is a vowel, print "YES"; otherwise, print "NO".

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    getline(cin, s);

    for (int i = (int)s.size() - 1; i >= 0; i--) {
        char c = tolower(s[i]);

        if (c == ' ' || c == '?') {
            continue;
        }

        if (c == 'a' || c == 'e' || c == 'i' ||
            c == 'o' || c == 'u' || c == 'y') {
            cout << "YES\n";
        } else {
            cout << "NO\n";
        }

        break;
    }

    return 0;
}
```

## Complexity
- Time Complexity: O(n)
- Space Complexity: O(n)

## Accepted Submission
Screenshot of the accepted Codeforces submission is attached below.
<img width="1731" height="855" alt="Screenshot 2026-10-11 100954" src="https://github.com/user-attachments/assets/c33e9f1f-bd43-4fce-82ef-7b0a9158dc43" />
