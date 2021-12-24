<!-- 待更新 -->
# `new`的迷你手册 <!-- omit in toc -->

`new`是一个运行在windows上的`shell`脚本，由`bash`执行，快速生成“希小”主题模板，而不需要`Ruby`、`RubyGem`等依赖。

[中文版本](Mini-Manual.md) | [English Version](Mini-Manual-en.md)  

- [使用](#使用)
- [疑难解答](#疑难解答)
  - [关于流程](#关于流程)
  - [提示和错误信息](#提示和错误信息)
    - [关于颜色](#关于颜色)
    - [错误排除](#错误排除)

## 使用

1. 运行`new/new.sh`
  ```bash
  ./new
  ```
2. 遵循提示创建新贴文：
   1. 输入新帖文标题：
      ```sh
      Please Enter New Post Title: # 输入标题，回车换行进入下一步
      ``` 
      请注意，此步骤之后将在`_posts`文件夹中建立
   2. 选择新帖文标签是否单一：
      ```sh
      Single tag?(y/n):# 使用单一标签请输入y，使用多标签输入n；其他输入会终止新贴文生成
      ```
   3. 输入新贴文标签：
      ```sh
      Please Enter Tag/Tags(SingleTag/tag1--tag2--tag3):# 单一标签直接输入标签名，多标签请依次输入，标签间用 -- 间隔 
      ```
   4. 选择新帖文标签是否单一：
      ```sh
      Single category?(y/n):# 使用单一分类请输入y，使用多分类输入n；其他输入会终止新贴文生成
      ```
   3. 输入新贴文分类：
      ```sh
      Please Enter Category/Categories(SingleCate/cate1--cate2--cate3):# 单一分类直接输入分类名，多分类请依次输入，分类间用 -- 间隔 
      ```
3. 创建成功后会显示成功提示并自动打开新帖文：
    ```sh
    Congratulations! New post as # 新贴文地址
    Input "r" to undo and restart # 输入 r 撤销生成并重新开始
    Input "d" to undo and delete new post # 输入 d 撤销并推出程序
    Input others to quit and open new post # 输入其他退出程序并使用默认程序打开新贴文
    ```
4. 确认创建后显示提示文字：
    ```sh
    Congratulations!
    Opening new post...
    ```

## 疑难解答

### 关于流程

<p><b>请不要手动（如使用<kbd>ctrl</kbd>+<kbd>C</kbd>）终止程序！</b>否则，您可能需要手动删除未配置完全的新贴文，它应该位于`_posts`文件夹。

### 提示和错误信息

#### 关于颜色

请注意，青色为成功提示，红色为错误提示。如：  
<img src="Success.png">  
和  
<img src="Error.png">

#### 错误排除

+ `ERROR:x1`
   出现该错误的原因是：您在今天生成过相同标题的贴文，这是`jekyll`不允许的。  
   请根据提示输入`r`重新开始、输入`b`备份旧贴文并继续生成新贴文、输入`o`覆盖旧贴文 或 输入其他推出。
+ `ERROR:x2`
   出现该错误的原因是：`Single tag?(y/n):`后只能输入<kbd>y</kbd>或<kbd>n</kbd>  
   请根据提示输入`t`从`Single tag?(y/n):`处继续、输入`r`重新开始 或 输入其他退出。
+ `ERROR:x3`
   出现该错误的原因是：`Single category?(y/n):`后只能输入<kbd>y</kbd>或<kbd>n</kbd>  
   请根据提示输入`t`从`Single category?(y/n):`处继续、输入`r`重新开始 或 输入其他退出。