# 《TabNet: Attentive Interpretable Tabular Learning》Paddle实现
## 模型间接  
　　新型的高性能、可解释的深度表格数据学习结构TabNet。TabNet在每个决策步骤中使用顺序注意力来选择要进行推理的特征，当学习能力用于最显著的特征时，可以兼具可解释性的需求，并可以实现更有效的学习。　　
## 代码结构
--data                        数据集  
----forest-cover-type.gz   
--pytorch_tabnet              Pytorch模型文件  
----abstract_model.py  
----callbacks.py  
----metrics.py  
----multiclass_utils.py  
----multitask.py  
----pretraining.py  
----pretraining_utils.py  
----sparsemax.py  
----tab_model.py  
----tab_network.py  
----utils.py  
--forest_example.ipynb        TabNet Pytorch实现   
## 模型介绍  
　　DNN可以通过拟合一个函数模拟决策树的学习过程,从而构建一个超平面的决策边界。TabNet基于一个tree-like的函数，通过构成系数Mask确定每个特征的比例，具体而言，TabNet构建了一个sequential multi-step的结构，设计了 instance-wise 的特征选择方法。第一step选择professional类的特征，第二step选择Investment类的特征。　　　　
  
　　TabNet网络由多个step的子模块构成，每个step关注不同层面的特征。每个step由Attentive transformer和Feature transformer两大block及一些辅助的运算构成。Attentive transformer作用是输出特征的mask,用于学习每个特征的重要程度，Feature transformer作用是特征的提取，生成对样本属性更有效的表征。　　　　
  　　
 > [TabNet讲解]:　https://zhuanlan.zhihu.com/p/126755362
