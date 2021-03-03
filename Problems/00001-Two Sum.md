# 1. 两数之和
## 注意事项
* 容易超时
## Python3
```python
# 解法一
# 运用python的内置函数
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            other_ = target - nums[i]
            if other_ in nums[i+1:]:
                return [i,(nums[i+1:].index(other_)+i+1)]
```

