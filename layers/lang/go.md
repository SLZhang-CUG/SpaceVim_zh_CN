#### Table of contents
(toc generated by [ghtoc](https://github.com/sk1418/ghtoc))
- [描述](#描述)
- [安装](#安装)
- [特性](#特性)
- [键绑定](#键绑定)


# 描述
这层是为了golang的开发。它还提供了其他语言特定的键映射

# 安装
在自定义文件内添加`call SpaceVim#layers#load('lang#go')｀

# 特性

 - 自动补全
 - 语法检查
 - 定义跳转
 - 参考查找

# 键绑定
**导入键绑定**

|键绑定|描述|
|-|-|
|`SPC l i`|go implements|
|`SPC l f`|go info|
|`SPC l e`|go rename|
|`SPC l r`|go run|
|`SPC l b`|go build|
|`SPC l t`|go test|
|`SPC l d`|go doc|
|`SPC l v`|go doc vertical|
|`SPC l c`|go coverage|

**代码格式化**

the default key bindings for format current buffer is SPC b f, and this key bindings is defined in format layer. you can also use g= to indent current buffer.

To make neoformat support go files, you should have go-fmt command available, or install goimports. go-fmt is delivered by golang’s default installation, so make sure you have correctly setup your go environment.



