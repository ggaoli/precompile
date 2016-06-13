# CSS预编译
---
## 为什么要学习css预编译
CSS入门简单，深入就比较难，虽然样式简单，但难以维护。需要考虑大量的样式，覆盖、权重和很多!important。
## 什么是 css预处理器

CSS预处理器定义了一种新的语言，其基本思想是，用一种专门的编程语言，为CSS增加了一些编程的特性，将CSS作为目标生成文件，然后开发者就只要使用这种语言进行编码工作。通俗的说，CSS预处理器用一种专门的编程语言，进行Web页面样式设计，然后再编译成正常的CSS文件，以供项目使用。CSS预处理器为CSS增加一些编程的特性，无需考虑浏览器的兼容性问题，例如你可以在CSS中使用变量、简单的逻辑程序、函数等等在编程语言中的一些基本特性，可以让你的CSS更加简洁、适应性更强、可读性更佳，更易于代码的维护等诸多好处。

## css预处理器语言
现今市面上主要有 `Sass`、`Less`、`Stylus` 这三类预处理器语言。

###1、背景介绍
- Sass背景介绍
>Sass是对CSS的语法的一种扩充，诞生于2007年，最早也是最成熟的一款CSS预处理器语言，它可以使用变量、常量、嵌套、混入、函数等功能，可以更有效有弹性的写出CSS。Sass最后还是会编译出合法的CSS让浏览器使用，也就是说它本身的语法并不太容易让浏览器识别，因为它不是标准的CSS格式，在它的语法内部可以使用动态变量等，所以它更像一种极简单的动态语言。
注：Sass官网地址：[http://sass-lang.com][1]

- Less背景介绍
>2009年开源的一个项目，受Sass的影响较大，但又使用CSS的语法，让大部分开发者和设计师更容易上手。
注：LESS的官网：[http://lesscss.org][2]

- Stylus背景介绍
> Stylus，2010年产生，来自于Node.js社区，主要用来给Node项目进行CSS预处理支持，不过Stylus的人气相对于Sass和Less则逊色很多。

注：Stylus官网：[http://learnboost.github.com/stylus][3]
###2、Sass和Less对比

> * 实现方式
Less是基于JavaScript引擎，需要在客户端处理的。<br>
Sass是基于Ruby环境，是在服务器端处理的。<br>
相比之下less环境相对Sass简单
注：很多开发者不会选择LESS因为JavaScript引擎需要额外的时间来处理代码然后输出修改过的CSS到浏览器。关于这个有很多种方式，我选择的是只在开发环节使用LESS。
> * 使用率(热度)
国内前端团队使用LESS的同学会略多于Sass
国外则普遍使用Sass,热度高
> * 功能
Sass较Less略强大一些
> * 已有成熟框架对比
Sass在市面上有一些成熟的框架，比如说`Compass`，而且有很多框架也在使用Sass，比如说Foundation，bootstrap也开始使用sass

###3、Sass和Less语法对比

##Sass入门
###Sass环境安装
 编写scss代码，通过sass的工作引擎编译成css代码，最后的部署阶段，其实部署的是生成的css代码，从这个流程可以看出sass并不是万金流，使用命令行也好，使用服务端集成框架也好，使用图形用户界面工具也好，最关键的环节是输入css，从这里也可表现出sass就是帮助我们更快的写出具有高可维护性的css代码
- Koala
koala 是一款桌面程序，支持 less 、 sass 、 coffeescript 即时编译，帮助 web 开发者更高效地使用 less 、 sass 、 coffeescript 开发。
下载： [http://koala-app.com/index-zh.html][4]
- 命令操作
1.安装ruby环境 官网地址：[http://www.ruby-lang.org/en/][5]
2.更改ruby包的sources
   - gem sources --remove https://rubygems.org/
   - gem sources --add https://ruby.taobao.org/（如果你系统不支持https，请将淘宝源更换成：gem sources -a http://gems.ruby-china.org）
   - gem install sass
   - gem update(更新ruby程序)
   - gem install sass --vertion=3.3
   - gem list (列出本地安装的所有ruby程序包)
   - gem uninstall sass --vertion=3.3.0(删除相应的程序包)


###Sass调试
> 1.Koala上点击相应的文件，然后就会出现右边的编译选项，即可选择是否开启source map，debug info <br>
> 2.打开Chrome浏览器，F12打开调试面板，点击调试面板右上角的齿轮图标打开设置，在general选项中勾选Enable CSS source map 和 Auto-reload generated CSS<br>
> 3.开启--sourcemap编译，f12打开调试面板，就可以看到原先右边的css文件变成了我们现在的scss文件<br>
> 4.点击scss文件，会跳到source里面的scss源文件，现在可以在里面进行修改，修改完成后可以右键选择save或save as命令，然后替换我们本地的scss源文件，刷新chrome就可以看到变化（注意，解析样式需要一定时间）。以后只要ctrl+s保存修改就可以在浏览器中看到修改效果了。













  [1]: http://sass-lang.com
  [2]: http://lesscss.org
  [3]: http://learnboost.github.com/stylus
  [4]: http://koala-app.com/index-zh.html
  [5]: http://www.ruby-lang.org/en/
