# ACM POTD - Day 6

## Problem
A. Quasi-palindrome (863A)

## Date
6 October 2026

## Problem Description
A number is called quasi-palindromic if some leading zeroes can be
added to make it a palindrome. We need to check whether the given
number is quasi-palindromic.

## Approach
We remove all trailing zeroes from the number because these zeroes can
be matched by adding leading zeroes.

After removing the trailing zeroes, we check whether the remaining
string is a palindrome. If it is a palindrome, we print "YES";
otherwise, we print "NO".

## Solution

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    cin >> s;

    while (!s.empty() && s.back() == '0') {
        s.pop_back();
    }

    string rev = s;
    reverse(rev.begin(), rev.end());

    if (s == rev) {
        cout << "YES\n";
    } else {
        cout << "NO\n";
    }

    return 0;
}
```

## Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)

## Accepted Submission

Proof of accepted submission:<img width="1671" height="927" alt="Screenshot 2026-10-07 024126" src="https://github.com/user-attachments/assets/f1901579-0acc-464f-980f-e8b44b697cb9" />
