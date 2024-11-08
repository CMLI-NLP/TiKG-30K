# TiKG-30K: A Tibetan Knowledge Graph Dataset Based on Representation Learning

<div align="center">

[![Paper](https://img.shields.io/badge/paper-ACL%20Anthology-brightgreen)](https://aclanthology.org/2023.ccl-1.13/)
[![Dataset](https://img.shields.io/badge/dataset-TiKG--30K-blue)](https://tikg-30k.cmli-nlp.com/)
[![Conference](https://img.shields.io/badge/conference-CCL%202023-orange)](https://aclanthology.org/volumes/2023.ccl-1/)
[![License](https://img.shields.io/badge/license-CC%20BY%204.0-green)](LICENSE)

</div>

## 项目简介

TiKG-30K 是一个基于表示学习的藏语知识图谱数据集，包含了146,679个三元组、30,986个实体和641种关系。该数据集旨在解决目前藏语等低资源语言缺少公开知识图谱数据集的问题，为藏语知识图谱表示学习及下游任务提供支持。

## 数据集统计

| 数据集分割 | 三元组数量 |
|------------|------------|
| 训练集     | 117,051    |
| 验证集     | 14,820     |
| 测试集     | 14,808     |
| 总计       | 146,679    |

**数据集特点**：
- 实体数量：30,986
- 关系类型：641
- 领域覆盖：地理、文化、历史等
- 数据格式：(头实体, 关系, 尾实体)三元组

## 构建方法

本项目通过以下步骤构建数据集：

1. **数据扩充**：
   - 利用藏文三元组中实体的同指关系
   - 借助其他语言丰富的知识库
   - 使用非文本介质（如地图POI）扩充知识

2. **数据优化**：
   - 跨语言近义词检索
   - 合并同义实体和关系
   - 修正错误三元组
   - 人工审核与优化

## 实验结果

在链接预测任务上，我们使用了多个经典的知识图谱表示学习模型进行评估：

| 模型     | MRR   | Hits@1 | Hits@3 | Hits@10 |
|----------|-------|---------|---------|----------|
| TransE   | 0.496 | 0.419   | 0.548   | 0.625    |
| DistMult | 0.399 | 0.367   | 0.416   | 0.457    |
| ComplEx  | 0.479 | 0.437   | 0.502   | 0.554    |
| RotatE   | 0.529 | 0.483   | 0.553   | 0.612    |
| pRotatE  | 0.526 | 0.468   | 0.557   | 0.630    |
| HAKE     | 0.534 | 0.483   | 0.561   | 0.629    |

## 数据集获取

您可以通过以下方式获取TiKG-30K数据集：

1. 访问官方网站: [https://tikg-30k.cmli-nlp.com/](https://tikg-30k.cmli-nlp.com/)

## 引用

如果您使用了TiKG-30K数据集，请引用我们的论文：

```bibtex
@inproceedings{zhuang2023tikg,
    title={TiKG-30K: 基于表示学习的藏语知识图谱数据集 (TiKG-30K: A Tibetan Knowledge Graph Dataset Based on Representation Learning)},
    author={Zhuang, Wenhao and Gao, Ge and Sun, Yuan},
    booktitle={Proceedings of the 22nd Chinese National Conference on Computational Linguistics},
    pages={145--154},
    year={2023}
}
```

## 相关链接

- [论文链接](https://aclanthology.org/2023.ccl-1.13/)
- [数据集网站](https://tikg-30k.cmli-nlp.com/)

## 许可证

本项目遵循 [Creative Commons Attribution 4.0 International License](LICENSE) 开源协议。

## 联系方式

如有任何问题，欢迎通过以下方式联系我们：

- 邮箱：tracy.yuan.sun@gmail.com

## 免责申明

本数据集/模型仅供学术研究使用。禁止用于任何商业或不道德的目的。
