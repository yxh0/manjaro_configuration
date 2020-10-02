# manjaro_configuration
This is a configuration sheet after installation of manjaro(PRC)

这是一份中国地区的manjaro配置单

## 换源
==逐条输入==
```
sudo pacman-mirrors -i -c China -m rank
sudo pacman -Syyu
```
这里会让你选择一个国内的源，华东地区选择上海交通大学，华北选择清华源，其余地区自行考量
##  添加arch源  
- 编辑pacman arch源

`sudo vi /etc/pacman.conf`
```
[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = https://mirrors.sjtug.sjtu.edu.cn/archlinux-cn/$arch
```
## 更新系统&密钥pkg签名
`sudo pacman -Syy && sudo pacman -S archlinuxcn-keyring`

## 现在可以全面更新系统了 
`sudo pacmam -Su`

