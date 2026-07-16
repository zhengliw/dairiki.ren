---
title: 在《我的世界：Java版》中启用Fcitx5
date: 2026-07-16 18:16:00 +0200
categories: [经验分享, Linux桌面]
tags: [linux, minecraft, input-method, fcitx]
---

今天遇到了一个奇怪的问题：在[niri](https://github.com/niri-wm/niri)下运行《我的世界：Java版》，聊天框无法调用Fcitx5的中文拼音输入法，`Ctrl+Space`也不响应，幸好解决方法也比较简单。

以[Prism Launcher](https://prismlauncher.org/)为例，需在`设置→Minecraft→环境变量`添加以下环境变量：

| 环境变量 | 值 |
| -------- | --- |
| `XMODIFIERS` | `@im=fcitx` |
| `GLFW_IM_MODULE` | `fcitx` |

如图：

![Prism Launcher中配置环境变量的截图](assets/images/2026-07-16-env-vars.jpg)

对应的指令，供参考：

```sh
export XMODIFIERS="@im=fcitx"
export GLFW_IM_MODULE=fcitx
```
