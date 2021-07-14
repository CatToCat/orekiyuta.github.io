---
title: Git Remote end hung up unexpectedly
date: 2021-07-13 19:43:07
tags: Git
---

## Scene
- 查看 github 发现今日没有自动提交
- 手动 push 一下，发现异常情况,应该也是网络问题
- ![](/images/gitRemoteEndHungUpUnexpectedly/Snipaste_2021-07-13_19-50-16.png)

## Solution
- 把远程连接 https 改用 ssh
- `git remote set-url origin git@github.com:OrekiYuta/Temp.git`
- ![](/images/gitRemoteEndHungUpUnexpectedly/Snipaste_2021-07-13_19-51-27.png)
<!-- more -->

- 还是不行的话,再执行`git config --global http.postBuffer 524288000`

## Other

- 👉 [Git, fatal: The remote end hung up unexpectedly](https://stackoverflow.com/questions/15240815/git-fatal-the-remote-end-hung-up-unexpectedly)
- 👉 [How do I get git to default to ssh and not https for new repositories](https://stackoverflow.com/questions/11200237/how-do-i-get-git-to-default-to-ssh-and-not-https-for-new-repositories)
- 👉 [Fix error : RPC failed; curl 92 HTTP/2 stream 0 was not closed cleanly: PROTOCOL_ERROR (err 1)](https://gist.github.com/daofresh/0a95772d582cafb202142ff7871da2fcs)
- 👉 [error: RPC failed; curl transfer closed with outstanding read data remaining](https://stackoverflow.com/questions/38618885/error-rpc-failed-curl-transfer-closed-with-outstanding-read-data-remaining)