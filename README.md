# Build Web App Skill

一个用于构建、扩展、调试和验收 Web 应用的 Codex Skill。

它要求 Codex 先理解现有代码库和技术栈，再完成实际实现，并通过自动化检查与浏览器验证交付结果，而不是只生成孤立的代码片段。

## 能做什么

- 从零创建网站、管理后台、落地页和 Web App
- 在 React、Next.js、Vue、Svelte 等现有项目中开发页面与组件
- 将产品需求、设计稿或截图转换为可用界面
- 接入 API，处理加载、空状态、错误和表单校验
- 改善响应式布局、键盘操作和无障碍体验
- 调试浏览器问题并检查关键用户流程
- 执行格式化、类型检查、测试、构建和视觉验收

## 设计原则

- 优先沿用项目已有的框架、组件和设计系统
- 交付端到端可运行的功能，而不是无关联的脚手架
- 覆盖 loading、empty、error、success 等真实状态
- 使用语义化 HTML，并保证键盘操作和可见焦点
- 对重要 UI 修改进行桌面端和移动端浏览器检查
- 不为了“看起来高级”而堆砌无意义的卡片、渐变和动画

## 目录结构

```text
build-webapp-skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── ui-quality.md
    └── verification.md
```

- `SKILL.md`：核心工作流程和工程约束
- `agents/openai.yaml`：Skill 的展示名称和默认提示词
- `references/ui-quality.md`：视觉、响应式和无障碍规范
- `references/verification.md`：自动化检查与浏览器验收清单

## 安装

将仓库克隆到 Codex Skills 目录：

```bash
git clone https://github.com/shushiha/build-webapp-skill.git ~/.codex/skills/build-webapp
```

Windows PowerShell：

```powershell
git clone https://github.com/shushiha/build-webapp-skill.git "$HOME\.codex\skills\build-webapp"
```

重新启动 Codex 或开启新会话后即可使用。

## 使用示例

```text
Use $build-webapp to build a responsive SaaS dashboard.
```

```text
使用 $build-webapp 给这个 Next.js 项目增加一个账户设置页面。
```

```text
使用 $build-webapp 检查这个页面的移动端布局、键盘操作和错误状态，并修复发现的问题。
```

## 工作流程

1. 检查仓库结构、依赖、路由、样式和测试方式
2. 将需求转换为可观察的交付结果
3. 规划最小但完整的端到端实现
4. 遵循项目现有模式完成开发
5. 运行检查并在浏览器中验证主要流程
6. 修复验收中发现的问题并总结结果

## License

本仓库暂未声明开源许可证。公开可见不代表自动授予复制、修改或再发布权限。
