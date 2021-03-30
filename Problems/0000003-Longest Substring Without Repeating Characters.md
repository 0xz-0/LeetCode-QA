# 3. 无重复字符的最长子串
## Python3
```python
# 暴力
class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        if len(s) <= 1:
            return len(s)
        max_len = 1
        for i in range(len(s)):
            for j in range(i + 1, len(s)):
                if s[j] in s[i:j]:
                    break
                max_len = max(max_len, j - i + 1)
        return max_len
```

