# The Minimo Theme
[中文版本](README.md) | [English Version](README-en.md)  

*Minimo is a Jekyll theme **ONLY** for Github Pages, adapted from [*jekyll-theme-minimal*](https://github.com/pages-themes/minimal).
You can [preview the theme to see what it looks like](https://scbzfarmingtest。github.io/jekyll-theme-minimo), or [have a quick start](#quick-start).*  

<p><b>Note:</b> If you do <b style="background-color: red; color: white;">NOT CHANGE</b> the texts and images of licenses, <b style="background-color: red; color: white;">YOUR ORIGINAL STUFFS IN YOUR WHOLE SITE SHOULD APPLY TO <a href="http://www.gnu.org/licenses/gpl-3.0.en.html#/">GPLv3</a> AND <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0 (International)</a></b></p>

## About

Minimo is adapted from [*jekyll-theme-minimal*](https://github.com/pages-themes/minimal).  

<p><b style="color: red;">Please note: Minimo only works on Github Pages!</b></p>

This means that a direct clone of the repository will NOT be able to:  
   + be debugged locally,
   + implemented with other CI/CD,
   + guaranteed to run on other platforms.  

## Contents

- [The Minimo Theme](#the-minimo-theme)
  - [About](#about)
  - [Contents](#contents)
  - [Quick Start](#quick-start)
  - [Customization](#customization)
  - [References](#references)

## Quick Start

To use the Minimo theme:

1. Clone this repo, by
    ```bash
    # You Must have `git` and add it to path first
    git clone --bare git@github.com:scbzfarmingtest/jekyll-theme-minimo.git
    ```
    For `git` installation, see [*Git Offical Website*](https://git-scm.com/).
2. Edit site's variables in `_config.yml`:
    ```yml
    title: [Your site title]
    author: [Your name]
    description: [Your site description]
    ```
3. Create a new Github repository named `YourGithubUserName.github.io`.
4. Push your local repo (created in Step 1) to Github, by
    ```bash
    # In URL, replace {{YGUN}} with your Github user name
    git remote add origin https://github.com/{{YGUN}}/{{YGUN}}.github.io.git #See below notes
    git branch -M main
    git push -u origin main
    ```
    Through this method, you may need to authorize by *Git Credential Manager*.  
    Instead, you may also use `ssh` to remote, use
     ```bash
     # In URL, replace {{YGUN}} with your Github user name
     git remote add origin git@github.com:{{YGUN}}/{{YGUN}}.github.io.git
     ```
    Through this method, you may need to authorize by a *GPG key*. See also in [GitHub docs](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-new-gpg-key-to-your-github-account).
5. Use Shell script `new` to creat new posts, by
    ```bash
    # You must have bash/git_bash and add it to path
    ./new
    ```
    Then follow the instructions. For more, please see <a href="documentation/Mini-Manual.md"><i>Mini-manual of <code>new</code></i></a>.

## Customization

Generally speaking, you can:  
1. edit `_includes/head-custom.html` to use different/more `css` style.
2. edit `_layouts/default.html` and `_layouts/post.html` to use different/more `css` style.
3. create a folder `assets/css` and create `.css` files or create `.sass` files and use `@import` line where used.

~~Another suggestion is to create a *Recent Post Page* in *Home Page*, such as [recent page in my blog](https://scbzfarmingtest.github.io/recent).~~  
~~However, I copied the [codes](https://stackoverflow.com/questions/46672231/in-jekyll-how-to-show-posts-from-last-week) by [Joonas](https://stackoverflow.com/users/603568/joonas) from stackoverflow. (Please let my show my thanks!) Under SE policy, posts are all under CC BY-SA 4.0 (International), which means that to use his code, this theme must under CC BY-SA 4.0 as well. This is definitely not my hope.~~  

~~I would thus recommend you to build your *recent posts page* by your own. **The image I use have been storaged as `assets/images/recent.png` already, which is definitely under CC0 1.0 License. Feel free to use it!**~~

Since [Joonas](https://stackoverflow.com/users/603568/joonas) "re-grant" his [codes](https://stackoverflow.com/questions/46672231/in-jekyll-how-to-show-posts-from-last-week) as:
> as far as I'm concerned no lisence, use however you want  

Now you can use *recent posts page*

## References

1. [*jekyll-theme-minimal*](https://github.com/pages-themes/minimal)
2. [Chinese translation of Jekyll docs](https://jekyllcn.com/docs/)
3. [Jekyll official docs](https://jekyllcn.com/docs/home/)
4. [Liquid China website](https://liquid.bootcss.com/)
5. [Liquid official reference](https://shopify.dev/api/liquid/)
6. [Linux documentation, by die.net](https://linux.die.net/)
7. [Shell guidance by runoob.com](https://www.runoob.com/linux/linux-shell.html)
8. [Github docs](https://docs.github.com/en)
    The main references are principles of *Actions* (especially *CI/CD* and *WorkFlows*) and *Github Pages*.

**Appreciation!**