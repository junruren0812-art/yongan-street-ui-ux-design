# yongan-street-ui-ux-design

永安街游戏 UI/UX 产品设计仓库，用于统一管理界面设计文档、线框图和版本变更记录。

## 仓库目录

```text
yongan-street-ui-ux-design/
├── README.md
├── docs/
│   └── UI/
│       └── main-scene/
│           ├── v0.6.md
│           ├── v0.6/
│           │   ├── figma-page-tree.md
│           │   ├── figma-ui-spec.md
│           │   └── reviews/
│           │       └── 2026-09-10-round-01.md
│           ├── v0.7.md
│           └── v0.7/
│               ├── global-rules.md
│               └── round-01-action-list.md
├── assets/
│   └── wireframe/
│       └── main-scene/
│           ├── v0.6.png
│           ├── v0.7.png
│           └── v0.7-global-rules.png
└── changelog.md
```

## 页面索引

| 页面 | 当前版本 | 设计文档 | 线框图 | 状态 |
|---|---|---|---|---|
| 主场景 | v0.7 | [查看文档](docs/UI/main-scene/v0.7.md) | [查看线框图](assets/wireframe/main-scene/v0.7.png) | 待评审 |

## 历史版本

- 主场景 v0.6：[设计文档](docs/UI/main-scene/v0.6.md) · [Figma 页面树](docs/UI/main-scene/v0.6/figma-page-tree.md) · [Figma UI 规格](docs/UI/main-scene/v0.6/figma-ui-spec.md) · [Round 01 评审](docs/UI/main-scene/v0.6/reviews/2026-09-10-round-01.md) · [线框图](assets/wireframe/main-scene/v0.6.png)
- 主场景 v0.7：[Figma](https://www.figma.com/design/hSygViz2j9LkQ419P8kHIV/Main-Scene---Wireframe-v0.7?node-id=202-2&p=f) · [设计文档](docs/UI/main-scene/v0.7.md) · [全局规范](docs/UI/main-scene/v0.7/global-rules.md) · [规范板预览](assets/wireframe/main-scene/v0.7-global-rules.png) · [Round 01 修改清单](docs/UI/main-scene/v0.7/round-01-action-list.md) · [十状态线框图](assets/wireframe/main-scene/v0.7.png)

## 目录说明

- `docs/UI/`：UI 页面设计与交互说明
- `assets/wireframe/`：页面线框图与设计图片
- `changelog.md`：版本变更记录

## 文件命名规范

- 页面目录使用小写英文和连字符，例如 `main-scene`
- 设计文档与线框图使用相同版本号
- 新版本不覆盖旧版本，例如从 `v0.6` 新增到 `v0.7`

## 当前进度

- [x] 建立项目目录
- [x] 创建主场景 v0.6、v0.7 基础文档
- [x] 归档主场景 v0.6 Figma 页面树和 UI 规格
- [x] 用 Figma 画板截图替换 v0.6 占位图片
- [x] 建立主场景 v0.6 Round 01 评审文档
- [x] 完成主场景 v0.6 Round 01 Game UX 评审
- [x] 确认并建立 v0.7 Round 01 修改清单
- [x] 完成 v0.7 修改清单中的 8 个最低状态线框
- [x] 用正式线框图替换 v0.7 占位图片
- [x] 完善 v0.7 主场景功能与交互说明
- [x] 创建并锁定 v0.7 `00_Global_Rules`
- [x] 按 Layer Order 拆分整理 01–07
- [x] 拆分重搭 08 并修复场景覆盖 HUD
- [x] 新增 09 点烟 QTE 与 10 第一人称街景，补齐 08→09→10 条件过渡
- [x] 将 Figma 文件更新为 `Main Scene / Wireframe v0.7`，同步 GitHub 文档与 PNG 迭代记录
- [ ] 确认 v0.7 修改清单中的系统边界与触发规则
- [ ] 完成设计评审

## 维护者

任俊茹
