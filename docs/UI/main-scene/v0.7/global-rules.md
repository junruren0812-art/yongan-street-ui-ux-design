# Main Scene v0.7 — Global Rules

- 页面：主场景 / Main Scene
- 版本：v0.7
- 状态：已锁定，作为 01–10 精修基准
- 更新时间：2026-09-12
- 负责人：任俊茹
- Figma 规范板：[00_Global_Rules](https://www.figma.com/design/hSygViz2j9LkQ419P8kHIV/Main-Scene---Wireframe-v0.7?node-id=202-2&p=f)
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
| Smoking QTE / Panel | 1320 × 310px |
| Smoking QTE / Track | 1080 × 36px |
| Smoking QTE / Target | 默认 216 × 36px，占轨道 20%（允许 18%–22%） |
| Smoking / Timer | 1320 × 56px |
| SKIP | 160 × 48px |

单张页面不得自行缩放同名组件；需要变化时应先更新全局规范。

### 4.1 Scene Feedback Layout Rules

| 状态 | Scene Background | Feedback X | Feedback Y | Feedback W | Feedback H | 对齐基准 |
|---|---|---:|---:|---:|---:|---|
| 07 自由探索 / After Clue | `1920 × 1080` 全画布 | 610 | 816 | 700 | 72 | 完整画布中心 |
| 08 对话模式 | `1920 × 1080` 全画布 | 274 | 816 | 700 | 72 | 上一版左场景视觉中心 |

约束规则：

- 07 与 08 必须使用同一套 `1920 × 1080` 场景空间，底图连续铺满画布；对话面板、HUD 与导航叠加在底图上方，未被面板覆盖的区域不得留白。
- 08 仅通过底图内部的 Camera Framing 调整人物视觉中心，不改变 Scene Background 的画布尺寸和边界。
- 07 与 08 的 Scene Feedback 使用同一尺寸：`W=700 / H=72`，避免状态切换时产生缩放跳变；位置按各自视觉中心分别对齐。
- 08 Feedback 中心点沿用上一版左侧场景视觉中心 `X=624`，因此左边界为 `X=274`；右边界为 `X=974`，与 `X=1310` 的 Dialogue Panel 保留 `336px` 水平间距。
- `Global Navigation` 顶边为 `Y=920`，Feedback 底边为 `Y=888`，两者保留 `32px` 垂直净空。
- 禁止为适应当前视觉中心缩小底图或 Feedback，也禁止出现空白区、覆盖人物面部、对话选项及全局导航。

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
│  │  └─ Dialogue_Scene_Camera_Framing
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

08 已完成拆分重搭：场景使用完整 `1920 × 1080` 背景，标题 HUD、时间、操作提示、地点、对话面板和笔记本均为场景上方的独立可编辑图层。Camera Framing 只调整视觉中心，不改变底图边界。

## 8. 09–10 点烟节点图层规则

```text
09_Smoking_Relaxation_QTE
├─ 01_QTE_Background_Viewport
│  ├─ Environment_Background
│  └─ Environment_Animation
├─ 02_Backdrop_Mask
├─ 03_Narrative_Prompt
├─ 04_QTE_Track
├─ 05_Smoke_Timer
└─ 06_Global_Navigation / SKIP

10_Smoking_FirstPerson_Street
├─ 01_First_Person_Street_Viewport
│  ├─ Environment_Background
│  ├─ Environment_Animation
│  └─ FirstPerson_Foreground
├─ 02_Inner_Monologue
├─ 03_Smoke_Timer
└─ 04_Global_Navigation / SKIP
```

执行原则：

- 09 的 QTE 是单次、低压力操作；失败不得使用红色惩罚反馈，也不得要求重试。
- 09、10 的烟条使用同一位置和尺寸，避免成功切换时跳动。
- 09 的 `QTE_Background_Viewport` 与 10 的 `First_Person_Street_Viewport` 均固定为 `X0 / Y0 / W1920 / H1080`，作为可替换背景接口。
- `Environment_Background` 接收按时间加载的静态图；`Environment_Animation` 接收视频、序列帧或 Timeline 动画，二者不得包含 QTE、烟条、独白或 SKIP。
- 10 的 `FirstPerson_Foreground` 独立承载手部、香烟和烟雾，替换环境动画时不得重做前景 UI。
- 10 的第一人称街景必须铺满画布；手部、香烟与烟雾属于主观视角前景层。
- `SKIP` 始终位于右上安全区内，层级高于 QTE、独白和场景。

## 9. 当前执行状态

- [x] 创建并锁定 `00_Global_Rules`
- [x] 按规则整理 01–07 图层
- [x] 拆分重搭 08 合成 UI
- [x] 修复 08 场景覆盖 HUD 的问题
- [x] 新增 09 点烟 QTE 与 10 第一人称街景图层规则
- [ ] 逐张进行内容、尺寸与文案精修
- [ ] 十张完成后统一配色
