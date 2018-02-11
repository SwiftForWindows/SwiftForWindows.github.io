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
- `Newlibc module` is included. It is a Glibc-like module for the Cygwin C runtime library.
- Compiler Source: <b>[swift-4.0.3+cygwin.20180212](https://github.com/tinysun212/swift-windows/releases/tag/swift-4.0.3+cygwin.20180212)</b> from tinysun212
   (based on: [swift-4.0.3-RELEASE](https://github.com/apple/swift/releases/tag/swift-4.0.3-RELEASE) from apple/swift)

Example
-------
- To run compiler, download and extract the compressed file and append the path '$(pwd)/usr/bin' to the environment PATH.
  ```
  $ wget -q https://github.com/tinysun212/swift-windows/releases/download/swift-4.0.3%2Bcygwin.20180212/swift-4.0.3.cygwin.20180212-bin.tar.gz

  $ tar zxf swift-4.0.3.cygwin.20180212-bin.tar.gz

  $ export PATH=$PATH:$(pwd)/usr/bin

  $ swift --version
  Swift version 4.0.3 (swift-4.0.3+cygwin.20180212)
  Target: x86_64-unknown-windows-cygnus
  ```
- You can test the package manager with the example in https://swift.org/package-manager/.
  ```  
  $ git clone https://github.com/apple/example-package-dealer.git
  Cloning into 'example-package-dealer'...
  remote: Counting objects: 40, done.
  remote: Total 40 (delta 0), reused 0 (delta 0), pack-reused 40
  Unpacking objects: 100% (40/40), done.

  $ cd example-package-dealer

  $ swift run Dealer
  Fetching https://github.com/apple/example-package-deckofplayingcards.git
  Fetching https://github.com/apple/example-package-fisheryates.git
  Fetching https://github.com/apple/example-package-playingcard.git
  Cloning https://github.com/apple/example-package-deckofplayingcards.git
  Resolving https://github.com/apple/example-package-deckofplayingcards.git at 3.0.4
  Cloning https://github.com/apple/example-package-fisheryates.git
  Resolving https://github.com/apple/example-package-fisheryates.git at 2.0.4
  Cloning https://github.com/apple/example-package-playingcard.git
  Resolving https://github.com/apple/example-package-playingcard.git at 3.0.3
  Compile Swift Module 'PlayingCard' (3 sources)
  Compile Swift Module 'FisherYates' (2 sources)
  Compile Swift Module 'DeckOfPlayingCards' (1 sources)
  Compile Swift Module 'Dealer' (1 sources)
  Linking ./.build/x86_64-unknown-cygwin/debug/Dealer
  ♢5
  ♡J
  ♢7
  ♠︎K
  ♡6
  ♠︎4
  ♣︎10
  ♡9
  ♢8
  ♢K
  ```

Notice
-------
- Cygwin runtime is not included. You should install the Cygwin 64bit environment.
- No GUI support.
- NOT compatible with the MinGW-w64 port and the MSVC port.
- DOWNLOAD the binary from <b>[swift-4.0.3+cygwin.20180212](https://github.com/tinysun212/swift-windows/releases/tag/swift-4.0.3+cygwin.20180212)</b>
