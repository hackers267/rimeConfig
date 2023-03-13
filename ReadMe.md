# RimeConfig

本仓库是为了可以在linux的上使用Rime而做的配置记录。因为`Rime`是一个开源的高定制的输入法方案，其灵活性和可定制性特别适合于喜爱开源的极客们。

> `Rime`的安装以`ArchLinux`系统为例，其他linux平台的请到[官网]()查看。o

## 安装

```shell
paru -S fcitx5-im fcitxt-rime
```

安装完`Rime`后，需要对`~/.pam_environment`,`~/.xprofile`和`~/.xinitrc`文件进行配置。

```
# .pam_environment
GTK_IM_MODULE=fcitx5
QT_IM_MODULE=fcitx5
XMODIFIERS="@im=fcitx5"
```

```
#.xprofile
export GTK_IM_MODULE=fcitx5
export XMODIFIERS=@im=fcitx5
export QT_IM_MODULE=fcitx5
fcitx5 &
```

```
# .xinitrc
export GTK_IM_MODULE=fcitx5
export XMODIFIERS=@im=fcitx5
export QT_IM_MODULE=fcitx5
```
> 注意：上述内容需要添加在`exec($get_session)`之前

## 启用表型码

克隆本仓库到`~/.local/share/fcitx5/rime`目录中。重新部署`Rime`即可。
