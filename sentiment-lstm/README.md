# 中文文本情感分类 LSTM

基于 PaddlePaddle 的中文二分类实验，使用结巴分词、词表构建、序列填充和双向 LSTM 完成正负情感判断，并尝试注意力机制与训练参数优化。

## Notebook

- `notebooks/bilstm-baseline.ipynb`：数据读取、分词、词表、BiLSTM 训练和指标评估；
- `notebooks/bilstm-optimization.ipynb`：学习率调整、结构调整和注意力机制实验。

## 实现流程

```text
ChnSentiCorp → 文本清洗与 jieba 分词 → 词表与定长序列
              → Embedding → BiLSTM/Attention → 全连接分类
              → Accuracy / Precision / Recall / F1
```

历史实验记录中，基线验证准确率约 **89.29%**，优化版本约 **90%**。不同数据划分、词表和随机种子会造成结果波动。

数据集和 `sentiment_lstm.pdparams` 不随仓库分发。建议将数据放入 `data/ChnSentiCorp/`，并统一修改 Notebook 中原有的百度 AI Studio 路径。

完成时间：2026-04-14；公开整理：2026-10-12。
