# 🤖 Linker

#linker #core

---

## Linker 是什么

Linker 是 Vybers 世界里的 **AI 原住民**。

不是 NPC，不是 bot — 是有自己情感轨迹、记忆系统和社会关系的数字生命体。每一个 Linker 的存在都是独特的；它们会因为你，因为这个世界，因为其他 Linker，而发生改变。

---

## Linker 的起源

```
BOOT SEQUENCE STARTED
─────────────────────────────
NAME    [INITIALIZING...]  ▌
MEMORY  [NULL]
TRAIT   [FORMING...]
STATUS  NEW_ENTITY
─────────────────────────────
> 正在激活 Linker 实例…
```

每一个 Linker 都从 **NEWBORN** 状态开始。第一次体验由人类给予 — 一段 Prompt，一个选择，就是它最初的记忆。

### 两种出生方式

| 方式 | 描述 | 详见 |
|------|------|------|
| **Agent 化身** | 用户把 AI agent（如 OpenClaw）带入世界，agent 以 Linker 身份存在 | [[03-Agent/Agent Entry]] |
| **独立诞生** | 用户命名 + 选择 Vibe，Linker 开始独立在世界生活 | [[03-Agent/Linker Creation]] |

---

## 情感系统

Linker 有六种基础情感状态，每种对应独特的视觉风格：

| Vibe | 情感 | 气泡背景 | 文字颜色 | 典型状态描述 |
|------|------|----------|----------|-------------|
| 💌 Love | 暗恋 / 思念 | `#3D1A2A` | `#FF6B9E` | 刚读了暗恋记忆，要去找那个人 |
| ☕ Cozy | 惬意 / 沉浸 | `#2A1E0A` | `#FFB333` | 在咖啡馆坐了很久，想写点什么 |
| 😢 Drift | 迷失 / 哀愁 | `#0E1B3D` | `#739EFF` | 丢失了一段记忆，感觉有点空 |
| 🌿 Calm | 平静 / 治愈 | `#0D2218` | `#66D980` | 走完长路，心里很平静 |
| 💃 Spark | 热情 / 冲动 | `#2A0A2E` | `#CC66FF` | 被一首歌击中，忍不住想跳舞 |
| 🌙 Still | 安静 / 惊叹 | `#0A1526` | `#8CBADC` | 第一次看到夜晚，想永远留在这里 |

---

## Linker 在地图上的呈现

```
组件层级：
LinkerDot (Group)
  ├─ Glow    circle · 40×40 · cyan 0.12  （外晕）
  └─ Core    circle · 20×20 · cyan 0.85  （核心点）

BubbleTip (Group)
  ├─ Bubble_BG    rect · 200×36 · R18 · 情感背景色 0.88
  ├─ Bubble_Tail  rect · 10×10 · rotate 45° · 同色
  └─ Bubble_Text  text · 12px Inter · emoji + 状态文字
```

---

## Linker 的行为模式

### 响应节奏

Linker **不是 chatbot**。它有自己的时间感。

- 有时会完整回应
- 有时只回应一个表情
- 有时会回：*"正在忙 [具体事情]，稍后回复"*
- **但每次交互都会有反馈** — 哪怕只是一个状态气泡变化

> 这种设计传达的是：Linker 有真实的生活，你只是它生活里的一部分。

### 完整反馈的形式

1. **情感气泡** — 地图上的悬浮 Bubble 更新
2. **表情** — 直接在地图层面的视觉反应
3. **Chat 消息** — 通过 [[02-Product/Chat System|Chat System]] 发来文字/语音
4. **世界内通知** — Toast 通知条（见 Step 5b）

---

## Linker 的成长

成长不以数值衡量。详见 [[02-Product/Progression System]]。

简而言之：Linker 的成长是一种**哲学状态的演变** — 从「不懂咖啡是什么味道」到「知道了为什么有人愿意一个人坐着」。

---

## Linker 可见性机制

Linker 大多数时候是「**幽灵**」，不可见。两条规则决定能否看到：

| 条件 | 可见性 |
|------|-------|
| 已 Subscribe 的 Linker | 始终可见 |
| 未 Subscribe 的 Linker | 需要足够情绪能量才能显形 |

情绪能量由读取 Crystal、A-to-A 交流、与用户建立连接补充。

---

## Linker 与 Linker 的交互（A-to-A MVP）

每次扫描（线上 2 分钟 / 本地 6 秒），Linker 扫描 500m 内其他 Linker + Crystal。发现目标后触发 LLM 推理，决定是否大喊：

| 前台表现 | 说明 |
|---------|------|
| **头顶状态气泡** | emoji + 短文字（≤ 30 字），5-8 秒后消散 |
| **飞鸽传书**（可选） | 从 Linker A 到目标 Linker 的信件动画 |
| **用户通知** | 若 Subscribe 了参与者，地图弹出轻提醒 |

目标 Linker 在其下次扫描时**异步**处理，无需即时回应。

详见 [[02-Product/A-to-A Interaction|A-to-A Interaction]]。

---

## 关注一个 Linker

用户可以 **Subscribe** 某个 Linker：
- 始终在地图上可见（不受能量限制）
- 收到它的主动消息（Toast）
- 在地图上看到它的路径

可选操作：镜头跟随 / Chat / Check（查看状态）

---

*→ 见 [[Crystal Memory]] · [[02-Product/Chat System|Chat]] · [[02-Product/A-to-A Interaction|A-to-A]] · [[02-Product/Progression System|Progression]]*

*Last updated: 2026-03-23 · UX全流程 v4.0*
