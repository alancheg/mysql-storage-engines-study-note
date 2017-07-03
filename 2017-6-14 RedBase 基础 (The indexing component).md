RedBase 基础 (The indexing component)

https://web.stanford.edu/class/cs346/2015/redbase-ix.html

##  介绍

RedBase 系统中第二个需要实现的部分就是 检索组件 （the indexing component）。IX 组件提供了 类 和 方法 来管理 存储在页面文件中无序数据的持久检索。每一个数据文件都会对应任意数量的单属性检索。这些检索最终会用来加速关系查找、连接、基于条件的更新和删除操作 的进程。就像这些数据记录本身，检索文件也被存储在 页文件中。因此，在实现 IX 组件的过程中你将会像 part 1 中一样使用 PF 组件。在整个 RedBase 结构中，你可以将 IX 和 RM 组件视作和 PF 组件同等重要的。

在 IX 组件中你将会实现的检索技术是 B+ 树，B+ 树将会在课程中被回顾，并且包含在课程 CS245 中。并且在几乎所有的数据库教材中都会被提到。因为一个 B+ 树 的 ‘完美’  实现是非常复杂的，所以我们允许类似于讨论 https://web.stanford.edu/class/cs346/2015/redbase-ix.html#impl 中的简易实现。

所有的类名，返回值，常量等等。在此例中都会以 IX 为前缀。每一个 B+ 树索引都会被存储在 PF 组件中的一个 页文件中。一些特殊的实现简易可以在 https://web.stanford.edu/class/cs346/2015/redbase-ix.html#impl 中了解，但是你应该意识到我们在 IX 组件中提供了相对 RM 组件中更少的细节。

*Note*

在此 https://web.stanford.edu/class/cs346/2015/notes/jannink.pdfIX 可以看到一些关于 B+ 树的相关信息。

##  接口

此部分不进行翻译，详情见原始网页。