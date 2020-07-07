* [Windows平台下](#windows%E5%B9%B3%E5%8F%B0%E4%B8%8B)
  * [1\. Vim的安装](#1-vim%E7%9A%84%E5%AE%89%E8%A3%85)
    * [1\.1 在windows平台下安装vim](#11-%E5%9C%A8windows%E5%B9%B3%E5%8F%B0%E4%B8%8B%E5%AE%89%E8%A3%85vim)
  * [2\. Vim的四种模式](#2-vim%E7%9A%84%E5%9B%9B%E7%A7%8D%E6%A8%A1%E5%BC%8F)
  * [3\. Vimrc文件的配置](#3-vimrc%E6%96%87%E4%BB%B6%E7%9A%84%E9%85%8D%E7%BD%AE)
    * [3\.1 设置文件编码](#31-%E8%AE%BE%E7%BD%AE%E6%96%87%E4%BB%B6%E7%BC%96%E7%A0%81)
    * [3\.2 显示行号](#32-%E6%98%BE%E7%A4%BA%E8%A1%8C%E5%8F%B7)
    * [3\.3 突出显示当前行](#33-%E7%AA%81%E5%87%BA%E6%98%BE%E7%A4%BA%E5%BD%93%E5%89%8D%E8%A1%8C)
    * [3\.4 突出显示当前列](#34-%E7%AA%81%E5%87%BA%E6%98%BE%E7%A4%BA%E5%BD%93%E5%89%8D%E5%88%97)
    * [3\.5 设置突出显示行|列的颜色](#35-%E8%AE%BE%E7%BD%AE%E7%AA%81%E5%87%BA%E6%98%BE%E7%A4%BA%E8%A1%8C%E5%88%97%E7%9A%
      84%E9%A2%9C%E8%89%B2)
    * [3\.6 在Vim中启用鼠标](#36-%E5%9C%A8vim%E4%B8%AD%E5%90%AF%E7%94%A8%E9%BC%A0%E6%A0%87)
    * [3\.7 "显示括号匹配"](#37-%E6%98%BE%E7%A4%BA%E6%8B%AC%E5%8F%B7%E5%8C%B9%E9%85%8D)
    * [3\.8 括号自动匹配](#38-%E6%8B%AC%E5%8F%B7%E8%87%AA%E5%8A%A8%E5%8C%B9%E9%85%8D)
    * [3\.9 设置缩进](#39-%E8%AE%BE%E7%BD%AE%E7%BC%A9%E8%BF%9B)
    * [3\.10 设置粘贴模式](#310-%E8%AE%BE%E7%BD%AE%E7%B2%98%E8%B4%B4%E6%A8%A1%E5%BC%8F)
    * [3\.11 设置非可见字符(tab|空格)可见](#311-%E8%AE%BE%E7%BD%AE%E9%9D%9E%E5%8F%AF%E8%A7%81%E5%AD%97%E7%AC%A6tab%E7%A9
      %BA%E6%A0%BC%E5%8F%AF%E8%A7%81)
    * [3\.12 状态行的设置](#312-%E7%8A%B6%E6%80%81%E8%A1%8C%E7%9A%84%E8%AE%BE%E7%BD%AE)
    * [3\.13 显示光标当前位置](#313-%E6%98%BE%E7%A4%BA%E5%85%89%E6%A0%87%E5%BD%93%E5%89%8D%E4%BD%8D%E7%BD%AE)
    * [3\.14 打开文件类型检测](#314-%E6%89%93%E5%BC%80%E6%96%87%E4%BB%B6%E7%B1%BB%E5%9E%8B%E6%A3%80%E6%B5%8B)
    * [3\.15 ★重要·打开语法高亮显示★](#315-%E9%87%8D%E8%A6%81%E6%89%93%E5%BC%80%E8%AF%AD%E6%B3%95%E9%AB%98%E4%BA%AE%E
      6%98%BE%E7%A4%BA)
    * [3\.16 代码折叠](#316-%E4%BB%A3%E7%A0%81%E6%8A%98%E5%8F%A0)
  * [3\. 在Vim中安装并使用插件](#3-%E5%9C%A8vim%E4%B8%AD%E5%AE%89%E8%A3%85%E5%B9%B6%E4%BD%BF%E7%94%A8%E6%8F%92%E4%BB%B6)
* [3\.1 ★★★插件管理工具——Vundle★★★](#31-%E6%8F%92%E4%BB%B6%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7vundle)
      * [3\.1\.1 安装Vundle](#311-%E5%AE%89%E8%A3%85vundle)
      * [3\.1\.2 配置Vundle](#312-%E9%85%8D%E7%BD%AEvundle)
      * [3\.1\.3 安装插件](#313-%E5%AE%89%E8%A3%85%E6%8F%92%E4%BB%B6)
      * [3\.1\.4 卸载插件](#314-%E5%8D%B8%E8%BD%BD%E6%8F%92%E4%BB%B6)
      * [3\.1\.5 更新插件](#315-%E6%9B%B4%E6%96%B0%E6%8F%92%E4%BB%B6)
      * [3\.1\.6 其它关于配置的说明](#316-%E5%85%B6%E5%AE%83%E5%85%B3%E4%BA%8E%E9%85%8D%E7%BD%AE%E7%9A%84%E8%AF%B4%E6%98
    %8E)
* [3\.2 史诗级代码补全插件——YouCompleteMe](#32-%E5%8F%B2%E8%AF%97%E7%BA%A7%E4%BB%A3%E7%A0%81%E8%A1%A5%E5%85%A8%E6%
  8F%92%E4%BB%B6youcompleteme)
  * [3\.2\.1 安装前的准备](#321-%E5%AE%89%E8%A3%85%E5%89%8D%E7%9A%84%E5%87%86%E5%A4%87)
    * [3\.2\.2 下载源码](#322-%E4%B8%8B%E8%BD%BD%E6%BA%90%E7%A0%81)
    * [3\.2\.3 编译源码](#323-%E7%BC%96%E8%AF%91%E6%BA%90%E7%A0%81)
    * [3\.2\.4 编译命令举例](#324-%E7%BC%96%E8%AF%91%E5%91%BD%E4%BB%A4%E4%B8%BE%E4%BE%8B)
    * [编译完成后的配置](#%E7%BC%96%E8%AF%91%E5%AE%8C%E6%88%90%E5%90%8E%E7%9A%84%E9%85%8D%E7%BD%AE)



# Windows平台下

## 1. Vim的安装

安装过程比较简单

[单击此处打开 Vim 的官网](https://www.vim.org/) 

#### 	1.1 在windows平台下安装vim

在此链接中选择合适自己的版本进行下载。https://github.com/vim/vim-win32-installer/releases

本人安装的版本是：gvim_8.2.1101_x64_signed.exe

GVim是Vim的图形前端。

在安装过程中，选择组件时建议**选择完整安装**，其余选项均保持默认即可。

## 2. Vim的四种模式

- 正常模式：

  - 在此模式下使用快捷命令，或**按:输入命令**。

  - 若要执行外部命令，按 :! 即可执行外部命令
    如：

    ```bash
    :!cl file.cpp 
    ```

    即可使用cl执行编译file.cpp的命令

- 插入模式：可以输入文本，在正常模式下，按以下命令进入插入模式。

  | 字符 | 小写时插入的位置     | 大写时插入的位置     |
  | ---- | -------------------- | -------------------- |
  | i    | 在当前字符前面插入   | 在当前行的最前面插入 |
  | a    | 在当前字符后插入     | 在当前行的最后插入   |
  | o    | 在当前行的下一行插入 | 在当前行的上一行插入 |

- 可视模式：正常模式下按v可以进入可视模式， 在可视模式下，移动光标可以选择文本。按V进入可视行模式， 总是整行整行的选中。ctrl+v进入可视块模式。

- 替换模式：正常模式下，按R进入。
  替换模式也有四种不同的类型

  | 字符 | 模式                         | 作用                                                         |
  | ---- | ---------------------------- | ------------------------------------------------------------ |
  | R    | 进入替换（REPLACE）模式      | 新输入的文本将直接替代/覆盖已经存在的内容                    |
  | r    | 单字符REPLACE                | 新输入的字符将替代光标之下的当前字符，然后自动返回到常规模式 |
  | gR   | 进入虚拟替换（VREPLACE）模式 | 同R有区别                                                    |
  | gr   | 单字符VREPLACE               | 同r有区别                                                    |

  - 单字符命令中增加数字前缀，可以一次性替换多个字符（都替换成同一个字符）
    例如 

    ```bash
    3r*|3gr*
    ```

    会将后面三个字符均替换成\*号

  - REPLACE和VREPLACE的区别

    | 模式     | 对于\<Tab\>的区别                                            | 对于\<NL\>的区别                                             |
    | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
    | REPLACE  | 新字符将直接替代\<Tab\>键所占用的所有空格的位置，会破坏文档格式 | 输入\<Enter\>回车键将增加新行                                |
    | VREPLACE | 在原有\<Tab\>键处输入字符，将仅仅替代单个空格，文本格式保持不变 | 输入\<Enter\>回车键将用新行替代当前行内容（即清空当前行,**且是从当前字符所在位置开始往后清空**） |

    也就是说，**REPLACE将Tab只当作一个字符（整体）来看，而VREPLACE则将Tab当作多个空格来看** 

## 3. Vimrc文件的配置

说明：

- **以下配置均可以在vim的命令模式下手动开启或关闭**，
  在命令模式下输入命令前首先输入 ：
  但**不修改**配置文件，只会**对当前vim编辑窗口生效**，重启即无效

- _vimrc文件是vim的配置文件，修改它就可以修改vim的一些默认配置，比如语法高亮，缩进长度等。其**位置就在vim的安装目录**下。

- 以下配置均只做**简单**但较为实用的介绍或配置，仅适合新手作为一个上手

- 在配置文件中，使用**双引号**作为注释，形如

  ```bash
  "显示行号"
  set nu
  ```

- 如有需要用到双引号作为字符串的情况，例如需要使用 `clang-format -style=“…” ` 可以使用转义字符 \\"  

- 对于大部分配置而言，需要关闭开启的配置，在命令前加上no即可，例如

  ```bash
  "显示行号"
  set nu
  "取消显示行号"
  set nonu
  ```

以下是一些常用配置及其中文说明

### 3.1 设置文件编码

若打开文件时中文显示乱码，则通过以下配置修改文件的编码，仅作示例

```bash
set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
set termencoding=utf-8
set encoding=utf-8
```

### 3.2 显示行号

```bash
set nu
set number
```

nu是number的缩写，这两条配置的效果是相同的，若要取消，在命令前加上no

**取消显示行号**

```bash
set nonu
set nonumber
```

### 3.3 突出显示当前行

```bash
set cursorline
set cul
```

cul是cursorline的缩写

### 3.4 突出显示当前列

```bash
set cursorcolumn
set cuc
```

### 3.5 设置突出显示行|列的颜色

vim中高亮行的默认颜色为darkred（深红）

```bash
"开启光亮光标行
  set cursorline
  hi CursorLine   cterm=NONE ctermbg=darkred ctermfg=white guibg=darkred guifg=white
"开启高亮光标列
  set cursorcolumn
  hi CursorColumn cterm=NONE ctermbg=darkred ctermfg=white guibg=darkred guifg=white
```

一般来说，只需要高亮行即可

**对于其它的一些语法高亮等本文不作记录** ,如有兴趣，参考：https://yyq123.blogspot.com/2017/02/vim-syntax-highlight.html

一些推荐使用的颜色：

```bash
black, brown, grey, blue, green, cyan, magenta, yellow, white，darkgrey
```



### 3.6 在Vim中启用鼠标

貌似不使用这个设置也能使用鼠标

```bash
"启用鼠标"
"set mouse=a"
"set selection=exclusive"
"set selectmode=mouse,key"
```



### 3.7 "显示括号匹配"

```bash
set sm
set showmatch
```

**可以设置显示匹配的时常，个人建议不这么做**

```bash
set matchtime=1  "单位是十分之一秒"
```



### 3.8 括号自动匹配

```bash
inoremap ( ()<LEFT>
inoremap { {}<LEFT>
inoremap [ []<LEFT>
```

该配置会在输入左括号时自动匹配右括号，推荐在**替换模式**下使用该配置，这样就可以在输入右括号时免去使用方向键

**按此格式可以设置引号自动匹配**

```bash
"引号自动匹配添加"
inoremap " ""<LEFT>
inoremap ' ''<LEFT>
```

当然，更实用的方式是使用插件 [delimitMate](https://github.com/Raimondi/delimitMate),该插件对括号补全有一个最实用的功能：在一对括号之间回车，自动分为 3 行并调整缩进

### 3.9 设置缩进

```bash
set tabstop=4 "tab的长度"
set shiftwidth=4 "自动缩进的长度"
set smartindent 	"设置自动缩进的方式为此"
```

自动缩进的三种方式：

- set autoindent
  每行的缩进值与上一行相等，使用 set noautoindent 可以取消设置
  当你在输入状态用回车键插入一个新行，或者在 normal 状态用 o 或者 O 插入一个新行时，autoindent 会自动地将当前行的缩进拷贝到新行，也就是"自动对齐”
- set cindent
  它会按照 C 语言的语法，自动地调整缩进的长度，比如，当你输入了半条语句然后回车时，缩进会自动增加一个 TABSTOP 值，当你键入了一个右花括号时，会自动减少一个 TABSTOP 值。
- set smartindent
  在这种缩进模式中，每一行都和前一行有相同的缩进量，同时这种缩进形式能正确的识别出花括号，当遇到右花括号（}），则取消缩进形式。此外还增加了识别C语言关键字的功能。如果一行是以#开头的，那么这种格式将会被特殊对待而不采用缩进格式。

### 3.10 设置粘贴模式

```bash
"set paste" "使用此设置，通过鼠标右键粘贴时不会变更格式"
set pastetoggle=<F9>	"在插入模式下，按F9自动切换粘贴模式"
```



### 3.11 设置非可见字符(tab|空格)可见

**显示非可见字符**

```bash
set list
```

**切换可见或不可见**

```bash
set list!
```

**设置显示模式**

```bash
set listchars
```

样例：
将制表符（tab）显示为>-；将尾部空格（trail）显示为-

```bash
"设置tab和空格的可见字符"
set listchars=tab:>-,trail:-
"设置不可见可见字符的颜色"
hi SpecialKey guifg=darkgrey ctermfg=darkgrey
```

需要修改颜色修改 darkgrey（灰色） 为别的颜色即可

对于样式的更详细配置参考：https://segmentfault.com/a/1190000021101602

### 3.12 状态行的设置

```bash
"设置显示当前文件名(%t)，是否修改过(%m,若修改过会显示+号),文件总行数，当前行占比和光标位置。
set statusline=%t%m\ LEN=%L\ [%p%%]\ %c,%l
"总是显示状态行"
set laststatus=2
```

关于状态行的更多设置和选项本人认为过于冗余本文不做描述

### 3.13 显示光标当前位置

该命令不能与状态行同时使用，同时本人建议只使用该选项而不开启状态行，或两者都不使用，是否使用根据个人习惯而定

```bash
set ruler
```



### 3.14 打开文件类型检测

```bash
"打开文件类型检测"
"filetype plugin indent on"
" 打开文件类型检测 "
"filetype on"
```

对于该配置建议阅读：https://vimjc.com/vim-filetype.html

### 3.15 ★重要·打开语法高亮显示★ 

```bash
" 打开语法高亮显示 "
syntax on
```

启用vim自带的语法高亮功能



### 3.16 代码折叠

Vim支持多种折叠形式：手动折叠**manual**、基于缩进行折叠**indent**、基于语法进行折叠**syntax**、未更改文本折叠**diff**等

建议使用 indent 或者 syntax

```bash
"基于缩进进行代码折叠
set foldmethod=indent
"启动 Vim 时关闭折叠
set nofoldenable
```

如不设置第二个配置，在每次启动vim时所有的代码都默认是折叠状态的

对于代码折叠，有更智能的插件：[SimpleFold](https://github.com/tmhedberg/SimpylFold) 

**代码折叠的快捷键：** 

| 命令 | 作用               |
| ---- | ------------------ |
| za   | 打开或关闭当前折叠 |
| zM   | 关闭所有折叠       |
| zR   | 打开所有折叠       |

---

---

## 3. 在Vim中安装并使用插件

### 3.1 ★★★插件管理工具——Vundle★★★

**以下介绍的所有插件都是利用Vundle工具进行安装的** 

[Vundle](https://github.com/VundleVim/Vundle.vim)是一个Vim插件管理器，用于方便地安装、更新和卸载插件。且其本身就是一个插件。

####  3.1.1 安装Vundle

Vundle基于Git架构，每一个插件都是一个项目的Repository，通过Vundle可以用简单的指令，可以一键安装/更新/删除所有插件

安装有两种方式：

1.在 https://github.com/VundleVim/Vundle.vim.git 下载 Vundle.vim 文件保存到 `vim安装目录/vimfiles/vundle` 下即可。

2.使用git的安装（推荐）

**首先要下载 Git** ，下载地址：https://gitforwindows.org/

安装完毕后**配置环境变量**（如果不知道环境变量是什么，请使用搜索引擎搜索），完成后运行CMD输入以下命令：`git --version` 若成功打印出版本信息则说明安装成功

然后执行以下命令将 Vundle 安装到指定目录

`git clone https://github.com/VundleVim/Vundle.vim.git vim安装目录/vimfiles/vundle/Vundle.vim`

**必须要安装Git并且配置环境变量成功才能执行！** 

例如：

```bash
git clone https://github.com/VundleVim/Vundle.vim.git "D:\Program Files\Vim\vimfiles\vundle\Vundle"
```

记得安装目录中如果带有空格需要加上引号，因此也建议在所有的路径字符串中加上引号

值得注意的是，在Git中自带了一个Vim编辑器

#### 3.1.2 配置Vundle

无论以何种方式安装，都需要进行如下配置

在vimrc中将如下配置模板粘贴进去

```bash
"==================================Vundle插件管理器的配置=================================="

set nocompatible               "去除VIM一致性，必须"
filetype off                   "必须"

"设置包括vundle和初始化相关的运行时路径"
set rtp+=$VIM/vimfiles/vundle/Vundle
call vundle#begin()

Plugin 'VundleVim/Vundle.vim'	"启用vundle管理插件，必须"

"在此增加其他插件，安装的插件需要放在vundle#begin和vundle#end之间"
"安装github上的插件格式为 Plugin '用户名/插件仓库名'"

 call vundle#end()
 
filetype plugin indent on     "加载vim自带和插件相应的语法和文件类型相关脚本，必须"

"==================================Vundle插件管理器的配置=================================="
```



#### 3.1.3 安装插件

**注意事项：**安装的路径一定要设置好，==第七行的 `set rtp=` 后接的是你的Vundle的安装路径==，你可以在使用Git安装Vundle的时候指定其它路径比如在Vundle：

**第一步**，配置。在模板中，把要安装的插件按此格式：`Plugin '需要安装的插件'` 添加到`call vundle#begin() `和 `call vundle#end()` 之间，也就是第8行到第16行之间即可完成第一步的配置工作

例如：

```bash
"==================================Vundle插件管理器的配置=================================="

set nocompatible               "去除VIM一致性，必须"
filetype off                   "必须"

"设置包括vundle和初始化相关的运行时路径"
set rtp+=$VIM/vimfiles/vundle/Vundle
call vundle#begin('$VIM/vimfiles/vundle/')

Plugin 'VundleVim/Vundle.vim'	"启用vundle管理插件，必须"
Plugin 'Valloric/YouCompleteMe'
Plugin 'Chiel92/vim-autoformat'

"在此增加其他插件，安装的插件需要放在vundle#begin和vundle#end之间"
"安装github上的插件格式为 Plugin '用户名/插件仓库名'"

 call vundle#end()
 
filetype plugin indent on     "加载vim自带和插件相应的语法和文件类型相关脚本，必须"

"==================================Vundle插件管理器的配置=================================="
```

追加了两条Plugin即可完成配置

**第二步**，安装。

在vim中执行 `PluginInstall` 命令即可自动完成所有插件的安装

**其它安装方式**

或者，你也可以在vim下使用 `:PluginInstall 插件名` 命令来直接安装

例如：`:PluginInstall Valloric/YouCompleteMe` 



#### 3.1.4 卸载插件

先在[vimrc](https://link.zhihu.com/?target=http%3A//yyq123.blogspot.com/2012/01/vim-vimrc.html)配置文件中注释或者删除对应插件的配置信息，执行：

`PluginClean`

即可删除指定插件

#### 3.1.5 更新插件

自动批量更新所有已安装的插件命令：

`PluginUpdate`

使用以下命令，可以查看更多帮助信息：

`:help vundle`

#### 3.1.6 其它关于配置的说明

`call vundle#begin()`的括号中可以填写其它插件在安装时的安装路径，例如我设置的路径是：``$VIM/vimfiles/vundle/Plugin`。`$VIM`表示vim的安装目录

对于Vundle和Plugin的安装路径，完全是自由的，可以自己选择其位置。

---

### 3.2 史诗级代码补全插件——YouCompleteMe

#### 3.2.1 安装前的准备

YCM是一个用于自动代码补全的神器，它**基于语义分析**补齐：通过分析源文件，经过语法分析以后进行智能补全。YCM几乎对现在所有流行的编程语言都提供了非常强大的补齐功能

它不仅强大，同时也是传说中Vim上最难安装的插件。

在Windows下，安装YCM之前，你的电脑应该存在有如下的环境：

- Python2 or Python3 (**必须使用和你使用的vim所支持的python版本以及和vim架构一致的版本**，比如，vim是64bit的，且支持python3，那么你的python也必须是python3.* 64bit 的)
  在此处：https://www.python.org/downloads/windows/
- Visual Studio（需要安装了*开发窗口桌面程序*）
  在此处安装最新版或旧版本https://visualstudio.microsoft.com/zh-hans/vs/older-downloads/
- cmake（需要配置到系统环境变量中）
  在此处：https://cmake.org/download/
  如果的VS中安装了cmake，也可以直接使用VS中的cmake，只需要将环境变量配置好即可

对于Vim，你的Vim必须支持Python2或Python3，要查看是否支持，在vim中输入命令 `:version` 即可查看，如果支持，你应该可以在列表中查看到类似 `+python2/dyn` `+python3/dyn` 的字样，若前面的符号是 - ，则说明不支持，请重新安装或编译你的vim，如果你在安装vim选择组件的过程中选择了完整安装，那么应该是支持的。

#### 3.2.2 下载源码

可以使用Git来进行安装，但本文仅介绍使用Vundle的方式。

YCM的git地址:https://github.com/ycm-core/YouCompleteMe

在 vimrc 中 Vundle 的配置部分中添加 `Plugin 'Valloric/YouCompleteMe'` 然后在 Vim 中执行安装命令即可下载YCM的源码。下载过程可能会比较长。

在下载完源码后，在**YCM的源码目录**运行 `git submodule update --init --recursive` 来获取 YouCompleteMe 必要的相关依赖。同样下载过程可能会比较长。

#### 3.2.3 编译源码

本文只介绍最简单的编译方式，详细请参考 [YCM](https://github.com/ycm-core/YouCompleteMe) 

**下载完毕后，在源码目录执行**

`python install.py --语言选项 --msvc **`编译。

对于语言选项，有如下选项：

- C-family languages support：`--clangd-completer`
- C# support: install Mono and add `--cs-completer` 
- Go support: install [Go](https://golang.org/doc/install) and add `--go-completer`
- JavaScript and TypeScript support: install [Node.js and npm](https://docs.npmjs.com/getting-started/installing-node#1-install-nodejs--npm) and add `--ts-completer` 
- Rust support:  `--rust-completer` 
- Java support: install [JDK8 (version 8 required)](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) and add `--java-completer`

**例如：**`python install.py --clangd-completer`

即可编译具有C族语言的语义补全功能的 YouCompleteMe 插件。

对于 -msvc 选项，你需要指定你的VS版本，其默认值是16。

YCM支持MSVC 14（Visual Studio 2015），15（2017）和MSVC 16（Visual Studio 2019）

#### 3.2.4 编译命令举例

例如，我的python版本是**python3.8**，我想要编译**带有C族语义补全功能的YCM插件**且我的**VS版本是2017**，那么我的编译命令应该是

`python install.py --clangd-completer --msvc 15`

在YCM源码目录执行即可。

#### 编译完成后的配置

此处暂仅给出一个样例

```bash
"==================================YCP插件的配置=================================="
let g:ycm_add_preview_to_completeopt = 0
let g:ycm_show_diagnostics_ui = 0
let g:ycm_server_log_level = 'info'
let g:ycm_min_num_identifier_candidate_chars = 2
let g:ycm_collect_identifiers_from_comments_and_strings = 1
let g:ycm_complete_in_strings=1
let g:ycm_key_invoke_completion = '<c-z>'
set completeopt=menu,menuone

noremap <c-z> <NOP>

let g:ycm_semantic_triggers =  {
           \ 'c,cpp,python,java,go,erlang,perl': ['re!\w{2}'],
           \ 'cs,lua,javascript': ['re!\w{2}'],
           \ }

"设置补全菜单的颜色"
highlight PMenu ctermfg=0 ctermbg=242 guifg=black guibg=darkgrey
highlight PMenuSel ctermfg=242 ctermbg=8 guifg=darkgrey guibg=black
"==================================YCP插件的配置=================================="
```

