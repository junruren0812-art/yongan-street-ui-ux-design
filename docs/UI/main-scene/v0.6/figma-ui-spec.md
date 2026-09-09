# Main Scene / Wireframe v0.6 — Figma UI 规格

## 来源

- Figma：[Main Scene / Wireframe v0.6](https://www.figma.com/design/hSygViz2j9LkQ419P8kHIV/Main-Scene---Wireframe-v0.6?node-id=0-1)
- 设计讨论：[游戏交互设计思路](https://chatgpt.com/share/6aa18aae-8c60-83ee-9aeb-32e1b1d3571d)
- 页面树：[figma-page-tree.md](figma-page-tree.md)
- 导出图片：[v0.6.png](../../../../assets/wireframe/main-scene/v0.6.png)

## 1. 版本状态

- 页面：`Main Scene`
- 版本：`Wireframe v0.6`
- 状态：`Wireframe / In Progress`

## 2. 画布规格

| 字段 | 规格 |
|---|---:|
| Resolution | `1920 × 1080 px` |
| Aspect Ratio | `16:9` |
| Safe Area | `48 px` |
| Grid | `8 px` |

## 3. 布局与尺寸

| 元素 | 尺寸 | 位置 |
|---|---:|---|
| Scene Background | `1920 × 1080 px` | 未提供精确坐标 |
| Narrative Panel | `528 × 696 px` | `X 1344 / Y 144` |
| Avatar Group | `208 × 96 px` | 未提供精确坐标 |
| Location | `320 × 48 px` | 未提供精确坐标 |
| Notebook Group | `280 × 120 px` | 右下区域，未提供精确坐标 |

## 4. Safe Area

- 已确认值：`48 px`
- 尚未确认：
  - 是否四边统一内缩
  - Safe Area 的实际 Frame 尺寸
  - 各组件是否必须完全限制在 Safe Area 内
  - 各元素相对 Safe Area 的锚定与约束方式

## 5. Grid

- 已确认值：`8 px`
- 尚未确认：
  - Grid 类型
  - 列数、列宽、gutter 与 margin
  - 是否为方格网格或布局网格
  - Grid 起始偏移

## 6. HUD

### 左上区域

包含：

- 时间：`17:35`
- 时段：`黄昏`
- 叙事控制：
  - `[Space] 继续`
  - `[ESC] 返回`

明确变更：

- 时间信息移动到左上角。
- 叙事控制移动到左上角。

### 右下区域

包含：

- `Notebook`
- `[E] 互动`
- `[Tab] 笔记本`

明确关系：

- Notebook 与互动提示组合在右下角。
- 探索控制位于 Notebook 下方。

## 7. 交互按钮分类

### 叙事控制

| 按键 | 操作 |
|---|---|
| `Space` | 继续 |
| `ESC` | 返回 |

### 探索控制

| 按键 | 操作 |
|---|---|
| `E` | 互动 |
| `Tab` | 笔记本 |

## 8. 已接受的设计决策

### Decision #001：主场景保持全屏

- 决策：Scene 保持全屏。
- 状态：`Accepted`
- 原因：环境叙事很重要。

### Decision #002：对话使用覆盖层

- 决策：Dialogue 以 overlay 形式覆盖场景，而不是替换场景或裁切场景区域。
- 状态：`Accepted`
- 原因：
  - 对话占据叙事体验的较大部分。
  - 同时必须保留环境信息的可见性。

### Decision #003：叙事控制与探索控制视觉分离

- 决策：Narrative controls 与 exploration controls 必须在视觉上分开。
- 状态：`Accepted`
- 原因：之前的布局混合了两类控制；分开可以减少交互歧义。

## 9. v0.6 设计结论

1. 场景保持全屏。
2. Dialogue 作为场景上的覆盖层显示，不裁切场景区域。
3. 时间信息放置在左上角。
4. 叙事控制与探索控制分离。
5. Notebook 与互动提示组合在右下角。
6. 叙事控制位于左上区域。
7. 探索控制位于 Notebook 下方。

## 10. 下一步

- Review dialogue readability：检查对话内容可读性。
- Validate interaction hierarchy：验证交互层级。
- Test object interaction state：测试物体交互状态。
- Prepare high-fidelity visual design：准备高保真视觉设计。

## 11. 尚未确认的规格

### 位置与尺寸

- Avatar Group、Location、Notebook Group 的精确 X/Y 坐标
- 左上 HUD 各元素的精确坐标
- 按钮、文字、图标的独立尺寸
- Narrative Panel 内部 padding、间距与对齐方式
- 响应式缩放与其他分辨率适配规则

### 视觉

- 字体、字号、字重、行高、字距
- 颜色、透明度、描边、圆角、阴影
- 背景图或场景美术规格
- 图标样式与尺寸
- 按钮各交互状态
- 对话面板、Avatar 和 Notebook 的具体视觉形式

### 交互

- `[Space] 继续`在无后续文本时的行为
- `[ESC] 返回`的目标状态或页面
- `[E] 互动`的触发距离、目标选择规则与反馈
- `[Tab] 笔记本`是按下、按住还是切换开关
- 键盘焦点、手柄和触屏映射
- Dialogue overlay 是否阻断场景探索输入
- 动画、转场、反馈时长和缓动参数

## 12. 不归入 v0.6 的后续建议

以下只出现在后续版本示例中，尚未确认为 v0.6 内容：

- Interactive Object Highlight
- Interaction Icon
- Object Hover State
- Object Selected State
- Notebook interaction flow 调整
- Object inspection hierarchy 调整
- Interaction prompt hierarchy 修正
