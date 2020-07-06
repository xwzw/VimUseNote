# Windows平台下

## Vim的安装

安装过程比较简单

[单击此处打开 Vim 的官网](https://www.vim.org/) 

#### 	在windows平台下安装vim

在此链接中选择合适自己的版本进行下载。https://github.com/vim/vim-win32-installer/releases

本人安装的版本是：gvim_8.2.1101_x64_signed.exe

GVim是Vim的图形前端。

在安装过程中，选择组件时建议**选择完整安装**，其余选项均保持默认即可。

## Vim的四种模式

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

## Vimrc文件的配置

说明：

- **以下配置均可以在vim的命令模式下手动开启或关闭** 
  _vimrc文件是vim的配置文件，其**位置就在vim的安装目录**下。
  在命令模式下输入命令前首先输入 ：
  但不修改配置文件的话只会**对当前vim编辑窗口生效**，重启即无效

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

### 1. 设置文件编码

若打开文件时中文显示乱码，则通过以下配置修改文件的编码，仅作示例

```bash
set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
set termencoding=utf-8
set encoding=utf-8
```

### 2.显示行号

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

### 3.突出显示当前行

```bash
set cursorline
set cul
```

cul是cursorline的缩写

### 4.突出显示当前列

```bash
set cursorcolumn
set cuc
```

### 5.设置突出显示行|列的颜色

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



### 6.在Vim中启用鼠标

貌似不使用这个设置也能使用鼠标

```bash
"启用鼠标"
"set mouse=a"
"set selection=exclusive"
"set selectmode=mouse,key"
```



### 7."显示括号匹配"

```bash
set sm
set showmatch
```

**可以设置显示匹配的时常，个人建议不这么做**

```bash
set matchtime=1  "单位是十分之一秒"
```



### 8.括号自动匹配

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

### 9.设置缩进

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

### 10.设置粘贴模式

```bash
"set paste" "使用此设置，通过鼠标右键粘贴时不会变更格式"
set pastetoggle=<F9>	"在插入模式下，按F9自动切换粘贴模式"
```



### 11.设置非可见字符(tab|空格)可见

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

### 12.状态行的设置

```bash
"设置显示当前文件名(%t)，是否修改过(%m,若修改过会显示+号),文件总行数，当前行占比和光标位置。
set statusline=%t%m\ LEN=%L\ [%p%%]\ %c,%l
"总是显示状态行"
set laststatus=2
```

关于状态行的更多设置和选项本人认为过于冗余本文不做描述

### 13.显示光标当前位置

该命令不能与状态行同时使用，同时本人建议只使用该选项而不开启状态行，或两者都不使用，是否使用根据个人习惯而定

```bash
set ruler
```



### 14.打开文件类型检测

```bash
"打开文件类型检测"
"filetype plugin indent on"
" 打开文件类型检测 "
"filetype on"
```

对于该配置建议阅读：https://vimjc.com/vim-filetype.html

### 15.★重要·打开语法高亮显示★ 

```bash
" 打开语法高亮显示 "
syntax on
```

启用vim自带的语法高亮功能



### 16.代码折叠

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

