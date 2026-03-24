# 设计系统生成器 — Claude Code 技能

### 从任何设计参考资料生成 design.md、design-guidelines.md 和 design-components.md

**🇨🇳 中文** | **[🇪🇸 Español](README.es.md)** | **[🇺🇸 English](README.md)**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/Skill-blue?style=flat-square" alt="Skill">
  <img src="https://img.shields.io/github/license/albertzhangz10/design-system-skill?style=flat-square&color=green" alt="MIT License">
  <img src="https://img.shields.io/github/stars/albertzhangz10/design-system-skill?style=flat-square" alt="GitHub Stars">
</p>

> 告别手动编写设计系统文档。上传任何设计参考资料，即可获得 3 个可直接使用的 Markdown 文件，AI 编码工具（Cursor、Claude Code、Copilot）可原生理解。

**[也可以使用网页版 — 无需安装](https://figmadesignmd.com/)**

一个 Claude Code 技能，可从任何参考资料（图片、PDF、链接、截图、品牌指南或现有代码）生成全面的设计系统文档。非技术用户（设计师、产品经理）可直接使用[网页版](https://figmadesignmd.com/)。

## 问题

设计系统散落在 Figma、品牌 PDF 和各种文档中——但 AI 编码工具所需的文档却无处可寻。每次开始新项目，你都要手动编写 Token 规范、组件指南和无障碍规则。

## 解决方案

一条命令。三份文档。来自任何设计参考。

```
/design-system
```

## 生成内容

| 文件 | 内容 | 自动 |
|------|------|:----:|
| **design.md** — 颜色、排版、形状、阴影、状态、布局、动效 | Token 文件、图片、PDF | ✅ |
| **design-guidelines.md** — 无障碍、手势、内容设计、注意事项 | 参考资料 + 推断 | ✅ |
| **design-components.md** — 30+ 组件，含变体、尺寸、状态 | 参考资料 + 推断 | ✅ |

## 工作流程

```
步骤 1  提供任何设计参考资料（图片、PDF、链接、文字、代码）
步骤 2  AI 分析所有材料中的设计语言
步骤 3  生成 3 个结构化的 Markdown 文件
步骤 4  将文件写入项目目录
步骤 5  保存前与用户确认
```

### 支持的输入类型

| 类型 | 示例 |
|------|------|
| 图片 | 截图、设计稿、设计工具导出 |
| PDF | 品牌指南、样式指南、设计规范 |
| 链接 | 设计系统文档、组件库、线上网站 |
| 文字 | 设计语言的文字描述 |
| 代码 | CSS 文件、Tailwind 配置、主题文件、设计 Token |

### 输出格式

每个文件：
- 以 H1 标题开头，并交叉引用其他 2 个文件
- 使用 Markdown 表格展示 Token 值和组件规范
- 包含具体度量值（dp/sp/px）、十六进制颜色和 CSS 值
- 按类别组织注意事项（颜色、形状、阴影、排版等）
- 按工作流分组组件（操作、输入、导航、容器、反馈）

### 组件覆盖

| 类别 | 组件 |
|------|------|
| **操作** | Button、Icon Button、FAB、Toolbar、Link |
| **输入** | Text Field、Checkbox、Radio、Switch、Slider、Dropdown、Combobox、Picker、Textarea |
| **导航** | Nav Bar/Rail/Drawer、Tabs、Breadcrumb、Menu、Search、App Bar |
| **容器** | Card、Dialog、Bottom Sheet、Drawer、Popover、Accordion、Divider |
| **数据展示** | Avatar、Badge、List、Carousel、Icon、Image、Tag/Chip、Skeleton、Tooltip |
| **反馈** | Progress Indicator、Spinner、Snackbar/Toast、Message Bar |

## 安装

```bash
# 克隆到 .claude/skills 目录
git clone https://github.com/albertzhangz10/design-system-skill.git .claude/skills/design-system
```

或将 `SKILL.md` 文件复制到项目的 `.claude/skills/design-system/` 目录。

## 使用

```
/design-system                    # 在当前目录生成
/design-system ./docs/            # 自定义输出路径
```

然后提供设计参考资料——拖放图片、粘贴链接或描述设计语言。

## 要求

| 要求 | 必需 | 备注 |
|------|:----:|------|
| Claude Code | ✅ | 建议使用最新版本 |
| 设计参考资料 | ✅ | 图片、PDF、链接、文字或代码的任意组合 |

## 许可证

MIT 许可证 — 详见 [LICENSE](LICENSE) 文件。

## 致谢

由 [Albert Zhang](https://github.com/albertzhangz10) 开发。

灵感来自 [Google Stitch design.md](https://stitch.withgoogle.com/docs/design-md/overview) —— `design.md` 的格式和结构基于他们的工作。
