## 序：写给刚接触 AI 的人

你大概已经看过很多说法：人工智能、机器学习、深度学习、大模型、Agent、RAG、提示词、微调。每个词都像很关键，可放在一起就成了一团。更让人着急的是，各种学习路线把 Python、线性代数、PyTorch、Transformer、论文、项目一起推到你面前，你不知道哪一步该先走。

这本手册先不让你学全，它先给你一张地图。地图把名词按三层摆好：问题层问「想让机器做什么」，机制层问「机器靠什么做到」，工程层问「怎么把它真的做出来」。然后按一条能走完的十二站路线，把每层最要紧的一组词讲清楚，每站给一个今天就能做的小动作。

**这不是任何一本书的精读，也不是工具教程。** 它是综合整理：以官方术语表和入门教程为一手依据，以本地三本中文 AI 书为交叉参照，再补一份学习方向与路线的综合报告。凡涉及学习顺序、周期、岗位分工和优先级，一律写「综合报告口径」。十二站的顺序、现场场景、速查表和判断清单属于「延伸，非语料原文」，不带行内代码标记。

与已归档的《主流AI技术精读》《AIAgent开发指南》《大模型可解释性精读》分工：那些书各自深入一条线，这本只负责让人看清全局、认得名词、选得出下一步方向。

## AI 全景地图

+----------------------------------------------------------------------+
| AI STARTER: FROM TERMS TO A DIRECTION                                 |
|                                                                      |
| [1] map -> [2] layers -> [3] data -> [4] learning -> [5] training     |
| [6] network -> [7] Transformer -> [8] LLM -> [9] prompt              |
| [10] RAG & agent -> [11] eval & safety -> [12] direction             |
|                                                                      |
| problem layer  -> mechanism layer -> engineering layer               |
+----------------------------------------------------------------------+

这张图不是课程表，而是依赖顺序：不知道 `classification` 与 `generation` 的区别，就不好判断 `accuracy` 和 `BLEU` 为什么不是一回事；没弄清 `training` 与 `inference`，就很难理解为什么 `fine-tuning` 要另备算力；不先认识 `token` 与 `context window`，后面所有提示与检索技巧都会变成玄学。

## 十二站速查表

| 站 | 主题 | 一句话 |
|---|---|---|
| 1 | 画地图 | `Artificial Intelligence` 是目标，`Machine Learning` 是路径，`Deep Learning` 是一类方法 |
| 2 | 名词三层 | `feature` 属机制层，`benchmark` 属评测，`deployment` 属工程 |
| 3 | 数据与特征 | `training set`、`validation set`、`test set` 用途不能混 |
| 4 | 四种学习语法 | `self-supervised learning` 是大模型预训练的常见路线 |
| 5 | 训练回路 | `loss function` 量化差距，`gradient descent` 指导更新 |
| 6 | 神经网络骨架 | `neural network` 是可微计算图，深度不是智能程度 |
| 7 | Transformer | `token`、`embedding`、`attention mechanism` 是三件套 |
| 8 | 大模型 | `fine-tuning` 改参数，`prompt` 只改输入 |
| 9 | 提示与上下文 | `chain-of-thought` 与 `structured output` 是输出组织手段 |
| 10 | RAG 与 Agent | `RAG` 更新知识库，`agent` 管理多步与工具 |
| 11 | 评测与安全 | `hallucination` 与 `alignment` 落在不同层面 |
| 12 | 学习方向 | 按问题类型选五条路，不按框架热度选 |

## 名词的三层读法

问题层的词描述任务：`classification`、`regression`、`clustering`、`generation`、`retrieval`。看到一个新模型，先问它解决哪一类任务。

机制层的词描述模型怎么学：`feature`、`loss function`、`gradient descent`、`backpropagation`、`generalization`、`parameter`、`hyperparameter`。这一层跨框架稳定，学会一次能读很多资料。

工程层的词描述怎么落地：`data pipeline`、`deployment`、`monitoring`、`MLOps`、`model evaluation`。这一层变化最快，应该在机制层之后再系统学，否则只会照抄步骤。

## 语料边界与口径

本地原书（C 级）：《人工智能简史》《深度学习》《深度学习：智能时代的核心驱动力量》三本满文字层中文书，合约 118 万字，用于中文名词的常见说法与历史脉络。

官方术语与教程（A 级）：Google Machine Learning Glossary、scikit-learn Glossary、PyTorch Learn the Basics、Hugging Face LLM Course、NVIDIA AI Glossary、IBM Machine Learning、OWASP LLM Top 10、NIST AI Risk Management Framework，逐字留存正文。

综合报告（B 级）：十二站顺序、学习节奏、岗位方向、优先级与「先学什么」属于综合判断，一律写「综合报告口径」。涉及法规只写公开口径差异，不构成法律意见。

## 症状 → 章节索引

| 症状 | 优先看 |
|---|---|
| 名词都会，串不成一条线 | 第 1、2 章 地图与三层读法 |
| 分不清训练集和测试集 | 第 3 章 数据与特征 |
| 听不懂「自监督」和「微调」的差别 | 第 4、8 章 |
| 看到损失、梯度就跳过 | 第 5 章 训练回路 |
| 把注意力当成模型的眼睛 | 第 7 章 Transformer |
| 提示写了很久仍不稳定 | 第 9 章 提示与上下文 |
| 知识更新就想着重训 | 第 10 章 RAG 与 Agent |
| 不知道该往哪个方向走 | 第 12 章 学习方向与路线图 |