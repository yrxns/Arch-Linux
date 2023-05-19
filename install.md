[Arch Linux官网](https://wiki.archlinuxcn.org/wiki/%E5%AE%89%E8%A3%85%E6%8C%87%E5%8D%97)

### 联网
---

```
ip link
```

```
iwctl

help

station list

station <wlan> scan

station <wlan> get-networks

station <waln> connect <name>

quit / exit

ping baidu.com
```

### 更新系统时间
---

    timedatectl set-ntp true

    timedatectl status



### 硬盘分区
---

    fdisk -l

    fdisk

| 挂载点    | 分区      | 分区类型     | 建议大小 |
|-----------|-----------|--------------|----------|
| /mnt/boot | /dev/sda1 | EFI系统分区  | > 300M   |
| [SWAP]    | /dev/sda2 | Linux swap   | > 512M   |
| /mnt      | /dev/sda3 | Linux x86-64 | 剩余空间 |

格式化分区

    mkfs.fat -F32 /dev/sda1

    mkfs.ext4 /dev/sda3

    mkswap /dev/sda2

    swapon /dev/sda2

挂载分区

    mount /dev/sda3 /mnt

    mount --mkdir /dev/sda1 /mnt/boot

换源

    vim /etc/pacman.conf                (打开 Color,可以在安装软件的时候打印一些提示)

    vim /etc/pacman.d/mirrorlist

> Server = https://repo.huaweicloud.com/archlinux/$repo/os/$arch
>
> Server = https://mirrors.tuna.tsinghua.edu.cn/archlinux/$repo/os/$arch

    pacman -Syyu

