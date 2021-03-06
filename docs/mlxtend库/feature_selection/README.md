# feature_selection

<img src=".\img\1289939-20200818162206980-658514880.png" alt="1289939-20200818162206980-658514880" style="zoom:80%;" />

**序列前向选择(SFS，Sequential Forward Selection)**：从空集开始，每次加入一个选最优。
**序列后向选择(SBS，Sequential Backward Selection)**：从全集开始，每次减少一个选最优。



**Embedded**：在嵌入式特征选择中，**特征选择算法**本身作为**组成部分嵌入到学习算法里**。最典型的即决策树算法，如ID3、C4.5以及CART算法等，决策树算法在树增长过程的每个递归步都必须选择一个特征，将样本集划分成较小的子集，选择特征的依据通常是划分后子节点的纯度，划分后子节点越纯，则说明划分效果越好，可见决策树生成的过程也就是特征选择的过程。

**Filter**：过滤式特征选择的**评价标准从数据集本身的内在性质**获得，与特定的学习算法无关，因此具有较好的通用性。通常选择**和类别相关度大的特征或者特征子集**。过滤式特征选择的研究者认为，相关度较大的特征或者特征子集会在分类器上获得较高的准确率。**过滤式特征选择的评价标准**分为四种，即**距离度量、信息度量、关联度度量以及一致性度量**。
优点：算法的通用性强；省去了分类器的训练步骤，算法复杂性低，因而**适用于大规模数据集；可以快速去除大量不相关的特征，作为特征的\*预筛选器\*非常合适**。缺点：由于算法的评价标准独立于特定的学习算法，所选的特征子集在分类准确率方面通常低于Wrapper方法。

**Wrapper**：封装式特征选择是**利用学习算法的性能评价特征子集的优劣**。因此，对于一个待评价的特征子集，Wrapper方法需要**训练一个分类器**，根据分类器的性能对该特征子集进行评价。Wrapper方法中用以评价特征的学习算法是多种多样的，例如**决策树、神经网络、贝叶斯分类器、近邻法、支持向量机**等等。
优点：相对于Filter方法，Wrapper方法找到的特征子集分类性能通常更好。缺点：Wrapper方法选出的特征通用性不强，当**改变学习算法时，需要针对该学习算法重新进行特征选择；由于每次对子集的评价都要进行分类器的训练和测试，所以算法计算复杂度很高**，尤其对于大规模数据集来说，算法的执行时间很长。



参考：

- <a href="https://blog.csdn.net/cymy001/article/details/79169862" target="_blank">特征工程：特征生成，特征选择</a> 

