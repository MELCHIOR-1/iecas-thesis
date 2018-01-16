# iecas-thesis

=======================================

## 说明

本项目初始fork的github上莫晃锐写的最新的国科大论文模版[ucasthesis](https://github.com/mohuangrui/ucasthesis)，在此基础上，针对中科院电子所的学位论文特点，做了些修改。形成适用于电子所学位论文的模版iecas-thesis.



## 试用

如果使用的是windows系统，首先安装TexLive环境。然后编译Thesis.tex文件。两种方法：

1. 双击Compile.bat，然后在Tmp中会生成Thesis.pdf中。
2. 直接在Texmaker或WinEdit或Texworks等编辑器中编译，则在当前文件夹中生成Thesis.pdf。注意，在编辑器中编译可能需要4步才能生成最终的版本（pdfLatex->Bibtex->pdfLatex->pdfLatex）

如果遇到什么问题，可以查看README4ucasthesis.md文档和HowToUse.pdf文档。

## 修改日志

### 2018-01-16

- 修改正文行间距为1.5倍行间距;
- 修改目录显示深度为3层，可以显示章节x.x.x.x;
- 修改Compile.bat的默认编译选项为pdfLatex。使用XeLatex编译①②③④⑤时无法显示。

### 2018-01-15

- 去掉封面中文题目的下划线；
- 将封面的“培养单位”改成“研究所”；
- 将“研究成果声明”和“关于学位论文使用权的说明”改成电子所的模版；
- 将页眉改成居中，页码改到页脚居中显示；
- 将英文改为Times New Roman字体；



## 申明

此Latex模版为非官方的学位论文模版，是基于本所前几届的师兄师姐的博士论文论文格式整理而来。若有任何错误的地方，欢迎大家及时指正。

欢迎提issue，或者邮件交流（shawpan@yeah.net）