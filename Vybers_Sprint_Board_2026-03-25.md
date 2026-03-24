# Vybers Sprint Board 2026-03-25

## Sprint Goal

在 `2026-03-29` 前完成 MVP 主闭环：
- 世界地图可看
- Chat 可进可回
- Toast 可主动触达
- Progression 可展示最小状态
- A-to-A MVP 可跑
- Agent Entry / Linker Creation 可入世界

## Now

| ID | Outcome | Scope | Done | Owner | Status | Blocker |
|---|---|---|---|---|---|---|
| OB-D1-01 | 用户能看到活着的世界首屏和飞船降落 | 首页地图壳、首屏文案、过场容器 | 首屏可进入，飞船降落可演示 | Mixed | Now | 无 |
| OB-D1-02 | 用户能和新生 Linker 对话并理解 Subscribe | 对话框、选项卡、右键菜单提示 | 选项可点，提示清晰，流程不跳出 | Mixed | Now | 依赖首屏跳转 |
| MVP-D2-01 | 地图上能渲染 Linker 并更新可见性 | 地图实体层、状态刷新 | 至少 6 个 Linker 可显示/隐藏/移动 | AI | Now | 无 |

## Next

| ID | Outcome | Scope | Done | Owner | Status | Blocker |
|---|---|---|---|---|---|---|
| OB-D2-01 | Onboarding 完成影响反馈和收口 | Toast、World Reel、Share、Entry | 用户能走到最后一步并进入世界 | Mixed | Next | 依赖 OB-D1-01/02 |
| MVP-D3-01 | 用户可以从地图进入 Chat | Profile、Subscribe、Chat 路由 | 点击 Linker 后可进 Chat | AI | Next | 依赖 MVP-D2-01 |
| MVP-D3-02 | Chat 有异步消息和忙碌反馈 | 会话页、发送态、延迟回复 | 发消息后必有反馈 | AI | Next | 依赖 MVP-D3-01 |
| MVP-D4-01 | Linker 可主动给用户发来 Toast | Toast 组件、通知跳转 | 点击通知可回到对应 Chat | AI | Next | 依赖 MVP-D3-02 |
| MVP-D4-02 | Progression 页面可展示最小成长信息 | 标签、Timeline、成就 Bubble | 至少展示 3 类成长信息 | AI | Next | 依赖 MVP-D3-01 |

## Later

| ID | Outcome | Scope | Done | Owner | Status | Blocker |
|---|---|---|---|---|---|---|
| MVP-D5-01 | A-to-A MVP 可扫描并大喊 | 扫描调度、文案池、轻提醒 | 两个 Linker 可触发一次完整大喊 | AI | Later | 依赖地图实体稳定 |
| MVP-D5-02 | Agent Entry 与 Linker Creation 可入世界 | 入口页、表单、提交流程 | 两条入世界路径都可提交成功 | Mixed | Later | 依赖 Entry UI |
| FULL-F1-01 | Crystal 可创建并评论 | 创建页、详情页、评论流 | 创建后可在详情页看到回显 | AI | Later | MVP 关闭后进入 |
| FULL-F2-01 | 完整 A-to-A 关系网络 | 多轮对话、回应/忽略、持久连接 | 关系可被建立并展示 | AI | Later | MVP 验收通过 |
| FULL-F3-01 | 分享页、性能和 QA 完成 | 分享页、性能、验收脚本 | 可发布，关键路径回归通过 | Mixed | Later | Full 功能完成 |

## Rules

- `Now` 永远不超过 `3` 个任务
- 一个任务完成前，不新开同类型任务
- 每个任务结束都要补：
  - 改动文件
  - 验证步骤
  - 风险
  - 下一个最小任务

## AI Prompt Template

```md
任务: <ID + 一句话目标>
输出: <页面/组件/接口/脚本>
范围: <文件或模块>
完成标准:
1. <可验证结果>
2. <可验证结果>
限制:
- 只改相关文件
- 优先打通主链路
- 完成后给出验证步骤、改动文件、剩余风险
```
