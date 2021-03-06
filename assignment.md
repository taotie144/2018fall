# Assignments

对网络提交（包括Git仓库和发送至助教）的作业，截止时间统一为所述日期22时整。

对纸质提交的作业，截止时间统一为所述日期课前。


| Date       | Homework          | Project                                  | HW Due        | Proj Due   |
| :--------- | :---------------- | :--------------------------------------- | :------------ | :--------- |
| 11.8, Thu |      | [Lab2-1](https://clarazhang.gitbooks.io/compiler-f2018/content/llvmIRGen.html#211-lab2-1预热实验)| | 11.19, Mon    | 
| 11.5, Mon | [H8-1](#h8-1)     | | 11.12, Mon    | |
| 10.25, Mon | [H7-2](#h7-2)     | [Lab1-3](https://clarazhang.gitbooks.io/compiler-f2018/content/parser.html#lab1-3-生成-ast-的-c1-解析器) | 10.29, Mon    | 11.12, Mon  |
| 10.22, Mon | [H7-1](#h7-1)     |                                          | 10.29, Mon    |            |
| 10.18, Thu | [H6-2](#h6-2)     |                                          | 10.22, Mon    |            |
| 10.15, Mon | [H6-1](#h6-1)     |                                          | 10.22, Mon    |            |
| 10.11, Thu | [H5](#h5)         | [Lab1-2](https://clarazhang.gitbooks.io/compiler-f2018/content/parser.html#Lab1-2-c1-的语法分析) | 10.15, Mon    | 10.15, Mon |
| 10.8, Mon  |                   | [Lab1-2](https://clarazhang.gitbooks.io/compiler-f2018/content/parser.html#Lab1-2-c1-的语法分析) |               | 10.15, Mon |
| 9.29, Sat  | [H4-2](#h4-2)     | [Lab1-2](https://clarazhang.gitbooks.io/compiler-f2018/content/parser.html#Lab1-2-c1-的语法分析) | 10.8, Mon     | 10.15, Mon |
| 9.27, Thu  | [H4-1](#h4-1)     |                                          | 10.8, Mon     | -          |
| 9.20, Thu  | [H3-2](#h3-1)     | [Lab1-1](https://clarazhang.gitbooks.io/compiler-f2018/content/parser.html) | 9.27, Thu     | 9.24, Mon  |
| 9.17, Mon  | [H3-1](#h3-1)     | [Lab1-1](https://clarazhang.gitbooks.io/compiler-f2018/content/parser.html) | 9.27, Thu     | 9.24, Mon  |
| 9.13, Thu  | ~~[H2-2](#h2-2)~~ | [Environment](https://clarazhang.gitbooks.io/compiler-f2018/content/environment.html) | ~~9.17, Mon~~ | -          |
| 9.10, Mon  | [H2-1](#h2-1)     | None                                     | 9.17, Mon     | -          |
| 9.6, Thu   | [H1](#h1)         | None                                     | 9.9, Sun      | -          |
| 9.3, Mon   | [H0](#h0)         | None                                     | 9.6, Thu      | -          |

## 习题课课件


## Homework

### H0

使用`ssh-keygen`生成公私钥，并将公钥发送至助教张宇翔。命名应为`名的全拼-姓的全拼.pub`(名和姓的全拼均小写)，请按照自己的姓名修改文件名。

### H1
**
本次作业请在git仓库中`HW/H1`中添加文件`answer.md`并附上**源程序文件**以及编译和运行程序的 `Makefile` 文件或**shell脚本**来回答问题。

1. 安装一个具备完善GNU工具链的环境，如任意Linux发行版/Windows Subsystem for Linux/MacOS（至少你要一个brew）；

2. 在你安装的环境下，练习使用GCC/Clang，结合使用-E（预处理器，结果大致阅读了解，在作业中指出做了哪些类型的变换）、-S、-c、-o、-m32/64参数，观察程序编译后输出的代码。请：
  - 在`HW/H1/c`中添加你的源程序、`Makefile`、shell脚本等
  - 在`HW/H1/c`中添加`readme.md`中说明该目录下的文件及子目录和使用方式
  - 在`HW/H1/answer.md`中回答本题，指出你的源代码在`HW/H1`中的位置、不同编译选项下输出的汇编码，并对汇编码加注释
    - **注释**至少要说明不同汇编命令的含义、源程序中的变量以及中间结果在汇编码中的对应

3. 根据[课件](http://staff.ustc.edu.cn/~yuzhang/compiler/2017f/lectures/lexicalAnalysis.pdf)第16页的NFA，手工编写能识别输入串中多个满足NFA的记号的词法分析程序，写出<==><、a<=b的识别过程。**注意**：非关系运算符识别输出为other。**高级要求**：能输出每个记号对应在字符流中的起止位置。请：
  - 将源代码、`Makefile`、shell脚本等存档在在`HW/H1/lexer`目录中
  - 在`HW/H1/lexer`中添加`readme.md`中说明该目录下的文件及子目录和使用方式（包括Building和Usage）
  - 在`HW/H1/answer.md`中给出在做这一题的主要考虑、问题以及解答
  - 关于**编程语言**，默认是C语言。希望学生在提交作业时不要把检查者当成专家，要提供脚本和说明，告诉检查者怎么快速编译运行你写的程序以及程序中的要点


**注意**

- 临时文件和编译生成的目标文件、可执行程序不要提交到库中。
- `.md`是现在最常用的简单样式说明用途的文本格式之一Markdown的后缀名，你们应大致了解Markdown的排版方式，以合理的形式展现代码。关于Markdown的使用可以参考[GitHub Guide: Mastering Markdown](https://guides.github.com/features/mastering-markdown)，你也可以自行查找一些资料来了解这一Markup Language的使用方式。
- 自行查找 Makefile 文件的编写，也可以参考 [bison-examples](http://staff.ustc.edu.cn/~yuzhang/compiler/proj/bison-examples.zip) 中的 Makefile
- 评价标准见 [github](https://github.com/ustc-compiler/2018fall/blob/master/hwevalstd.xlsx)

### H2-1
Book 2.3\(c\), 2.4\(c\)\(e\), 2.7\(c\) （注: 手工构造NFA和DFA, 用算法将NFA变换成DFA，再构造最简的DFA）

### ~~H2-2~~
~~Book 3.2~~

### H3-1
Book 3.2 

```
3.2 考虑文法
S --> aSbS | bSaS | \epsilon
(a) 为句子abab构造两个不同的最左推导，以此说明该文法是二义的。
(b) 为abab构造对应的最右推导。
(c) 为abab构造对应的分析树。
(d) 这个文法产生的语言是什么？
```
### H3-2
Book 3.4 3.6(d), (f)a的个数比b的个数多的串  3.8(a) 

```
3.4 文法
    R --> R '|' R | R R | R | ( R ) | a | b
产生字母表{a, b}上所有不含 \epsilon 的正规式。注意，第一条竖线加了引号，它是正规式的或运算符号，而不是文法产生式右部各选择之间的分隔符，另外在这儿是一个普通的终结符。该文法是二义的。
(a) 证明该文法产生字母表{a, b}上的所有正规式。
(b) 为该文法写一个等价的非二义文法。它给予算符、连接和 | 的优先级和结合性同2.2节中定义的一致。
(c) 按上面两个文法构造句子ab | ba的分析树。

3.6  为字母表\Sigma = {a, b}上的下列每个语言设计一个文法，其中哪些语言是正规的？
(d) 不含abb作为子串的所有串。
(f) a的个数比b的个数多的串。

3.8  (a) 消除习题3.1文法的左递归。
注：习题3.1的文法如下
  S --> (L) | a     L --> L,S | S
```

### H4-1
Book 3.12

```
3.12 下面的文法是否为 LL(1)文法?说明理由。
S --> A B | P Q x	A --> x y	B --> b c
P --> d P | \epsilon	Q --> a Q | \epsilon
```

### H4-2
- Book 3.11

```
3.11 构造下面文法的 LL(1)分析表。
S --> a B S | b A S | \epsilon
A --> b A A | a
B --> a B B | b
```
- 阅读并理解 [PL/0编译器](http://staff.ustc.edu.cn/~yuzhang/compiler/2012s/pl0.zip) ([PL/0说明文档](http://staff.ustc.edu.cn/~yuzhang/compiler/old_pl0project.pdf))， 叙述PL/0编译器中test函数的作用及它的三个参数的含义, 并举例说明第二个参数带来的好处和引起的问题。

### H5
Book 3.19  3.20

```
3.19 考虑下面的文法
E --> E + T | T
T --> T F | F
F --> F* | a | b
(a) 为此文法构造SLR分析表。
(b) 为此文法构造LALR分析表。

3.20 证明下面的文法
	S --> S A | A
	A --> a
是SLR(1)文法，但不是LL(1)文法。
```

### H6-1
Book 3.27  3.31  3.33  3.37

```
3.27 文法G的产生式如下：
    S --> I | R	    I --> d | I d 	R --> WpF
    W --> Wd | \epsilon     F --> F d | d
(a) 令d表示任意数字，p表示十进制小数点，那么非终结符S, I, R, W和F在编程语言中分别表示什么？
(b) 该文法是LR(1 )文法吗？为什么？

3.31 下面两个文法中哪一个不是LR(1)文法？对非LR(1)的那个文法，给出那个有移进‑归约冲突的规范的LR(1)项目集。
    S --> a A c			S --> a A c
    A --> A b b | b		A --> b A b | b

3.33 为语言
    L = {a^{m}b^{n} | 0<= m <= 2n}（即a的个数不超过b的个数的两倍）
写三个文法，它们分别是LR(1)的、二义的和非二义且非LR(1)的。
注： a^{m}b^{n} 为在latex中的公式表示方法，表示m个a后跟n个b

3.37 下面是一个二义文法
    S --> AS | b
    A --> S A | a
如果为该文法构造LR分析表，则一定存在某些有分析动作冲突的条目，它们是哪些？假定分析表这样来使用：出现冲突时，不确定地选择一个可能的动作。给出对于输入abab所有可能的动作序列。
```
### H6-2
Book 4.3

```
4.3 为文法
    S --> ( L ) | a
    L --> L , S | S
(a) 写一个语法制导定义，它输出括号的对数。
(b) 写一个语法制导定义，它输出括号嵌套的最大深度。
```

### H7-1
Book 4.12(b) 并写出相应的语法制导定义、预测翻译器

```
4.12 为文法
    S --> ( L ) | a
    L --> L , S | S
(b) 分别写出相应的语法制导定义、翻译方案以及预测翻译器，它打印出每个a在句子中是第几个字符。例如，当句子是(a,(a,(a,a),(a)))时，打印的结果是 2  5  8  10  14。
```

### H7-2
Book 4.12(b) 写出自下而上分析的栈操作代码

### H8-1
Book 5.7 5.12 5.15 5.17

```
5.7 下列文法定义字面常量表的表。符号的解释和图5.2文法的那些相同，增加了类型list，它表示类型T的元素表；增加了nil，表示空表，其元素可以是任何类型。
  P --> D; E
  D --> D; D | id : T
  T --> list of T | char | integer
  E --> (L) | literal | num | id | nil
  L --> E, L | E
写一个类似5.3节中的翻译方案，以确定表达式(E )和表(L)的类型。

5.12 拓展5.3.3节的类型检查，使之能包含记录。有关记录部分的类型和记录域引用表达式的语法如下：
  T --> record fields end
  fields --> fields; field | field
  field --> id : T
  E --> E.id

5.15 找出下列表达式的最一般的合一代换：
(a) (pointer (\alpha)) x (\beta --> \gamma )
(b) \beta X (\gamma --> \delta )
如果(b)的\delta 是\alpha 呢？

5.17 效仿例5.5，推导下面map的多态类型：
map : \forall \alpha. \forall \beta. ( (\alpha-->\beta)x list(\alpha)) --> list (\beta)
map的ML定义是
  fun map (f, l ) =
    if null (l ) then nil
    else cons (f (hd (l)), map (f, tl (l ) ) );
在这个函数体中，内部定义的标识符的类型是：
  null : \forall \alpha.list(\alpha) --> boolean;
  nil : \forall \alpha.list(\alpha);
  cons : \forall \alpha.(\alpha x list(\alpha)) --> list(\alpha);
  hd : \forall \alpha.list(\alpha) \alpha;
  tl : \forall \alpha. list(\alpha) --> list(\alpha);
```
