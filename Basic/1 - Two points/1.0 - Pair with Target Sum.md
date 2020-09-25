## Pair with Target Sum

类似题目：LeetCode：[1. 两数之和](https://leetcode-cn.com/problems/two-sum/)

给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。

你可以假设每种输入只会对应一个答案。但是，数组中同一个元素不能使用两遍。

示例:

给定 nums = [2, 7, 11, 15], target = 9

因为 nums[0] + nums[1] = 2 + 7 = 9
所以返回 [0, 1]

~~~C++
#include <iostream>
#include <algorithm>

using namespace std;

void findPair(int arr[], int n, int target) {
    int low = 0;
    int high = n - 1;

    // https://blog.csdn.net/w_linux/article/details/76222112
    sort(arr, arr + n);
    for (int i = 0; i < n; i++)
        cout << arr[i]<<" ";

    // 左指针右移，右指针左移，止到左右指针相遇
    // 若左右的和大于target，则右指针左移，因为要让和变小，又因为数组是增序
    // 若左右的和小于target，则左指针右移，因为要让和变大，更接近target值
    // 因为题目只会对应一个答案，所以不出现没有答案的情况，无所谓返回或输出错误
    while (low < high) {
        int sum = arr[low] + arr[high];
        if (sum == target) {
            cout << endl << "[" << low << ", " << high << "]" << endl;
            cout << "{" << arr[low] << ", " << arr[high] << "}" << endl;
            return;
        }

        if (sum > target)
            high--;
        else low++;

    }
    // return -1;
}

// Driver code
int main() {
    //int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    //int arr[] = {-1, -2, -3, -4, -5, -6, -7, -8, -9, -10};
    int arr[] = {8, 7, 2, 5, 3, 1};
    int n = sizeof(arr) / sizeof(arr[0]);
    int target = 4;

    findPair(arr, n, target);


    return 0;
}
~~~



- [ ] 用Hash，Map



## Reference

[1](https://www.techiedelight.com/find-pair-with-given-sum-array/)

[2](https://www.geeksforgeeks.org/count-pairs-with-given-sum/) Count pairs with given sum

[3](https://leetcode.com/discuss/interview-question/356960) Amazon | OA 2019 | Find Pair With Given Sum

 

