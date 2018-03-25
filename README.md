# iecas-thesis

=======================================

## 说明

本项目初始fork的github上莫晃锐写的最新的国科大论文模版[ucasthesis](https://github.com/mohuangrui/ucasthesis)，在此基础上，针对中科院电子所的学位论文特点，做了些修改。形成适用于电子所学位论文的模版iecas-thesis.



因莫晃锐的模板在2018年3月13日进行了显著改动，如果之前使用旧模版，建议的更新方式为`移植你的旧有文件到新模板中`:



        1. 下载解压新模板
        2. 替换 Tex 文件夹中的除 Frontpage.tex 以外的文件
        3. 修改 Tex 文件夹中的 Frontpage.tex 条目信息
        4. 替换 Img 文件夹
        5. 替换 Biblio/ref.bib


## 试用

如果使用的是windows系统，推荐安装TexLive环境（如果使用CTEX套装，默认与WinEditor搭配，编译时可能出现“找不到CJKpunct.sty”，请勿混淆CTEX套装与ctex宏包，CTEX套装是集成了许多LATEX组件的LATEX编译系统，因已停止维护，**不建议使用**）。可以使用TexLive编译，WinEditor编辑哟。

然后编译Thesis.tex文件。两种方法：

1. 双击 artratex.bat，然后在 Tmp 文件夹中会生成Thesis.pdf中。
2. 直接在Texmaker或WinEdit或Texworks等编辑器中编译，则在当前文件夹中生成Thesis.pdf，推荐使用pdfLaTeX排版。注意，在编辑器中编译可能需要4步才能生成最终的版本（pdfLatex->Bibtex->pdfLatex->pdfLatex）



如果遇到什么问题，可以查看README_ucasthesis.md文档和模版使用说明.pdf文档。





## 修改日志

### 2018-03-24

- 修复了目录章节缩进不对的问题，改为章标题不缩进，第一级节标题缩进一个汉字，第二级节标题缩进2个汉字。
- 修复了图表列表显示问题，现在列表中只显示中文图标的标题。
- 修复了目录中的显示内容问题。改为不显示图表列表信息。

### 2018-03-20

- 修复了论文章节顺序的bug，改为正文后为参考文献，然后是附录，致谢，最后是作者简历。

### 2018-03-19

- 解决了连续公式之间间隔太大的问题。重写了gather环境，多个连续公式时请使用`\begin{gather}`代替`\begin{equation}`。

### 2018-03-17

- 发现格式要求里与GB7714-2015格式并不一样，所以修改了`.bst`文件，为了跟标准文件区别开来，将文件改为`iecas-plain.bst`，并修改了`artratex.sty`中的第230行，改为默认使用iecas-plain.bst文件：`        \bibliographystyle{Biblio/iecas-plain}% author year scheme`

### 2018-03-15

国科大出了新模版，今年电子所也要按照国科大的来，格式大变，所以请大家忽略之前的修改日志。哼哧哼哧几十年，一夜回到解放前 (┬＿┬)

下载了莫晃锐的最新模版，在此基础上进行了修正。

- 按照要求，将英文关键字“Keywords”改为“Key Words”；

- 按照要求，重写了公式样式，新的公式中公式编号前面会有三个点（第一次遇见这种样式）；

- 按照要求，将图表标题改成中英双标题，中文在上，英文在下；
  - 对于双标题，在代码中将`\caption{中文}`改成`\bicaption{中文}{English}`就可以了；
  - 图片标题位于图片下方，因此`\bicaption`应该在`\includegraphics`的下方；
  - 表格标题位于表格上方，因此`\bicaption`应该在`tabular`的上方；

- 按照要求，参考文献格式改成作者+年份的格式，具体为在thesis.tex中25行改为`\usepackage[super,myhdr,list,authoryear]{Style/artratex}% document settings`

- 根据《中国人名汉语拼音字母拼写规则》（GB/T 28039—2011），英文封面中的姓和名分写，**姓在前，名在后，姓名之间用空格分开。姓和名需写全拼，开头字母大写**；

- 注释掉`ucasthesis.cfg`第144行，使附录按照 附录A，附录B 编号；

  ​


### 2018-03-06

- 修正了页眉章节显示问题。由原来的“第1章”改为“第一章”。

### 2018-03-04

- 经过和师弟的讨论，发现使用XeLaTeX编译要比pdfLaTeX编译出来的文档要好看和方便，主要体现在以下几个方面：
  1. pdfLaTeX编译出来的文档中如果汉字中夹杂着英文，可能导致文字超出行末，此时需要在中文和英文之间加上空格，而使用XeLaTeX编译则不会出现此问题；
  2. 对于引用（`\cite{}'）中含有中文的情况，pdfLaTeX无法编译，而XeLaTeX可以编译；
- 之前没有使用XeLaTeX的最大原因就是它比pdfLaTeX编译要慢很多。感谢时宗洋同学找到的解决方案：
  1. 以管理员身份运行fc-cache
  2. 在texlive安装路径bin/win32下，设置xelatex.exe以管理员身份启动。
  3. 启动编辑器（如TeXworks）时以管理员身份启动
- 修改默认编译器为XeLaTeX，将Style文件夹下ucasthesis.cfg文件的96行中的①替换为{\Large{\ding{172}}}，使在XeLaTeX编译的情况下能正确显示。

### 2018-03-02

- **ucasthesis作者莫晃锐在2月4日进行了重大更新**，对一些基础库和样式做了调整。此次iecas-thesis模版针对最新版的ucasthesis模版进行了重构；
- 根据电子所17年10月24日2018届毕业生动员会上PPT有关论文的要求进行了调整（主要为封面的调整）；
- 参考文献格式改为chinesebst-mod.bst，该文件从蒋成龙师兄的模版中复制过来，在此对蒋成龙师兄表示感谢！（ucasthesis中默认使用的是gbt7714-unsrt.bst文件，使用该样式英文参考文献中作者名称全是大写，若想改回这种样式，修改Style文件夹下的artratex.sty文件，将第205行 `\bibliographystyle{Biblio/chinesebst-mod}`改为`\bibliographystyle{Biblio/gbt7714-unsrt}`即可）
- 将页脚的页码改为底下居中显示；
- 新模板的摘要有页码，旧模板没有，师兄的论文中英文摘要部分是连续页码，新模板符合要求；
- 感谢时宗洋同学提醒，修复了新版模版中附录字母序号不显示的问题；


### 2018-01-27
- 为章节文件(Chap_Guide.tex 、Chap_Intro.tex)添加了“magic comments”，这样就可以在章节文件中直接编译整个工程。

### 2018-01-16

- 修改正文行间距为1.5倍行间距;
- 修改目录显示深度为3层，可以显示章节x.x.x.x;
- 修改Compile.bat的默认编译选项为pdfLatex。使用XeLatex编译①②③④⑤时无法显示。（若非得使用XeLatex编译，可将Style文件夹下ucasthesis.cfg文件的96行中的①替换为{\large{\textcircled{\small{1}}}}，其他的数字以此类推）

### 2018-01-15

- 去掉封面中文题目的下划线；
- 将封面的“培养单位”改成“研究所”；
- 将“研究成果声明”和“关于学位论文使用权的说明”改成电子所的模版；
- 将页眉改成居中，页码改到页脚居中显示；
- 将英文改为Times New Roman字体；



## 申明

此Latex模版为非官方的学位论文模版，是基于本所前几届的师兄师姐的博士论文论文格式整理而来。若有任何错误的地方，欢迎大家及时指正。

欢迎提issue，或者邮件交流（shawpan@yeah.net）