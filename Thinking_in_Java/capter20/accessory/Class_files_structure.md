# Class 类文件的结构
Class文件是一组<font color=red>以8位字节为基础单位的二进制流</font>。<font color=orange>Class文件中各个数据项目严格按照顺序紧凑地排列，
数据项目之间不存在任何分隔符，这使得整个Class文件中存储的内容几乎全部都程序运行的必要数据，没有空隙存在</font>。
当遇到需要占用1字节以上空间的数据项时，则按照高位在前的方式分割成多个8位字节进行存储。

根据Java虚拟机规范的规定，Class文件格式采用一种类似于C语言结构体的伪结构来存储数据，这种伪结构中只有两种数据类型：
无符号数和表。

<font color=green>**无符号数**</font> 属于基本的数据类型，以<font color=#1E90FF>u1、u2、u4、u8</font>来分别代表<font color=#1E90FF>1字节、2字节、4字节、8字节</font>的无符号数，
 无符号数可以用来描述：数字、索引引用、数量值或者按照UTF-8编码构成的字符串值。
 
 <font color=green>**表**</font> 是由多个符号数或者其他表作为数据项而构成的复合数据类型，所有表都习惯性地以“_info”结尾。
表是用于描述有层次关系的复合结构的数据，整个Class文件本质上就是一张表。

构成Class文件这张“表”的各数据项如下表1所示：

<center><font size=5>表1 Class文件格式</font></center>

|  名称  |  类型  |   数量  |
| :---:  |  :---: | :---: |
| magic | u4 | 1 |
| minor_version | u2 | 1 |
| major_version | u2 | 1 |
| constant_pool_count | u2 | 1|
| <font color=#1E90FF>constant_pool</font> | cp_info | constant_pool_count-1 |
| access_flags | u2 | 1 |
| this_class | u2 | 1 |
| super_class | u2 | 1 |
| interfaces_count | u2 | 1|
| interfaces | u2 | interfaces_count |
| fields_count | u2 | 1 |
| <font color=#1E90FF>fields</font> | field_info | fields_count |
| methods_count | u2 | 1 |
| <font color=#1E90FF>methods</font> | method_info | methods_count |
| attributes_count | u2 | 1 | 
| <font color=#1E90FF>attributes</font> | attribute_info | attributes_count |

无论是无符号数还是表，当需要描述同一类型但数量不定的多个数据时，经常会使用 一个前置的容量计数器加若干个连续数据项的形式，
这时称这一系列连续的某类型的数据为该类型的集合。

## 总结
Class文件的结构不像XML等描述性语言，它没有任何分隔符，上面表1中的所有数据项无论是顺序还是数量，
甚至于数据存储的字节序这样的细节，都是被严格限定的，哪个字节代表什么含义，长度有多少，先后顺序如何，
都不允许改变。

***PS: Class文件中每种数据项的详细说明见这位仁兄的文章：[Java类文件结构](https://www.cnblogs.com/mathilda365/p/10648328.html)***

## （完）

### [返回](../20.5_Annotation-based_unit_testing.md)

