# Noto Sans as EMUI Default

## Introduction 简介

A Magisk module which can set Noto Sans as default fonts (including Chinese) systemlessly in Huawei EMUI, unless you change the display fonts via Theme app (com.huawei.android.thememanager).

Currently tested on EMUI 8, if you find any problems in other EMUI versions, please report to me.

这个 Magisk 模块可以设置 Noto Sans 为默认字体（包括中文字体），除非你通过“主题”应用（com.huawei.android.thememanager）更换了显示字体。

目前只在 EMUI 8 上测试过，如果你在其他 EMUI 版本上发现问题，请向我反馈。

## Usage 使用

1. Download the module from release page.
2. Magisk app > Modules > Install from storage > Select the downloaded module file.
3. When the installation is complete, reboot your device.

---

1. 从发行版页面下载模块。
2. Magisk 应用 > 模块 > 从本地安装 > 选择下载的模块文件。
3. 安装完成后，重启你的设备。

## Principal 原理

Taking EMUI 8 as an example, there are four files in `/system/fonts` that control the default font: `DroidSans.ttf`, `DroidSans-Bold.ttf`, `DroidSansChinese.ttf`, and `DroidSansMono.ttf`. Among them, `DroidSans.ttf` points to the Regular weight of the Roboto font, `DroidSans-Bold.ttf` points to the Bold weight of Roboto, `DroidSansChinese.ttf` actually contains "HanYiQiHei-50S", and `DroidSansMono.ttf` is suspected to be a custom font. In general, replacing `DroidSans.ttf`, `DroidSans-Bold.ttf`, and `DroidSansChinese.ttf` with Noto Sans and its Chinese fonts of appropriate weights will change the default font to Noto Sans.

In this module, the Chinese font used is Noto Sans SC, which follows the simplified Chinese glyph standards of mainland China.

以 EMUI 8 为例，在 `/system/fonts` 中控制默认字体的有四个文件，分别为：`DroidSans.ttf`、`DroidSans-Bold.ttf`、`DroidSansChinese.ttf` 和 `DroidSansMono.ttf`。其中，`DroidSans.ttf` 指向 Roboto 字体的 Regular 字重，`DroidSans-Bold.ttf` 指向 Roboto 的 Bold 字重，`DroidSansChinese.ttf` 实际为“汉仪旗黑-50S”，`DroidSansMono.ttf` 疑似为定制字体。在一般情况下，我们只需要替换 `DroidSans.ttf`、`DroidSans-Bold.ttf` 和 `DroidSansChinese.ttf` 为合适字重的 Noto Sans 及其中文字体，就可以把默认字体改成 Noto Sans。

在本模块中，使用的中文字体是 Noto Sans SC，它遵循中国大陆的简体中文字形标准。

## License 许可证

GNU General Public License v3.0 or any later version. GNU 通用公共许可证第三版或任何以后版本。
