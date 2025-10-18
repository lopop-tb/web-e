# Vercel 部署指南

## 项目配置检查 

### 1. package.json 配置
-  build 脚本: "build": "next build"
-  dev 脚本: "dev": "next dev" 
-  start 脚本: "start": "next start"
-  所有依赖已正确安装

### 2. Next.js 配置
-  使用 App Router (app/ 目录)
-  next.config.mjs 已优化
-  图片优化配置完成
-  构建输出优化完成

### 3. Vercel 配置
-  vercel.json 配置文件已创建
-  框架检测: Next.js
-  区域设置: 香港和新加坡

## 部署步骤

### 方法一：使用 Vercel CLI（推荐）

1. 安装 Vercel CLI
`ash
npm install -g vercel
`

2. 登录 Vercel
`ash
vercel login
`

3. 部署项目
`ash
vercel
`

4. 生产环境部署
`ash
vercel --prod
`

### 方法二：使用 Vercel 网页界面

1. 访问 https://vercel.com
2. 使用 GitHub/GitLab/Bitbucket 账号登录
3. 点击 "New Project"
4. 导入您的 Git 仓库
5. Vercel 会自动检测到 Next.js 项目
6. 点击 "Deploy"

## 部署后

- 您将获得一个类似 your-project-name.vercel.app 的域名
- 可以自定义域名（在 Vercel 控制台中）
- 支持自动 HTTPS
- 全球 CDN 加速

## 注意事项

- API 路由需要动态渲染（这是正常的）
- 图片已配置为未优化模式以兼容 Vercel
- 构建警告不影响部署
- 项目已优化为生产环境

## 故障排除

如果部署失败，请检查：
1. Node.js 版本兼容性
2. 依赖包是否正确安装
3. 环境变量配置
4. 构建日志中的错误信息
