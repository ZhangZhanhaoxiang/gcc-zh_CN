# 非官方 GCC 中文翻译增强

**警告**：本仓库的中文翻译内容未经官方审核和校验，不能确保其准确性. 

## 简介

当终端的 `$LANG` 设置为 `zh_CN.UTF-8` 时，gcc 的提示信息会变成中文，它通常来自于 `/usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo` 文件. 

但即使是最新版的 gcc，其中文翻译覆盖范围依然较少. 故创建本仓库，旨在通过更新上述翻译文件来增强 gcc 的中文翻译. 

## 如何使用

本仓库中的翻译文件适配 gcc 的版本为 13.2.0，建议先将 gcc 更新到最新版本. 

克隆仓库到本地：

```bash
$ git clone https://github.com/zzhx2006/gcc-zh_CN
$ cd gcc-zh_CN
```

一般系统会默认自动安装 `gettext` 软件包. 使用 `msgfmt` 工具编译出 `.mo` 文件：

```bash
$ msgfmt gcc-zh_CN.po -o gcc.mo
```

建议先备份原有的 `.mo` 文件，然后将编译出的文件复制到指定目录. 

```bash
$ mv /usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo /usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo.bak
$ cp gcc.mo /usr/share/locale/zh_CN/LC_MESSAGES/
```
此时的 gcc 提示信息即为本仓库的翻译. 

## 如何贡献

1. Fork 本仓库. 
2. 通过翻译工具进行翻译. 
3. 新建一个分支，然后将改动提交到该分支（避免在 main 分支上做改动）. 
4. 在新建的分支上提出 Pull Request. 

## 关于 GNU Translation Project

GNU 翻译项目官网提供了丰富的资源和信息，包括：

- 项目概述：介绍了翻译项目的目标和运作方式. 
- 包和团队列表：列出参与项目的软件包和负责不同语言翻译的团队，每个团队页面都提供了联系信息和相关链接. 
- 对维护者、翻译者和协调者的指导：详细解释了如何参与翻译项目，包括对翻译者的免责声明要求和与处理 PO 文件提交的机器人交互的指南. 
- 翻译工具：介绍了一些翻译工具，如 Lokalize 和 poEdit，以及如何获取和安装这些工具. 
- 报告错误：指导如何报告在处理的项目中发现的翻译错误. 
- 讨论：提供了关于翻译和翻译相关软件的技术讨论列表的信息. 

更多详细信息，请访问 [GNU 翻译项目官网](https://translationproject.org/html/welcome.html). 

## 更多资源

- [游戏本地化深度指南：如何高效翻译与处理多语言PO文件 - 知乎](https://zhuanlan.zhihu.com/p/662483399)
- [如何使用 poedit 翻译？ - 知乎](https://www.zhihu.com/question/27039330)
- [gettext 翻译介绍和简单使用 – 深度科技社区](https://www.deepin.org/zh/gettext/)
- [语言文件.po .pot和.mo简介及汉化 - 51CTO博客](https://blog.51cto.com/xxstar/1940854)

