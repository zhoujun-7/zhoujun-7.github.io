# al-folio 中文支持

这个项目为 al-folio 主题添加了完整的中文语言支持。

## 功能特性

### 🌐 多语言支持
- **英文版本**: `/about/` - 原始英文页面
- **中文版本**: `/about_zh/` - 完整中文化页面
- **语言切换**: 导航栏中的语言下拉菜单

### 📱 响应式设计
- 完全响应式布局
- 支持移动端和桌面端
- 优化的中文排版

### 🎨 自定义样式
- 中文友好的字体和间距
- 优化的社交媒体图标颜色
- 改进的标题层次结构

## 文件结构

```
al-folio/
├── _pages/
│   ├── about.md          # 英文版本（主页）
│   ├── about_zh.md       # 中文版本
│   └── language.md       # 语言切换菜单
├── _data/
│   └── navigation_zh.yml # 中文导航配置
├── _config.yml           # 英文配置
├── _config_zh.yml        # 中文配置
└── README_ZH.md          # 本文件
```

## 使用方法

### 1. 访问不同语言版本

- **英文主页**: `https://zhoujun-7.github.io/`
- **中文主页**: `https://zhoujun-7.github.io/about_zh/`

### 2. 通过导航菜单切换

在网站导航栏中，点击 "Language" 下拉菜单，选择：
- English - 切换到英文版本
- 中文 - 切换到中文版本

### 3. 页面内语言切换

在每个页面的底部都有语言切换链接：
- [English Version](/about/)
- [中文版本](/about_zh/)

## 自定义配置

### 修改中文内容

编辑 `_pages/about_zh.md` 文件来修改中文页面的内容：

```markdown
---
layout: about
permalink: /about_zh/
title: 关于我
subtitle: 个人简介和研究兴趣
nav: true
nav_order: 1
profile:
  align: right
  image: prof_pic_zj.jpg
  image_circular: false
  more_info: >
    <p>中国地质大学博士研究生</p>
    <p>研究方向：3D计算机视觉</p>
social: true
selected_papers: true
latest_posts: true
---
```

### 修改导航菜单

编辑 `_data/navigation_zh.yml` 文件来自定义中文导航：

```yaml
main:
  - title: "首页"
    url: "/about_zh/"
    description: "个人主页"
  - title: "博客"
    url: "/blog/"
    description: "最新文章"
```

### 使用中文配置

如果你想完全使用中文配置，可以：

1. 备份当前的 `_config.yml`
2. 将 `_config_zh.yml` 重命名为 `_config.yml`
3. 重新构建网站

## 技术细节

### 语言标识

- 英文页面: `lang: en`
- 中文页面: `lang: zh`

### SEO 优化

- 中文页面使用中文关键词
- 优化的中文描述和标题
- 支持中文搜索引擎

### 字体支持

- 支持中文字符显示
- 优化的行高和字间距
- 响应式字体大小

## 部署说明

### GitHub Pages

1. 推送代码到 GitHub
2. 在仓库设置中启用 GitHub Pages
3. 选择 `gh-pages` 分支作为源
4. 等待自动部署完成

### 本地测试

```bash
# 安装依赖
bundle install

# 本地运行
bundle exec jekyll serve

# 访问 http://localhost:4000
```

## 维护和更新

### 添加新页面

1. 创建新的 Markdown 文件
2. 添加适当的前置信息
3. 设置导航顺序
4. 添加语言切换链接

### 更新内容

- 英文内容: 编辑 `_pages/about.md`
- 中文内容: 编辑 `_pages/about_zh.md`
- 导航配置: 编辑 `_data/navigation_zh.yml`

### 同步更新

建议同时更新两个语言版本，保持内容一致性。

## 故障排除

### 常见问题

1. **页面不显示**: 检查 `nav: true` 和 `nav_order` 设置
2. **链接失效**: 确认 `permalink` 设置正确
3. **样式问题**: 检查 CSS 文件是否正确加载

### 获取帮助

如果遇到问题，可以：
1. 检查 GitHub Actions 日志
2. 查看 Jekyll 构建错误
3. 参考 al-folio 官方文档

## 贡献

欢迎提交 Issue 和 Pull Request 来改进中文支持！

## 许可证

本项目基于 al-folio 主题，遵循相同的许可证。
