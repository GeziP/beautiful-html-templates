# Quaero Beautiful HTML Templates

为 AI 驱动的演示文稿生成而设计的精美 HTML 模板库。

30+ 生产级 HTML 幻灯片模板，内置 Quaero institutional chrome — 让任何 AI agent 都能自动选择合适的模板，生成漂亮的演示文稿。

## 快速开始

告诉你的 AI agent：

```
克隆 https://github.com/GeziP/quaero-beautiful-html-templates，按照 AGENTS.md 的指引为我生成一份 HTML 演示文稿。
```

使用本库的 Agent 应先阅读 [`AGENTS.md`](./AGENTS.md)。这是操作手册：如何读取 `index.json`、匹配用户需求与模板、克隆并替换内容。

## Quaero Chrome

每个模板都包含 Quaero institutional chrome — 一套统一的顶栏和底栏，会根据幻灯片背景自动调整明暗：

- 顶栏显示当前幻灯片标题和页码
- 底栏显示 Quaero logo 和保密声明
- 根据背景亮度自动切换明/暗文字

## 模板结构

所有模板位于 `templates/` 目录：

```
templates/<template-slug>/
  template.html      # 独立的 HTML 幻灯片
  template.json      # 元数据：风格、配色、适用场景
  styles.css         # （可选）外部样式
  deck-stage.js      # （可选）自定义幻灯片引擎
```

浏览 [`templates/`](./templates/) 文件夹查看所有模板。每个 `template.json` 描述了模板的视觉系统、风格和适用场景 — Agent 用这些元数据来匹配用户需求。

## 工作流程

1. Agent 询问用户演示场景和期望风格
2. Agent 读取 `index.json`，匹配 3 个候选模板
3. Agent 为每个候选模板生成封面预览
4. Agent 克隆用户选择的模板并替换内容
5. Agent 将完成的演示文稿写入指定位置

详见 [`AGENTS.md`](./AGENTS.md)。

## 许可证

[MIT](./LICENSE) — 自由使用、修改和分发。
