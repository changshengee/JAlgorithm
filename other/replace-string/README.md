#题意
-------
题目描述


请实现一个函数，将一个字符串中的空格替换成“%20”。
例如，当字符串为We Are Happy.则经过替换之后的字符串为We%20Are%20Happy。
>We Are Happy
>
>We%20Are%20Happy

#替换
-------

我们可以考虑**先遍历一遍字符串, 计数空格的数目**, 

我们知道了空格的数目，其实就是知道了替换后字符串的长度，那么只需要进行一次替换就可以了

因为我们的工作变为

*	遍历一遍字符串， 统计字符出现的数目, 计算替换后的字符串长度

*	再遍历一遍字符串，完成替换

[代码如下](./ReplaceString.java)

