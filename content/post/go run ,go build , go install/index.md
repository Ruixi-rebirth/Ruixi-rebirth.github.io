---
title: "Go Run ,Go Build , Go Install"
date: 2021-11-26T07:47:36+08:00
tags:
  - Go
categories:
  - Devops
image: go.jpg
draft: false
---

在实际操作之前，我们需要知道 go 有三种源码文件：

1，命令源码文件；声明自己属于 main 包，并且包含 main 函数的文件，每个项目只能有一个这样的文件，即程序的入口文件

2，库源码文件；不能直接被执行的源码文件

3，测试源码文件

go run : 编译并直接运行程序，不产生可执行文件，只产生临时文件，方便用户调试（即在 bin 目录和 pkg 目录不产生任何文件）,其后只能+命令源码文件。

go build : 既可以+库源码文件，又可以+命令源码文件,主要功能是检查是否有编译错误

+库源码文件：只是检查编译错误，不产生任何文件,如果库源码文件有语法错误，编译不通过会报错。

+命令源码文件：产生一个可执行文件

go install : 执行的过程：编译库源码文件->编译命令源码文件->移动编译文件，命令源码文件的编译后的二进制文件移到$GOPATH/bin目录下；库源码文件的编译移到$GOPATH/pkg 目录,后缀名为.a 的文件。这个移动目录的过程称为安装。

Ps：上述的二进制可执行文件可独立运行，当然可以放在任何目录下运行啦
