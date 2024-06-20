---
abbrlink: ''
categories: []
date: '2024-06-20T16:27:50.050579+08:00'
tags: []
title: ML
updated: '2024-06-20T16:28:48.080+08:00'
---
# 人工智能、机器学习和深度学习

机器学习是人工智能的一个实现途径

深度学习是机器学习的一个方法发展而来的

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/6d2fb3c8-ffce-432d-bc22-14ff366f3a67/Untitled.png)

# 机器学习

## 定义

从`数据`中`自动分析获取模型`，并利用`模型`对未知数据进行`预测`

## 工作流程

1. 获取数据
2. 数据基本处理
3. 特征工程
4. 机器学习（模型训练）
5. 模型评估（AB test）

## 数据集

在数据集中：

* 一行数据称为样本
* 一列数据称为特征
* 有些数据有目标值（标签值），有些数据没有目标值

数据类型构成：

* 数据类型一：特征值+目标值（目标值分为离散还是连续）
* 数据类型二：只有特征值，没有目标值

数据划分：

* 训练数据（训练集）—— 构建模型
  * 0.7 - 0.8
* 测试数据（测试集）—— 模型评估
  * 0.2 - 0.3

## 数据基本处理

对数据进行缺失值，异常值进行处理

## 特征工程

### 定义

把数据转换为机器更容易识别的数据

### 为什么需要特征工程

数据和特征决定机器学习的上限，而模型和算法只是逼近这个上限而已

### 包含内容（特征提取、特征预处理、特征降维）

* 特征提取
  * 将数据转换为可用于机器学习的数字特征
* 特征预处理
  * 通过一些`转换函数`将特征数据`转变为更加适合算法模型`的特征数据
* 特征降维
  * 在某些限定条件下，降低随机变量(特征)个数，得到一组“不相关”主变量的过程

## 机器学习

选择合适的算法对模型进行训练

## 模型评估

对训练好的模型进行评估

# 机器学习算法

## 监督学习（特征值和目标值，有标准答案）

输入数据是由输入特征值和目标值所组成

* 输出是连续的值（回归问题：预测房价）
  ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/2181811a-b758-417e-9ece-d215124e0c1e/Untitled.png)
* 输出是有限个离散值（分类问题：判断肿瘤是良性还是恶性）
  ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/bb425274-f782-42c8-a700-8b87cc71cb26/Untitled.png)

## 无监督学习（仅特征值，无标准答案）

输入数据是由输入特征值所组成

* 输出是对样本集进行分类（聚类）

## 半监督学习（有特征值，但是一部分有目标值，一部分没有目标值）

训练集同时包含了标记样本数据和未标记样本数据

## 强化学习（动态过程，上一步数据的输出是下一步数据的输入）

自动进行决策，并且可以做连续决策。目标是获得最多的累计奖励

四要素：agent、action、environment、reward

> 例如： ⼩孩就是 **agent**，他试图通过采取**⾏动**（即⾏⾛）来操纵**环境**（⾏⾛的表⾯），并且从**⼀个状态转变到另⼀个状态**（即 他⾛的每⼀步），当他完成任务的⼦任务（即⾛了⼏步）时，孩⼦得到**奖励**（给巧克⼒吃），并且当他不能⾛路时，就 不会给巧克⼒

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/c7fc4265-8778-49e0-8192-c75a65df8a74/Untitled.png)

# 模型评估

## 分类模型评估

### 准确率

* 预测正确的数 占 样本总数 的比例

### 精确率——查的准

* 正确预测为正 占 全部预测为正 的比例

### 召回率——查的全

* 正确预测为正 占 全部正样本 的比例

### F1-score——评估模型的稳定性

### AUC指标

* 评估样本不均衡的情况

## 回归模型评估

### 均方根误差（Root Mean Squared Error）RMSE

衡量回归模型误差率的常用公式，仅能比较误差是相同单位的模型

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/6f447276-e140-43b5-8c3d-28782b9b80c6/Untitled.png)

### 相对平方误差（Relative Squared Error）RSE

可以比较误差是不同单位的模型

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/adcbf276-0ebd-4cfe-ab72-5e6e47fc3706/Untitled.png)

### 平均绝对误差（Mean Absolute Error）MAE

仅比较误差是相同单位的模型，与RMSE近似，但误差值相对较小

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/f19ec449-66d5-4c89-b529-d430d675562a/Untitled.png)

### 相对绝对误差（Relative Absolute Error）RAE

可以比较误差是不同单位的模型

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/de994c79-c1a3-4dc0-b62d-81c16a2b14c5/Untitled.png)

### 决定系数（Coefficient of Determination）

决定系数(R^2)回归模型汇总了回归模型的解释度

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/f630be31-e3d5-4af3-8071-cf149a629276/Untitled.png)

## 拟合

### 欠拟合

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/18f5375a-0b6f-4f0e-b9ad-50ff75ef6258/Untitled.png)

### 过拟合

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9fe7a54a-8bce-41ae-8c86-bf9c91adf57c/cb217620-c0d7-47b4-9aa8-251ee71cfadf/Untitled.png)

# **GPU与CPU对⽐**

**什么类型的程序适合在GPU上运⾏？**

* \*\*计算密集型的程序。\*\*所谓计算密集型(Compute-intensive)的程序，就是其⼤部分运⾏时间花在了寄存器运算上， 寄存器的速度和处理器的速度相当，从寄存器读写数据⼏乎没有延时。可以做⼀下对⽐，读内存的延迟⼤概是⼏百个时钟周期；读硬盘的速度就不说了，即便是SSD, 也实在是太慢了。
* \*\*易于并⾏的程序。\*\*GPU其实是⼀种SIMD(Single Instruction Multiple Data)架构， 他有成百上千个核，每⼀个核在 同⼀时间最好能做同样的事情。
