# Einstein Skill

<p align="center">
  <a href="README.md">🇺🇸 English</a> |
  <a href="README.zh.md">🇨🇳 中文</a>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-AGPL--3.0-blue" alt="许可证：AGPL-3.0"></a>
</p>

<p align="center">
  <img src="assets/einstein-laboratory-banner.png" alt="棕褐色实验室中观察试管的 Albert Einstein">
</p>

## 这件事为什么存在

### 问题张力

AI 很擅长局部分析，可以推导一个后果、总结一篇论文、优化一段计算。理论构造需要另一种动作。理论家往往已经看见了几个都说得通的角度，却更在意其中哪个角度能够解释两种描述为什么属于同一个结构。比如，internal global charge spectrum 为什么可能和 spacetime representation 有关系？如果只是把两个主题并列出来，问题最有意思的部分仍然没有被回答。

### 核心洞见

真正有价值的跃迁经常是一座局域到整体的桥梁。局部、内部、微观或代数数据，可能组织起整体、几何、时空或表示层面的结构。这座桥梁完全可能是错的。它值得追的原因在于，它压缩了原本分开的事实，让联系显得不再偶然，并且产生了一个值得主动击破的新后果。

### Skill 的回应

Einstein Skill 把这个理论选择显式化。它先扫描问题的多个角度，选出压缩力和生成力最强的方向，做思想实验，提出一个大胆猜想，然后才生成竞争性解释并进行先例审计。稳健分析和高风险外推分开呈现。物理品味和可接受的风险由人提供，检索、比较和证据边界由 Agent 完成。

### 边界

它不是爱因斯坦角色扮演 Prompt，也不保证原创性、物理正确性或与爱因斯坦工作的历史等价性。它提供的是一套有纪律的方式，让漂亮的猜想在被检验前保持完整，同时不把优美误当成证据。

## 文献依据

下面的文献支撑这个工作流的设计动机，但不能证明这个 Skill 一定能提高科学发现能力。

| 设计问题 | 文献 | 对本项目的启发 |
| --- | --- | --- |
| 从预测走向理论构造，缺少什么能力？ | [Shalyt、Regev、Soljačić 与 Kaminer，*Can AI Follow In Einstein's Footsteps?*（2026）](https://arxiv.org/abs/2607.27794) | 将提出正确问题、发明原则和设计证伪测试概括为范式级物理发现中的关键缺口。 |
| LLM 生成研究想法时会出现什么问题？ | [Si、Yang 与 Hashimoto，*Can LLMs Generate Novel Research Ideas?*（2024）](https://arxiv.org/abs/2409.04109) | 通过受控的人类评审研究讨论了新颖性、可行性、自我评估和生成多样性，支持保留人的品味并生成竞争性解释。 |
| 研究想法应当如何评价？ | [Guo 等，*IdeaBench*（2024）](https://arxiv.org/abs/2411.02429) | 将新颖性、可行性和洞见等维度分开，避免把“新”当成模型自报的单一分数。 |
| 这个名字对应的历史理论锚点是什么？ | [A. Einstein，*Zur Elektrodynamik bewegter Körper*（1905）](https://doi.org/10.1002/andp.19053221004) | 作为 Einstein 名称背后的原始论文来源。 |

### References

1. Michael Shalyt, Nathan Regev, Marin Soljačić, and Ido Kaminer, “Can AI Follow In Einstein's Footsteps?”, arXiv:2607.27794 (2026). [arXiv record](https://arxiv.org/abs/2607.27794).
2. Chenglei Si, Diyi Yang, and Tatsunori Hashimoto, “Can LLMs Generate Novel Research Ideas? A Large-Scale Human Study with 100+ NLP Researchers”, arXiv:2409.04109 (2024). [arXiv record](https://arxiv.org/abs/2409.04109).
3. Sikun Guo et al., “IdeaBench: Benchmarking Large Language Models for Research Idea Generation”, arXiv:2411.02429 (2024). [arXiv record](https://arxiv.org/abs/2411.02429).
4. A. Einstein, “Zur Elektrodynamik bewegter Körper”, *Annalen der Physik* (1905). [Publisher record and DOI](https://doi.org/10.1002/andp.19053221004).

## 工作流概览

这套工作流先做理论选择，再把选择变成一个可以被主动击破的候选：

## 使用

```text
$einstein
我想研究 subsystem symmetry 是否可以产生 Hořava gravity。
不要先做形式化，也不要先写文献综述。先找到隐藏假设，
做一个思想实验，再提出真正不同的概念方向。
```

## 核心循环

```text
现象或张力
  → 角度扫描
  → 最有解释力、最优美的角度
  → 局域 → 整体桥梁
  → 隐藏原语
  → 思想实验
  → 大胆猜想
  → 竞争性解释
  → 后果与证伪条件
  → 新颖性检索
  → 人的选择与修订
```

默认先做创意阶段，再进入文献检索。漂亮的猜想是发现启发，不是证据。稳健分析和高风险外推要分开呈现。候选概念形成后，Skill 会检索精确术语、近义说法、历史表述、邻近领域、作者、研究组和引用链，并将结果标记为 `unverified`、`near-prior`、`distinct-so-far` 或 `absorbed-by-prior-art`，而不会直接声称“前人从未提出”。

## 它强制 Agent 完成的事情

- 质疑原问题中被固定的对象、关系、局域性、对称性、尺度、边界、观察者或背景。
- 先比较多个角度，并明确哪个角度具有最强的压缩性、桥接力和生成力。
- 检查局部、内部、微观或代数数据能否组织整体、几何、时空或表示层结构。
- 先说清楚一个核心猜想，再提出两个或三个竞争性解释。
- 对每个候选说明它解释了什么、会产生什么后果、怎样可能失败。
- 把稳健解释与大胆外推的明确风险分栏呈现。
- 只有在用户尚未表达物理品味时才追问。
- 当候选暴露出重要边界时保留被放弃的方案。
- 遇到强反驳后重新修改或放弃概念，而不是继续添加装饰性术语。

## 文件结构

```text
assets/einstein-laboratory-banner.png # 生成的 README 卷首图
SKILL.md                                  # 运行时工作流
agents/openai.yaml                        # Codex 元数据
references/creative-protocol.md           # 详细创意流程
references/concept-ledger-template.md     # 持久化概念台账
evals/evals.json                          # 行为压力案例
docs/related-projects.md                  # 公开设计对比
.github/PULL_REQUEST_TEMPLATE.md          # 以故事为先的 PR 结构和文献要求
docs/pull-request-story-and-references.md # PR 行文与引用规范
```

## 安装

将仓库克隆到客户端使用的 Skill 目录。Codex 的默认位置通常是：

```bash
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
git clone https://github.com/JunkaiWang-TheoPhy/einstein-skill.git \
  "$CODEX_HOME/skills/einstein"
```

完成创意阶段后，可以配合 [`research-me`](https://github.com/JunkaiWang-TheoPhy/research-me-skill) 做来源检索和新颖性审计。私人研究上下文应保存在私有会话记录中。

## 局限

这个 Skill 改进的是概念搜索过程，不能证明概念前所未有或物理上正确。新颖性仍需要系统检索和专家判断。思想实验只有在改变可观测量、约束或本体设定时才具有科学价值，漂亮的类比本身不是科学结果。

## 版本与许可证

版本为 `0.1.2`。本项目采用 [GNU Affero General Public License v3.0](LICENSE) 许可。
