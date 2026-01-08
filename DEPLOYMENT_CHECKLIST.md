# Vercel 部署检查清单

## 已完成的配置

- [x] 更新了 [next.config.ts](file:///c:/code/nextjs-app/next.config.ts) 以包含适合 Vercel 的配置
- [x] 添加了 [vercel.json](file:///c:/code/nextjs-app/vercel.json) 部署配置文件
- [x] 修正了 [postcss.config.mjs](file:///c:/code/nextjs-app/postcss.config.mjs) 配置
- [x] 创建了 [tailwind.config.ts](file:///c:/code/nextjs-app/tailwind.config.ts) 配置文件
- [x] 更新了 [README.md](file:///c:/code/nextjs-app/README.md) 包含部署说明
- [x] 创建了 [.env.example](file:///c:/code/nextjs-app/.env.example) 环境变量示例文件

## 部署到 Vercel 的步骤

### 方法 1：Git 集成（推荐）

1. 将项目推送到 GitHub、GitLab 或 Bitbucket
2. 访问 [Vercel Dashboard](https://vercel.com/dashboard)
3. 点击 "Add New Project"
4. 选择你的代码仓库
5. Vercel 会自动检测这是 Next.js 项目并配置构建设置
6. 点击 "Deploy" 完成部署

### 方法 2：使用 Vercel CLI

1. 安装 Vercel CLI：
   ```bash
   npm i -g vercel
   ```

2. 登录 Vercel 账户：
   ```bash
   vercel login
   ```

3. 部署项目：
   ```bash
   vercel
   ```

## 项目兼容性

- ✅ Next.js 16.1.1 兼容 Vercel
- ✅ 使用 App Router 架构
- ✅ TypeScript 配置正确
- ✅ Tailwind CSS 配置正确
- ✅ 包管理器为 pnpm（Vercel 支持）

## 环境变量

如果项目需要环境变量，请在 Vercel 仪表板的项目设置中添加。

## 自定义配置

[vercel.json](file:///c:/code/nextjs-app/vercel.json) 文件包含了以下配置：
- 使用 Next.js 框架适配器
- 设置函数最大执行时间为 60 秒
- 配置了适当的路由规则

## 故障排除

如果在构建时遇到问题：
1. 确保所有依赖项都已正确安装
2. 检查 [next.config.ts](file:///c:/code/nextjs-app/next.config.ts) 中的配置是否正确
3. 验证 [postcss.config.mjs](file:///c:/code/nextjs-app/postcss.config.mjs) 和 [tailwind.config.ts](file:///c:/code/nextjs-app/tailwind.config.ts) 配置
4. 确保所有环境变量都已正确设置
5. 确认 [tailwind.config.ts](file:///c:/code/nextjs-app/tailwind.config.ts) 文件存在并配置正确