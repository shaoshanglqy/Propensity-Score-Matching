# Propensity-Score-Matching

### Description

 PSM 是一种样本匹配方法，它可以有效的消除组别之间的干扰因素，避免在无法进行随机选择情况下时两组样本之间的selection bias。
  
  在理想情况下，两组样本的各个可观测变量应该相似才能避免在比较这两组样本时由这些可观测变量X的不同所带来的选择性偏差。解决这种选择性偏差的一种方法是X数量很少，我们可通过观测来进行人工匹配；另一种方法是进行完全随机，使样本分布满足大数定律，以消除这些变量对两组样本带来的影响。但是在实际情况下，很多时候变量X的数量较多，无法通过人工匹配，并且实验环境难以进行随机抽样，此时我们可以使用PSM，即倾向性评分匹配的方法来取出两组数量相同的样本。

### 算法步骤
通过降维将X从多维变为1维，并采用logistic Regression方法来得到每个样本的Propensity Score，然后进行得分匹配，最常用的匹配方法为最邻近匹配法(Nearest Neighbor Matching, NNM)

参考：
python：https://github.com/benmiroglio/pymatch
R：https://datascienceplus.com/how-to-use-r-for-matching-samples-propensity-score
