## Pattern: Fast & Slow pointers, 快慢指针类型

这种模式，有一个非常出门的名字，叫龟兔赛跑。咱们肯定都知道龟兔赛跑啦。但还是再解释一下快慢指针：这种算法的两个指针的在数组上（或是链表上，序列上）的移动速度不一样。还别说，这种方法在解决有环的链表和数组时特别有用。

通过控制指针不同的移动速度（比如在环形链表上），这种算法证明了他们肯定会相遇的。快的一个指针肯定会追上慢的一个（可以想象成跑道上面跑得快的人套圈跑得慢的人）。

咋知道需要用快慢指针模式勒？

问题需要处理环上的问题，比如环形链表和环形数组
当你需要知道链表的长度或是某个特别位置的信息的时候
那啥时候用快慢指针而不是上面的双指针呢？

有些情形下，咱们不应该用双指针，比如我们在单链表上不能往回移动的时候。一个典型的需要用到快慢指针的模式的是当你需要去判断一个链表是否是回文的时候。

## 经典题目：

- [x] LinkedList Cycle (easy)

Middle of the LinkedList (easy)

Start of LinkedList Cycle (medium)

Happy Number (medium)

## Reference

[双指针技巧总结](https://github.com/labuladong/fucking-algorithm/blob/master/%E7%AE%97%E6%B3%95%E6%80%9D%E7%BB%B4%E7%B3%BB%E5%88%97/%E5%8F%8C%E6%8C%87%E9%92%88%E6%8A%80%E5%B7%A7.md)

[常见链表问题](https://leetcode-cn.com/problems/linked-list-cycle/solution/yi-wen-gao-ding-chang-jian-de-lian-biao-wen-ti-h-2/)