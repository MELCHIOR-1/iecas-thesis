# iecas-thesis

=======================================

## 说明

本项目初始fork的github上莫晃锐写的最新的国科大论文模版[ucasthesis](https://github.com/mohuangrui/ucasthesis)，在此基础上，针对中科院电子所的学位论文特点，做了些修改。形成适用于电子所学位论文的模版iecas-thesis.

本模版按照电子所17年10月24日2018届毕业生动员会上PPT有关论文的要求（见下图）进行编写。对于PPT中未提到的格式，参考了所里前几届毕业生的论文格式。



<div align=center><img width = "60%" src="https://github.com/MELCHIOR-1/iecas-thesis/raw/master/Img/format_1.png"/>

<img width = "60%" src="https://github.com/MELCHIOR-1/iecas-thesis/raw/master/Img/format_2.png"/>

<img width = "60%" src="https://github.com/MELCHIOR-1/iecas-thesis/raw/master/Img/format_3.png"/>

</div>




因莫晃锐的模板在2018年2月4日进行了显著改动，如果之前使用旧模版，建议的更新方式为`移植你的旧有文件到新模板中`:
        1. 下载解压新模板
        2. 替换 Tex 文件夹中的除 Frontpage.tex 以外的文件
        3. 修改 Tex 文件夹中的 Frontpage.tex 条目信息
        4. 替换 Img 文件夹
        5. 替换 Biblio/ref.bib


## 试用

如果使用的是windows系统，推荐安装TexLive环境（如果使用CTEX，编译时可能出现“找不到CJKpunct.sty”）。然后编译Thesis.tex文件。两种方法：

1. 双击 artratex.bat，然后在 Tmp 文件夹中会生成Thesis.pdf中。
2. 直接在Texmaker或WinEdit或Texworks等编辑器中编译，则在当前文件夹中生成Thesis.pdf，推荐使用pdfLaTeX排版。注意，在编辑器中编译可能需要4步才能生成最终的版本（pdfLatex->Bibtex->pdfLatex->pdfLatex）



如果遇到什么问题，可以查看README_ucasthesis.md文档和模版使用说明.pdf文档。

建了个iecas-thesis模板使用交流群，也可以扫一扫下方的二维码，欢迎加群提问交流。


<div align=center><img width = "20%" src="https://github.com/MELCHIOR-1/iecas-thesis/raw/master/Img/QRcode.jpg"/>

</div>


## 修改日志

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