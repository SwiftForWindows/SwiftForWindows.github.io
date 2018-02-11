---
layout:     post
title:      Swift compiler for Cygwin (20180212)
author:     Han Sangjin
subtitle:  	Includes Swift 4.0.3 compiler
category:  release
---
<!-- Start Writing Below in Markdown -->

What is this?
-------------
- Swift compiler for Cygwin 64bit
- **`Foundation module` and `Package Manager` is included.**
  - You can test the package manager with the example.
  ```
  $ git clone https://github.com/apple/example-package-dealer.git
  $ cd example-package-dealer
  $ swift run Dealer
  ```
- `Newlibc module` is included. It is a Glibc-like module for the Cygwin C runtime library.
- Compiler Source: <b>[swift-4.0.3+cygwin.20180212](https://github.com/tinysun212/swift-windows/releases/tag/swift-4.0.3+cygwin.20180212)</b> from tinysun212
   (based on: [swift-4.0.3-RELEASE](https://github.com/apple/swift/releases/tag/swift-4.0.3-RELEASE) from apple/swift)

Notice
-------
- Cygwin runtime is not included. You should install the Cygwin 64bit environment.
- No GUI support.
- NOT compatible with the MinGW-w64 port and the MSVC port.
- DOWNLOAD the binary from <b>[swift-4.0.3+cygwin.20180212](https://github.com/tinysun212/swift-windows/releases/tag/swift-4.0.3+cygwin.20180212)</b>
