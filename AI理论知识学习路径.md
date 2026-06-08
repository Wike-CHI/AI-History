# AI 理论知识系统学习路径

> 目标：本科水平 AI 理论功底 — 数学基础 + CS 核心 + ML/DL 理论
> 所有教材均为国内外大学标准教材，基于出版社官网与高校课程大纲核实

---

## 全景路线图

```
┌─────────────────────────────────────────────────────┐
│                  第 1-4 月：数学基石                    │
│  线性代数 → 微积分 → 概率统计 → 优化理论               │
└──────────────────────┬──────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────┐
│                第 5-8 月：CS 核心                      │
│  数据结构 → 算法 → 信息论 → 计算理论                    │
└──────────────────────┬──────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────┐
│            第 9-14 月：ML/DL 理论                      │
│  ML 基础 → 深度学习 → 强化学习 → 贝叶斯方法           │
└──────────────────────┬──────────────────────────────┘
                       ↓
┌─────────────────────────────────────────────────────┐
│              第 15-18 月：高级主题                      │
│  NLP / CV / 因果推理 / AI 安全                        │
└─────────────────────────────────────────────────────┘
```

---

## 阶段一：数学基石（约 4 个月）

### 📐 1.1 线性代数（第 1 个月）

**本科水平要求：** 能从几何与代数两个角度理解线性变换，掌握矩阵分解在 ML 中的应用。

| 教材 | 说明 |
|---|---|
| **《Linear Algebra and Its Applications》6th ed. (2020)** — David C. Lay, Steven R. Lay, Judi J. McDonald | 全球最广泛使用的工科线代教材，Pearson 出版，Amazon 4.4★ |
| **《Linear Algebra》4th ed. (2024)** — Gilbert Strang, Wellesley-Cambridge | MIT 18.06 官方教材，Strang 在 MIT OCW 与 YouTube 有完整视频课 |
| **《Matrix Analysis and Applied Linear Algebra》 (2000)** — Carl D. Meyer, SIAM | 更偏矩阵理论与数值方法，适合进阶 |

**配套视频：**
- MIT 18.06 Linear Algebra (Gilbert Strang): https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/
- 3Blue1Brown "线性代数的本质" 系列: YouTube/B 站

**关键掌握：**
```
向量空间 · 线性变换 · 矩阵分解（LU/QR/SVD/特征值）
正定矩阵 · 伪逆 · PCA 的数学推导 · 梯度与 Jacobian
```

### 🔢 1.2 微积分（第 2 个月）

**本科水平要求：** 单变量与多变量微积分熟练，理解梯度、链式法则在反向传播中的角色。

| 教材 | 说明 |
|---|---|
| **《Calculus: Early Transcendentals》9th ed. (2021)** — James Stewart, Cengage | 全球最畅销的微积分教材（累计销量超百万册），习题丰富 |
| **《Thomas' Calculus》15th ed. (2023)** — Hass, Heil, Weir, Pearson | 另一本经典，适合自学的习题结构与清晰表述 |
| **《Calculus on Manifolds》(1965)** — Michael Spivak, CRC | 本科进阶，理解微分形式的现代视角（不需要全读，选读相关章节） |

**配套视频：**
- MIT 18.01 Single Variable Calculus + 18.02 Multivariable Calculus: https://ocw.mit.edu/

**关键掌握：**
```
极限与连续性 · 微分与积分 · 多元函数微积分
梯度下降 · 拉格朗日乘子 · 泰勒展开 · 链式法则
反向传播的数学推导
```

### 🎲 1.3 概率与统计（第 3 个月）

**本科水平要求：** 深刻理解概率分布、贝叶斯推断、统计检验，能阅读 ML 论文中的概率部分。

| 教材 | 说明 |
|---|---|
| **《Introduction to Probability》2nd ed. (2019)** — Blitzstein & Hwang, CRC | 哈佛 STAT 110 教材，豆瓣 9.4，直觉与严谨兼备，附免费课程 |
| **《Probability and Statistics for Engineers and Scientists》10th ed. (2024)** — Walpole, Myers, Pearson | 偏应用统计，工科标准教材 |
| **《All of Statistics: A Concise Course in Statistical Inference》 (2004)** — Larry Wasserman, Springer | 从概率到统计的速通，覆盖 ML 需要的统计推论 |
| **《Introduction to Statistical Learning》(ISLR) 2nd ed. (2021)** — James, Witten, Hastie, Tibshirani, Springer | **ML 入门与统计的桥梁**，免费 PDF，全彩，R/Python 代码 |

**配套视频：**
- Harvard STAT 110 (Blitzstein): https://projects.iq.harvard.edu/stat110
- Stanford STATS 216 (ISLR 配套): https://online.stanford.edu/courses/sohs-ystats216-statistical-learning

**关键掌握：**
```
概率公理 · 条件概率/贝叶斯定理 · 常见分布族 · 大数定律与中心极限定理
参数估计(MLE/MAP) · 贝叶斯推断 · 假设检验 · 线性回归
偏差-方差权衡 · 交叉验证 · Bootstrap
```

### ⚡ 1.4 优化理论（第 4 个月）

**本科水平要求：** 理解凸与非凸优化的核心算法，能分析 ML 训练收敛性。

| 教材 | 说明 |
|---|---|
| **《Convex Optimization》 (2004)** — Boyd & Vandenberghe, Cambridge | **凸优化圣经**，斯坦福 EE364A 教材，免费电子版 |
| **《Numerical Optimization》2nd ed. (2006)** — Nocedal & Wright, Springer | 数值优化标准参考书，偏算法实现 |
| **《Optimization for Machine Learning》 (2011)** — Sra, Nowozin, Wright, MIT Press | ML 方向的优化专题论文集 |

**配套视频：**
- Stanford EE364A Convex Optimization (Boyd): https://stanford.edu/~boyd/ee364a/

**关键掌握：**
```
凸集与凸函数 · KKT 条件 · 梯度下降族（SGD / Adam / RMSProp）
牛顿法与拟牛顿法 · 对偶理论 · 拉格朗日法
随机优化 · 在线学习 · 学习率调度
```

---

## 阶段二：CS 核心（约 4 个月）

### 🧱 2.1 数据结构与算法（第 5-6 个月）

**本科水平要求：** 能分析算法复杂度，独立实现常见数据结构与算法。

| 教材 | 说明 |
|---|---|
| **《Introduction to Algorithms》(CLRS) 4th ed. (2022)** — Cormen, Leiserson, Rivest, Stein, MIT Press | **算法标准教材**（豆瓣 9.3），被全球 1000+ 大学采用 |
| **《Algorithm Design》 (2005)** — Kleinberg & Tardos, Pearson | 康奈尔算法课教材，偏问题建模与设计方法 |
| **《算法笔记》(2023)** — 胡凡，机械工业出版社 | 中文优秀算法入门，与 PAT 考试结合 |

**配套视频：**
- MIT 6.006 Introduction to Algorithms: https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-spring-2020/
- Stanford CS161: https://web.stanford.edu/class/cs161/

**关键掌握：**
```
复杂度分析（大 O/Ω/Θ） · 排序与搜索 · 树/图
哈希表 · 动态规划 · 贪心算法 · 图算法（最短路径/最小生成树）
NP 完全性基本概念
```

### 📡 2.2 信息论基础（第 7 个月）

**本科水平要求：** 理解熵、互信息、KL 散度在 ML 中的核心角色。

| 教材 | 说明 |
|---|---|
| **《Elements of Information Theory》2nd ed. (2006)** — Cover & Thomas, Wiley | **信息论标准教材**（引用超 4 万），工程视角 |
| **《Information Theory, Inference and Learning Algorithms》 (2003)** — David MacKay, Cambridge | 信息论 → 推断 → 学习，**强烈推荐**，免费 PDF |

**配套视频：**
- Cambridge Information Theory (MacKay 门下): YouTube

**关键掌握：**
```
熵 · 条件熵 · 互信息 · KL 散度 · 交叉熵
最大熵原理 · 数据压缩（Huffman / Lempel-Ziv）
信息论在 ML 中的应用（决策树 / 变分推断 / 生成模型）
```

### 💻 2.3 计算理论（第 8 个月）

**本科水平要求：** 理解可计算性、计算复杂性、图灵机与 Church-Turing 论题。

| 教材 | 说明 |
|---|---|
| **《Introduction to the Theory of Computation》3rd ed. (2012)** — Michael Sipser, Cengage | **计算理论标准教材**（豆瓣 9.4），MIT 6.045 / 6.840 教材 |
| **《Computational Complexity: A Modern Approach》 (2009)** — Arora & Barak, Cambridge | 进阶复杂性理论 |
| **《Alan Turing: The Enigma》 (2014)** — Andrew Hodges | 图灵传，与计算理论配合阅读 |

**配套视频：**
- MIT 6.045 Automata, Computability, and Complexity: https://ocw.mit.edu/courses/18-404j-theory-of-computation-fall-2020/

**关键掌握：**
```
确定性/非确定性自动机 · 正则语言 · 下推自动机
图灵机（单带/多带） · 停机问题 · Church-Turing 论题
P vs NP · NP 完全性 · Cook-Levin 定理
```

---

## 阶段三：ML/DL 理论（约 6 个月）

### 🤖 3.1 机器学习（第 9-10 个月）

**本科水平要求：** 系统掌握监督/无监督/强化学习的算法原理与数学推导。

| 教材 | 说明 |
|---|---|
| **《Pattern Recognition and Machine Learning》(PRML, 2006)** — Christopher Bishop, Springer | **ML 经典教材**（引用超 7 万），偏贝叶斯视角 |
| **《The Elements of Statistical Learning》(ESL) 2nd ed. (2009)** — Hastie, Tibshirani, Friedman, Springer | **统计学习圣经**，免费 PDF |
| **《Understanding Machine Learning: From Theory to Algorithms》 (2014)** — Shalev-Shwartz & Ben-David, Cambridge | 理论 ML（PAC 学习 / VC 维 / 泛化界），免费 PDF |
| **《机器学习》（西瓜书）(2016)** — 周志华，清华大学出版社 | 中文 ML 最佳教材（豆瓣 8.7），适合初学者 |

**配套视频：**
- Stanford CS229 Machine Learning (Andrew Ng): https://cs229.stanford.edu/
- 上海交通大学 机器学习 (张伟楠): B 站
- 李宏毅 机器学习 (台大): YouTube / B 站

**关键掌握：**
```
回归（线性/逻辑） · SVM（原问题/对偶/核方法）
决策树 · 集成方法（Bagging/Boosting/随机森林）
聚类（K-means/DBSCAN/GMM） · 降维（PCA/t-SNE/UMAP）
贝叶斯学习 · 高斯过程 · 隐变量模型
PAC 学习理论 · VC 维 · 偏差-方差
```

### 🧠 3.2 深度学习（第 11-12 个月）

**本科水平要求：** 理解主流架构的数学原理，能独立实现与训练。

| 教材 | 说明 |
|---|---|
| **《Deep Learning》(Goodfellow, Bengio, Courville, 2016)** — MIT Press | **"花书"**，深度学习标准教材，免费电子版 |
| **《Dive into Deep Learning》(2023)** — Zhang, Lipton, Li, Smola, Cambridge | 代码驱动的深度学习教材，免费在线版，PyTorch |
| **《Understanding Deep Learning》 (2023)** — Simon Prince, MIT Press | 最新 DL 教材（2023），兼顾理论与代码，图/文质量极高 |

**配套视频：**
- Stanford CS231n CNNs: https://cs231n.stanford.edu/
- Stanford CS224n NLP: https://web.stanford.edu/class/cs224n/
- Stanford CS236 Deep Generative Models: https://deepgenerativemodels.github.io/

**关键掌握：**
```
多层感知机 · 反向传播（矩阵形式推导） · 正则化（Dropout / BN / LayerNorm）
CNN（卷积/池化/经典架构） · RNN/LSTM/GRU · Attention / Transformer
梯度消失/爆炸 · 预训练与微调 · 迁移学习
生成模型（VAE / GAN / Diffusion）
Scaling Law · 大模型基本原理
```

### 🎮 3.3 强化学习（第 13 个月）

**本科水平要求：** 理解 MDP、贝尔曼方程、主流 RL 算法。

| 教材 | 说明 |
|---|---|
| **《Reinforcement Learning: An Introduction》2nd ed. (2018)** — Sutton & Barto, MIT Press | **RL 圣经**（引用超 6 万），免费电子版 |
| **《Algorithms for Reinforcement Learning》 (2011)** — Csaba Szepesvári, Morgan & Claypool | 偏算法理论，简洁高效 |
| **《深度强化学习》 (2024)** — 王树森，人民邮电出版社 | 中文 RL 教材，结合实践 |

**配套视频：**
- David Silver RL 课程（DeepMind/YouTube）: https://www.davidsilver.uk/teaching/
- UC Berkeley CS285 (Levine): https://rail.eecs.berkeley.edu/deeprlcourse/

**关键掌握：**
```
MDP · 贝尔曼期望/最优方程 · 策略迭代/价值迭代
MC / TD / Q-learning · SARSA · Eligibility Traces
DQN · Policy Gradient · Actor-Critic · PPO
探索-利用平衡 · 多臂赌博机 · 逆强化学习
```

### 🧮 3.4 贝叶斯方法与概率图模型（第 14 个月）

**本科水平要求：** 理解概率图模型的表示、推断、学习。

| 教材 | 说明 |
|---|---|
| **《Probabilistic Graphical Models: Principles and Techniques》 (2009)** — Koller & Friedman, MIT Press | **PGM 标准教材**（引用超 1.5 万），偏数学 |
| **《Machine Learning: A Probabilistic Perspective》(MLaPP, 2012)** — Kevin Murphy, MIT Press | ML 的概率视角（引用超 4.5 万），Daphne Koller 推荐 |

**配套视频：**
- Stanford CS228 Probabilistic Graphical Models: https://cs228.stanford.edu/

**关键掌握：**
```
贝叶斯网络 · 马尔可夫网络 · 因子图 · 条件随机场(CRF)
精确推断（变量消除/置信传播） · 近似推断（变分/MCMC）
结构学习 · EM 算法 · 潜在变量模型
因果推理初步（Pearl 的 do-calculus）
```

---

## 阶段四：高级主题（约 4 个月）

### 🔭 4.1 因果推理（第 15 个月）

| 教材 | 说明 |
|---|---|
| **《Causality: Models, Reasoning and Inference》2nd ed. (2009)** — Judea Pearl, Cambridge | 因果推理奠基之作（引用超 4 万） |
| **《The Book of Why》(2018)** — Pearl & Mackenzie, Basic Books | 科普版，比 Causality 更易懂 |

**关键掌握：**
```
因果图 · do-calculus · 混杂/对撞/中介
反事实推理 · 个人治疗效应(ITE) · 因果发现
Double ML · 工具变量
```

### 🗣️ 4.2 自然语言处理（第 16 个月）

| 教材 | 说明 |
|---|---|
| **《Speech and Language Processing》3rd ed. (2024 draft)** — Jurafsky & Martin, Stanford | NLP 标准教材，免费在线版 |
| **《Foundations of Statistical Natural Language Processing》 (1999)** — Manning & Schütze, MIT Press | 统计 NLP 经典 |

**关键掌握：**
```
词嵌入 · 语言模型 · Transformer 的完整推导
微调 · RLHF · 推理与工具使用
评估基准与方法
```

### 👁️ 4.3 计算机视觉（第 17 个月）

| 教材 | 说明 |
|---|---|
| **《Computer Vision: Algorithms and Applications》2nd ed. (2022)** — Richard Szeliski, Springer | 免费 PDF，偏算法工程 |

**关键掌握：**
```
图像滤波/特征 · 目标检测（R-CNN/YOLO/DETR）
语义分割 · 图像生成 · 多模态学习
```

### 🛡️ 4.4 AI 伦理与安全（第 18 个月）

| 教材 | 说明 |
|---|---|
| 参考以下资料： |
| **《The Alignment Problem》(2020)** — Brian Christian, Norton | AI 对齐问题的科普/历史 |
| **AIMA 第 27 章 哲学、伦理与 AI 安全 (2020)** — Russell & Norvig | 第 4 版新增章节 |
| **《Human Compatible: AI and the Problem of Control》 (2019)** — Stuart Russell, Viking | AI 安全奠基之作 |

**关键掌握：**
```
对齐问题 · 可解释性 · 公平性 · 鲁棒性
价值学习 · Inverse RL · 可审计性
```

---

## 每周时间安排建议

### 方案 A：历史与理论并行（贯穿式）

```
周一至周五：历史阅读（1h）+ 数学/理论（1h）
周末：理论深入学习（3-4h）

示例 — 第 1 周：
   历史：计算机史 · Pascal → ENIAC
   理论：线性代数 · 向量空间与子空间
```

### 方案 B：历史优先 → 理论攻坚（推荐）

```
第 1-12 周：优先完成历史学习路径（已有 12 周计划）
第 13-30 周：进入理论知识系统学习（本页 18 个月理论路径）
```

### 方案 C：纯理论专注（不需要历史时）

```
按本文件阶段一到阶段四的顺序，从数学基石开始逐月推进
```

---

## 推荐的学习节奏

```
每天 2 小时 × 6 天 = 12 小时/周

分配建议：
  45min  教材阅读（逐节推导）
  30min  配套视频 / 可视化讲解
  30min  习题与编程实践
  15min  笔记整理（费曼输出）
```

---

## 数学基础速查表（按 AI 任务映射）

| AI 任务 | 需要的数学工具 |
|---|---|
| 线性回归/逻辑回归 | 微积分 + 线代 + 概率 |
| SVM | 优化（对偶）+ 线代（核） |
| PCA | 线代（特征值分解/SVD） |
| 神经网络/反向传播 | 微积分（链式法则）+ 线代（矩阵运算） |
| Transformer/Self-Attention | 线代（投影）+ 概率（softmax） |
| 贝叶斯网络 | 概率 + 图论 |
| 强化学习 | 概率（MDP）+ 优化（贝尔曼） |
| GAN / VAE / Diffusion | 概率 + 信息论 + 优化 |
| 因果推理 | 概率 + 图论 + 逻辑 |

---

## 资源链接速查

### 免费在线教材

- **ISLR** (统计学习导论): https://www.statlearning.com/
- **ESL** (统计学习要素): https://hastie.su.domains/ElemStatLearn/
- **PRML** (模式识别与机器学习): https://www.microsoft.com/en-us/research/people/cmbishop/prml-book/
- **Deep Learning (花书)**: https://www.deeplearningbook.org/
- **Dive into Deep Learning**: https://d2l.ai/
- **Understanding Deep Learning**: https://udlbook.github.io/udlbook/
- **Convex Optimization (Boyd)**: https://web.stanford.edu/~boyd/cvxbook/
- **Understanding Machine Learning (Shalev-Shwartz)**: https://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/
- **Speech and Language Processing (Jurafsky)**: https://web.stanford.edu/~jurafsky/slp3/
- **Computer Vision (Szeliski)**: https://szeliski.org/Book/
- **Reinforcement Learning (Sutton & Barto)**: http://incompleteideas.net/book/the-book-2nd.html
- **Information Theory (MacKay)**: https://www.inference.org.uk/mackay/itila/

### 课程主页

- **CS50x 2026** 哈佛 CS 导论: https://cs50.harvard.edu/x/2026
- **CS221** Stanford AI 原理: https://cs221.stanford.edu/
- **CS229** Stanford 机器学习: https://cs229.stanford.edu/
- **CS231n** Stanford 深度学习/视觉: https://cs231n.stanford.edu/
- **CS224n** Stanford NLP: https://web.stanford.edu/class/cs224n/
- **CS228** Stanford 概率图模型: https://cs228.stanford.edu/
- **CS285** UC Berkeley 深度强化学习: https://rail.eecs.berkeley.edu/deeprlcourse/
- **CS236** Stanford 深度生成模型: https://deepgenerativemodels.github.io/
- **MIT 18.06** 线性代数 (Strang): https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/
- **MIT 18.01/18.02** 微积分: https://ocw.mit.edu/
- **Harvard STAT 110** 概率 (Blitzstein): https://projects.iq.harvard.edu/stat110
- **Stanford EE364A** 凸优化 (Boyd): https://web.stanford.edu/~boyd/ee364a/
- **David Silver** RL 课程: https://www.davidsilver.uk/teaching/

### 可视化与视频

- **3Blue1Brown** 深度学习系列: https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi
- **3Blue1Brown** 线性代数本质: YouTube 搜索 "Essence of linear algebra"
- **StatQuest** (Josh Starmer) ML/统计: https://www.youtube.com/@statquest
- **AIMA 可视化交互站** (非官方): https://jsurrea.github.io/aima-visualizations

### 中文资源 🇨🇳

- **李宏毅 机器学习 2025** (B站): https://www.bilibili.com/video/BV1TAtwzTE1S
- **李宏毅 官网 2025**: https://speech.ee.ntu.edu.tw/~hylee/ml/2025-spring.php
- **CS231n 2017 中字版** (B站): https://www.bilibili.com/video/BV1nJ411z7fe
- **CS 自学指南** (北大出品, 完整路线): https://csdiy.wiki/
- **《机器学习》（西瓜书）** 周志华: 清华大学出版社
- **《统计学习方法》** 李航: 清华大学出版社

### 工具推荐

| 用途 | 推荐 |
|---|---|
| 公式推导 | 纸笔 + 论文草稿本 |
| 代码实践 | Jupyter Notebook + PyTorch |
| 可视化 | 3Blue1Brown / distill.pub |
| 笔记 | Obsidian + MathJax / Notion |
| 自测 | ChatGPT / Claude 作为"AI 导师" |

---

## 进度跟踪

- [ ] 阶段一：数学基石
  - [ ] 1.1 线性代数（第 1 个月）
  - [ ] 1.2 微积分（第 2 个月）
  - [ ] 1.3 概率统计（第 3 个月）
  - [ ] 1.4 优化理论（第 4 个月）
- [ ] 阶段二：CS 核心
  - [ ] 2.1 数据结构与算法（第 5-6 个月）
  - [ ] 2.2 信息论（第 7 个月）
  - [ ] 2.3 计算理论（第 8 个月）
  - [ ] 2.4 概率图模型（第 8 个月）
- [ ] 阶段三：ML/DL 理论
  - [ ] 3.1 机器学习（第 9-10 个月）
  - [ ] 3.2 深度学习（第 11-12 个月）
  - [ ] 3.3 强化学习（第 13 个月）
  - [ ] 3.4 贝叶斯方法（第 14 个月）
- [ ] 阶段四：高级主题
  - [ ] 4.1 因果推理（第 15 个月）
  - [ ] 4.2 NLP（第 16 个月）
  - [ ] 4.3 计算机视觉（第 17 个月）
  - [ ] 4.4 AI 伦理与安全（第 18 个月）
