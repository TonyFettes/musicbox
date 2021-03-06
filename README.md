# NetEase-MusicBox

**感谢为 MusicBox 的开发付出过努力的[每一个人](https://github.com/darknessomi/musicbox/graphs/contributors)！**

高品质网易云音乐命令行版本，简洁优雅，丝般顺滑，基于Python编写。

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE)
[![versions](https://img.shields.io/pypi/v/NetEase-MusicBox.svg)](https://pypi.org/project/NetEase-MusicBox/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/NetEase-MusicBox.svg)](https://pypi.org/project/NetEase-MusicBox/)

## Demo

[![NetEase-MusicBox-GIF](https://qfile.aobeef.cn/3abba3b8a3994ee3d5cd.gif)](https://pypi.org/project/NetEase-MusicBox/)

## 正在做的

本 fork 主要修复一些现有的 Bug，添加一些小功能，添加许多新 Bug。

本人不会 `Python`，所以目前并不打算进行大改和重构。
本人使用 Arch Linux 系统，所以可能不会修一些系统相关的 Bug，如果你遇到了问题，欢迎提 PR。

- [ ] 优化按键逻辑，降低时延，提高容错性
- [ ] 将一些分支判断命题抽象成函数减少 `menu.py` 中代码行数
- [x] 尝试修复 [darknessomi #816](https://github.com/darknessomi/musicbox/issues/816)
      [darknessomi #829](https://github.com/darknessomi/musicbox/issues/829)
- [x] 尝试实现功能 [darknessomi #828](https://github.com/darknessomi/musicbox/issues/828)
- [x] 修复评论按 `L` 后出现的按键逻辑混乱
- [x] 每页行数根据终端窗口大小变化，config 中提供 `auto` 选项
- [x] 修复长按 `j` 或 `k` 时歌词颜色闪烁的 Bug
- [x] 添加功能（合并 PR [darknessomi PR #653](https://github.com/darknessomi/musicbox/pull/653)）

## 可能打算做的

按照可能的实现难度粗略的排序

1. 消减 Unicode glyph 字符数量
1. Nofitication 添加 Action
1. 鼠标左右键的支持
1. 歌曲评论的回复
1. 修复模糊搜索的一堆 Bug
1. 更多配置选项，例如每次显示歌词行数
1. 版权问题的歌曲灰色显示、不自动跳过并显示 notification
1. 歌曲快进快退 [darknessomi #849](https://github.com/darknessomi/musicbox/issues/849)
1. 运行时更改配置
1. 歌曲信息终端内显示，使用 `libcaca/w3m` 显示专辑封面

## 不打算做的

| 不打算做的 | 原因 |
|-|-|
| 尝试修复 [darknessomi #857](https://github.com/darknessomi/musicbox/issues/857) | 当前版本无法复现 |
| 后台运行 | [FeelUOwn](https://github.com/feeluown/FeelUOwn) 可以后台运行，但是目前命令行控制功能不太完善 |
| 用 Rofi 和 dmenu 控制 | 以 [FeelUOwn](https://github.com/feeluown/FeelUOwn) 插件或者 [Mopidy](https://github.com/mopidy/mopidy) 插件实现可能会更好 |
| 最小化显示模式 ( i3bar 等的适配 ) | 同上 |
| 容器和可定制界面 | 感觉没必要，也写不出来 |
| 类 VIM 的增量搜索功能和命令 | 要不直接做成 VIM 插件吧 |
| 类似 lsp 的中间层，适配多后端和多前端 | 目前已经有 [FeelUOwn](https://github.com/feeluown/FeelUOwn) 和 [Mopidy](https://github.com/mopidy/mopidy) 这两个项目了 |

## 功能特性

1. 320kbps的高品质音乐
2. 歌曲，艺术家，专辑检索
3. 网易22个歌曲排行榜
4. 网易新碟推荐
5. 网易精选歌单
6. 网易主播电台
7. 私人歌单，每日推荐
8. 随心打碟
9. 本地收藏，随时加❤
10. 播放进度及播放模式显示
11. 现在播放及桌面歌词显示
12. 歌曲评论显示
13. 一键进入歌曲专辑
14. 定时退出
15. Vimer式快捷键让操作丝般顺滑
16. 可使用数字快捷键
17. 可使用自定义全局快捷键
18. 对当前歌单列表进行本地模糊搜索

### 键盘快捷键

有 num + 字样的快捷键可以用数字修饰，按键顺序为先输入数字再键入被修饰的键，即 num + 后的快捷键。

| Key       | Effect          |                    |
| --------- | --------------- | ------------------ |
| <kbd>j</kbd>         | Down            | 下移               |
| <kbd>k</kbd>         | Up              | 上移               |
| num + <kbd>j</kbd>   | Quick Jump      | 快速向后跳转n首    |
| num + <kbd>k</kbd>   | Quick Up        | 快速向前跳转n首    |
| <kbd>h</kbd>         | Back            | 后退               |
| <kbd>l</kbd>         | Forword         | 前进               |
| <kbd>u</kbd>         | Prev Page       | 上一页             |
| <kbd>d</kbd>         | Next Page       | 下一页             |
| <kbd>f</kbd>         | Search          | 当前列表模糊搜索   |
| <kbd>\[</kbd>        | Prev Song       | 上一曲             |
| <kbd>]</kbd>         | Next Song       | 下一曲             |
| num + <kbd>\[</kbd>  | Quick Prev Song | 快速前n首          |
| num + <kbd>]</kbd>   | Quick Next Song | 快速后n首          |
| num + <kbd>Shift</kbd> + <kbd>g</kbd>   | Index for Song  | 跳到第n首          |
| <kbd>=</kbd>         | Volume +        | 音量增加           |
| <kbd>-</kbd>         | Volume -        | 音量减少           |
| <kbd>Space</kbd>     | Play/Pause      | 播放/暂停          |
| <kbd>?</kbd>         | Shuffle         | 手气不错           |
| <kbd>m</kbd>         | Menu            | 主菜单             |
| <kbd>p</kbd>         | Present/History | 当前/历史播放列表  |
| <kbd>i</kbd>         | Music Info      | 当前音乐信息       |
| <kbd>Shift</kbd> + <kbd>p</kbd> | Playing Mode    | 播放模式切换       |
| <kbd>a</kbd>         | Add             | 添加曲目到打碟     |
| <kbd>Shift</kbd> + <kbd>a</kbd> | Enter Album     | 进入专辑           |
| <kbd>g</kbd>         | To the First    | 跳至首项           |
| <kbd>Shift</kbd> + <kbd>g</kbd> | To the End      | 跳至尾项           |
| <kbd>z</kbd>         | DJ List         | 打碟列表           |
| <kbd>s</kbd>         | Star            | 添加到收藏         |
| <kbd>c</kbd>         | Collection      | 收藏列表           |
| <kbd>r</kbd>         | Remove          | 删除当前条目       |
| <kbd>Shift</kbd> + <kbd>j</kbd> | Move Down       | 向下移动当前项目   |
| <kbd>Shift</kbd> + <kbd>k</kbd> | Move Up         | 向上移动当前项目   |
| <kbd>Shift</kbd> + <kbd>c</kbd> | Cache           | 缓存歌曲到本地     |
| <kbd>,</kbd>         | Like            | 喜爱               |
| <kbd>.</kbd>         | Trash FM        | 删除 FM            |
| <kbd>/</kbd>         | Next FM         | 下一FM             |
| <kbd>q</kbd>         | Quit            | 退出               |
| <kbd>t</kbd>         | Timing Exit     | 定时退出           |
| <kbd>w</kbd>         | Quit & Clear    | 退出并清除用户信息 |

## 安装

### 必选依赖

1. `mpg123` 用于播放歌曲，安装方法参见下面的说明
2. `python-fuzzywuzzy` 用于模糊搜索

### 可选依赖

1. `aria2` 用于缓存歌曲
2. `libnotify-bin` 用于支持消息提示（Linux平台）
3. `pyqt python-dbus dbus qt` 用于支持桌面歌词
   (Mac 用户需要 `brew install qt --with-dbus` 获取支持 DBus 的 Qt)
4. `python-levenshtein` 用于模糊搜索

### PyPi安装（*nix系统）

```bash
    pip3 install NetEase-MusicBox
```

### Git clone安装master分支（*nix系统）

```bash
    git clone https://github.com/darknessomi/musicbox.git && cd musicbox
    poetry build && poetry install
```

### macOS安装

```bash
    pip3 install NetEase-MusicBox
    brew install mpg123
```

### Linux安装

**注意：通过以下方法安装可能仍然需要`pip3 install -U NetEase-MusicBox`更新到最新版**。

#### Fedora

首先添加[FZUG](https://github.com/FZUG/repo/wiki)源，然后`sudo dnf install musicbox`。

#### Ubuntu/Debian

```bash
    pip3 install NetEase-MusicBox

    sudo apt-get install mpg123
```

#### Arch Linux

```bash
    pacaur -S netease-musicbox-git # or $ yaourt musicbox
```

#### Centos/Red Hat

```bash
    pip3 install NetEase-MusicBox
    wget http://mirror.centos.org/centos/7/os/x86_64/Packages/mpg123-1.25.6-1.el7.x86_64.rpm
    sudo yum install -y mpg123-1.25.6-1.el7.x86_64.rpm
```

## 配置和错误处理

配置文件地址: `~/.config/netease-musicbox/config.json`
可配置缓存，快捷键，消息，桌面歌词。
由于歌曲 API 只接受中国大陆地区访问，非中国大陆地区用户请自行设置代理（可用polipo将socks5代理转换成http代理）：

```bash
export http_proxy=http://IP:PORT
export https_proxy=http://IP:PORT
curl -L ip.cn
```

显示IP属于中国大陆地区即可。

### 已测试的系统兼容列表

| OS       | Version               |
| -------- | --------------------- |
| Arch     | Rolling               |

### 错误处理

当某些歌曲不能播放时，总时长为 00:01 时，请检查是否为版权问题导致。

如遇到在特定终端下不能播放问题，首先检查**此终端**下mpg123能否正常使用，其次检查**其他终端**下musicbox能否正常使用，报告issue的时候请告知以上使用情况以及出问题终端的报错信息。

同时，您可以通过`tail -f ~/.local/share/netease-musicbox/musicbox.log`自行查看日志。
mpg123 最新的版本可能会报找不到声音硬件的错误，测试了1.25.6版本可以正常使用。

### 已知问题及解决方案

- [#374](https://github.com/darknessomi/musicbox/issues/374) i3wm下播放杂音或快进问题，此问题常见于Arch Linux。尝试更改mpg123配置。
- [#405](https://github.com/darknessomi/musicbox/issues/405) 32位Python下cookie时间戳超出了32位整数最大值。尝试使用64位版本的Python或者拷贝cookie文件到对应位置。
- [#347](https://github.com/darknessomi/musicbox/issues/347) 暂停时间超过一定长度（数分钟）之后mpg123停止输出，导致切换到下一首歌。此问题是mpg123的bug，暂时无解决方案。
- [#791](https://github.com/darknessomi/musicbox/issues/791) 版权问题，master分支已经修复

## 使用

```bash
    musicbox
```

Enjoy it !

## 更新日志

2018-11-28 版本 0.2.5.4    修复多处错误

2018-06-21 版本 0.2.5.3    修复多处播放错误

2018-06-07 版本 0.2.5.1    修复配置文件错误

2018-06-05 版本 0.2.5.0    全部迁移到新版api，大量错误修复

[更多>>](https://github.com/darknessomi/musicbox/blob/master/CHANGELOG.md)

## LICENSE

[MIT](LICENSE)
