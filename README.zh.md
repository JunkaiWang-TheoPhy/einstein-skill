# Einstein Skill

<p align="center">
  <a href="README.md">🇺🇸 English</a> |
  <a href="README.zh.md">🇨🇳 中文</a>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-AGPL--3.0-blue" alt="许可证：AGPL-3.0"></a>
</p>

## 简介

Einstein Skill 是一个面向科学问题和复杂概念问题的创意发明工作流。它先比较问题的多个角度，选出最优美且最有生成力的方向，检查局部事实能否组织整体结构，再帮助 Agent 找到隐藏原语、构造思想实验、改变问题的本体设定、提出大胆猜想，并在开始检索前明确可能的后果。

它不是爱因斯坦角色扮演 Prompt，也不保证原创性、物理正确性或与爱因斯坦工作的历史等价性。它提供的是一种更有纪律的创意过程，避免把新措辞误认为新概念。

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
