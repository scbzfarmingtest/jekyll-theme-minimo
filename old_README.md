# “希小”模板
[中文版本](README.md) | [English Version](README-en.md)  

“希小”是一个**仅**用于Github Pages的Jekyll主题模板。它改编自[*jekyll-theme-minimal*](https://github.com/pages-themes/minimal)。 
您可以[预览主题](https://scbzfarmingtest。github.io/jekyll-theme-minimo)，或[快速开始](#快速开始).*

<p><b>请注意：</b>如果你<b style="background-color: red; color: white;">不改变</b>许可协议的文字和图片，<b style="background-color: red; color: white;">你整个网站的原创内容应该适用于<a href="http://www.gnu.org/licenses/gpl-3.0.en.html#/">GPLv3</a>和<a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0 (International)</a>协议。</b></p>

## 关于

“希小”模板依据[*jekyll-theme-minimal*](https://github.com/pages-themes/minimal)改编而成。  

<p><b style="color: red;">请注意：“希小”模板仅能在<i>Github Pages</i>上运行！</b></p>

这意味着直接克隆本仓库将：
+ 无法在本地调试；
+ 无法借助其他CI/CD实现；
+ 也不保证能在其他平台可以运行。

## 目录

- [“希小”模板](#希小模板)
  - [关于](#关于)
  - [目录](#目录)
  - [快速开始](#快速开始)
  - [个性化](#个性化)
  - [参考文件](#参考文件)

## 快速开始

使用此模板，请：

1. 克隆这个仓库。
    ```bash
    # 你必须先有`git`并将它加入到系统环境
    git clone --bare git@github.com:scbzfarmingtest/jekyll-theme-minimo.git
    ```
    针对`git`的安装，请查看 [Git官网](https://git-scm.com/)。
2. 在`_config.yml`文件中编辑全站变量：
    ```yml
    title: [网站标题]
    author: [作者]
    description: [网页简介]
    ```
3. 创建一个新的Github库，命名为`YourGithubUserName.github.io`；
4. 将你的本地仓库（通过步骤一克隆的仓库）推送到Github：
    ```bash
    # 在URL中，将{{YGUN}}替换为您的Github用户名
    git remote add origin https://github.com/{{YGUN}}/{{YGUN}}.github.io.git #见下文贴士
    git branch -M main
    git push -u origin main
    ```
    通过这种方法，您可能需要*Git Credential Manager*授权。  
    另外，您也可以使用`ssh`来推送：
     ```bash
     # 在URL中，将{{YGUN}}替换为您的Github用户名
     git remote add origin git@github.com:{{YGUN}}/{{YGUN}}.github.io.git
     ```
    通过该方法，您可能需要使用*GPG key*进行授权。详见[GitHub文档](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-new-gpg-key-to-your-github-account).
5. 使用Shell脚本`new`来建立新的帖子：
    ```bash
    # 你必须先有bash或git bash并将它加入到系统环境
    ./new
    ```
    之后请遵循指示。更多请点击 <a href="documentation/Mini-Manual.md"><code>new</code>的迷你手册</a>。

## 个性化

总的来说，你可以：
1. 编辑`_includes/head-custom.html`来使用不同或更多的`css`样式；
2. 编辑`_layouts/default.html`和`_layouts/post.html`来使用不同或更多的`css`样式；
3. 建立一个`assets/css`文件夹，其中建立`css`文件或建立`sass`文件并在使用出加入`@import`命令。

~~此外，建议在主页上创建一个*最近发表*的页面，比如我的博客的[近闻](https://scbzfarmingtest.github.io/recent)。~~  
~~然而，[该代码](https://stackoverflow.com/questions/46672231/in-jekyll-how-to-show-posts-from-last-week)是从stackoverflow上复制而来的，作者的昵称是[Joonas](https://stackoverflow.com/users/603568/joonas)。(请允许我表达谢意！) 在stackoverflow的政策下，帖子应当遵循《署名—非商业性使用—相同方式共享 4.0 协议国际版》，这意味着要使用他的代码，“希小”模板也必须遵循该协议，这显然不是我的初衷。~~  

~~因此，我建议你自己建立*最近发表*页面。**我博客使用的图标已经存储为assets/images/recent.png，该图标遵循《CC0 1.0许可》，您可以尽情享用!**~~ 

由于[Joonas](https://stackoverflow.com/users/603568/joonas)“重新授权了”他的[代码](https://stackoverflow.com/questions/46672231/in-jekyll-how-to-show-posts-from-last-week)：
> as far as I'm concerned no lisence, use however you want  

现在你可以使用*最近发布*页面

## 参考文件

1. [原模版*jekyll-theme-minimal*](https://github.com/pages-themes/minimal)
2. [Jekyll的中文翻译网](https://jekyllcn.com/docs/home/)
3. [Jekyll官方网站](http://jekyllrb.com/docs/)
4. [Liquid中文网](https://liquid.bootcss.com/)
5. [Liquid官网文档](https://shopify.dev/api/liquid/)
6. [Linux文档，die.net制作](https://linux.die.net/)
7. [Shell 教程 |菜鸟教程](https://www.runoob.com/linux/linux-shell.html)
8. [Github文档](https://docs.github.com/en)
    主要参考了Actions（尤CI/CD和workflows）以及Github Pages的机制。

**感激非常!**
