<!--
 * @Description: 
 * @Author: zhangfu 18072150332@163.com
 * @Date: 2025-11-24 17:37:51
 * @LastEditors: zhangfu 18072150332@163.com
 * @LastEditTime: 2025-11-24 18:16:58
-->
前端开发者的Rust迷你书

## mdBook 快速入门
mdBook 是一个用于创建和管理 Rust 项目文档的工具。它基于 Markdown 格式，支持代码高亮、表格、数学公式等。

## Rust环境安装
### 安装 Rust
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### 安装 mdBook
```
cargo install mdbook
```

## 实时预览
```
mdbook serve --open
```

## 构建发布
构建文档
```
mdbook build
```