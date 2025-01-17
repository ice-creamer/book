<--!
# Learning Rust by Writing a Command Line App in 15 Minutes
-->
# １５分で学ぶ、Rust言語によるコマンドラインアプリケーション開発

<--!
This tutorial will guide you through writing
a CLI (command line interface) application
in [Rust].
It will take you roughly fifteen minutes
to get to a point where you have a running program
(around chapter 1.3).
After that, we'll continue to tweak our program
until we reach a point where we can ship our little tool.

[Rust]: https://rust-lang.org/
-->
このチュートリアルでは、CLI（コマンドラインインターフェース）をRust言語で書いてみましょう。
プログラムを走らせるまでに、およそ15分かかります（1.3章あたり）
その後は、このプログラムを小規模な製品としてリリースできるまで、調整を重ねていきます。

<--!
You’ll learn all the essentials about how to get going,
and where to find more information.
Feel free to skip parts you don't need to know right now
or jump in at any point.
-->
<aside>

**Prerequisites:**
This tutorial does not replace a general introduction to programming,
and expects you to be familiar with a few common concepts.
You should be comfortable with using a command line/terminal.
If you already know a few other languages,
this can be a good first contact with Rust.

**Getting help:**
If you at any point feel overwhelmed or confused with the features used,
have a look at the extensive official documentation that comes with Rust,
first and foremost the book,
The Rust Programming Language.
It comes with most Rust installations
(`rustup doc`),
and is available online on [doc.rust-lang.org].

[doc.rust-lang.org]: https://doc.rust-lang.org

You are also very welcome to ask questions –
the Rust community is known to be friendly and helpful.
Have a look at the [community page]
to see a list of places where people discuss Rust.

[community page]: https://www.rust-lang.org/community

</aside>

What kind of project do you want to write?
How about we start with something simple:
Let’s write a small `grep` clone.
That is a tool that we can give a string and a path
and it’ll print only the lines that contain the given string.
Let’s call it `grrs` (pronounced “grass”).

In the end,
we want to be able to run our tool like this:

```console
$ cat test.txt
foo: 10
bar: 20
baz: 30
$ grrs foo test.txt
foo: 10
$ grrs --help
[some help text explaining the available options]
```

<aside class="note">

**Note:**
This book is written for [Rust 2018].
The code examples can also be used on Rust 2015,
but you might need to tweak them a bit;
add `extern crate foo;` invocations, for example.

Make sure you run Rust 1.31.0 (or later)
and that you have `edition = "2018"` set
in the `[package]` section of your `Cargo.toml` file.

[Rust 2018]: https://doc.rust-lang.org/edition-guide/index.html

</aside>
