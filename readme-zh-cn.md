[English](./README.md) | **简体中文**

<p align="center">
  <img src="./docs/brand/logo.png" width="120" height="120" alt="Questionnaire Star · Respondent logo" />
</p>

<div align="center">

# 问卷星 · C 端

<p><strong>面向问卷填写者的轻量前端原型</strong></p>

<p>
  <a href="https://github.com/tuolola/qustion-star-c"><img src="https://img.shields.io/badge/GitHub-Repository-2563eb?style=for-the-badge" alt="GitHub repository" /></a>
  <a href="https://gitee.com/guolola/qustion-star-c"><img src="https://img.shields.io/badge/Gitee-Original-0f766e?style=for-the-badge" alt="Original Gitee repository" /></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Frontend-Next.js%2015-111827?style=flat-square" alt="Frontend: Next.js 15" />
  <img src="https://img.shields.io/badge/UI-React%2019-2563eb?style=flat-square" alt="UI: React 19" />
  <img src="https://img.shields.io/badge/Language-TypeScript-3178c6?style=flat-square" alt="Language: TypeScript" />
  <img src="https://img.shields.io/badge/Status-Early%20prototype-0f766e?style=flat-square" alt="Status: Early prototype" />
</p>

</div>

## 项目简介

使用 Next.js App Router、React 与 TypeScript 编写的问卷填写端早期原型。当前源码在 `/question/[id]` 展示示例问卷，包含文本输入与单选题组件，适合作为学习和继续开发的起点。

## 核心能力

| 模块 | 说明 |
| --- | --- |
| 问卷路由 | 通过动态路由接收问卷标识，并写入隐藏字段。 |
| 文本输入 | 提供带题目与占位提示的输入组件。 |
| 单选题 | 提供选项及横向、纵向排列配置。 |
| 样式组织 | 使用 CSS Modules 管理题目和页面样式。 |

## 快速开始

准备与仓库锁定的 Next.js 15 依赖兼容的 Node.js 环境。

```bash
git clone https://github.com/tuolola/qustion-star-c.git
cd qustion-star-c
npm ci
npm run dev
```

访问 `http://localhost:3000/question/demo`。当前源码没有根路径 `src/app/page.tsx` 首页，请直接打开问卷路由。

## 项目结构

| 目录 / 文件 | 职责 |
| --- | --- |
| `src/app/question/[id]/` | 示例问卷页面与页面样式 |
| `src/components/QuestionInput/` | 文本输入组件 |
| `src/components/QuestionRadio/` | 单选题组件 |
| `src/app/layout.tsx` | 应用根布局 |

## 常用命令

| 命令 | 用途 |
| --- | --- |
| `npm run dev` | 启动开发服务器 |
| `npm run build` | 生成生产构建 |
| `npm run start` | 启动已构建的生产服务 |

## 当前范围与配置

示例题目目前写在页面中；表单 action 为空，尚未实现提交接口、持久化和结果页。收集真实答卷前，需要接入后端并补充提交校验。原有 `lint` 脚本调用 `next lint`，与当前框架版本的兼容性需另行调整。配套 [B 端编辑器](https://github.com/tuolola/questionnaire-star---react) 是独立前端，本仓库没有提供两端共用的完整后端。

## 视觉标识

青绿色问卷纸张、勾选符号与星芒，表达填写者完成问卷的过程。

## 许可证与第三方材料

原仓库未提供项目根级许可证。公开仓库本身不等于授予通用开源许可；使用、修改或分发前，请联系维护者确认授权。第三方源码、SDK、字体及资源继续遵循各自附带的许可证。
