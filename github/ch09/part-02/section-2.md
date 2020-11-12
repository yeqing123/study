# 二、共筑爱巢之 -- vi 简介

一提到文本编辑器我们就会想到 World ，它是Windows操作系统下的图形用户界面下的文字处理软件。Linux 命令行下当然就不能用图形用户界面了，Linux 命令行下的文字处理软件主要有：Nano、Emacs 和 Vi。
我们着重讲 vi，为什么呢？有以下三个理由：  
1. 很多 Linux 系统都预装了 vi ，如果我们的 Linux 没有图形用户界面，比如一台远程的服务器或者一个 XWindow 配置损坏了的系统，那么 vi 就成了我们的救星
（虽然 Namo 已经流行起来，但还没有普及）；
2. vi 轻量级而且执行速度快，尤其是相比图形用户界面的文本编辑器，加载速度更快；
3. 很多高手都在使用 vi，熟练使用 vi 使人感觉很牛叉，可以满足我们装B的需求 :-)

vi 的名字来源于单词 visual，现在大多数的 Linux 发行版，不包含真正的 vi，而是一款 vi 的高级版叫 vim ，它是 vi improved 的缩写。
Vim是从 vi 发展出来的一个文本编辑器。代码补完、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用。
简单的来说， vi 是老式的字处理器，不过功能已经很齐全了，但是还是有可以进步的地方。 vim 则可以说是程序开发者的一项很好用的工具。
连 vim 的官方网站 (http://www.vim.org) 自己也说 vim 是一个程序开发工具而不是文字处理软件。

下面来介绍如何操作 vim：
1. 如何启动和关闭 vim? 启动就是按 vi 或 vim。如果要打开某个文件，在vi 或 vim 后面跟文件名，如果文件不存在则 vim 会自动新建一个文件。退出就是按 :q 或 :q!，如果冒号出不来可以多按几次 Escape 键。
2. 如何操作 vi/vim? vi 有两种命令模式，一个是**普通（normal）模式**，一个是**插入（insert）模式**。启动vi 后首先进入的是普通模式，
  普通模式是不能插入文本的，因此我们就需要进入到*插入模式*，按 i 键（insert）是在光标位置插入，a 键(append)是在光标位置追加，如果按 A 键就是在光标所在的行尾追加，
  s 键会删除光标所在的字符，然后进入插入模式， S 键会删除整行文本，并进入插入模式。进入插入模式就可以编辑文本了。
  编辑完成后按 Escape 键进入普通模式。保存并退出 vim，可以按 :wq，不保存并退出按 :q!
3. 为什么刚启动 vi 后是*普通模式*呢？因为它有很多快捷的键盘操作，可以让我们方便的进行文本操作，详细的键盘操作如下表所示：  
<table class="multi">
<caption class="cap">表13-1: 光标移动按键</caption>
<tr>
<th class="title">按键</th>
<th class="title">移动光标</th>
</tr>
<tr>
<td valign="top" width="25%">l or 右箭头</td>
<td valign="top">向右移动一个字符</td>
</tr>
<tr>
<td valign="top">h or 左箭头</td>
<td valign="top">向左移动一个字符</td>
</tr>
<tr>
<td valign="top">j or 下箭头</td>
<td valign="top">向下移动一行</td>
</tr>
<tr>
<td valign="top">k or 上箭头</td>
<td valign="top">向上移动一行</td>
</tr>
<tr>
<td valign="top">0 (零按键) </td>
<td valign="top">移动到当前行的行首。</td>
</tr>
<tr>
<td valign="top">^</td>
<td valign="top">移动到当前行的第一个非空字符。</td>
</tr>
<tr>
<td valign="top">$</td>
<td valign="top">移动到当前行的末尾。</td>
</tr>
<tr>
<td valign="top">w</td>
<td valign="top">移动到下一个单词或标点符号的开头。</td>
</tr>
<tr>
<td valign="top">W</td>
<td valign="top">移动到下一个单词的开头，忽略标点符号。</td>
</tr>
<tr>
<td valign="top">b</td>
<td valign="top">移动到上一个单词或标点符号的开头。</td>
</tr>
<tr>
<td valign="top">B</td>
<td valign="top">移动到上一个单词的开头，忽略标点符号。</td>
</tr>
<tr>
<td valign="top">Ctrl-f or Page Down </td>
<td valign="top">向下翻一页</td>
</tr>
<tr>
<td valign="top">Ctrl-b or Page Up </td>
<td valign="top">向上翻一页</td>
</tr>
<tr>
<td valign="top">numberG</td>
<td valign="top">移动到第 number 行。例如，1G 移动到文件的第一行。</td>
</tr>
<tr>
<td valign="top">G</td>
<td valign="top">移动到文件末尾。</td>
</tr>
</table>



<table class="multi">
<caption class="cap">表13-2: 文本行打开按键</caption>
<tr>
<th class="title">命令</th>
<th class="title">打开行</th>
</tr>
<tr>
<td valign="top" width="25%">o</td>
<td valign="top">当前行的下方打开一行。</td>
</tr>
<tr>
<td valign="top">O</td>
<td valign="top">当前行的上方打开一行。</td>
</tr>
</table>




<table class="multi">
<caption class="cap">表13-3: 文本删除命令</caption>
<tr>
<th class="title">命令</th>
<th class="title">删除的文本</th>
</tr>
<tr>
<td valign="top" width="25%">x</td>
<td valign="top">当前字符</td>
</tr>
<tr>
<td valign="top">3x</td>
<td valign="top">当前字符及其后的两个字符。</td>
</tr>
<tr>
<td valign="top" width="25%">dd</td>
<td valign="top">当前行。</td>
</tr>
<tr>
<td valign="top" width="25%">5dd</td>
<td valign="top">当前行及随后的四行文本。</td>
</tr>
<tr>
<td valign="top" width="25%">dW</td>
<td valign="top">从光标位置开始到下一个单词的开头。</td>
</tr>
<tr>
<td valign="top" width="25%">d$</td>
<td valign="top">从光标位置开始到当前行的行尾。</td>
</tr>
<tr>
<td valign="top" width="25%">d0</td>
<td valign="top">从光标位置开始到当前行的行首。</td>
</tr>
<tr>
<td valign="top" width="25%">d^</td>
<td valign="top">从光标位置开始到文本行的第一个非空字符。</td>
</tr>
<tr>
<td valign="top" width="25%">dG</td>
<td valign="top">从当前行到文件的末尾。</td>
</tr>
<tr>
<td valign="top" width="25%">d20G</td>
<td valign="top">从当前行到文件的第20行。</td>
</tr>
</table>


<table class="multi">
<caption class="cap">表13-4: 复制粘贴命令 </caption>
<tr>
<th class="title">命令</th>
<th class="title">复制的内容</th>
</tr>
<tr>
<td valign="top" width="25%">yy</td>
<td valign="top">当前行。</td>
</tr>
<tr>
<td valign="top">5yy</td>
<td valign="top">当前行及随后的四行文本。</td>
</tr>
<tr>
<td valign="top">yW</td>
<td valign="top">从当前光标位置到下一个单词的开头。</td>
</tr>
<tr>
<td valign="top">y$</td>
<td valign="top">从当前光标位置到当前行的末尾。</td>
</tr>
<tr>
<td valign="top">y0</td>
<td valign="top">从当前光标位置到行首。</td>
</tr>
<tr>
<td valign="top">y^</td>
<td valign="top">从当前光标位置到文本行的第一个非空字符。</td>
</tr>
<tr>
<td valign="top">yG</td>
<td valign="top">从当前行到文件末尾。</td>
</tr>
<tr>
<td valign="top">y20G</td>
<td valign="top">从当前行到文件的第20行。</td>
</tr>
<tr>
<td valign="top">p</td>
<td valign="top">在当前行的后面粘贴1遍</td>
</tr>
<tr>
<td valign="top">3p</td>
<td valign="top">在当前行的后面粘贴3遍，p前面的数字可以自己定义</td>
</tr>
<td valign="top">P</td>
<td valign="top">在当前行的前面粘贴1遍</td>
</tr>
<tr>
<td valign="top">3P</td>
<td valign="top">在当前行的前面粘贴3遍，P前面的数字可以自己定义</td>
</tr>
</table>




<table class="multi">
<catption="cap">表13-5：查找和替换</catption>
<tr>
<th class="title">条目</th>
<th class="title">含义</th>
</tr>
<tr>
<td valign="top" width="25%">:</td>
<td valign="top">冒号字符运行一个 ex 命令。</td>
</tr>
<tr>
<td valign="top">s</td>
<td valign="top">指定操作。在这种情况下是，替换（查找与替代）。</td>
</tr>
<tr>
<td valign="top">/keyword</td>
<td valign="top">查找关键字，系统会在整个文本中查找，按 n 向下查找，按 N 向上查找</td>
</tr>
<tr>
<td valign="top">g</td>
<td valign="top">这是“全局”的意思，意味着对文本行中所有匹配的字符串执行查找和替换操作。如果省略 g，则只替换每个文本行中第一个匹配的字符串。</td>
</tr>
<tr>
<td valign="top">:%s/old_word/new_word</td>
<td valign="top">在当前行中，将old_word替换成new_word</td>
</tr>
<td valign="top">:%s/old_word/new_word/g</td>
<td valign="top">在整个文本中，将old_word替换成new_word</td>
</tr>
</table>




<table class="multi">
<caption class="cap">表13-5: 替换确认按键</caption>
<tr>
<th class="title">按键</th>
<th class="title">行为</th>
</tr>
<tr>
<td valign="top" width="25%">y</td>
<td valign="top">执行替换操作</td>
</tr>
<tr>
<td valign="top">n</td>
<td valign="top">跳过这个匹配的实例</td>
</tr>
<tr>
<td valign="top">a</td>
<td valign="top">对这个及随后所有匹配的字符串执行替换操作。</td>
</tr>
<tr>
<td valign="top">q or esc</td>
<td valign="top">退出替换操作。</td>
</tr>
<tr>
<td valign="top">l</td>
<td valign="top">执行这次替换并退出。l 是 “last” 的简写。</td>
</tr>
<tr>
<td valign="top">Ctrl-e, Ctrl-y</td>
<td valign="top">分别是向下滚动和向上滚动。用于查看建议替换的上下文。</td>
</tr>
</table>

<table class="multi">
<caption class="cap">表13-7：多文件操作</caption>
<tr>
<th class="title">按键</th>
<th class="title">行为</th>
</tr>
<tr>
<td valign="top">vi or vim filename1 filename2...</td>
<td valign="top">vi 或 vim 后面跟多个文件，可以同时打开多个文件</td>
</tr>
<tr>
<td valign="top">:n</td>
<td valign="top">切换到下一个文件</td>
</tr>
<tr>
<td valign="top">:N</td>
<td valign="top">切换到上一个文件</td>
</tr>
<tr>
<td valign="top">:sp</td>
<td valign="top">同时打开多个vim窗口，按 Ctrl-ww 可以让光标在多个窗口之间切换</td>
</tr>
<tr>
<td valign="top">:e new_fileName</td>
<td valign="top">新建一个文件</td>
</tr>
</table>

**_ps:_**  
**_关于 vi/vim 的操作快捷键还有很多内容，这里就不在一一赘述，有兴趣的小伙伴可以自己在网上查找相关的文档和手册。重要的是多加练习熟能生巧，才能更熟练的掌握 vim 编辑器的使用。_**

## （完）


