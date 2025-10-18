#  诺天科技企业官网 - 部署指南

##  项目状态
 **项目已准备就绪，可以部署！**

##  已解决的问题
1.  字体加载问题 - 已添加 fallback 字体
2.  图片路径问题 - 已修复所有图片引用
3.  构建错误 - 已修复所有语法错误
4.  Git 存储库 - 已初始化并提交代码

##  项目信息
- **项目名称**: 诺天科技企业官网
- **技术栈**: Next.js 14 + TypeScript + Tailwind CSS
- **状态**: 构建成功，可以部署

##  创建 GitHub 存储库

### 方法一：使用 GitHub 网页界面（推荐）

1. **访问 GitHub**
   - 打开 https://github.com
   - 登录您的账号

2. **创建新存储库**
   - 点击右上角的 "+" 号
   - 选择 "New repository"
   - 存储库名称：
uotech-website 或 
uotech-corporate-site
   - 描述：诺天科技企业官网 - AI机器人智能制造解决方案
   - 选择：Public（公开）或 Private（私有）
   - **不要**勾选 "Add a README file"
   - **不要**勾选 "Add .gitignore"
   - **不要**勾选 "Choose a license"
   - 点击 "Create repository"

3. **获取存储库 URL**
   - 复制显示的 HTTPS 或 SSH URL
   - 例如：https://github.com/yourusername/nuotech-website.git

### 方法二：使用 GitHub CLI（如果已安装）

`ash
gh repo create nuotech-website --public --description "诺天科技企业官网"
`

##  推送代码到 GitHub

在项目目录中运行以下命令：

`ash
# 添加远程存储库（替换为您的实际 URL）
git remote add origin https://github.com/yourusername/nuotech-website.git

# 推送代码到 GitHub
git push -u origin master
`

##  部署到 Vercel

### 方法一：通过 GitHub 连接（推荐）

1. **访问 Vercel**
   - 打开 https://vercel.com
   - 使用 GitHub 账号登录

2. **导入项目**
   - 点击 "New Project"
   - 选择您刚创建的 GitHub 存储库
   - Vercel 会自动检测到 Next.js 项目

3. **部署设置**
   - 框架：Next.js（自动检测）
   - 构建命令：
pm run build（自动设置）
   - 输出目录：.next（自动设置）

4. **开始部署**
   - 点击 "Deploy" 按钮
   - 等待部署完成（通常 2-3 分钟）

### 方法二：使用 Vercel CLI

`ash
# 安装 Vercel CLI
npm install -g vercel

# 登录 Vercel
vercel login

# 部署项目
vercel

# 生产环境部署
vercel --prod
`

##  重要说明

1. **确保 GitHub 存储库不为空** - 已通过 Git 提交解决
2. **确保所有文件都已提交** - 已通过 git add . 和 git commit 解决
3. **确保构建成功** - 已通过 
pm run build 验证

##  部署后

- **域名**: your-project-name.vercel.app
- **自动 HTTPS**: 免费 SSL 证书
- **全球 CDN**: 快速访问
- **自动部署**: 每次 Git push 自动更新

##  如果遇到问题

1. **"存储库为空"错误**
   - 确保已运行 git add . 和 git commit
   - 确保已推送到 GitHub：git push -u origin master

2. **构建失败**
   - 检查 Node.js 版本 >= 18
   - 运行 
pm install 安装依赖
   - 运行 
pm run build 测试构建

3. **部署失败**
   - 检查 Vercel 控制台的构建日志
   - 确保所有环境变量已正确设置

##  完成！

按照上述步骤操作，您的项目就能成功部署了！

**下一步**：
1. 创建 GitHub 存储库
2. 推送代码到 GitHub
3. 在 Vercel 中导入并部署项目
4. 将部署链接发给客户
