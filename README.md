# 贡献 GCC 中文翻译

当终端的 `$LANG` 环境变量设置为 `zh_CN.UTF-8` 时，gcc 编译器的提示信息会显示为中文，这些中文信息通常来源于 `/usr/share/locale/zh_CN/LC_MESSAGES/gcc.mo` 文件. 

## 如何贡献

1. 浏览[官网](https://translationproject.org/)了解 Translation Project，STFW 了解 GNU `gettext` 工具的基本使用；
2. 尝试在本地编辑和翻译 `.po` 文件中的几个词条，并预览翻译效果；
3. 浏览[官网](https://translationproject.org/html/translators.html)了解如何成为一名 Translator；
4. 按照[官网](https://translationproject.org/html/whydisclaim.html)要求提交一份 disclaimer（免责声明）；
5. 向 [TP coordinator](mailto:coordinator@translationproject.org) 和简体中文翻译团队领导者 [Boyuan Yang](mailto:073plan@gmail.com) 发送邮件请求加入简体中文翻译团队；
6. 按照[官网](https://translationproject.org/html/robot.html)要求使用 TP-Robot 提交自己的翻译文件；

## `tools/` 文件夹说明

- `podiff.py`: 从 [amandasaurus/podiff](https://github.com/amandasaurus/podiff) 仓库的修改而来，原作者为 Rory McCann 和 Ian McEwen；用来比较两个 `.po` 文件之间的差异；原仓库的旧文件使用 Python2 编写，本仓库将其更新到 Python3 后继续使用；
- `sendpo.sh`: 从[官网的 `sendpo.sh` 文件](https://translationproject.org/extra/sendpo.sh)修改而来；用来处理翻译好的 `.po` 文件以准备发送给 TP-Robot；官网的文件使用了 `mail` 命令从命令行直接发送邮件，本仓库删除了使用 `mail` 命令的部分，仅保留压缩和编码操作，便于使用现代邮件客户端发送邮件；
- `update.sh`: 用来更新本地的翻译；

## 参考资源

- [游戏本地化深度指南：如何高效翻译与处理多语言PO文件 - 知乎](https://zhuanlan.zhihu.com/p/662483399)
- [如何使用 poedit 翻译？ - 知乎](https://www.zhihu.com/question/27039330)
- [gettext 翻译介绍和简单使用 – 深度科技社区](https://www.deepin.org/zh/gettext/)
- [语言文件.po .pot和.mo简介及汉化 - 51CTO博客](https://blog.51cto.com/xxstar/1940854)
