# 六、难舍难分之 -- 高级键盘操作技巧

## 高级键盘操作技巧
1. 移动光标 move cursor
*注意：C 代表 Ctrl  A 代表 Alt，使用Alt键之前要先对Xshell的属性中的键盘进行设置，否则使用Alt时会执行Xshell的默认操作*  

- C-a 将光标移动到行首  
- C-e (e代表单词end)将光标移动到行尾
- C-f (f代表单词forward)将光标向前移动一个字符
- C-b 将光标向后(backward)移动一个字符
- A-f 将光标向前（forward）移动一个单词
- A-b 将光标向后(backward)移动一个单词
- C-l 清理屏幕，等效于 clear 命令

2. 修改文本 modify text
- C-d 删除光标后的一个字符
- C-t 交换光标前后的两个字符
- A-t 交换光标所在位置前面的两个单词
- A-l 将光标之后的单词字母变成小写（l代表单词lower）
- A-u 将光标之后的单词字母变成大写(u代表单词uper)

3. 复制/剪切和粘贴（copy & paste text）
- C-k 剪切光标之后的文本
- C-u 剪切光标之前的文本
- A-d 剪切光标之后的单词部分
- A-backspace 剪切光标之前的单词部分
- C-y 粘贴文本

4. 自动补全（auto complete）
自动补全用tab或两个tab键，当我们按一个tab键希望系统自动补全时，如果出现多个文件名匹配，系统不知道补哪一个时，就会出现“嘟。。。”的提示音，此时再按一下tab键就会出现多个匹配的文件名称供我们选择。  
*注意：自动补全除了对文件名进行补全，还可以对变量名进行补全*

5. 查看历史（history）
  - history 查看所有输入命令的历史，默认Bash会记住最后的500个命令
  - history | grep keyword 根据关键词所有历史
  - !num 根据历史的编号，直接执行该历史
  - !! 直接执行最近的一条历史
  - C-p 查看前一个(preview)历史
  - C-n 查看后一个(next)历史
  - A-< 查看第一条历史（history head）
  - A-> 查看最后一个条历史(history end)
  - C-r 在输入的同时，在历史中搜索相匹配的命令，也可按Tab键进行自动补全

## （完）