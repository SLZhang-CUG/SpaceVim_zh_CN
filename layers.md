[TOC]

# 介绍
spacevim是一个社区驱动的vim配置，旨在提供layer功能。layer有助于收集相关的vim插件以提供功能。
这种方法有助于保持配置的组织性，并减少用户的开销，使他们不必考虑要安装哪些vim插件。
## 开启layer
下面是一个通过某些选项开启`shell` layer的实例
```vim
call SpaceVim#layers#load('shell',
        \ {
        \ 'default_position' : 'top',
        \ 'default_height' : 30,
        \ }
        \ )
```
## 关闭layer
一些layer默认为启用状态，下面是一个关闭`shell` layer的实例
```vim
call SpaceVim#layers#disable('shell')
```
# 可用layer
姓名|简介

