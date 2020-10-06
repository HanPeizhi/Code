Cyclic Sort，循环排序，圈排序

这种模式讲述的是一直很好玩的方法：可以用来处理数组中的数值限定在一定的区间的问题。这种模式一个个遍历数组中的元素，如果当前这个数它不在其应该在的位置的话，咱们就把它和它应该在的那个位置上的数交换一下。你可以尝试将该数放到其正确的位置上，但这复杂度就会是O(n^2)。这样的话，可能就不是最优解了。因此循环排序的优势就体现出来了。

咋鉴别这种模式？这些问题一般设计到排序好的数组，而且数值一般满足于一定的区间如果问题让你需要在排好序/翻转过的数组中，寻找丢失的/重复的/最小的元素经典题目：

Cyclic Sort (easy)

Find the Missing Number (easy)

Find all Missing Numbers (easy)

Find the Duplicate Number (easy)

Find all Duplicate Numbers (easy)



## Reference

[Cycle Sort](https://www.geeksforgeeks.org/cycle-sort/)

[Leetcode 刷題 pattern - Cyclic Sort](https://blog.techbridge.cc/2020/02/16/leetcode-%E5%88%B7%E9%A1%8C-pattern-cyclic-sort/)

https://www.zhihu.com/question/36738189