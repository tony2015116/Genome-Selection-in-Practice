## 使用说明

<p align="center">
<a href="./README_ZH.md">中文</a> • <a href="./README.md">English</a>
</p>

如果您打算运用R语言以及Quarto来创作一本书籍，这个模板将会是您的得力助手。它不仅配置齐全，而且易于定制，能够满足您从文字编辑到图表插入等各种排版需求。无论您是数据科学、学术研究还是任何其他领域的作者，这个模板都能让您的书籍制作过程更加顺畅和高效。

1.  点击“使用这个模板”（Use this template）按钮开始创建基于模板的新项目。📚

2.  克隆或下载您的新项目到本地环境。📁

3.  打开项目文件夹，根据需要修改`custom.scss`和`_quarto.yml`。`fonts`文件夹用于存放本地生成PDF时使用的字体。修改`.github`文件夹中的`publish.yml`以适应您的需求。如果书中需要运行R/Python代码，需在`requirements.txt`中添加对应的包或库。根据需要更换`analysis.png`和`cover.png`图片。🛠️

4.  在终端运行`quarto install`和`quarto uninstall`命令来管理Quarto扩展。🔧

5.  在终端运行`quarto render`命令以生成书籍。🖨️

6.  进行必要的修改后，提交您的项目变更到您的GitHub仓库。🌐

7.  在终端中运行`quarto publish gh-pages`命令，发布您的书籍到GitHub Pages。🚀

8.  现在，您可以开始愉快地编辑您的`.qmd`文件了。✍️

9.  编辑完成后，更新`_quarto.yml`中的章节信息，并提交这些更改。📝

10. 使用Git命令`git add .`、`git commit`和`git push`将更改推送到GitHub仓库。💾

喜欢的话，给个Star吧💖
