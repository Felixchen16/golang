## Golang

> 一个21世纪的C语言，让你用写Python代码的开发效率编写C语言代码。

## Go性能强悍

与其他现代高级语言（如Java/Python）相比，使用C，C++的最大好处是它们的性能。因为C/ C++是编译型语言而不是解释的语言。 处理器只能理解二进制文件，Java和Python这种高级语言在运行的时候需要先将人类可读的代码翻译成字节码，然后由专门的解释器再转变成处理器可以理解的二进制文件。![-w839](https://github.com/Felixchen16/golang/blob/master/docs/pic/1.1.jpg?raw=true)同C,C++一样，Go语言也是编译型的语言，它直接将人类可读的代码编译成了处理器可以直接运行的二进制文件，执行效率更高，性能更好。![-w1112](https://github.com/Felixchen16/golang/blob/master/docs/pic/1.2.jpg?raw=true)

可以看出，Go 语言在性能上更接近于 Java 语言，虽然在某些测试用例上不如经过多年优化的 Java 语言，但毕竟 Java 语言已经经历了多年的积累和优化。Go 语言在未来的版本中会通过不断的版本优化提高单核运行性能。

## 语法简洁

Go 语言简单易学，学习曲线平缓，不需要像 C/C++ 语言动辄需要两到三年的学习期。Go 语言被称为“互联网时代的C语言”。Go 语言的风格类似于C语言。其语法在C语言的基础上进行了大幅的简化，去掉了不需要的表达式括号，循环也只有 for 一种表示方法，就可以实现数值、键值等各种遍历。

## 代码风格统一

Go 语言提供了一套格式化工具——`go fmt`。一些 Go 语言的开发环境或者编辑器在保存时，都会使用格式化工具进行修改代码的格式化，这样就保证了不同开发者提交的代码都是统一的格式。

## 开发效率高

![img](https://github.com/Felixchen16/golang/blob/master/docs/pic/1.3.jpg?raw=true)Go语言实现了开发效率与执行效率的完美结合，让你像写Python代码（效率）一样编写C代码（性能）。