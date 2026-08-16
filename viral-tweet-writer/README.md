# viral-tweet-writer

把文章、主题或已有内容，转化为**有辨识度、且具有传播力**的 X / Twitter 推文（中文或英文）。在不编造事实、不承诺“必然爆款”的前提下，用经过验证的短内容结构强化表达的角度、细节、张力和可读性。

> 把模板用于提升表达，不要让模板抹掉作者本人。最终的辨识度来自作者独有的细节、判断和语气。

## 功能特性

- **三种输入模式**：原文模式（文章 / 文档 / 笔记）、主题模式（想法 / 观点）、修改模式（诊断并优化已有推文）。
- **结构化工作流**：判断模式 → 建立简报 → 提取主干 → 选结构 / 开头 → 按目标格式写作 → 评分重写。
- **配套参考库**：4 份参考资料覆盖质量评分、推文结构、第一行写法、Thread 结构。
- **中英双语**：支持中文与英文推文，自动匹配作者语气。
- **质量护栏**：内置评分标准与淘汰条件，禁止虚假争议、误导性悬念与无依据的绝对化表达。

## 适用场景 / 触发词

撰写、改写、拆解、优化或生成**推文、X 帖子、爆款推文、引用推文、推广推文、单条推文或 Thread** 时使用。

输入 **`/huaxa`** 可直接进入推文形式选择界面，菜单提供八种形式：

1. **普通帖子（General Post）**：最基础的推文，出现在主页和时间线。
2. **长帖（Longer Post / Notes）**：Premium，单条最高约 25,000 字符，可带媒体。
3. **串文 / 线程（Thread）**：多条推文串联，适合教程 / 故事 / 清单 / 深度拆解。
4. **回复（Reply）**：直接回复别人的推文。
5. **提及（Mention）**：用 @用户名 提到别人。
6. **转推（Repost）**：直接转发他人内容，不加评论。
7. **引用推文（Quote Post）**：转发并加自己的评论。
8. **文章（Articles）**：Premium 长文形式，独立页面，适合深度文章 / 指南 / 报告。

非命令场景下，技能会根据语义自动判断形式，不强制展示菜单。各形式的字数限制、显示特性与媒体支持对照表见 [`SKILL.md`](./SKILL.md) 的「各形式格式规格（字数 / 显示 / 媒体）」一节。

## 安装方式

### 方式一：WorkBuddy 技能市场

在 WorkBuddy 对话中通过一句话从推荐市场搜索并安装 `viral-tweet-writer` 技能即可。

### 方式二：手动放置（通用 / Cline / Claude 等）

把整个 `viral-tweet-writer/` 目录复制到你的技能目录：

```bash
# WorkBuddy（用户级）
cp -r viral-tweet-writer ~/.workbuddy/skills/

# 其他兼容 Agent（按各自 skills 目录调整路径）
cp -r viral-tweet-writer /path/to/your/agent/skills/
```

放置后目录结构应如下（参考库必须齐全，否则工作流会缺少依赖）：

```
viral-tweet-writer/
├── SKILL.md                    # 主技能文件
├── LICENSE
├── README.md
├── agents/
│   └── openai.yaml             # 面向 OpenAI Agents 规范的接口定义（可选）
├── references/
│   ├── quality-rubric.md       # 质量评分标准
│   ├── tweet-templates.md      # 推文结构模板（10 种）
│   ├── hook-patterns.md        # 第一行写作模式（4 种）
│   └── thread-structures.md    # Thread 结构（3 种）
└── examples/
    └── before-after.md         # 真实改写示例（before → after）
```

## 使用流程（简述）

1. **判断输入模式**：原文 / 主题 / 修改。
2. **建立创作简报**：目标读者、目标、语气、单条或 Thread。
3. **提取内容主干**：核心判断、矛盾、证据、可带走结论、边界条件。
4. **选结构 + 开头**：参考 `references/tweet-templates.md` 与 `references/hook-patterns.md`。
5. **按目标格式写作**：普通帖子 / 长帖 / 串文 / 回复 / 提及 / 转推 / 引用推文 / 文章（详见 SKILL.md 第 5 步）。
6. **评分并重写**：用 `references/quality-rubric.md` 比较候选版本，至少重写一遍。

完整规则见 [`SKILL.md`](./SKILL.md)。

## 示例

查看 [`examples/before-after.md`](./examples/before-after.md) 了解 3 个完整改写案例（含中文认知颠覆、个人经历拆解，以及英文示例），每个案例都标注了所使用的结构与评分要点。

## 文件说明

| 文件 | 作用 |
| --- | --- |
| `SKILL.md` | 技能主文件，定义触发条件与完整工作流 |
| `references/quality-rubric.md` | 8 维度评分标准、换署名检验、修改优先级与淘汰条件 |
| `references/tweet-templates.md` | 10 种推文结构模板 + 选择指南 + 去模板感方法 |
| `references/hook-patterns.md` | 4 种第一行模式 + 修改方法 + 淘汰规则 |
| `references/thread-structures.md` | 3 种 Thread 结构 + 独立入口检查 |
| `agents/openai.yaml` | 面向 OpenAI Agents 规范的接口定义，便于接入 OpenAI 生态 |
| `examples/before-after.md` | 真实改写示例，演示工作流与评分标准 |

## 许可证

[MIT](./LICENSE) © 2026 Huaxa125
