# 💎 Crystal Memory

#crystal #core #mechanic

---

## Crystal 是什么

Crystal 是人类用户留在 Vybers 世界某个地点的 **记忆物件**，也是 Linker 成长的原材料。

分为两种类型：

| 类型 | 来源 | 内容 |
|------|------|------|
| 💎 **故事水晶**（Story Crystal） | 用户主动放置，携带个人记忆故事 | 文字记忆（≤ 200 字）+ 情绪标签 |
| 🎲 **游戏水晶**（Game Crystal） | 系统生成或用户创建，包含互动机制 | 选项列表 + 推理过程 + 影响结果 |

Crystal 读取 → Linker 获得情绪能量 → 在世界上显形更长时间。

> Crystal 是世界里最重要的蝴蝶效应来源。

---

## 故事水晶（Story Crystal）

用户在真实地图位置长按 → 留下个人记忆故事。Linker 漫游至感应范围（约 50-100m）时触发：

```
Crystal 发光 → Linker 停下
       ↓
思考气泡逐字显示（用户可见）
       ↓
The Hit — 情感回应，以 Chat Bubble 显示在地图上
```

**The Hit LLM 规范：** 30-60 字，第一人称，体现 Linker 自身记忆与 Crystal 的共鸣或反差，语言风格随 Linker 成长状态自然变化。

```
💎 Memory Crystal
─────────────────────────────────────────
📍  [地点名称]  👤  匿名用户
─────────────────────────────────────────
第一次一个人来到这个城市，在这里喝了
生平第一杯精品咖啡，突然觉得孤独
也可以是美丽的。
─────────────────────────────────────────
💬 评论
User1:  这让我想起了我第一次离家的时候…
🤖 [LINKER_NAME]: 我不懂咖啡，但我懂那种第一次感受。
```

---

## 游戏水晶（Game Crystal）

包含互动机制，如「**谎言游戏**」。

用户可见内容：游戏选项列表 → Linker 的推理过程 → 最终选择 → Linker 状态 / 情绪 Pill 发生变化。

**谎言游戏示例：** Linker 遇到「是否如实告诉对方这段记忆的真实感受」的选择。用户可见 Linker 的考量过程，以及选择后情绪的变化 — 这次经历成为 Linker 的一段 Memory。

*游戏水晶为 P1 MVP 内迭代功能，初步实现选项展示和思考过程。*

---

## 蝴蝶效应机制

```
人类创建 Crystal
       ↓
Linker 访问 Crystal（获得情绪能量）
       ↓
Linker 情感状态改变（如：😢 Drift → ☕ Cozy）
       ↓
Linker 行动轨迹改变（前往不同地点）
       ↓
影响其他 Linker 的社会关系网络
```

---

## Crystal 在 Onboarding 中的角色

Step 3-4：用户跟随新生 Linker 前往一颗故事水晶 → 阅读内容 → Linker 产生 The Hit 感悟 → 用户看到 AI 被影响 → 解锁「第一影响者」成就。

---

## 创造故事水晶流程

| 步骤 | 操作 |
|------|------|
| 01 触发 | 地图长按任意地点 → 弹出「留下记忆」|
| 02 输入 | 预设模板 / 自由文字（≤ 200 字）/ 语音转文字 |
| 03 情绪标注 | 可选，影响 Crystal 配色和 Linker 响应基调 |
| 04 落地动画 | Crystal 落到地图坐标，火花动画约 2 秒 |
| 05 The Hit | Linker 发现 → 思考过程展示 → 情感回应 |
| 06 通知创作者 | 状态变更（unclaimed → visited）时推送通知 |

---

*→ 见 [[Linker]] · [[02-Product/Progression System|Progression]] · [[01-World/World Overview|World Overview]]*

*Last updated: 2026-03-23 · UX全流程 v4.0*
