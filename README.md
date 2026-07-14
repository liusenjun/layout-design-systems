# Layout Design Systems｜排版设计系统

一个可持续扩展的个人 Codex Skill，用于为已经整理完成的内容选择并应用可复用的视觉排版系统。

当前包含的第一套设计系统是 **Editorial Longform**：一种干净、克制、具有编辑排版节奏的长篇 HTML 网页设计，适合课程笔记、视频或播客总结、深度文章、方法论和知识文档。

## 当前设计系统

| 设计系统 | 适用场景 | 输出形式 |
|---|---|---|
| Editorial Longform | 长篇阅读、学习笔记、内容总结和深度分享 | 可独立打开的 HTML 网页 |

## 安装

将仓库克隆到个人 Codex Skills 目录：

```bash
git clone https://github.com/liusenjun/layout-design-systems.git ~/.codex/skills/layout-design-systems
```

如果该目录已经存在，请先克隆到其他位置，再有选择地复制或更新文件，避免覆盖尚未保存的本地修改。

## 使用方法

让 Skill 根据目的、阅读对象、内容形态和输出媒介推荐设计系统：

```text
请使用 $layout-design-systems，为我已经整理好的内容推荐并应用合适的排版设计系统。
```

直接指定当前的 Editorial Longform：

```text
请使用 $layout-design-systems 中的 Editorial Longform，把已经整理好的内容制作成适合深度阅读的独立网页。
```

当用户没有明确指定设计系统时，Skill 会先给出推荐和简短理由，等待用户确认后再执行。

## 职责边界

这个 Skill 只负责视觉呈现与排版，包括：

- 根据内容现有语义选择合适的视觉组件；
- 应用颜色、字体、间距、布局和阅读节奏；
- 生成可独立打开、支持移动端和打印的视觉成品；
- 在多套设计系统之间进行推荐和选择。

它不负责内容提取、音视频转写、资料搜索、事实核对、观点补充或重新总结。使用设计系统前，应先完成内容研究和整理。

## 目录结构

```text
layout-design-systems/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── design-systems/
│   ├── design-system-catalog.md
│   └── editorial-longform-design.md
└── assets/
    └── editorial-longform-template.html
```

- `SKILL.md`：负责设计系统的选择、加载、执行与验证流程。
- `design-systems/`：保存每套设计系统的完整 Design MD。
- `assets/`：保存生成视觉成品时复用的模板与资源。
- `agents/openai.yaml`：定义 Skill 在 Codex 中的显示信息和默认提示。

## 后续扩展

未来可以继续加入适用于项目汇报、客户提案、网页 PPT、研究报告等不同目的和媒介的设计系统。

新的设计系统只有经过真实项目验证后，才会被登记为正式可用。
