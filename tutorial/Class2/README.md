# Boston Housing Price Prediction using PyTorch

本项目基于 **PyTorch** 实现了一个用于预测波士顿房价的**全连接神经网络（FNN）**模型，并包含完整的数据处理、训练、评估和可视化流程。

## 📌 亮点

- 使用 `sklearn.datasets.fetch_openml` 加载波士顿房价数据集  
- 数据标准化处理，划分训练集与测试集  
- 自定义 PyTorch 数据集 `BostonHousingDataset`  
- 构建简单的前馈神经网络 `FNN`  
- 训练过程中的损失可视化  
- 打印计算图结构以辅助调试  

## 📦 依赖环境

建议使用 Python 3.9，以下是所需的主要依赖库：

```
torch
scikit-learn
matplotlib
numpy
```

可以询问大模型该如何配置本项目的环境

## 🚀 如何运行

在终端运行主程序：

```
python FNN_with_PyTorch.py
```

程序将：

1. 加载并标准化波士顿房价数据  
2. 构建并训练一个简单的全连接神经网络  
3. 输出每轮训练和测试的均方误差（MSE）损失  
4. 绘制训练和测试损失曲线  
5. 打印最后一轮的反向传播计算图结构（可选）  

## 📈 模型结构

```
输入层 (13维) →
全连接层 (64维) →
ReLU 激活 →
全连接层 (1维输出)
```

## 📊 可视化示例

训练过程结束后，会弹出如下损失曲线图：

- 蓝线：训练损失  
- 红线：测试损失  

## 🧠 补充说明

- 解除line107-108以及line153-159注释后，可以打印出最后一次反向传播过程的计算图

## 📚 数据来源

- 数据集来自 [OpenML - boston](https://www.openml.org/d/531)，包含 506 条数据，13 个特征，1 个目标值（房价）  
