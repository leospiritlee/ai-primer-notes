# 第2章 名词分三层：问题、机制、工程

**一句话**：把 `classification` 放进问题层、`loss function` 放进机制层、`deployment` 放进工程层，一团名词就变成三格抽屉。

**为什么需要它**：入门资料常把模型名、指标名、框架名、岗位名混在一起讲。你记住了词，却在读新资料时仍然不知道它重要在哪。三层读法不是为了考试分类，而是为了决定「这个词现在要不要深究」。

**核心结构**：问题层是任务词，如 `classification`、`regression`、`clustering`、`retrieval`、`generation`；机制层是学习词，如 `feature`、`model`、`parameter`、`loss function`、`gradient descent`、`generalization`；工程层是落地词，如 `data pipeline`、`deployment`、`monitoring`、`MLOps`、`model evaluation`。

**关键设计**：三层之间有稳定依赖。不知道任务是什么，就无法选指标；不知道机制，就无法判断工具在做什么；不知道工程，就无法让结果可复现。综合报告口径建议初学按这个顺序投入注意力，而不是按框架热度。

**拆解**：
### 1. 问题层决定指标
`classification` 常看 `accuracy`、`precision`、`recall`、`F1`；`generation` 常看 `BLEU`、`ROUGE` 或人工评测。跨任务搬指标，是入门常见错误。

### 2. 机制层跨框架稳定
`loss function`、`backpropagation`、`optimizer` 这些词不随框架改名。把机制层学好，换 `PyTorch`、`TensorFlow` 或 `JAX` 只是语法差异。

### 3. 工程层变化最快
`deployment`、`monitoring`、`MLOps` 的具体工具年年变，但其职责稳定：让结果可复现、可回滚、可观察。先记职责，再记工具名。

### 4. 出口标准是能归位
给任意一个陌生名词，先判断它属于哪一层；判断不出来，就说明还没读到它的定义句。出口标准：随手挑十个词归层，错不超过两个。

**今天怎么做**：把收藏夹里十个 AI 名词抄下来，逐一写「问题/机制/工程」；发现某层太空，就把下一站作为补层重点。

<div class="chapend" markdown="1">

**容易误解的地方**：以为工具名就是机制名。`Transformers`、`LangChain`、`vLLM` 属于工程实现，不等于背后的学习原理。

**记住这一句**：名词先归层——任务、机制、工程，归不进就回去读定义。

</div>
