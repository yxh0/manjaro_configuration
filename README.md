# manjaro_configuration
This is a configuration sheet after installation of manjaro(PRC)

这是一份中国地区的manjaro配置单

## 换源
sudo pacman-mirrors -i -c China -m rank
sudo pacman -Syyu

##  添加arch源  
- 编辑pacman arch源

sudo vi /etc/pacman.conf

[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = https://mirrors.sjtug.sjtu.edu.cn/archlinux-cn/$arch

## 更新系统&密钥pkg签名
sudo pacman -Syy && sudo pacman -S archlinuxcn-keyring

## 更新系统 
sudo pacmam -Su

