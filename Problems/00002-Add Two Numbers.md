# 2. 两数相加

## Python3
```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:
        num1_char = ''
        num2_char = ''
        while l1 is not None:
            num1_char += str(l1.val)
            l1 = l1.next
        while l2 is not None:
            num2_char += str(l2.val)
            l2 = l2.next
        num1 = int(num1_char[::-1])
        num2 = int(num2_char[::-1])
        total_char = str(num1+num2)
        total_char = total_char[::-1]
        ln_list = list()
        for i in range(len(total_char)):
            value = total_char[i]
            ln_list.append(ListNode(int(value)))
        for x in range(len(ln_list)-1):
            ln_list[x].next = ln_list[x+1]
        return ln_list[0]         
```
