# 非官方 GCC 中文翻译增强

**警告**：本仓库提供的中文翻译内容未经官方审核和校验，因此不能保证其准确性. 

## 简介

当终端的 `$LANG` 环境变量设置为 `zh_CN.UTF-8` 时，GCC 编译器的提示信息会显示为中文，这些中文信息通常来源于 `/usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo` 文件. 

然而，即使是最新版的 GCC，其中文翻译的覆盖范围仍然有限. 为了解决这个问题，我们创建了本仓库，旨在通过更新上述翻译文件来增强 GCC 的中文翻译. 

## 如何使用

本仓库中的翻译文件适用于 GCC 的 13.2.0 版本，建议您先将 GCC 更新到最新版本. 

1. 克隆本仓库到本地：

```bash
$ git clone https://github.com/zzhx2006/gcc-zh_CN
$ cd gcc-zh_CN
```

2. 通常情况下，系统会默认自动安装 `gettext` 软件包. 使用 `msgfmt` 工具编译出 `.mo` 文件：

```bash
$ msgfmt gcc-zh_CN.po -o gcc.mo
```

3. 为了保险起见，建议先备份原有的 `.mo` 文件，然后将编译出的文件复制到指定目录. 

```bash
$ mv /usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo /usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo.bak
$ cp gcc.mo /usr/share/locale/zh_CN/LC_MESSAGES/
```

完成以上步骤后，GCC 编译器的提示信息将使用本仓库提供的翻译. 

## 如何贡献

1. 首先，Fork 本仓库. 
2. 使用翻译工具进行翻译. 
3. 创建一个新的分支，并将您的修改提交到该分支（以避免在主分支上直接进行修改）. 
4. 在新建的分支上，向本仓库的主分支提出 Pull Request. 

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
