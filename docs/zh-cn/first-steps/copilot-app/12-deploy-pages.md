---
title: "课程 12 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot 应用配置 Pages 工作流、审查拉取请求，并验证已发布的 Space Quiz。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

将 Space Quiz 部署到 GitHub Pages，让所有人都能访问。Copilot 可以准备工作流并指导部署，但你需要负责审查更改并确认网站已上线。

在本课程中，你将：

- 请求 Copilot 配置 GitHub Pages 部署。
- 在合并之前审查工作流和拉取请求。
- 跟踪部署过程并验证已发布的网站。

## 场景

Space Quiz 已经位于 GitHub 仓库中，但其他人仍需要一种简单的方式来体验它。使用 GitHub Pages 发布这个单文件网站后，用户可以通过公开 URL 访问，而无需添加服务器或运行时依赖项。

## 请求 Copilot 部署网站

在 `space-quiz` 的 Copilot 应用会话中发送以下提示：

```plaintext
为此仓库启用 GitHub Pages。创建一个 GitHub Actions 工作流，在需要时构建网站并将其部署到 GitHub Pages。如果仓库中还没有 README，请添加一个，介绍应用以及如何在本地运行。使用这些更改创建拉取请求，并在必需的检查通过后合并。持续监控部署，直到成功，然后报告在线网站的最终 URL。如果你没有启用 Pages 或合并的权限，请明确告诉我需要批准或执行什么操作；网站上线之前不要报告成功。
```

![三阶段示意图：已合并的 space-quiz 拉取请求；成功运行的 GitHub Actions Deploy website 工作流，包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及在 yourname.github.io/space-quiz/ 上线的 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示要求代理创建并合并拉取请求，以及更改仓库的 Pages 设置。继续之前，请审查差异、部署权限和 GitHub 显示的任何审批请求。

## 审查工作流并验证部署

1. 确认只有在仓库尚无 README 时才添加 README。
2. 审查拉取请求中的更改，包括工作流的构建和部署步骤。
3. 只有必需的拉取请求检查通过后才合并。
4. 跟踪 GitHub Actions 部署运行，直到成功。
5. 打开报告中的 URL，确认 Space Quiz 可以正常加载。

如果代理无法启用 Pages 或合并拉取请求，请按照它提供的具体说明操作。只有部署成功且网站可以正常加载后，才能将任务视为完成。

## 总结和后续步骤

Space Quiz 现已作为在线网站供用户访问，你也亲自验证了部署，而不是仅依赖代理的报告。继续学习[课程 13：回顾与后续步骤][next-lesson]。

[next-lesson]: ../13-review/
