# 博客功能说明

## 功能概述

为 Web3 前端模板项目新增了完整的博客功能，包括：

- 📝 博客文章列表页面
- 📖 博客文章详情页面
- 🏷️ 标签系统
- 📱 响应式设计
- 🎨 美观的UI界面

## 页面结构

```
/blog                 # 博客列表页面
/blog/[slug]          # 博客详情页面（动态路由）
```

## 文件结构

```
src/
├── lib/
│   └── blog.ts              # 博客数据类型定义和模拟数据
├── app/
│   ├── blog/
│   │   ├── page.tsx         # 博客列表页面
│   │   └── [slug]/
│   │       ├── page.tsx     # 博客详情页面
│   │       └── not-found.tsx # 404页面
│   └── page.tsx             # 主页（已添加博客入口）
```

## 技术特性

### 1. 类型安全
- 使用 TypeScript 定义了完整的博客数据类型
- 支持文章标题、摘要、内容、作者、发布日期、标签等字段

### 2. Markdown 支持
- 使用 `react-markdown` 库渲染文章内容
- 支持标题、段落、列表、代码块等 Markdown 语法
- 自定义样式组件，保持与项目整体风格一致

### 3. 响应式设计
- 移动端友好的卡片布局
- 使用 CSS Grid 实现响应式网格
- 桌面端支持多列显示，移动端自动调整为单列

### 4. 用户体验优化
- 文章阅读时间预估
- 悬停效果和过渡动画
- 清晰的导航路径
- 友好的404页面

## 使用的技术栈

- **Next.js 14** - 框架和路由
- **TypeScript** - 类型安全
- **NextUI** - UI组件库
- **Tailwind CSS** - 样式框架
- **Lucide React** - 图标库
- **React Markdown** - Markdown渲染

## 数据管理

目前使用模拟数据，包含三篇示例文章：
1. Web3 入门指南
2. React Hooks 完全指南  
3. Next.js 性能优化实战

### 扩展数据源

可以轻松替换为其他数据源：
- 静态 Markdown 文件
- CMS 系统（如 Strapi、Contentful）
- 数据库（如 PostgreSQL、MongoDB）
- Git 仓库中的 Markdown 文件

## 访问地址

- 博客列表：`http://localhost:3000/blog`
- 博客详情：`http://localhost:3000/blog/[文章ID]`

例如：`http://localhost:3000/blog/web3-introduction`

## 特色功能

1. **标签系统**：每篇文章支持多个标签分类
2. **阅读时间**：自动计算并显示预估阅读时间
3. **SEO友好**：使用语义化HTML和清晰的URL结构
4. **无障碍访问**：支持键盘导航和屏幕阅读器
5. **性能优化**：图片懒加载、代码分割等

## 后续扩展建议

- [ ] 添加搜索功能
- [ ] 支持文章分类
- [ ] 添加评论系统
- [ ] RSS订阅支持
- [ ] 分页功能
- [ ] 相关文章推荐
- [ ] 文章收藏功能
- [ ] 社交分享按钮

## 开发说明

博客功能完全独立，不影响现有的 Web3 功能。可以根据需要进行定制和扩展。 