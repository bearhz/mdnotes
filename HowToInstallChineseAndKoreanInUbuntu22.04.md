# mdnotes

## How to install Chinese and Korean in ubuntu22.04
### 1 安装fcitx
1.1 登录sogou网站，下载deb安装文件
1.2 安装fcitx和依赖项
```
sudo apt update
sudo apt install -y fcitx-bin fcitx-table
```
### 2 安装搜狗拼音安装包和依赖项
2.1 进官网下载deb文件
2.2 安装deb文件
```
sudo dpkg -i sogoupinyin_*.deb
sudo apt --fix-broken install
```
2.3 安装依赖项
```
sudo apt install libqt5qml5 libqt5quick5 libqt5quickwidgets5 qml-module-qtquick2
sudo apt install libgsettings-qt1
```
### 3 安装hangul
```
sudo apt install -y fcitx-hangul
```
重启电脑
### 4 安装系统语言
进入settings/Region&Language。点Manage Installed Languages。点Install/Remove Languages...。添加简体和繁体中文，添加韩文。
重启电脑
### 5 Configure Fcitx添加sogou和hangul
5.1 Set up Fcitx as the default input method framework
```
im-config -n fcitx
```
5.2 进入fcitx config，添加sogou和hangul
```
fcitx-config-gtk3
```
添加sogou和hangul
### 6 重启fcitx或重启电脑
```
fcitx-autostart
```
### 7 设置切换快捷键
进入fcitx配置，进入Global Config选项，修改Trigger Input Method。
我是韩国键盘，选择了hangul按键。（其他国家键盘没有该按键）

