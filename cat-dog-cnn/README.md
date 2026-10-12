# 猫狗图像分类 CNN

基于 PaddlePaddle 与 MobileNetV3-Large 的猫狗二分类实验。项目使用迁移学习完成数据预处理、训练、验证和测试集预测。

## 核心内容

- 自定义 `Dataset` 与 `DataLoader`；
- 图像缩放、归一化和数据增强；
- 使用预训练 MobileNetV3-Large 替换分类头；
- 训练过程记录、验证集评估与预测结果生成。

主 Notebook：`notebooks/cat-dog-mobilenetv3.ipynb`。

原始实验记录中的最终验证准确率为 **97.80%**。公开版清除了训练日志和运行输出，结果需要在准备好数据集后重新复现。

## 数据目录约定

建议将 Kaggle Dogs vs. Cats 数据放入未跟踪的 `data/cat-dog/`，并根据本机目录修改 Notebook 开头的路径配置。数据集和原有 `best_model.pdparams` 不包含在仓库中。

完成时间：2026-04-14；公开整理：2026-10-12。
