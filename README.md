# Neuro Mechanism Graph｜神经机制图解

神经退行性疾病相关的**蛋白病理与清除机制**交互图解。每一页的核心设计是一条视觉规则：

- **实线** = 细胞本来就会做的事（已被广泛验证的通用生物学）
- **虚线** = 某个具体方案自己要证明的事（待实验检验的假设）
- **点虚线（洋红）** = 会让方案失效的分支

专业名词与动词在正文旁直接给出中英对照，页末另有术语表。


## 专题

### 蛋白病理与清除

| 专题 | 内容 | 关键词 |
|---|---|---|
| [`tau-ptau181-clearance`](./topics/tau-ptau181-clearance/) | 多功能肽从识别 pTau181 到溶酶体水解的六步机制图解 | pTau181、Arg 解聚、LIR–LC3、自噬体、溶酶体 |
| [`amyloid-beta-clearance`](./topics/amyloid-beta-clearance/) | Aβ 的四条并行清除通路，以及"存量 vs 速率"的读数区分 | neprilysin、IDE、LRP1/RAGE、APOE、类淋巴、脑膜淋巴 |

### 错误折叠的传播

| 专题 | 内容 | 关键词 |
|---|---|---|
| [`alpha-synuclein-propagation`](./topics/alpha-synuclein-propagation/) | 把"类朊病毒传播"拆成模板化、细胞间转移、区域推进、致病后果四段 | 种子扩增、RT-QuIC、细胞外囊泡、隧道纳米管、Braak 分期 |

### RNA 稳态与剪接

| 专题 | 内容 | 关键词 |
|---|---|---|
| [`tdp43-nuclear-loss`](./topics/tdp43-nuclear-loss/) | 核内功能丧失与胞质聚集两张面孔，以及隐蔽外显子这条因果链 | 自调控、隐蔽外显子、STMN2、UNC13A、相分离、LATE |

### 胶质细胞与降解机器

| 专题 | 内容 | 关键词 |
|---|---|---|
| [`microglial-phagocytosis`](./topics/microglial-phagocytosis/) | 吞噬六步流程、"吃我／别吃我"两类信号与 TREM2 旁路 | C1q/C3/CR3、CD47–SIRPα、CD22、TREM2–DAP12、DAM |
| [`autophagy-lysosome-pathway`](./topics/autophagy-lysosome-pathway/) | 六步流程与自噬通量判读；本库多个专题的共同出口 | ULK1、LC3 脂质化、p62、SNARE 融合、TFEB、bafilomycin |

### 专题之间的关系

- pTau181 专题把 LIR 装进人工分子，走的是自噬—溶酶体专题里"泛素 → 受体 → LC3"的那个接口。
- 小胶质细胞吞噬的最后两步，与自噬—溶酶体专题共用同一套降解机器。
- Aβ 专题的"胶质吞噬"一条通路，在小胶质细胞专题里展开。

## 结构

```
Neuro-Mechanism-Graph/
├── index.html                              目录页（浅底／深色自适应）
├── README.md
├── .nojekyll
└── topics/
    ├── tau-ptau181-clearance/
    ├── amyloid-beta-clearance/
    ├── alpha-synuclein-propagation/
    ├── tdp43-nuclear-loss/
    ├── microglial-phagocytosis/
    └── autophagy-lysosome-pathway/
        ├── index.html                      单文件专题页，可离线打开
        └── README.md                       来源、分层、参考文献与局限
```

每个专题目录的结构相同：一个自足的 `index.html` 加一份说明用的 `README.md`。

## 本库规则

1. **页面不得依赖在线资源**：不引用 CDN、不引用在线字体（中文使用本地字体栈），单个 `index.html` 下载后即可离线阅读。参考文献的外链除外。
2. **必须分层标注**：页面要分清"已验证的通用生物学／本方案的假设／会让方案失效的分支"，不把假设写成结论。
3. **术语必须中英对照**：名词与动词都要标注，并在页末汇总为术语表。
4. **只提供机制讲解与自查**，不提供临床建议或个体化医学意见。
5. **参考文献以标题给出**：条目写明作者、期刊、年份与论文标题，外链指向 PubMed 检索而非固定编号，避免编号写错却看不出来。
6. 只有 `main` 分支，每次提交直接推送到 `main`。

## 局限

各专题的原始材料未必公开，页面中不含未公开的序列、配方或定量参数；参考文献用于支持通用生物学背景，不代表对任一具体方案有效性的验证。

页面中的化学式均为示意式，不是定量反应式；所有"若机制成立应当看到的模式"一类表格都是**预期**，不是实验结果。几个领域（类淋巴通路的驱动力、α-syn 的区域推进、TDP-43 的相分离路径）至今仍有实质分歧，页面用虚线如实标注，而不是择一叙述。
