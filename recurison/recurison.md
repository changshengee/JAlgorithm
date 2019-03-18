# 递归

## 定义

函数用他自己来定义

## 递归的四条基本法则

1.基准情形：某些情况，无需递归就能解出
2.不断推进：对于那些需要递归求解的情形，每次递归调用都必须要使状况朝某一种基准情形推进
3.设计法则：假设所有的递归调用都能运行
4.合成效益法则：在求解一个问题的同一实例时，切勿在不同的递归调用中做重复性动作。

## 具体实例

操作系统的目录结构

## 1.4.1 线性递归

### 定义：

算法可能朝着更深一层自我调用，且每一递归实例对自身对多调用一次，于是，
每一层次上至多有一个实例，且他们之间构成一个线性的次序关系。

### 减而治之

递归每深入一层，待求解问题的规模都缩减一个常数

### [代码](/SumArray.java)

```
import org.junit.Test;

/**
 * 数组求和递归算法
 *
 * @author changshengee
 * @date 2019/02/19
 **/
public class SumArray {

  /**
   * 数组 前n个数 求和算法 线性递归版
   *
   * @param arr 数组
   * @param n   求和个数
   * @return 求和值
   */
  public int sum(int[] arr, int n) {
    if (n < 1) {
      // 平凡情况，递归基 -》直接计算
      return 0;
    } else {
      //一般情况 计算前n-1项之和，再加上第n项（arr[n-1]）
      return sum(arr, n - 1) + arr[n - 1];
    }
  }
```

## 递归分析

递归跟踪 递归方程

## 递归模式

### 多