---
title: DBSCAN算法及其并行化实现
date: 2019-05-29 09:29:40
tags:
---

## DBSCAN算法及其并行化实现

###1.目录
1)目录
2)DBSCAN算法
3)DBSCAN算法的特性
4)DBSCAN算法延伸
一般DBSCAN的实现
kd树, BBD树, r树
5)DBSCAN并行化(MR框架)
6)一款综合性的DBSCAN算法

###2.DBSCAN算法
DBSCAN算法是最著名的基于密度的聚类算法


###3.DBSCAN算法的特性
1)对输入数据的顺序不敏感
2)可以识别任意形状的数据
3)可以识别离群点
缺点:
1)参数敏感
2)不同密度的类簇

###4.DBSCAN算法延伸



###5.DBSCAN算法并行化
目前已经实现的:
https://github.com/alitouka/spark_dbscan
MRDBSCAN-FCS-Feb.2014.pdf

###6.一些应用
``` bash
# 可以的应用方向
## 1.森林火灾

## 2.流行病传播/疫情扩散

## 3.水文/气象监测

## 4.人群检测

## 6.交通数据中的应用
交通拥堵,人流分布

## 7.城市规划

## 8.图像分割/类簇识别

## 9.网络攻击

## 10.文本数据聚类

## 11.其他
天文/医药/客流人群识别/...

# 算法可以做文章的地方
## 1.支持多维度(但并不支持超高维稀疏特征)
## 2.快速的空间切割算法,同时保证负载均衡
## 3.基于分布式图计算的多分区类簇信息合并,基于spark框架实现效率很高
## 4.基于交叠分区的DBSCAN并行化策略,基于spark框架实现效率很高(是别人的观点,但目前还不是很知名,相关文献少)
```



