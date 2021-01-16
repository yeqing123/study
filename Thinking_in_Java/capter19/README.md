# 第十九章 枚举类型
## 目录
- [（一）基本enum特性](19.1_Basic_enum_features.md)
- [（二）向enum中添加新方法](19.2_Adding_methods_to_an_enum.md)
- [（三）switch语句中的enum](19.3_enums_in_switch_statements.md)
- [（四）values()的神秘之处](19.4_The_mystery_of_values（）.md)
- [（五）实现，而非继承](19.5_Implements,not_inherits.md)
- [（六）随机选取](19.6_Random_selection.md)
- [（七）使用接口组织枚举](19.7_Using_interfaces_for_organization.md)
- [（八）使用EnumSet替代标志](19.8_Using_EnumSet_instead_of_flags.md)
- [（九）使用EnumMap](19.9_Using_EnumMap.md)
- [（十）与常量相关的方法](19.10_Constant-specific_methods.md)
- [（十一）多路分发](19.11_Multiple_dispatching.md)
- [（十二）总结](19.12_Summary.md)


**关键字enum可以将一组具名的值的有限集合创建为一种新的类型，而这些具名的值可以作为常规的程序组件使用。这是一种非常有功的功能。**

在第5章结束的时候，我们已经简单地介绍了枚举的概念。现在，你对Java已经有了更深刻的理解，因此可以更深入地学习Java SE5中的枚举了。你将在本章中看到，使用enum可以做很多有趣的事情，
同时，我们也会深入其他的Java特性，例如泛型和放射。在这个过程中，我们还将学习一些设计模式。