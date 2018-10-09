# The green book
This repository contains the markdown files used to build the green book, a Dream Maker guide to help both newbies and veterans.

## Requirements
Building the book requires [rust] and cargo, which comes pre-packaged with rust. It also requires [mdBook], which can be installed through cargo:

[rust]: https://www.rust-lang.org/en-US/
[mdBook]: https://github.com/azerupi/mdBook

```bash
$ cargo install mdbook
```

## Building
To build the book, get a copy of this repository by downloading it in any way you want. Once done, open a command prompt and `cd` in the root of the repository folder, with the src folder and the book.toml, then type:

```bash
$ mdbook build
```
The output will be in the `book` subdirectory. To check it out, open the index.html file in your web browser.

## Contributing
The book can only succeed if knowledgeable people contribute! You can make new pages in the src folder, you can follow [this format] to see how to.

[this format]: https://rust-lang-nursery.github.io/mdBook/format/index.html