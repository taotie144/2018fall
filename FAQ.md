# FAQ 




- <a href="#1">`1. ssh/git相关`</a>
- <a href="#2">`2. HW相关`</a>
  - <a href="#2new">`new`</a>
- <a href="#3">`3. Lab相关`</a>
  - <a href="#3new">`new-尤其是Lab1-3相关的信息`</a>
- <a href="#4">`4. 其他系统/平台/环境等相关`</a>
- <a href="#5">`5. 课程资源`</a>
  - <a href="#5new">`new`</a>
- <a href="#6">`6. 目录结构`</a>
  - <a href="#6new">`new`</a>

 <a id="1"/>
 
## 1. ssh/git相关

1.1 服务器是否外网ip可以访问?
> 可以, 不限于校园网ip

1.2 把私钥弄丢了怎么办?
> 重新生成,发给助教

1.3.1 生成了公私钥之后,怎么ssh到服务器上的git?
> 可以配置~/.ssh/config文件,配置方式如:

``` text
Host pc
HostName 202.38.79.111
    User git
    Port 13022
    IdentityFile path/to/your/id_rsa
```

>或者

``` bash
eval $(ssh-agent -s)
ssh-add path/to/your/id_rsa
```

1.3.2 如果提示权限太open怎么办?
> 这个error指的是私钥的权限太open,不够安全, 可以用`ll`查看,用`chmod` 修改,一般`chmod 600`是推荐的权限.

1.3.3 如果要求填入下面这样的密码怎么办?

``` bash
git@202.38.79.111's password:
``` 

> 这个提示是让你填写我们服务器上的git用户的密码.说明你的公私钥的登录方式发生了错误,一般情况下是你的私钥没有配置正确.(极少数情况下是老师的公钥没配置正确).配置方式参照前两个问题.


1.3.4 对于助教反馈的`reply.md`,没有通过`git branch -r` 看到鸭?
> 记得先git pull.
> 对于git的用法,务必参考你们git库下面的REAMDME-git!!!!!!!

### ~~new~~ [10.10 updated.]

1.4 不能git add *吗?为什么?
> 如果没有配置gitignore的话,不建议这样做.
> add * means add all files in the current directory, except for files, whose name begin with a dot. This is your shell functionality and Git only ever receives a list of files.

<a id="2"/>

## 2. HW相关  

2.1 作业的程序有语言要求吗?

> 默认要求是C,但也可以在向老师/助教提供充分的说明(比如如何快速的编译,运行)的条件下,提交其他语言的程序.

2.2 第二个作业有程序的复杂度要求吗?
> 如果没有明确的要求,就没有要去.

2.3 词法分析那题的输入输出格式具体有什么要求
> 对于作业hw(而非实验lab),我们没有用自动化的测试工具进行测试.输入输出格式没有具体要求,向大家开放.大家可以自行设计.唯一的要求是将输入输出格式在说明文档,在这次是readme.md里面进行必要的说明,只要求语言人性化一点,助教可以马上看懂即可.

2.4 不同编译选项输出的汇编码要贴到answer吗?
> 可以不贴,但需要给出必要的描述.可以贴,但需要必要的注释,不建议大段的粘贴.

2.5 平时这种小实验是独立做了就满分吗?
> 嗯,但是会指出存在的问题.

2.6 提交到git的目录结构?
> 就是子目录下的`README.md`是写对目录里文件的使用，`answer.md`是写对作业中问题的回答和分析。写readme的目的是希望让你们养成在发布的文件夹上写说明的习惯

2.7 现在才给评价标准是不是晚了点?
> 我们的评价标准是根据第一次大家的提交发现的问题总结的.目的是为了让大家在之后的lab/hw提交中知道标准.

### ~~new~~ [9.21 updated.]

2.8 纸质作业交到哪里?什么时候交?
> 纸质作业交到讲桌旁边的白色小桌子上,截止日期当天上课前交.

### ~~new~~ [10.10 updated.]

2.9 说语言是否正规是什么意思啊，什么叫正规?
> "语言正规" -> "语言能用正规式表示"

2.10 HW4-1作业\epsilon是空集的意思吗?
> 是的

 <a id="2new"/>

### new [11.3 updated.]

2.11 作业19题 `F->F*|a|b` 的*是一个符号还是闭包?
> 就是终结符 *,还没到语义的层次.

2.12 怎么这几次作业分级了?分数怎么算?
> 作业评分分为了ABC三个等级，最后的分数是一样的，等级划分是为了更好地关心大家的学习情况.也希望各位同学认真对待平常的作业


<a id="3"/>

## 3. Lab相关

3.1 antlr用4.5行吗？因为想直接apt解决，apt里的最新版本是4.5.3?
> 严格按照文档要求来，之后实验批改是半自动的，不要因为版本问题给自己和助教找麻烦。

3.2 怎么确认装好了llvm？
> 可以写个简单的程序,用安装好的目录的clang编译一下.

3.3 lab1的ddl是什么时候?
> 老师没有明确给出ddl的实验,至少会在一周之后以后才截止.但是根据往年的经验,你做得越早,效果越好!

3.4 llvm打包错误是什么意思?
> 这个是去年助教的说法,我去问一下.[to be continued.]

3.5 能不能解释一下C1语言中Identifier,IntConst,FloatConst的自然语言定义？参考的文件打不开.
> 今年我们的C1是参照标准的C99进行修改的,参照的这个pdf文件,我们放在了qq群文件里.在这里建议大家学会科学上网.科大LUG(Linux User Group)是个分享技术的好平台,大家可以去交流/学习一下.

3.6 编译llvm的时候卡住是不是意味着又爆内存了?
> 这个可以通过top/htop等指令查看内存的使用情况.

3.7 执行antlr4指令之后提示 Error: Could not find or load main class org.antlr.v4.Tool什么意思?
> CLASSPATH变量没有配置好,或者配置好了,但是没有更新Shell,可以source sh, 或者重新打开该shell.
> 配置方式:把.jar文件本身的路径放到CLASSPATH里

### ~~new~~ [9.21 updated.]

3.8 '\\'除了注释中需要考虑吗?
> 不需要,我们在本次实验中只考虑注释中的'\\'.

3.9 ft_测试是要 lexer 报错退出吗?
> 可以报error,也可以是其他的识别错误的例子.测试样例不需要想的很复杂.这个我们的要求不是很严格,你言之有理即可.

3.10 整型常理忽略后缀的话，八进制不就包含在十进制的表达中了，都不用分那么细了吧?
> 并不,017是八进制,而且文法中0是八进制,二者并无重合.

3.11 ISO/IEC为什么没有提到负整型常量啊?
> 看文法.运算符.

3.12 虚拟机编译安装llvm时候 内存不足卡住怎么办?
> make -j1, 单线程占用的内存少.然后多分配内存.
> make -j的话,会按照你给虚拟机分配的cpu，自动多线程。多线程会占用更多的内存

3.13 请问下3e4这种应该被看做是int还是float啊？
> 看文法.

3.14 C1语言不用识别字符串的吗？
> 看文档.没有字符串这个类型.

3.15 请问token中没有预定义注释，我们是自己新建一个token吗？
> 注释是给人看的，编译器不需要注释，所以就就直接扔掉了. ('->skip')

3.16 关于注释中'\\'的其他问题?
> 不建议大家过度的考虑由于反斜杠导致错误情况，错误的测试用例应该根据同学们之前编写程序的经验去构造，而不是凭空的去构造。错误用例不再数量多少，关键是要能够反映出大家的思考。

3.17 像x=09这种这种问题，antlr会识别成0和9两个intconst，而不是报错，这种类型的错误是不是要留到语法的部分处理？
> 是的.

### ~~new~~ [10.10 updated.]

3.18 请问token中只有IntConst一个整常数，那所以八进制十进制十六进制都共用这一个token吗？
> 是的

3.19 /*没闭合要怎么做啊，是直接识别成除号和乘号吗?
> 是的.得等语法阶段处理.

3.20 lab1-2要看的论文放在哪里?
> [LL-star-PLDI11](http://www.antlr.org/papers/LL-star-PLDI11.pdf)
> [Adaptive LL(*) Parsing](https://dl.acm.org/ft_gateway.cfm?id=2660202&ftid=1506866&dwn=1&CFID=17892232&CFTOKEN=9d3af2ee44ada410-60234D49-93D0-37F6-F814006BAFD6CD54)

3.21 对于lab1-2的建议?
> 建议先用比C1更小的语言来实验、阅读论文并回答问题。对于Antlr的特征及机制理解，尽量用能反映特征的最小语言来实验。要结合生成的parser源码来理解

3.22 lab1-2可以引入其它的文法规则吗，比如C1Parser.g4原文件上没有的RelOp?
> 可以

3.23 GitCommit的评价标准是什么样的?
> commit message不能太短，然后没有提交无用文件

3.24 GitCommit的参考是怎样的呢?
> 参考的某同学的版本如下:
```
Date:   Mon Sep 24 16:46:57 2018 +0800
    [lab1-1] Add docs
Date:   Mon Sep 24 15:36:05 2018 +0800
    [lab1-1] Add many test cases
Date:   Mon Sep 24 15:21:40 2018 +0800
    [lab1-1] Fix LineComment (multi-line cases, v0.0.2)
Date:   Mon Sep 24 14:03:41 2018 +0800
    [lab1-1] Finish C1Lexer.g4 (v0.0.1)
Date:   Mon Sep 24 13:59:51 2018 +0800
    [lab1-1] Add lexer test scripts & simple test cases
Date:   Mon Sep 24 13:49:09 2018 +0800
    [lab1-1] Add c1recognizer skeleton
```

3.25 lab应该提交到哪个分支呢?
> master分支,但是这个规定也有一部分是因为我们的设计给大家带来的不必要的麻烦.后面应该不会每次多弄一个reply的分支了

3.26 E是不是0分鸭?
> 不一定，等级和分数的关系，应该期末才会确定(当然不会告诉你们，目的是不让你们把精力花在一分两分的计较上)

3.27 lab1-2的设计描述文件到底是放在doc下还是lab1-answer下?
> doc下,lab1-answer下只放3个问题的回答和可能有的相应的图片文件

3.28 tokens里面有notequal为什么测试要输出“!=”?
> 直接是字符串匹配(只有一个alternative)的token都是直接输出字符串

3.29 lab1-1的reply里的answer指的是?
> answer指的是lab1-1*.md文档内容评价

3.30 lab1-1的function部分的ABCDE等级划分标准是?
> 共25个测试用例，正确率100%为A，正确率每降低25%降一档

3.31 parser文件可以为了消除左递归改变生成规则吗，这样生成的树会不会不一样?
> 可以,会,但是parser的测试采用人工测试.

3.32 第二次评测1-1的提交是10/15吗?
> 是的.使用10月15号22:00前最后一次提交的版本进行检测

3.33 空在parser里怎么表达？
> 可以用问号,可以用 什么都不写,比如 a : ; 或者 a : | IntConst;

3.34 lab1-2的参考输出里面的EOF没有输出?
> 看antlr4的[官方parser rules](https://github.com/ANTLR/antlr4/blob/master/doc/parser-rules.md)

3.35 lab1-2的自动评测会要求语法树和预期输出一模一样吗?
> 不会.我们用人工检查.

3.36 话说markdown怎么在代码框中插入数学公式，$$好像不行?
> lqx同学:[Markdown中插入数学公式的方法]
(https://blog.csdn.net/xiahouzuoxin/article/details/26478179)

 <a id="3new"/>

### new [11.3 updated.]

3.37 LL(*)论文里面的predicate到底是什么东西?
> 翻译成语义断言（semantic predicate)）.两种断言都是用于产生式预测的，断言都是用host language实现的.

3.38 话说LL regular是什么呀?
> LL*里有LL regular文法的定义，做题应该是够用的

3.39 lyp:给大家推荐个工具画状态图，graphviz
> 赞👍

3.40 zzh:typora作为markdown编辑器画图也很棒,跨平台,支持各种状态图，流程图语法!
> 赞👍

3.41 那个，1-1第二次评分的话，那个push message的评分是怎么给的呢?
> 跟1-2一起push

3.42 1-3里说的对于项目文件组织的理解，是指c1recognizer这个目录下的文件还是build出的那些文件?
> c1recognizer这个目录下的文件

3.43 c1r_ref_(ubuntu/mac)怎么使用，是作为可执行文件直接执行吗？?
> 如果你有了依赖库,并且放在了lib的path下面,是可以的.

3.44 我运行不了，它告诉我缺少antlr runtime
> Libs_for_c1r_ref.zip群文件(也上传到了GitHub)是你们运行c1r_ref_(ubuntu/mac)的时候可能需要的动态库,可以ldd c1r_ref_(ubuntu/mac)然后看一下还缺哪些库(一般就只缺antlr的一个库),然后放在ldd(或者otool -L)输出结果中,那些已经有的库对应的目录下面(可以ln 过去)

3.45 1-3每次make的时候都很慢是为什么捏?
> 这是因为每次make的时候都会有为了更新外部依赖库而导致的不必要的网络请求.(比如你暂时没网还想做实验)
> 所以我们改了一下CMakeLists.txt.如果不想每次make的时候都update一下外部依赖库,就改用GitHub最新上传的CMakeLists.txt.执行cmake的参数不变

3.46 1-3的检查会如何进行?和1-2一样人眼检查还是严格的diff?
> 最后的检查将通过严格比较参考的二进制文件输出和你的输出来进行评测


3.47 1-3的实验没有头绪?
> 先参考我们给出的`syntax_tree_builder::visitExp`下面的各种注释指引.

3.48 a[5]={1,2}这种情况我们需要考虑并且在后面3个填充0吗？
> 不需要,我们这一步只是为了构造语法树.最后评测按照参考的二进制文件输出.

3.49 那个block_syntax里面怎么只有stmt_syntax啊?好像整个syntax tree.h里都没有decl那一片?
> var_def_stmt_syntax就够了,这里的数据结构的实现不需要和我们的理论的文法定义严格一致,只需要最后功能实现一致即可.这个实现的选择其实更利于实现.


3.50 std::bad_cast的错误指什么?antlrcpp::Any又是干嘛的?
> 这个问题可以从`syntax_tree_builder.cpp`的注释中得到解答.
```c++
// Returns antlrcpp::Any, which is constructable from any type.
// However, you should be sure you use the same type for packing and depacking the `Any` object.
// Or a std::bad_cast exception will rise.
// This function always returns an `Any` object containing a `expr_syntax *`.
antlrcpp::Any syntax_tree_builder::visitExp(C1Parser::ExpContext *ctx){
    ...
}
```

3.51 lab1-3中的ptr_list应该怎么赋值啊？用vector的方法push_back(visit(e).as<*_syntax>())报错说没有匹配的函数。
> 查看ptr_list的定义.参考`syntax_tree.h`(如果你配了vscode,那么可以通过快捷键直接查看定义)
``` c++
// Use unique postd::stringtype to reference stored objects
template <typename T>
using ptr = std::shared_ptr<T>;

// List of reference of type
template <typename T>
using ptr_list = std::vector<ptr<T>>;
```
> 参数外面再加一个ptr<T>()的类型转换(也可以这么叫...)即可.

3.52 std::shared_ptr是指针吗?干嘛的呢?
> std::shared_ptr是智能指针的一个,可以参考[这篇知乎回答](https://www.zhihu.com/question/20368881),可以暂时理解为为了更方便管理而对普通指针进行封装的新的类型.


3.53 对于c++的类型转换(static_cast,dynamic_cast)不太懂?
> 可以参考这篇博客[C++ 中static_cast、dynamic_cast总结](https://www.jianshu.com/p/5163a2678171)学习一下

3.54 而在我们的代码中,dynamic_cast在哪里用呢?
> 如果你的editor有IntelliSense,那么在C1Parser::BlockContext *ctx的成员中找到children,而这时你可能需要通过判断children这个std::vector<ParseTree *>的元素的具体类型,来判断这里是decl还是stmt.这时可以用下面这行代码进行判断.
```c++
//...
if (auto stmt = dynamic_cast<C1Parser::StmtContext *>(subtree)){}
//...
```

3.55 可是对于智能指针,向下转换时用dynamic_cast编译不能通过啊?
> 用`dynamic_pointer_cast`

<a id="4"/>

## 4. 其他系统/平台/环境等相关 

4.1 64位机器没办法运行32位的程序怎么办?
> wsl一般情况下只支持64位.ubuntu可以通过`apt-get install gcc-multilib`

4.2 linux可以查看xlsl文件？
> 可以.openoffice, soffice

4.3 `top`指令里的buff/cache是什么?
> 记得谷歌,谷歌之后,你会发现 [linux - What do the "buff/cache" and "avail mem" fields in top](https://unix.stackexchange.com/questions/390518/what-do-the-buff-cache-and-avail-mem-fields-in-top-mean) 这一条,然后发现:

``` text
[buffers]
    Memory used by kernel buffers (Buffers in /proc/meminfo)
[cache]
    Memory used by the page cache and slabs (Cached and  SReclaimable in /proc/meminfo)
[buff/cache]
    Sum of buffers and cache
```

### ~~new~~ [10.10 updated.]

4.4 llvm-build可以删掉吗？竟然有44.1GB?
> 其实可以在编译安装的时候选择release,并确定目标架构,这样就会占用很少的资源.但是我们建议大家用release,不确定目标架构,甚至安利debug,目的就是让大家体验一次比较大的工程的编译过程.

4.5 Wsl上是不是不能用grun -gui啊?
> 可以折腾wsl上的gui,但是这一阶段建议用mac或者完整的linux系统(而不是子系统)
<a id="5"/>

## 5. 课程资源 

5.1  bison-examples.zip解压缩不了?
> 通过快压可以.....

5.2 老师上课放的例子在主页的什么位置?
> 在bison-examples同一个[页面](<http://staff.ustc.edu.cn/~yuzhang/compiler/second/2017f.html>)下面,叫flex-examples.

### ~~new~~ [10.10 updated.]

5.3 web全称是?
> 计院方向课 -> [课程主页](http://staff.ustc.edu.cn/~jpq/courses/webinfo.html)

5.4 "lab1-1的九个维度上的评价标准"在哪里呀?在github上没找到
> https://github.com/ustc-compiler/2018fall/blob/master/labEvalStd(Reference).md

5.5 那么有什么好玩又有趣的编译相关的课外活动可以参加的吗?
# **有感兴趣在龙芯平台上开展编译器优化、JS引擎的垃圾收集优化的同学可以私信张老师!! 虽然大家对编译优化的知识还不太了解，但是可以通过具体的问题和平时的研讨与实战来领悟和提升。希望咱们能为构筑国家基础软硬件生态系统尽一份力。**

 <a id="5new"/>

### new [11.3 updated.]

5.6 请问习题课的ppt在哪里捏?ppt有错误咩??
> [老师主页](http://staff.ustc.edu.cn/~yuzhang/compiler/index.html)的schedule一栏上.具体链接为:
> - [TA1_H1](http://staff.ustc.edu.cn/~yuzhang/compiler/2018f/lectures/TA1-e.pdf)
> - [TA1_Lab1-1](http://staff.ustc.edu.cn/~yuzhang/compiler/2018f/lectures/TA1-p.pdf)
> - [TA2_H2-H6](http://staff.ustc.edu.cn/~yuzhang/compiler/2018f/lectures/TA2.pdf)

5.7 连接gitbook的时候提示:"您的链接不安全"怎么办?
> 这是因为gitbook的htpps暂时过期导致的,这种时候如果你信任这个网址的话,可以"添加信任",或者选择继续访问,针对浏览器的不同操作略有不同.




<a id="6"/>

## 6. 目录结构 

### 6.1 HW 目录结构

6.1.1 HW1
``` text
- <your repo>
  | H1
    | c
      | readme.md
      | *.c 
      | Makefile / *.sh
    | lexer
      | readme.md
      | *.c
      | Makefile / *.sh
    | answer.md
  ...
```

### 6.2 Lab 目录结构

6.2.1 Lab1-1
``` text
- <your repo>
  | c1recognizer              复制自公共仓库的 c1recognizer 项目，请勿遗漏内容。
    | cmake/
>>  | grammar/                修改其中的 C1Lexer.g4
    | include/c1recognizer/ 
    | src/
>>  | test/test_cases/lexer/  增加你的测试程序
>>  | doc/                    增加文档描述实验中遇到的问题、分析和设计，文件名前缀为lab1-1
    | 其他已有的文件
```

### ~~new~~ [10.10 updated.]
6.2.2 Lab1-2
``` text
- <your repo>
  | lab1-answer
    | lab1-2.*           回答lab1-2的问题1--问题3
    | 其他被引用图像文件
  | c1recognizer         复制自公共仓库的 c1recognizer 项目。请勿遗漏内容。
    | cmake/
>>  | grammar/           修改其中的 C1Parser.g4
    | include/c1recognizer/ 
    | src/
>>  | test/test_cases/   补充你的测试程序
>>  | doc/               增加文档描述实验中遇到的问题、分析和设计,文件名前缀为lab1-2.
    | 其他已有的文件
```

 <a id="6new"/>

### new [11.3 updated.]
6.2.2 Lab1-3
``` text

- <your repo>
  | lab1-answer
    | lab1-2.*
>>  | lab1-3.md          回答Lab1-3的问题
  | c1recognizer         复制自公共仓库的 c1recognizer 项目，请勿遗漏内容。
    | cmake/
    | grammar/           
    | include/c1recognizer/ 
>>  | src/                 修改完善recognizer.cpp和syntax_tree_builder.cpp
>>  | test/test_cases/   如果有更多的测试程序，可以在其中补充
>>  | doc/               增加lab1-3.md记录主要任务一节要求的内容
    | 其他已有的文件
```