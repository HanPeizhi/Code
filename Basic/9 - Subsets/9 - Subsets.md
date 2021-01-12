

## [78. 子集](https://leetcode-cn.com/problems/subsets/)

给你一个整数数组 nums ，返回该数组所有可能的子集（幂集）。解集不能包含重复的子集。


示例 1：

输入：nums = [1,2,3]
输出：[[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3]]
示例 2：

输入：nums = [0]
输出：[[],[0]]

~~~C++
class Solution {
public:
    vector<vector<int>> subsets(vector<int>& nums) {
        int n = nums.size();
        int max = 1 << n;   // 2^n
        vector<vector<int> > res;

        for(int mask = 0; mask < max; ++mask){
            vector<int> tmp;
            for(int i = 0; i < n; ++i){
                if(mask & (1 << i)){
                    tmp.push_back(nums[i]);
                }
            }
            res.push_back(tmp);

        } 
        return res;
    }
};
~~~



## Reference:

[1](https://leetcode-cn.com/problems/subsets/solution/zi-ji-by-leetcode-solution/)

[回溯 + 位运算技巧](https://leetcode-cn.com/problems/subsets/solution/hui-su-python-dai-ma-by-liweiwei1419/)

