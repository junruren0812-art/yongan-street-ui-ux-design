# 更新记录

本文件用于记录永安街游戏 UI/UX 设计版本变化，最新版本位于最上方。

## 主场景 v0.7 全局规范与图层重构 — 2026-09-11

### 新增

- 新增 `00_Global_Rules`，锁定 1920×1080 画布、48px 安全区、8px 网格、字号、间距、圆角、描边和组件尺寸
- 新增 Layer Order 规范与独立全局规范文档
- 新增全局规范板预览图 `assets/wireframe/main-scene/v0.7-global-rules.png`

### 调整

- 按 Layer Order 将 01–07 重构为可编辑分层 Frame
- 将 08 拆分为独立 Scene Viewport、Persistent HUD、Scene Feedback、Dialogue Panel 和 Global Navigation
- 保留 08 既定人物 Camera Framing，使场景裁切仅作用于 Scene Viewport
- 新增 Scene Feedback Layout Rules：07 按完整画布居中，08 按左侧 Scene Viewport 居中，并统一 32px 底部净空
- 将 08 Scene Viewport 按手动调整结果更新为 `X24 / Y88 / W1264 / H808`，反馈条叠加于场景底部并保留 8px 内边距
- 更新八状态总览图、v0.7 设计说明、修改清单和 README 索引

### 修复

- 修复 08 左侧场景图覆盖顶部标题、时间、操作提示和地点 HUD 的问题
- 修复 07 Scene Feedback 与笔记本栏距离过近，以及 08 Feedback 跨入场景与对话区域的问题

## 主场景 v0.7 状态线框完成 — 2026-09-10

### 新增

- 在 Figma 中保留 v0.6，并新增 `Main Scene / Wireframe v0.7` 页面
- 完成 Enter、Exploration、Price List Available／Selected／Inspection／After Read、After Clue 与 D104 Unlocked 共 8 个状态线框
- 补充 v0.7 状态转换、HUD 规则与交互反馈链说明

### 调整

- 用正式八状态总览替换 `assets/wireframe/main-scene/v0.7.png` 占位图
- 将 v0.7 文档状态更新为“待评审”
- 在 Round 01 修改清单中标记 8 个最低状态线框已完成

### 待确认

- 物件信息页与 Notebook 的系统关系
- “回忆／对话”触发与结果、线索正式写入时机、D104 未解锁选项表现
- 吴莉“倾听／对话”差异，以及手柄与触屏输入范围

## 主场景 v0.6 Round 01 评审完成 — 2026-09-10

### 评审结论

- Main Scene / Wireframe v0.6 有条件通过
- 核心 Game UX 与玩家认知链已成立
- 可以进入 v0.7 交互状态线框设计
- 在 P1 状态与反馈问题解决前，不建议进入高保真

### 新增

- 将完整 Game UX 评审结论写入 `docs/UI/main-scene/v0.6/reviews/2026-09-10-round-01.md`
- 新建 `docs/UI/main-scene/v0.7/round-01-action-list.md`
- 将评审问题转化为带优先级、验收标准和状态的 v0.7 修改项

### 后续

- 优先完成 v0.7 清单中的 P1 项
- 完成 8 个最低状态线框并进行复审

## 主场景 v0.6 Figma 资料归档 — 2026-09-10

### 新增

- 归档最终确认的 Figma 页面树
- 归档 Main Scene / Wireframe v0.6 UI 规格
- 补充 Figma 原文件与设计讨论来源链接

### 调整

- 用 Figma 画板截图替换 v0.6 线框图占位文件
- 更新 v0.6 设计文档与 README 索引

### 待确认

- 补齐未明确的组件坐标、视觉样式和交互状态规格

## 主场景 v0.7 — 2026-09-10

### 新增

- 新建主场景 v0.7 设计文档
- 新建主场景 v0.7 线框图占位文件
- 在 README 中将主场景当前版本更新为 v0.7

### 待确认

- 补充 v0.7 相较 v0.6 的实际设计变化
- 用正式线框图替换占位文件

## 主场景 v0.6 — 2026-09-10

### 新增

- 建立主场景 v0.6 基础设计文档
- 建立主场景 v0.6 线框图占位文件
- 建立 UI 文档和线框图目录规范

### 调整

- 后续已补充 v0.6 的 Figma 页面树、UI 规格和画板截图
