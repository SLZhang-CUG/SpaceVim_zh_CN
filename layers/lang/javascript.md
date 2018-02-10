

# 描述
提供JavaScript开发

# 安装
在自定义配置文件内加入`call SpaceVim#layers#load('lang#javascript')`

# 特性

 - 自动补全
 - 语法检查
 - 定义跳转
 - 参考查找

# layer配置
`auto_fix`:保存文件时自动修复问题，默认情况下禁用。
如果您需要此功能，则可以通过以下方式加载此模块

```vim
call SpaceVim#layers#load('lang#javascript',
            \ {
            \ 'auto_fix' : 1,
            \ }
            \ )

```

# 键绑定
## import键绑定

|键绑定|描述|
|-|-|
|`F4`(Insert/Normal)|Import symbol under cursor|
|`SPC j i`	|Import symbol under cursor|
|`SPC j f	`|Import missing symbols|
|`SPC j g	`|Jump to module under cursor|
|`<C-j>i `(Insert)	|Import symbol under cursor|
|`<C-j>f `(Insert)	|Import missing symbols|
|`<C-j>g `(Insert)	|Jump to module under cursor|

# generate键绑定

|模式|键绑定|描述|
|-|-|-|
|normal|`SPC l g d`|生成JSDoc|

