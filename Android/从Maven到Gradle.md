从Maven到Gradle
===
###（一）Maven
####1、定义
maven 是强大的构建工具，帮我们自动化完成构建工作，如清理、编译、测试、生成报告、打包部署等。  
除了编写源代码，我们每天还花了很多时间在编 译、运行单元测试、生成文档、打包和部署等烦琐的工作上，这就是构建。手工完成，成本非常高，于是有人用软件的方法让这一系 列工作完全自动化，使得软件的构建可以像全自动流水线一样，只需要一条简单的命令，所有烦琐的步骤都能够自动完成，很快就能得到最终结果。

####2、优点
#####（1）跨平台
在 windows、linux或者mac上都能使用。
#####（2）标准化构建过程
形成一种标准之后，统一构建过程，减少学习成本。
#####（3）提供免费的中央仓库
可以找到主流的开源类库，自动下载依赖库。

###（二）Gradle
####1、定义
Gradle 是近年来新兴的构建工具，Hibernate宣布从Maven迁移至Gradle，Android Studio 也是用Gradle做项目构建。

####2、优点
#####（1）详细的文档
在官网能看到非常详细的文档，。
#####（2）简洁、灵活
比Maven更简洁，一行脚本就能依赖一个库；Groovy语法比ant的xml灵活简单。
#####（3）能简单引用Maven免费的中央仓库
能直接使用Maven依赖库，也能方便兼容发布更新Maven库。

参考文章：
http://www.cnblogs.com/dcba1112/archive/2011/05/01/2033805.html
http://www.infoq.com/cn/news/2011/04/xxb-maven-6-gradle

