# Trait (特质) —— 也就是“接口”

如果你熟悉 TypeScript 的 `interface`，那你理解 **Trait** 会非常快。

Trait 定义了一种 **“共同的行为”**。它告诉编译器：不管你是什么类型（Struct），只要你实现了这个 Trait，你就肯定能做这件事。

## 1.定义一个 Trait
假设我们要处理各种各样的内容：推文 (Tweet)、新闻文章 (NewsArticle)。它们内部的数据结构完全不同，但我们希望它们都能 **“被总结” (Summarize)**。

我们可以定义一个 Trait：
```rust
// 定义行为：任何实现了 Summary 的类型，都必须有一个 summarize 方法
trait Summary {
    fn summarize(&self) -> String;
}
```
这就像在 TS 里写 `interface Summary { summarize(): string; }。`

## 2.实现 Trait (Impl)
现在我们把这个特质“贴”到具体的 Struct 上。

```rust
struct Tweet {
    username: String,
    content: String,
}

// 为 Tweet 实现 Summary
impl Summary for Tweet {
    fn summarize(&self) -> String {
        format!("{}: {}", self.username, self.content)
    }
}

struct NewsArticle {
    headline: String,
    author: String,
    content: String,
}

// 为 NewsArticle 实现 Summary
impl Summary for NewsArticle {
    fn summarize(&self) -> String {
        format!("{} by {}...", self.headline, self.author)
    }
}
```
看，虽然 `Tweet` 和 `NewsArticle` 长得不一样，但它们都能调用 `.summarize()！`

## 🧠 随堂小测验
Trait 最强大的地方在于它可以作为 **函数的参数类型**。这实现了 **多态 (Polymorphism)**。

假设我想写一个函数 `notify`，它的作用是把任何能“总结”的东西打印出来。

在 TypeScript 里，你可能会写：
```TypeScript
function notify(item: Summary) { ... }
```
在 Rust 里，我们需要一种特殊的语法来表示 **“任何实现了 Summary 的东西”。**

**请观察下面两种写法，你觉得哪一种是合法的 Rust 语法？**

*A.*
```rust
fn notify(item: impl Summary) {
    println!("Breaking News! {}", item.summarize());
}
```
*B.*
```rust
fn notify(item: Summary) {
    println!("Breaking News! {}", item.summarize());
}
```
(提示：Rust 的编译器需要在编译时确定变量的大小，Trait 本身不是一个具体的类型，而是一个行为约束。)