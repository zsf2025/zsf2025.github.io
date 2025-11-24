# 前端开发者的Rust迷你书
现在很多高性能的前端工具（如 SWC，Turbopack 等）都是用 Rust 编写的，掌握它已经成为前端工程师进阶的重要加分项。

这个是一本为前端人员量身定的Rust迷你电子书，我会大量使用Javascript/Typescript作为类比，通过“对比学习法”来帮助你理解Rust的核心概念。

为了“深入浅出”，我们不需要一开始就背诵复杂语法，而是通过一个个具体的场景来学习。以下是本书的一个章节规划：

# 目录
- 第一阶段: 基础语法与心态转变（MVP）
  - 第一章：变量与数据类型
    - [变量--默认的"偏执"](./src/chapter-1/变量.md)
    - [数据类型--告别"number"一把梭](./src/chapter-1/数据类型.md)
  - 第二章：所有权（Ownership）
    - [所有权 (Ownership) —— 内存管理的"第三条路"](./src/chapter-2/rust所有权.md)
    - [借用 (Borrowing) —— 省钱又省力的 "引用"](./src//chapter-2/rust借用.md)
  - 第三章：工具链初探(Cargo)
    - [工具链 (Cargo) —— 超越 NPM 的存在](./src/chapter-3/工具链cargo.md)
- 第二阶段: 进阶数据结构（最精彩的部分）
  - 第四章：结构体与枚举（Structs & Enums）
    - [结构体与枚举 —— 数据的"骨架"](./src/chapter-4/结构体与枚举.md)
  - 第五章：模式匹配（Pattern Matching）
    - [模式匹配 (match) —— 吃了"大力丸"的 switch](./src/chapter-5/模式匹配.md)
  - 第六章：错误处理（Result & Option）
    - [错误处理 —— 告别 null 和 try-catch](./src/chapter-6/错误处理.md)
- 第三阶段：抽象与并发（高级）
  - 第七章：Trait（特质）
    - [Trait (特质) —— 也就是“接口”](./src/chapter-7/Trait.md)
  - 第八章：集合类型（Collections）
    - [集合类型 (Collections) —— 数组与哈希表](./src/chapter-8/集合类型.md)
  - 第九章：前端的未来（WASM）
    - [完结：前端的未来 (WebAssembly)](./src/chapter-9/前端的未来.md)