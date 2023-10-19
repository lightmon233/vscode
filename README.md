## 配置vscode c++环境的另一种方法（不用官方c++插件）（windows）

### 网址

https://visualstudio.microsoft.com/

https://code.visualstudio.com/download#

https://www.mingw-w64.org/downloads/#mingw-builds

### 配置环节

- 1、准备环节：

- ![image-20231020011028052.png](http://tva1.sinaimg.cn/large/006nBDeUgy1hj13aysnbgj305r03v757.jpg)

  - 要先安装好visual studio，如果不安装的话后续clangd插件配置c++头文件路径会非常麻烦，安装了visual studio就可以直接用visual studio的c++头文件路径。

  - 要有**科学的网络环境**

  - 安装mingw编译器（直接用visual studio的编译器的话会在调试时出问题）

    **一定要安装<font color=red>8.x.x</font>的版本，12.x.x和13.x.x的版本总是有莫名奇妙的问题**（在调试时）

- 2、下载对应自己系统版本的vscode，如果系统账户是administrator就下载system版本，如果系统账户是微软在线账号，就下载user版本。

- 3、安装vscode，注意勾选安装到path

- ![image-20231020011732497](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20231020011732497.png)

- 4、安装插件：

  ![image-20231020011203347](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20231020011203347.png)

  - cmake
  - cmake tools（与上面的插件共同用于项目搭建和管理）
  - clangd（本地语言服务器，让vscode识别c++的语法，加入自动提示词和检查错误等功能）
  - codelldb 调试器

### 创建项目和运行代码

​	先打开你要使用的项目文件夹（空文件夹），按下键盘快捷键`ctrl + shift + p`，点击cmake quick start，选择项目名、c++编译器路径等等，创建好项目。

![image-20231020011255782](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20231020011255782.png)

​	点击 vscode UI界面下方的运行按钮即可运行代码。

![image-20231020011358834](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20231020011358834.png)

### 配置调试

​	点击左侧项目栏的debug图标，点击 运行和debug，vscode会自动生成launch.json脚本文件，把program的路径修改一下为`build/<项目名>.exe`即可。

​	调试只需打好断点，点击调试按钮。

![image-20231020011516379](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20231020011516379.png)

![image-20231020011609176](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20231020011609176.png)
