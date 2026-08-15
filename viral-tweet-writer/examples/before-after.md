# 改写示例（before → after）

以下示例用于演示 `viral-tweet-writer` 的工作流与评分标准。所有案例均为**示意性内容**，数字与场景用于展示结构，不代表真实数据。

---

## 示例 1 — 主题模式 · 认知颠覆 + 数字锚定（中文）

**输入主题**：很多创始人以为多发内容就能增长，但冷启动真正决定成败的是分发，不是产量。

**主推版本**

```
大多数人以为增长靠“多发内容”。
我做了 90 天测试：同样的质量，分发渠道换一下，阅读量差了 11 倍。
内容没变。变的是它先被谁看到。
冷启动的第一杠杆从来不是产量，是第一批看见你的人。
```

**选择理由**：用数字锚定制造具体反差，第一行直接颠覆常见认知，结尾给出可带走的判断。

**使用的结构 / 开头**
- 结构：认知颠覆型（`references/tweet-templates.md` §1）
- 开头：数字锚定型（`references/hook-patterns.md` §2）
- 评分：第一眼相关性高，细节有真实颗粒度（数字 + 时间窗），可信度由“测试”二字兜底。

---

## 示例 2 — 原文模式 · 个人经历拆解（中文）

**输入笔记（节选）**：我去年做了一门付费课程，投了 3 万块推广，只卖出 7 份。后来我停了投放，改写免费 Newsletter，半年涨到 1.2 万订阅，反而靠咨询赚回来了。

**主推版本**

```
去年我花 3 万推广付费课，卖了 7 份。
我没再投广告，改成每周写一封免费 Newsletter。
半年后：1.2 万订阅，咨询订单反而填满了档期。
教训：人们先想“跟你学”，才愿意“为你付费”。
```

**备选版本（Before/After 型）**

```
Before：3 万投放，7 单。
After：0 投放，1.2 万订阅。
中间只做了一件事——把“卖课”换成“先给”。
信任到位，付费是结果，不是起点。
```

**选择理由**：主推版把可衡量的失败结果放第一行，诚实保留失败过程；备选版用 Before/After 强化归因，两种传播逻辑明显不同。

**使用的结构 / 开头**
- 结构：个人经历拆解型（`references/tweet-templates.md` §2）/ Before-After 型（§5）
- 开头：数字锚定型
- 评分：换署名检验通过——失败金额、课程类型、Newsletter 频率都是作者专属细节。

---

## 示例 3 — 主题模式（英文）

**Input topic**: Most productivity advice treats willpower as infinite. It's actually a finite daily budget that gets spent on every small decision.

**Main version**

```
Your willpower isn't a muscle. It's a battery.
Every tiny decision—what to eat, which tab to open—drains it a little.
The top performers I studied didn't have more willpower.
They removed the decisions, so the battery stayed full for what mattered.
```

**Why it works**: Opens with a direct declaration reframing a common belief, then uses a concrete mechanism (decision fatigue) and ends with a defensible takeaway. Matches the "观点宣言型 / 直接宣言型" patterns adapted to English.

**Structures / hooks used**
- Structure: 框架输出型 / 认知颠覆型 (`references/tweet-templates.md` §1, §3)
- Hook: 直接宣言型 (`references/hook-patterns.md` §4)
- Rubric: clear judgment, real mechanism, no fabricated stats—claims scoped to "the top performers I studied."

---

## 反面示例（淘汰条件演示）

下面这条应被淘汰：

```
🔥 震撼！99% 的人都不知道的爆款秘籍，点赞收藏不然找不到！
```

**为什么淘汰**（依据 `references/quality-rubric.md` 淘汰条件）：
- 使用无依据的最高级与普遍化判断（“99%”“秘籍”）；
- 依赖互动诱饵与虚假紧迫感；
- 正文价值远低于开头承诺；
- 换成任何账号都毫无违和（未通过换署名检验）。
