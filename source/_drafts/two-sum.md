package _drafts
---
title: 两数之和
date: 2020-08-26 14:47:09
tags: 
- leetcode
- 算法
---

>来源：力扣（LeetCode）    
>链接：https://leetcode-cn.com/problems/two-sum

### 题目
>给定一个整数数组 nums 和一个目标指 target, 请你在数组中找出和为目标值的两个整数, 返回它们在数组中的下标.      
>你可以假设每种输入只会对应一个答案, 但数组中每个元素只会使用一次.

### 示例
```
给定 nums = [2, 7, 11, 15], target = 9 

因为 nums[0] + nums[1] = 2 + 7 = 9
所以返回 [0, 1]

```

### 思路
```
1.将给定数组按从小到大排序
2.判断目标值是否可能存在
3.循环遍历两个数和是否等于目标值, 相等返回结果, 当和大于目标值时结束当前循环, 进行下次循环
```

### 伪代码
```
sort(nums)
l = len(nums)
if sum(num[0] + num[1]) > target || sum(num[l-1] + num[l-2]) < target {
    return
}

for i:= 0; i < l; i ++ {
    for j = i+1; j < l; j ++ {
        s  :=  sum(num[i]+[j])
        if s == traget {  
            return num[i], num[j]
        }
        if sum > target {   
            continue
        }

    }
}

```

### 实现
```

```