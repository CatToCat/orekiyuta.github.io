---
title: Mklink in Win
date: 2021-10-24 02:23:11
tags: [Windows,LAN]
---

## Scene
- 当磁盘不够用,或者想转移当前目录文件存储的时候,又不能改变当前文件结构的情况
- Winodws 提供了文件路径映射功能。
<!-- more -->

## Solution
```
MKLINK [[/D] | [/H] | [/J]] Link Target

        /D      创建目录符号链接。默认为文件
                符号链接。
        /H      创建硬链接而非符号链接。
        /J      创建目录联接。
        Link    指定新的符号链接名称。
        Target  指定新链接引用的路径
                (相对或绝对)。
```
- 用法：`mklink /j "映射到这个目录" "想要映射过来的路径"` => `mklink /J "e:\test" "f:\test" `
- 需要注意的是, `mklink /j "目标路径" "源路径"`, 目标路径事先不能存在,因为会创建该路径造成冲突,无法创建
- 总之,常用的如下
    - `mklink /d "d:\target" "d:\origin"`
    - ```
        C:\Windows\system32>mklink /d "d:\target" "d:\origin"
        为 d:\target <<===>> d:\origin 创建的符号链接
      ```
    - `mklink /j "d:\target" "d:\origin"`  /j 只能创建本地磁盘映射, /d 可用于创建网络映射
    - ```
        C:\Windows\system32>mklink /j "d:\test" "\\192.168.1.10\AcerC\origin"
        完成该操作需要本地卷。

        C:\Windows\system32>mklink /d "d:\test" "\\192.168.1.10\AcerC\origin"
        为 d:\test <<===>> \\192.168.1.10\AcerC\origin 创建的符号链接
      ```
    
- 创建了映射之后,就可以在创建的映射目录里对目标路径进行操作了,就相当于操作目标路径的文件一样

- 此外, robocopy 没法移动文件到符号链接,对以上创建的映射无法生效
    - ```
        D:\>robocopy "d:\cc" "z:\test" /MIR /sl
        -------------------------------------------------------------------------------
        ROBOCOPY     ::     Windows 的可靠文件复制
        -------------------------------------------------------------------------------

        开始时间: 2021年10月24日 2:17:54
                源: d:\cc\
            目标: z:\test\

            文件: *.*

            选项: *.* /S /E /DCOPY:DA /COPY:DAT /PURGE /MIR /R:1000000 /W:30

        ------------------------------------------------------------------------------

        2021/10/24 02:17:54 错误 1463 (0x000005B7) 正在访问目标目录 z:\test\
        无法遵循符号链接，因为其类型已禁用。
        正在等待 30 秒... 正在重试...
      ```
## Other
- 👉 [windows 软链接的建立及删除](https://www.cnblogs.com/cnxkey/articles/7658462.html)
- 👉 [比较 Windows 上四种不同的文件（夹）链接方式](https://blog.walterlv.com/post/ntfs-link-comparisons.html)


