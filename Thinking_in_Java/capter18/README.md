# 第十八章：Java I/O 系统
## 目录
1. [File类](18.1_The_File_class.md)
2. [输入和输出](18.2_Input_and_output.md)
3. [添加属性和有用的接口](18.3_Adding_attributes_and_useful_interfaces.md)
4. [Reader和Writer](18.4_Readers_&_Writers.md)
5. [自我独立的类：RandomAccessFile](18.5_Off_by_itself_RandomAccessFile.md)
6. [I/O流的典型使用方式](18.6_Typical_uses_of_IO_streams.md)
7. [文件读写的实用工具](18.7_File_reading_&_writing_utilities.md)
8. [标准I/O](18.8_Standard_IO.md)
9. [进程控制](18.9_Process_control.md)
10. [新I/O](18.10_New_IO.md)
11. [压缩](18.11_Compression.md)
12. [对象序列化](18.12_Object_serialization.md)
13. [XML](18.13_XML.md)
14. [Preferences](18.14_Preferences.md)
15. [总结](18.15_Summary.md)

---

**对程序语言的设计者来说，创建一个好的输入/输出（I/O）系统是一项艰难的任务。**

现有的大量不同方案已经说明了一点。挑战似乎来自于要覆盖所有的可能性。不仅存在各种**I/O源端**和想要与之通信的**接收端**（文件、控制台、网络连接等），
而且还需要以多种不同的方式与它们进行通信（顺序、随机存取、缓冲、二进制、按字符、按行、按字等）。  

Java类库的设计者通过创建大量的类来解决这个难题。使用者一开始可能会对Java I/O系统提供了如此多的类而感到不知所措（具有讽刺意味的是：Java I/O设计的初衷是为了避免过多的类）。
自从Java 1.0版本以来，Java的I/O类库发生了明显的变化，在原来的面向字节的类中添加了面向字符和基于Unicode的类。在JDK 1.4中，又添加了nio类（对于“新I/O”来说，
这是一个从现在起我们将要使用若干年的名称，即使它们在JDK 1.4中就已经被引入了，因此它们已经“旧”了）添加进来是为了改进性能及功能。因此，在充分理解Java I/O系统以便正确使用之前，
我们需要学习相当数量的类。另外，很有必要理解I/O类库的演化过程，即使我们的第一反应是“不要用历史打扰我，只需要告诉我怎么用”。但问题是，如果缺乏历史的眼光，
很快我们就会对什么时候该使用哪些类，以及什么时候不该使用它们而感到迷惑。

本章就介绍Java标准类库中各种各样的类以及它们的用法。
