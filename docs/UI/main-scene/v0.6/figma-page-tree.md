# Main Scene / Wireframe v0.6 — Figma 页面树

> 本文仅记录已从最终对话与 Figma 文件中确认的页面、版本、区域和组件分组；未确认的 Figma 节点类型不作推测。

## 来源

- Figma：[Main Scene / Wireframe v0.6](https://www.figma.com/design/hSygViz2j9LkQ419P8kHIV/Main-Scene---Wireframe-v0.6?node-id=0-1)
- 设计讨论：[游戏交互设计思路](https://chatgpt.com/share/6aa18aae-8c60-83ee-9aeb-32e1b1d3571d)

## 当前确定的页面与版本

```text
Main Scene
└── Wireframe v0.6
```

- 当前对象：`Main Scene / Wireframe v0.6`
- 当前阶段：`Wireframe`
- 当前状态：`In Progress`

## 已明确的画面结构

```text
Wireframe v0.6
├── Scene Background
├── Narrative Panel
├── Avatar Group
├── Location
├── Notebook Group
└── HUD
    ├── Top Left
    │   ├── Time
    │   ├── Period
    │   └── Narrative Controls
    │       ├── [Space] 继续
    │       └── [ESC] 返回
    └── Bottom Right
        ├── Notebook
        └── Exploration Controls
            ├── [E] 互动
            └── [Tab] 笔记本
```

## 层级说明

- `Time`、`Period` 和叙事控制位于左上区域。
- `Notebook`、`[E] 互动`、`[Tab] 笔记本`位于右下区域。
- Notebook 与互动提示组合在右下角。
- 叙事控制与探索控制必须在视觉上分离：
  - 叙事：`[Space] 继续`、`[ESC] 返回`
  - 探索：`[E] 互动`、`[Tab] 笔记本`
- 对话中明确使用 Group 命名的对象：
  - `Avatar Group`
  - `Notebook Group`

## 尚未确认的节点类型

对话与现有页面未确认以下对象是 Frame、Group、Component 还是普通 Layer：

- Scene Background
- Narrative Panel
- Location
- HUD
- Top Left
- Bottom Right
- Notebook
- Time
- Period
- 各交互提示

## 尚未确认为当前 Figma 页面树的内容

以下页面只出现在项目结构或未来规划建议中，不应认定为已经建立：

- Dialogue
- Item
- Dream
- Character Profile
- Memory Map
- Design System
- Components
- High-fi
