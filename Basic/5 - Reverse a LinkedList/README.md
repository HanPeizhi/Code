## 6. Pattern: In-place Reversal of a LinkedList，链表翻转

在众多问题中，题目可能需要你去翻转链表中某一段的节点。通常，要求都是你得原地翻转，就是重复使用这些已经建好的节点，而不使用额外的空间。这个时候，原地翻转模式就要发挥威力了。

这种模式每次就翻转一个节点。一般需要用到多个变量，一个变量指向头结点（下图中的current），另外一个（previous）则指向咱们刚刚处理完的那个节点。在这种固定步长的方式下，你需要先将当前节点（current）指向前一个节点（previous），再移动到下一个。同时，你需要将previous总是更新到你刚刚新鲜处理完的节点，以保证正确性。

![img](https://pic2.zhimg.com/50/v2-79af44147f0e31ef768b8867a43acac5_hd.jpg?source=1940ef5c)

咱们怎么去甄别这种模式呢？如果你被问到需要去翻转链表，要求不能使用额外空间的时候经典题目：

Reverse a LinkedList (easy)

Reverse a Sub-list (medium)

Reverse every K-element Sub-list (medium)

## Reference

[LeetCode按照怎样的顺序来刷题比较好？](https://www.zhihu.com/question/36738189)