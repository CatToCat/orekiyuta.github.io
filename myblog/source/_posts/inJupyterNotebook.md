---
title: In Jupyter Notebook
date: 2020-12-30 22:29:11
tags: Jupyter
---

## Configure

- `pip install notebook`
- `jupyter notebook` 启动,工作空间是当前目录
- `jupyter notebook --generate-config` 创建配置文件，指定工作空间的目录
- `c.NotebookApp.notebook_dir = r'F:\Code'`打开配置文件找到这个配置并修改
<!-- more -->
## QuickStart
- 进入编辑器后，可以进行文本操作
- 点击右侧的 New ,新建文件
![](/images/inJupyterNotebook/Snipaste_2020-12-30_22-49-43.png)
- 绿色为编辑模式，蓝色为命令模式（按 ESC 切换）
- ![](/images/inJupyterNotebook/Snipaste_2020-12-30_22-53-12.png)
- ![](/images/inJupyterNotebook/Snipaste_2020-12-30_22-52-56.png)      
- 单元格类型有两种，默认是代码类型
    - 在命令模式按 Y 切换为代码类型
    - 按 M 切换为 Markdown 文本类型
![](/images/inJupyterNotebook/Snipaste_2020-12-30_22-55-20.png)

- 在单元格类输入内容后，ctrl + enter 执行
    - 代码单元格为执行代码，Markdown 单元格为输出文本样式
![](/images/inJupyterNotebook/Snipaste_2020-12-30_22-56-59.png)

- 常用快捷键
    - ctrl + enter 执行并光标停留在当前单元格
    - shift + enter 执行并在下面创建新单元格，进入命令模式
    - alt + enter 执行并在下面创建新单元格，进入编辑模式
    - 单元格类型切换 Y / M
    - 在命令模式下，A 在上一行插入单元格
    - 在命令模式下，B 在下一行插入单元格
    - 在命令模式下，DD 删除当前单元格

- 使用测试
![](/images/inJupyterNotebook/Snipaste_2020-12-30_23-27-24.png)
- 这里需要注意的是,每个单元格是单独执行的,分单元格写代码的话,要从上到到下按顺序执行各个单元格

## Reference
- 👉 [jupyter](https://jupyter.org/)