#### Table of contents
(toc generated by [ghtoc](https://github.com/sk1418/ghtoc))
- [描述](#描述)
- [特性](#特性)
- [安装](#安装)
    - [cscope](#cscope)
    - [layer](#layer)
    - [键绑定](#键绑定)

# 描述

提供一个灵活的[Cscope](http://cscope.sourceforge.net/)和[PyCscope](https://github.com/portante/pycscope)帮助。

如果想获得更多关于Cscope和其他类似工具异同点的信息，请阅读[Compatison with Similar Tools](https://github.com/oracle/opengrok/wiki/Comparison-with-Similar-Tools)。

# 特性

* 通过Cscope实现C/C++的tag索引和搜索
* 通过PyCscope实现python的tag索引和搜索

# 安装

## cscope

Arch
```shell
sudo pacman -S cscpope
```
ubuntu
```shell
sudo apt install cscope
```

## layer

在~/.SpaceVim.d/init.vim中加入下面的配置：
```vim
call SpaceVim#layers#load('cscope')
```

## 键绑定
|键绑定|描述|
|-|-|
|`SPC m c =`|Find assignments to this symbol(不会翻译)|
|`SPC m c i`|创建cscope索引|
|`SPC m c c`|查找这个函数调用的函数|
|`SPC m c C`|查找调用这个函数的函数|
|`SPC m c d`|查找这个标记的全局定义|
|`SPC m c r`|查找这个标记的引用|
|`SPC m c f`|查找文件|
|`SPC m c F`|找到哪些文件包含文件|
|`SPC m c e`|搜索正则表达式|
|`SPC m c t`|搜索文本|


