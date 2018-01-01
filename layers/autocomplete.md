[SpaceVim Layers](../layers.md):autocomplete

[TOC]

# 简介
提供SpaceVim中的自动补全功能。
支持一下补全插件：
[neocomplete](https://github.com/Shougo/neocomplete.vim)-支持lua的vim，即`+lua`

[neocomplcache](https://github.com/Shougo/neocomplcache.vim)-不支持lua的vim

[deoplete](https://github.com/Shougo/deoplete.nvim)-支持Python3的neovim，即`+python3`

[YouCompleteMe](https://github.com/Valloric/YouCompleteMe)-默认关闭状态，如想启用，见`:h g:spacevim_enable_ycm`

Snippets支持由[neosnippet](https://github.com/Shougo/neosnippet.vim)提供
# 安装
在你自己的配置文件中加入下面这行配置代码：
```vim
call SpaceVim#layers#load('autocomplete')
```
# 配置
## 键绑定
可以通过下面的layer变量完成自定义的补全
1. `auto-completion-return-key-behavior` 在按下`Return` / `Enter`时可设置要执行的操作，可用变量如下：
 * `complete` 补全当前所选
 * `smart` 补全当前所选并且给出snippets或者argvs
 * `nil`

2. `auto-completion-tab-key-behavior` 在按下`TAB`时可设置要执行的操作，可用变量如下：
 * `smart` 循环选择，片段展开，参数跳转
 * `complete` 补全当前所选
 * `cycle` 补全候选之间的共同前缀和循环
 * `nil` 插入一个回车

3. `auto-completion-complete-with-key-sequence`是一个由两个字符组成的字符串，表示一个按键序列，如果输入的序列足够快，则会执行一个补全行为。如果他的值是`nil`则禁用该功能。

4. `auto-completion-complete-with-key-sequence-delay`是等待自动完成键序列输入的秒数。默认值为0.1。

layer默认的配置如下：
```vim
call SpaceVim#layers#load('autocomplete', {
        \ 'auto-completion-return-key-behavior' : 'nil',
        \ 'auto-completion-tab-key-behavior' : 'smart',
        \ 'auto-completion-complete-with-key-sequence' : 'nil',
        \ 'auto-completion-complete-with-key-sequence-delay' : 0.1,
        \ })
```
`jk`是`auto-completion-complete-with-key-sequence`一个不错的选择，如果你还没有用它。

## Snippets文件
以下文件或者snippets默认添加：
* [Shougo/neosnippet-snippets](https://github.com/Shougo/neosnippet-snippets):neosnippet's默认的snippets,
* [honza/vim-snippets](https://github.com/honza/vim-snippets):snippets扩展,
* `~/.SpaceVim/snippets/`:Spacevim runtime snippets,
* `~/.SpaceVim.d/snippers/`:自定义全局snippets,
* `./.SpaceVim.d/snippets/`:自定义本地snippets(项目snippets)
可以通过设置`g:neosnippet$snippets_directory`添加额外的目录，在单个路径或路径列表的情况下可以采用一个字符串。

## 在自动补全弹窗中显示补全代码
默认情况下，补全代码是在自动补全弹窗中显示。如果想停用，可以将`auto-completion-enable-snippets-in-popup`设置为0。
```vim
call SpaceVim#layers#load('autocomplete', {
        \ 'auto-completion-enable-snippets-in-popup' : 0
        \ })
```

# LSP支持
# 键绑定
## 自动补全
|键绑定|描述|
|-|-|
|`<C-n>`|选择下一个|
|`<C-p>`|选择上一个|
|`<Tab>`|基于 `auto-completion-tab-key-behavior`|
|`<S-Tab>`|选择上一个|
|`<Return>`|基于 `auto-completion-return-kry-behavior`
## Neosnippet
|键绑定|描述|
|-|-|
|`M-/`|如果point之前的文本是一个片段的前缀，则将其展开|
|`SPC i s`|例出当前所有正在插入的yasnippets|


