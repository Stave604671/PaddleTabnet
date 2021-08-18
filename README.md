# 《TabNet: Attentive Interpretable Tabular Learning》Paddle实现
## 论文摘要
新型的高性能、可解释的深度表格数据学习结构TabNet。TabNet在每个决策步骤中使用顺序注意力来选择要进行推理的特征，当学习能力用于最显著的特征时，可以实现可解释性和更有效的学习。
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
