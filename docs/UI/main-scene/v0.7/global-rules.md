# Main Scene v0.7 — Global Rules

- 页面：主场景 / Main Scene
- 版本：v0.7
- 状态：已锁定，作为 01–08 精修基准
- 更新时间：2026-09-11
- 负责人：任俊茹
- Figma 规范板：[00_Global_Rules](https://www.figma.com/design/hSygViz2j9LkQ419P8kHIV/Main-Scene---Wireframe-v0.6?node-id=143-1055&p=f)
- 规范板预览：[v0.7-global-rules.png](../../../../assets/wireframe/main-scene/v0.7-global-rules.png)

## 1. 画布、安全区与网格

- 画布：`1920 × 1080`
- 外围安全区：`48px`
- Figma Layout Grid：`8px`
- 重要文字、HUD 与可操作控件必须位于安全区内。

## 2. 字号与字重

| 用途 | 字号 | 建议字重 |
|---|---:|---:|
| 辅助信息／状态说明 | 16px | 400–500 |
| 正文／操作提示 | 20px | 400–500 |
| 按钮／小标题 | 24px | 600 |
| 面板标题 | 32px | 700 |
| 场景标题 | 40px | 700 |

仅使用 `400 / 500 / 600 / 700` 四档字重；不新增中间字号，确需例外时必须在组件旁说明。

## 3. 间距、圆角与描边

- 间距单位：`8 / 16 / 24 / 32 / 48px`
- 小控件圆角：`8px`
- 普通面板圆角：`12px`
- 大浮层圆角：`16px`
- 标签：胶囊圆角
- 普通描边：`1px`
- 当前聚焦描边：`2px`
- 强交互热点描边：`4px`

## 4. 共用组件尺寸

| 组件 | 基准尺寸 |
|---|---|
| HUD / Time | 245 × 82px |
| HUD / Action Hint | 360 × 46px |
| HUD / Location | 240 × 44px |
| Notebook / Bar | 620 × 120px |
| Notebook / Item | 170 × 48px |
| Button | 高度 58px，最小宽度 170px，左右内边距 24px |
| Object / Modal | 1110 × 720px |
| Object / Header | 1020 × 54px |
| Dialogue / Panel | 570 × 790px |
| Dialogue / Option | 510 × 62px，选项间距 16px |

单张页面不得自行缩放同名组件；需要变化时应先更新全局规范。

### 4.1 Scene Feedback Layout Rules

| 状态 | X | Y | W | H | 对齐基准 |
|---|---:|---:|---:|---:|---|
| 07 自由探索 / After Clue | 610 | 816 | 700 | 72 | 完整画布中心 |
| 08 对话模式 | 304 | 816 | 640 | 72 | 左侧 `Scene Viewport` 中心 |

约束规则：

- 对话模式下，`Scene Viewport` 的可见底边固定为 `Y=816`；Feedback 从该边界开始，不再覆盖场景人物。
- Feedback 底边不得低于 `Y=888`。
- `Global Navigation` 顶边为 `Y=920`，两者至少保留 `32px` 垂直净空。
- 无侧边面板时以完整画布中心对齐；打开对话面板时改以左侧 `Scene Viewport` 中心对齐。
- 禁止始终使用 1920px 画布中心、手动拉伸 Feedback，或覆盖人物面部、对话选项及全局导航。
- 普通场景最大宽度为 `700px`；对话场景最大宽度为 `640px`。

## 5. 临时状态色

- 黄色：可互动、主要操作、新解锁。
- 青色：当前聚焦、已选中。
- 绿色：已查看、已理解、新认知反馈。

本阶段只锁定状态语义，最终色值在八张 UI 精修完成后统一确认。

## 6. Layer Order / 图层顺序

通用图层由下至上：

```text
01 Scene Background
02 Character / Object
03 Object State
04 Scene Feedback
05 Persistent HUD
06 Backdrop / Mask
07 Context Panel
08 Panel Interaction
09 Global Navigation
```

执行原则：

- `Camera Framing` 仅作用于 `Scene Viewport`。
- HUD、对话面板与笔记本不得被场景图片覆盖。
- 01–07 已按照通用顺序完成可编辑分层整理。
- 物品浮层出现时，Backdrop 可以压暗场景与场景 HUD；当前浮层内容与全局导航必须位于 Backdrop 上方。

## 7. 08 对话状态正式图层树

```text
08_D104_Option_Unlocked
├─ 01_Scene_Viewport
│  ├─ Scene_Background
│  │  └─ Left_Scene_Camera_Framing
│  └─ Character_Relationship
├─ 02_Persistent_HUD
│  ├─ Screen_Title
│  ├─ Time
│  ├─ Action_Hint
│  └─ Location
├─ 03_Scene_Feedback
├─ 04_Dialogue_Panel
│  ├─ Speaker
│  ├─ Dialogue_Content
│  ├─ Dialogue_Options
│  └─ Dialogue_Control
└─ 05_Global_Navigation
   └─ Notebook_Bar
```

08 已完成拆分重搭：场景位于独立裁切区域，标题 HUD、时间、操作提示、地点、对话面板和笔记本均为场景上方的独立可编辑图层。原 Camera Framing 与人物关系保持不变，顶部 HUD 遮挡问题已修复。

## 8. 当前执行状态

- [x] 创建并锁定 `00_Global_Rules`
- [x] 按规则整理 01–07 图层
- [x] 拆分重搭 08 合成 UI
- [x] 修复 08 场景覆盖 HUD 的问题
- [ ] 逐张进行内容、尺寸与文案精修
- [ ] 八张完成后统一配色
