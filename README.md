# HNUThesisTemplate

**湖南大学本科生毕业论文LaTeX模板**

基于远古巨坟[HNUThesis](http://hnuthesis.googlecode.com/)
修复了奇奇怪怪的BUG

---

## 使用说明

正文写在`body\`中，再在`thesis.tex`中添加`\include{body/***}`

请使用`UTF-8`

文献管理使用`BibTeX`

Windows环境可以执行`thesis.bat`编译

终端环境推荐

```bash
latex.exe -src -interaction=nonstopmode "thesis".tex
bibtex.exe "thesis"
latex.exe -src -interaction=nonstopmode "thesis".tex
dvipdfm.exe "thesis".dvi
```
基于不知道多久以前的学长留下来的模板做更新，参见 https://github.com/leaf-hsiao/HNUThesisTemplate

# 这是你们20级学长在2024/06/02毕业前给你们留的言
用的是Windows系统和VScode编译器使用MikTex，你们用当下的最新版应该没什么问题，有关系统报错部分只对VScode玩家负责：
1. 请在body区写论文正文
2. 运行请使用thesis.bat，不要直接在.tex文件的界面上运行。
3. 再说一遍，一定记得运行要在thesis.bat上点击run code 才可以运行出pdf档案来。
4. 参考文献丢到reference.bib里面，怎么操作自己去学，各大文献网站一定有导出Bibtex的方法。
5. 在路径preface的cover档案里把该修改的姓名学号班级指导教授还有论文题目改好，然后摘要也在这个档案里面写。注意这里的论文题目只会变更页眉的论文题目，封面的论文题目看第六点
6. 点开路径setup文件夹里的format.tex，划到266行看怎么修改论文题目。注意除了这个和日期以外其他的不要乱动。
7. 注意：除非pdf生成不出来，不然不要理系统报错。
8. 我在每个section都会有这样的语句\section[\textnormal{标题}]{\textbf{标题}}，这是为了满足目录部分不要加黑表达但是在正文中加黑表示重要性
9. 现在的thesis.bat用的是xelatex命令：
```bash
xelatex.exe -synctex=1 -interaction=nonstopmode "thesis".tex
bibtex.exe "thesis"
xelatex.exe -synctex=1 -interaction=nonstopmode "thesis".tex
xelatex.exe -synctex=1 -interaction=nonstopmode "thesis".tex
```

如果无法运行，可以试试这两个latex或者pdflatex:
```bash
latex.exe -src -interaction=nonstopmode "thesis".tex
bibtex.exe "thesis"
latex.exe -src -interaction=nonstopmode "thesis".tex
dvipdfm.exe "thesis".dvi
```

```bash
pdflatex.exe -synctex=1 -interaction=nonstopmode "thesis".tex
bibtex.exe "thesis"
pdflatex.exe -synctex=1 -interaction=nonstopmode "thesis".tex
pdflatex.exe -synctex=1 -interaction=nonstopmode "thesis".tex
```

10. 能踩的坑基本帮你们踩过了，但是换电脑换环境可能还是会出现问题，记得善用GPT系列的大模型解决问题。
