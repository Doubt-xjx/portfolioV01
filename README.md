<p align="center">
  <img src="/public/favicon.svg" width="50" alt="Logo" />
</p>
<h1 align="center">Personal portfolio</h1>

[![Site preview](/public/site-preview.png)](https://hamishw.com)

我的个人作品集网站，用于展示一些项目作品。使用 [Remix](https://remix.run/)、[Three.js](https://threejs.org/) 和 [Framer Motion](https://www.framer.com/motion/) 构建。查看[在线网站](https://hamishw.com)或[组件 Storybook](https://storybook.hamishw.com)。

## 技术栈

- **框架**: Remix.js, React 18
- **3D 渲染**: Three.js
- **动画**: Framer Motion
- **样式**: CSS Modules
- **部署**: Cloudflare Pages
- **包管理**: npm

## 项目结构

```
app/
├── assets/        # 静态资源文件
├── components/    # React 组件
├── hooks/         # 自定义 React Hooks
├── layouts/       # 布局组件
├── routes/        # 页面路由
└── utils/         # 工具函数
```

## 主要功能

- 响应式设计，支持多设备浏览
- 3D 交互效果和动画
- 暗色/亮色主题切换
- 项目展示页面
- 博客文章系统
- 联系表单

## 安装运行

确保你安装了 nodejs `19.9.0` 或更高版本，以及 npm `9.6.3` 或更高版本。安装依赖：

```bash
npm install
```

启动本地开发服务器：

```bash
npm run dev
```

查看组件 Storybook：

```bash
npm run dev:storybook
```

## 部署

本站使用 Cloudflare Pages 进行托管。部署到 Cloudflare Pages：

```bash
npm run deploy
```

## 开发指南

1. 组件开发遵循原子设计模式
2. 使用 CSS Modules 进行样式管理
3. 遵循 ESLint 和 Prettier 代码规范
4. 新功能开发请先编写 Storybook 组件文档

## 许可说明

我允许任何人使用代码或部分代码来构建自己的网站，这是开源的，人们可以从中学习和改编。但是，我建议你修改主题和组件，使其成为你自己的作品。如果你在很大程度上使用了本站的设计而没有修改，我希望你能注明我是网站的设计者。

我不允许将我的任何项目展示为你自己的作品（这是我正在使用的作品集网站，这些都是我实际参与的项目）。

## FAQs

<details>
  <summary>如何更改 <code>DisplacementSphere</code>（背景中旋转的斑点）的颜色？</summary>
  
  你需要编辑片段着色器。[查看此 issue 了解更多详情](https://github.com/HamishMW/portfolio/issues/19#issuecomment-870996615)。
</details>

<details>
  <summary>如何让联系表单工作？</summary>
  
  要使联系表单工作，请创建一个 AWS 账户并设置 SES（Simple Email Service）。然后将你的详细信息填入 `.dev.vars.example` 并将其重命名为 `.dev.vars`。你还需要在 Cloudflare 仪表板中将这些作为环境变量添加，以使其在生产环境中工作。或者如果你不介意通过 Gmail 发送，可以使用 [nodemailer](https://nodemailer.com/) 替代。
</details>
