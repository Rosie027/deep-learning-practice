# 机器学习与深度学习实践

本仓库汇总三个连续学习阶段：鸢尾花传统分类、猫狗图像 CNN 迁移学习，以及中文文本 LSTM 情感分类。它保留了主要 Notebook 和结果图，原始实验报告、个人信息、重复版本与模型权重不在公开目录中。

## 项目导航

| 子项目 | 方法 | 阶段结果 |
| --- | --- | --- |
| [`iris-classification`](iris-classification/) | KNN、SVM、决策树 | 测试准确率约 91%～100%，受划分与参数影响 |
| [`cat-dog-cnn`](cat-dog-cnn/) | MobileNetV3-Large 迁移学习 | 原始实验记录中的验证准确率 97.80% |
| [`sentiment-lstm`](sentiment-lstm/) | BiLSTM、注意力优化 | 基线约 89.29%，优化实验约 90% |

这些数字来自整理前 Notebook 和实验报告中的历史运行结果。公开 Notebook 已清除本机路径、运行日志和输出，重新运行可能因随机划分、数据版本和硬件环境产生差异。

## 目录结构

```text
deep-learning-practice/
├─ iris-classification/
│  ├─ README.md
│  ├─ notebooks/
│  └─ results/
├─ cat-dog-cnn/
│  ├─ README.md
│  └─ notebooks/
├─ sentiment-lstm/
│  ├─ README.md
│  └─ notebooks/
└─ requirements.txt
```

## 环境

建议使用 Python 3.10，并在独立虚拟环境中安装：

```bash
python -m pip install -r requirements.txt
```

PaddlePaddle 的 CPU/GPU 安装方式与操作系统、CUDA 版本有关。如需要 GPU，请先按对应环境安装 PaddlePaddle，再安装其余依赖。

## 迭代时间线

| 日期 | 阶段 |
| --- | --- |
| 2026-03-12 | 鸢尾花 KNN、SVM、决策树初步实验 |
| 2026-03-17 ～ 2026-03-18 | 参数调整、结果对比和实验总结 |
| 2026-04-14 | 猫狗分类 MobileNetV3 迁移学习整理 |
| 2026-04-14 | 中文情感 BiLSTM 基线与优化实验整理 |
| 2026-10-12 | 合并为学习仓库、去重、脱敏并补充 README |

日期来自现存文件的修改时间和实验记录，不等同于 Git 提交历史。

## 数据与隐私

- 鸢尾花数据直接使用 scikit-learn 内置数据集；
- 猫狗图片和 ChnSentiCorp 数据不随仓库分发；
- 模型权重和提交结果保留在私有归档，需要时可以另行作为 Release 发布；
- 原始课程报告含个人信息，因此公开仓库只保留技术总结。
