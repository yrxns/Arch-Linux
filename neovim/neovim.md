### 前置准备

[nerd-fonts](https://github.com/ryanoasis/nerd-fonts#option-2-release-archive-download)

下载 hack 字体压缩包

    wget https://github.com/yanoasis/nerd-fonts/releases/download/v3.0.1/Hack.tar.xz

安装 hack 字体

    sudo apt install unar

    unar Hack.tar.xz

    tar -xf Hack.tar.xz

    cp -r Hack  ~/.local/share/fonts/

    cp -r Hack  /usr/local/share/fonts/

    fc-cache -f -v

    fc-list | grep "Hack"

    sudo setfont Hack

检查能否正常显示小图标

[cheat-sheet](https://www.nerdfonts.com/cheat-sheet)
