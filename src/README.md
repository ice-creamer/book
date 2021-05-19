<--!
# Command line apps in Rust
-->
# Rust言語 によるコマンドラインアプリケーション開発
<--!
Rust is a statically compiled, fast language with great tooling and a rapidly growing ecosystem.
That makes it a great fit for writing command line applications:
They should be small, portable, and quick to run.
Command line applications are also a great way to get started with learning Rust;
or to introduce Rust to your team!
-->
Rust言語は静的にコンパイルされる、優れたツールと急成長を続けるエコシステムを備えた高速処理可能なプログラミング言語です。
そのため、Rust言語はコマンドラインアプリケーションを開発するのに最適です。
コマンドラインアプリケーションは、小さくてポータブル、かつ素早く実行できることが求められます。
コマンドラインアプリケーション開発は、Rust言語を学び始めるのにも、チームにRust言語を導入するのにも最適な方法です。
<--!
Writing a program with a simple command line interface (CLI)
is a great exercise for a beginner
who is new to the language and wants to get a feel for it.
There are many aspects to this topic, though,
that often only reveal themselves later on.
-->
単純なCLI（コマンドラインインターフェース）を使うプログラムを開発することは、プログラミング言語に慣れていない初心者がプログラミングに慣れるのに最適な練習方法です。
それでいながら、このテーマには様々な側面があり、後から初めて気づかされることも多くあります。
<--!
This book is structured like this:
We start with a quick tutorial,
after which you'll end up with a working CLI tool.
You'll be exposed to a few of the core concepts of Rust
as well as the main aspects of CLI applications.
What follows are chapters that go into more detail
on some of these aspects.
-->
この本の構成は次の通りです：
まずは簡単な練習問題から始まり、最終的に実用的なCLIツールを開発することができます。
Rust言語の中核となる概念やCLIアプリケーションの主な側面に触れることができます
その次の章では、それらの側面のいくつかを掘り下げて説明します。
<--!
One last thing before we dive right into CLI applications:
If you found an error in this book
or want to help us write more content for it,
you can find its source [in the CLI WG repository][book-src].
We'd love to hear your feedback!
Thank you!
-->
CLIアプリケーションの開発に取り掛かる前に、一言。
この本の内容に誤りを見つけた場合や、より多くの記事を書くことに協力したいと思われた方は、[in the CLI WG repository][book-src]をご覧ください。
それでは、皆さんのご意見、ご感想をお待ちしております。

[book-src]: https://github.com/rust-cli/book
