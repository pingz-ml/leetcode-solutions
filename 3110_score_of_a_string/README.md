# 3110. Score of a String

## Solution

```cpp
#include <iostream>
#include <string>
#include <numeric>

void init() {
    std::ios_base::sync_with_stdio(false);
    std::cin.tie(nullptr);
    std::cout.tie(nullptr);
}

class Solution {
public:

    int scoreOfString(const std::string& s) {
        init();

        int sum = 0;
        for (
            std::string::const_iterator p = s.begin(), q = p + 1;
            q != s.end();
            ++p, ++q
        ) {
            sum += std::abs(*p - *q);
        }

        return sum;
    }
};
```

## Rank

![Rank](rank.jpg)

## Time Complexity

![Time complexity](time_complexity.jpg)
