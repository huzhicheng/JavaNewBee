## 配置开发环境

俗话说，工欲善其事，必先利其器。代码这东西，都是在实践中来的，光看书没用。在动手写代码之后，当然需要把开发环境打造好了。

### 安装 JDK

配置开发环境的第一步就是安装 JDK 。如果你是刚接触 Java，可能还听过另外一个概念叫做 JRE，那么 JRE 和 JDK 有什么区别呢？

JRE 的全称是 Java Runtime Environment，是 Java 运行时环境，可以理解为运行 Java 需要的最基础环境基础，包括 JVM 和基础函数库。而 JDK 的全称是 Java Development Kit，是Java开发工具包，里面除了包含 JRE 的功能外， 还包含提供给开发者使用的一些其他组件，例如 javac 编译器、jvm 工具等。

所以，我们作为开发者，肯定是要安装 JDK 的，而在服务器上可以选择安装 JRE。

通过前面的介绍，我们已经知道了 JDK 有 Oracle JDK、OpenJDK，只是开发的话，这两个都可以选择，并且我们使用的过程中并不会感觉到有任何的差异。

而如果你通过访问 Oracle 或 OpenJDK 官网，可能找一会儿才能找到下载位置。其实不用那么麻烦，这里推荐一个第三方的 OpenJDK 下载网站 [Adoptium](https://adoptium.net/)，可以在上面很容易找到最友好的安装包。

当你登录网站的时候，网站会根据你当前使用的系统来自动推荐你可能要安装的版本。例如，当我使用 Mac 系统进入网站的时候，会自动推荐我 macOS 64位的 OpenJDK，并且有 8、11、16 三个长期支持版供下载，最终会以 pkg 包的方式被下载，直接双击安装即可。

![image-20210801180308510](https://hexo.moonkite.cn/blog/image-20210801180308510.png)

如果你是用的 Windows 系统，那对应的就会推荐你 Windows 系统的版本，文件是 msi 格式，仍然是直接双击安装即可。

![image-20210801181224397](https://hexo.moonkite.cn/blog/image-20210801181224397.png)



使用安装包安装的方式最简单，安装完什么都不用设置，直接就可以使用了。安装完成后，我们在命令窗口中，输入`java -version`可以查看 Java 的版本号，如果像下面这样显示，则表示安装正常了。

```shell
fengzheng$ java -version

java version "1.8.0_111"
Java(TM) SE Runtime Environment (build 1.8.0_111-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.111-b14, mixed mode)
```



### Hello World

然后就可以开始写第一个 Java 程序了，我们在随意一个目录新建一个 `Hello.java`的文件，并写下下面的代码。

```java
public class Hello {

    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

然后使用 `javac`命令编译上面的 `Hello.java`文件。进入 `Hello.java`所在的目录。

```bash
javac Hello.java
```

然后在当前目录会生成编译后的文件，名称为 `Hello.class`，这就是编译后的字节码文件。

运行此文件。不出意外的话，就会打印出 `Hello World`

```shell
java -classpath . Hello
```

到此 JDK 就安装完成了。



### 安装开发工具

JDK 安装好了，那我们写代码总不能用文本编辑器吧，选择一个好用的开发工具就很重要了。

一般 Java 开发的话，Eclipse 和 IDEA 二选一就可以了，以前是 Eclipse 用的人很多，现在是 IDEA 用的人多。我还是推荐你使用 IDEA 作为开发工具，真的非常好用。

[IDEA  官网下载](https://www.jetbrains.com/idea/download)，分为专业版和社区版，社区版是免费的。安装好之后，就可以开始正式 Java 开发之旅了。



