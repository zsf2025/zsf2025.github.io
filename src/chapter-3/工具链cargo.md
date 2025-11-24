# 工具链 (Cargo) —— 超越 NPM 的存在

写了这么多代码片段，是时候把它们变成一个真正的项目了。

作为前端，如果你没有 `npm` 或 `yarn/pnpm`，你会觉得寸步难行。 在 Rust 世界，我们有 **Cargo**。

Cargo 不仅仅是包管理器（像 npm），它还是：
* 构建工具（像 webpack/vite）
* 测试运行器（像 jest/vitest）
* 文档生成器
* 项目脚手架

## 1. 初始化项目对比
|动作|前端(npm)|Rust(Cargo)|
|--|--|--|
|初始化|`npm init -y`|`cargo new my_project`|
|添加依赖|`npm install serde`|`cargo add serde`|
|运行项目|`npm start(需配置script)`|`cargo run`|
|构建项目|`npm run build`|`cargo build --release`|

## 2. `Cargo.toml` vs `package.json`
当你运行 `cargo new hello_rust` 后，你会看到一个 `Cargo.toml` 文件。它就是 Rust 版的 `package.json`。

```TOML
[package]
name = "hello_rust"
version = "0.1.0"
edition = "2021"

[dependencies]
# 这里添加依赖
serde = "1.0"  # 类似于 JSON 处理库
```
看起来非常眼熟，对吧？

## 3. 依赖管理的爽点
前端最头疼的是什么？`node_modules` 黑洞！ Rust 的依赖管理机制虽然也会下载依赖，但它有几个让前端羡慕的特点：
1. **一致性：** `Cargo.lock` (类似 `package-lock.json`) 锁版本非常严格，几乎不会出现“我本地能跑，线上跑不起来”的情况。
2. **全局缓存：** 不同项目依赖同一个版本的库，Cargo 可能会复用磁盘上的编译产物，而不是每个项目都复制一份巨大的 `node_modules`。

## 随堂小测验（实操题）
假设你现在要在电脑上新建一个 Rust 项目，并且运行它。

在终端里，你应该依次输入哪两条命令？
1. 创建名为 `demo` 的项目。
2. 进入目录并把代码跑起来。

(这不需要写代码，只需要写出终端命令)

这章节很简单，恭喜你，我们完成了 **第一阶段：基础语法与工具链 (MVP)！** 🚀 现在的你已经能够写出简单的、线性的 Rust 程序了。

接下来我们要进入 **第二阶段：进阶数据结构。** 这一部分是 Rust 真正开始展现魅力，也是让很多前端开发者大呼“如果 JS 也能这样就好了”的地方。

我们翻开第四章！