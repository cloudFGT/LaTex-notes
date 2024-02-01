







# 0.如何熟练使用LaTeX
1. 多使用，用的越多，使用越熟练
2. 到GitHub借鉴别人的代码
3. 参考LaTeX相关书籍<font color ="#ff7f50" size="3">（LaTeX入门书籍在onedrive）</font>
4. 参考别人的模板
使用LaTeX实现特别的功能--->[stackchange网址](https://www.tex.stackchange.com/)






# 1.公式识别工具及相关网站
==公式识别==

- <font color ="#ff7f50" >quicker插件</font>
- <font color ="#ff7f50" >mathematica</font>
- <font color ="#ff7f50" >axmath</font>

3个都可以把数学公式翻译成LaTeX代码，前提是要使用<font color ="#ff7f50" >对应的数学包</font>

==在线相关网站==

1. [在线生成表格及公式输出](https://www.tablesgenerator.com) `https://www.tablesgenerator.com`
2. [在线绘图网站mathcha](https://www.mathcha.io)   `https://www.mathcha.io`  <font color ="#00bfff" size="5">(有离线版软件)</font>
3. [公式输出](https://www.latexlive.com)  `https://www.latexlive.com`
4. [latex模板网站](https://www.latextemplates.com) `https://www.latextemplates.com`
5. [latex模板网站](https://www.latexstudio.net) `https://www.latexstudio.net`
6. [latex在线编辑网站](https://www.overleaf.com) `https://www.onerleaf.com`<font color ="#00bfff" size="5">（需要科学上网）</font>






# 2.与LaTeX相关的其他工具
<font color ="#ff7f50" size="4">LaTeX中插入数学绘图和公式</font>

- 使用mathcha
- 使用axglyph
- 使用mathematica
- 使用matlab
- 使用python

<font color ="#ff7f50" size="4">LaTeX编辑器及编译器</font>
- texmacs<font color ="#00ff00" size="4">（编辑器）（不需要写代码，类似word）</font>
- winedit<font color ="#00ff00" size="4">（编辑器）</font>
- tex works<font color ="#00ff00" size="4">（编辑器）</font>
- texstudio<font color ="#00ff00" size="4">（编辑器）</font>
- texlive<font color ="#00ff00" size="4">（编译器）</font>



<font color ="#ff887a" size="4">未来的世界</font>





# 3.LaTeX相关问题及使用技巧

| 问题             | 说明                       |
| ---------------- | -------------------------- |
| ==换行==         | 在段落末尾添加2个  '\\'    |
| ==换段==         | 在段落末尾添加   \par      |
| ==添加新的一页== | 使用\newpage               |
| ==公式大小统一== | \$\displaystyle{你的公式}$ |
| ==生成目录==     |                            |
|                  |                            |
|                  |                            |
|                  |                            |











| 文档类型    | 备注                                       |
| :---------- | ------------------------------------------ |
| ==article== | 排版科技期刊、短报告、程序文档、邀请函等   |
| ==report==  | 排版多章节的长报告、短篇的书籍、博士论文等 |
| ==book==    | 排版书籍                                   |
| ==slides==  | 排版幻灯片                                 |





# 4.制作LaTeX模板







# 5.初级语法
$LaTex$模板代码
```latex
%导言区
\documentclass{article}  % 还可输入report,book,letter等
\usepackage[UTF8]{ctex}  % 使用宏包，使LaTeX支持中文
% 设置页面的环境,a4纸张大小，左右上下边距信息
\usepackage[a4paper,left=10mm,right=10mm,top=15mm,bottom=15mm]{geometry}

\title{标题}      %  文章标题
\author{作者名}   %  作者的名称
\date{\today}    %  当天日期

%正文区
\begin{document}
\maketitle       % 显示标题等信息
% 这部分可输入文章内容
\end{document}


```



### 文档格式
我们可以通过命令`\documentclass[options]{class}`来设置文档格式，其中options表示文档属性，class表示文档类型。

#### 文档类型
| 文档类型                                                  | 备注                                       |
| --------------------------------------------------------- | ------------------------------------------ |
| <table><tr><td bgcolor=#7fff00>article </td></tr></table> | 排版科技期刊、短报告、程序文档、邀请函等   |
| <table><tr><td bgcolor=#7fff00>report</td></tr></table>   | 排版多章节的长报告、短篇的书籍、博士论文等 |
| <table><tr><td bgcolor=#7fff00>book</td></tr></table>     | 排版书籍                                   |
| <table><tr><td bgcolor=#7fff00>slides</td></tr></table>   | 排版幻灯片                                 |











#### 文档属性
| 文档类型                                                     | 备注                                |
| ------------------------------------------------------------ | ----------------------------------- |
| <table><tr><td bgcolor=#7fff00>字体大小</td></tr></table>    | 10pt,11pt,12pt                      |
| <table><tr><td bgcolor=#7fff00>纸张大小</td></tr></table>    | a4paper,letterpaper...              |
| <table><tr><td bgcolor=#7fff00>公式对齐</td></tr></table>    | fleqn(左对齐),leqno(编号防置于左侧) |
| <table><tr><td bgcolor=#7fff00>标题页</td></tr></table>      | titlepage,notitlepage               |
| <table><tr><td bgcolor=#7fff00> 单双列排版</td></tr></table> | onecolumn,twocolumn                 |
| <table><tr><td bgcolor=#7fff00>单双面格式</td></tr></table>  | oneside,twoside                     |

### 宏包
LaTeX导言区可导入各种宏包，一个语句中可导入多个宏包，宏包间用逗号隔开即可。导入宏包时，可使用命令`\usepackage{ }`

| 文档类型                                                     | 备注         |
| ------------------------------------------------------------ | ------------ |
| <table><tr><td bgcolor=#7fff00>ctex</td></tr></table>        | 中文支持     |
| <table><tr><td bgcolor=#7fff00>amsmath</td></tr></table>     | 数学公式支持 |
| <table><tr><td bgcolor=#7fff00>algorithm,algorithmic</td></tr></table> | 算法排版     |
| <table><tr><td bgcolor=#7fff00>listings</td></tr></table>    | 插入代码块   |




### 注释
<table><tr><td bgcolor=#ffff00>单行注释</td></tr></table>

```text
% 注释内容
```

<table><tr><td bgcolor=#ffff00>多行注释</td></tr></table>

```text
\iffalse
注释内容
\fi
```



### 英文引号
<font color ="#ff7f50" size="4">要想正确输入英文引号，把左侧的引号用  代替即可，如下：</font>
```text
`English'
``English"
```


### 空格
| 命令                                                    | 说明           |
| ------------------------------------------------------- | -------------- |
| <table><tr><td bgcolor=#7fff00>\quad</td></tr></table>  | 空一个中文字符 |
| <table><tr><td bgcolor=#7fff00>\qquad</td></tr></table> | 空两个中文字符 |


### 换行&换段
| 命令                                                  | 说明                                 |
| ----------------------------------------------------- | ------------------------------------ |
| <table><tr><td bgcolor=#7fff00>换行</td></tr></table> | 在段落末尾添加`\\`  或者`\\[offset]` |
| <table><tr><td bgcolor=#7fff00>换段</td></tr></table> | \par                                 |

### 新页
使⽤ `\newpage` 进⾏换⻚，⼀般在⼀⻚的最后写

### 转义字符
我们可以使⽤` \+字符` 来表示转义字符，例如输⼊命令 `\%` ，表示`%`，否则会显示出 \



### 可选参数
LaTeX插⼊图⽚、表格等元素时，第⼀⾏后⾯有⼀个可选参数[htbp]，例 如，`\begin{figure}[htbp] ` 。

| 参数      | 说明                                                         |
| --------- | ------------------------------------------------------------ |
| h(here)   | <table><tr><td bgcolor=#ff887a>放置在当前位置</td></tr></table> |
| t(top)    | <table><tr><td bgcolor=#ff887a>放置在⻚⾯顶部</td></tr></table> |
| b(bottom) | <table><tr><td bgcolor=#ff887a>放置在⻚⾯底部</td></tr></table> |
| p(page)   | <table><tr><td bgcolor=#ff887a>放置在浮动⻚上</td></tr></table> |




### 基本语句
==\textbf{}：==
文本环境加粗。在数学环境使用的话，会使斜体效果消失。并且无法输出加粗的希腊字母。  
==\mathbf{}：==
会变为粗体，但同样会导致数学字母斜体形式的丢失。  
==\boldmath{}：==
数学环境里可以加粗且不会使斜体消失。需要添加amsmath宏包。  
==\boldsymbol{}：==
可以对希腊字母加粗，需要添加amsmath宏包。  
```ad-important

在数学环境中，比较推荐的方式是添加宏包\usepackage{bm}, 使用\bm{}命令加粗。

但是在xelatex或Luatex引擎的unicode-math环境中中，\bm{}会报错。此时，可以使用以下命令：

==\symbfit{}==：加粗，且有斜体效果  

==\symbf{}==：加粗，没有斜体效果  

==\mathbfcal{}==：加粗的\mathcal字体

```







## 5.2进阶语法

### 专属文件夹的设置
<b><font color ="#ea3a66" size="3">把所有相关的tex文档、图片、PDF放进一个文件夹中</font></b>

### 纸张布局
```latex
% 设置⻚⾯的环境,a4纸张⼤⼩，左右上下边距信息 
\usepackage[a4paper,left=10mm,right=10mm,top=15mm,bottom=15mm]{geometry}
```


### 标题级别
```latex
\section{⼀级标题} 
\subsection{⼆级标题} 
\subsubsection{三级标题}
```



### 摘要
在`\maketitle` 后输⼊以下命令即可填⼊摘要内容
```latex
\maketitle 
\begin{abstract}
%在此输⼊摘要内容
\end{abstract}
```



### 标题、作者、时间
若在引⾔区设置了标题、作者、时间，⼀定要在正⽂区中`\begin{document}` 后⼀⾏输⼊命令`\maketitle`  ，这样才能显示出标题、作者、时间。



### 引用、脚注
<b><font color ="#ea3a66" size="3">引用：</font></b>写在 `\begin{quote}` 和 `\end{quote}` 之间。
<b><font color ="#ea3a66" size="3">脚注：</font></b>在需要添加脚注的⽂字后添加 `\footnote{内容}` 即可

```latex
%示例
⻄游记\footnote{中国古典四⼤名著之⼀}⼩说开头写道：
\begin{quote}
{\kaishu 东胜神洲有⼀花果⼭，⼭顶⼀⽯，受⽇⽉精华，⽣出⼀⽯猴。之后因为成功闯⼊⽔帘洞，被花果⼭诸猴拜为“美猴王”。} \end{quote}
```







### 目录



### 架构
```latex

\documentclass{article} % article ⽂档
\usepackage[UTF8]{ctex}  % 使⽤宏包(为了能够显示汉字)
% 设置⻚⾯的环境,a4纸张⼤⼩，左右上下边距信息 
\usepackage[a4paper,left=10mm,right=10mm,top=15mm,bottom=15mm]{geometry

\title{标题}       % ⽂章标题
\author{作者名称}   % 作者的名称
\date{\today}      % 当天⽇期

% 正⽂开始 
\begin{document}
\maketitle          % 添加这⼀句才能够显示标题等信息

% ⽣成⽬录设置 
\renewcommand{\contentsname}{⽬录} 
%将content转为⽬录
\tableofcontents 
% 摘要开始部分
\begin{abstract} 
该部分内容是放置摘要信息的。 
\end{abstract}
\section{⼀级标题1} 第⼀段⼀级标题下的内容。\par %\par表示换段，也可直接段落间空⾏ 第⼆段⼀级标题下的内容。
\subsection{⼆级标题1.1} ⼆级标题下的内容。 
\subsubsection{三级标题下的内容1.1.1} 三级标题下的内容。 

\section{⼀级标题2} ⼀级标题2中的内容 

% 正⽂结束
\end{document}

```



### 章节标题的⾃定义设置
我们可以通过命令`\ctexset{}`  来实现对章节标题的⾃定义设置，其中{ }内可填⼊相 应的参数。

```latex
\documentclass{ctexart} %ctexbook,ctexrep 
\title{\zihao{3} \LaTeX{}章节标题设置} \author{\zihao{-4} 作者名} 
\date{\zihao{-4} \today



\pagestyle{plain}%⻚眉为空，⻚脚为⻚码
%=================设置章节标题格式==================
\ctexset{
section={
%format⽤于设置章节标题全局格式，作⽤域为标题和编号
%字号为⼩三，字体为⿊体，左对⻬
%+号表示在原有格式下附加格式命令
format+ = \zihao{-3} \heiti \raggedright,
%name⽤于设置章节编号前后的词语
%前、后词语⽤英⽂状态下,分开
%如果没有前或后词语可以不填
name = {,、},
%number⽤于设置章节编号数字输出格式
%输出section编号为中⽂
number = \chinese{section},
%beforeskip⽤于设置章节标题前的垂直间距
%ex为当前字号下字⺟x的⾼度
%基础⾼度为1.0ex，可以伸展到1.2ex，也可以收缩到0.8ex
beforeskip = 1.0ex plus 0.2ex minus .2ex,
%afterskip⽤于设置章节标题后的垂直间距
afterskip = 1.0ex plus 0.2ex minus .2ex,
%aftername⽤于控制编号和标题之间的格式
%\hspace⽤于增加⽔平间距
aftername = \hspace{0pt}
},
subsection={
format+ = \zihao{4} \kaishu \raggedright,
%仅输出subsection编号且为中⽂
number = \chinese{subsection},
name = {（,）},
beforeskip = 1.0ex plus 0.2ex minus .2ex,
afterskip = 1.0ex plus 0.2ex minus .2ex,
aftername = \hspace{0pt}
},
subsubsection={
%设置对⻬⽅式为居中对⻬
format+ = \zihao{-4} \fangsong \centering,
%仅输出subsubsection编号，格式为阿拉伯数字，打字机字体
number = \ttfamily\arabic{subsubsection},
name = {,.},
beforeskip = 1.0ex plus 0.2ex minus .2ex,

afterskip = 1.0ex plus 0.2ex minus .2ex,
aftername = \hspace{0pt}
}
}
\begin{document}
\maketitle
%测试⼿动设置章节标题格式
\section{引⾔}
\centering 你好，\LaTeX{}!
\section{实验⽅法}
\section{实验结果}
\subsection{数据}
\subsection{图表}
\subsubsection{实验条件}
\subsubsection{实验过程}
\subsection{结果分析}
\section{结论}
\section{致谢}
\end{document}


```







### 字体设置
#### 字体族设置
| 字体族     | 字体命令    | 字体声明      | 备注                           |
| ---------- | ----------- | ------------- | ------------------------------ |
| 罗马字体   | `\textrm{}` | `{\rmfamily}` | 笔画起始处有装饰               |
| 无衬线字体 | `\textsf{}` | `{\sffamily}` | 笔画起始处无装饰               |
| 打字机字体 | `\texttt{}` | `{\ttfamily}` | 每个字符宽度相同，又称等宽字体 |










#### 字体系列设置
#### 字体形状设置
#### 中文字体设置
#### 字体大小设置
#### 字体颜色设置






### 特殊公式
### 画图
### 表格
### 版面设计





































