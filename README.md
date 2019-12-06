# Replace_MathType

## 1. 基于Microsoft Office 365

### 1.1 Office 365

本库的基础软件是Windows 10 Office 365（下称365），一般的Office 2016 / 2019 可行性未知。Office 365 会给与最新的软件支持，所以在兼容性与新特性上面会有相当大的优势。

⚠️ 如何低价购买正版 Office 365？可淘宝（taobao.com）搜索「Office 365 家庭版 拆分」关键词。

下图显示了365的公式菜单，可以看到，已经官方支持LaTeX语法了！

![Word menu](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/figure/you_latex.gif)

> 特别注意，Office 365 的全部功能已经在 macOS 10.14.5 及以后的版本里得到了支持，而且，**Word for macOS 也支持LaTeX语法输入！**

### 1.2 mathpix 软件

mathpix是一个公式OCR软件，通过该软件，可以提取图片中的印刷体公式。

虽然该公司声称该软件可以提取手写的公式，但是实际效果并不好。

#### 1.2.1 macOS / Windows安装

本库给出了安装文件，位于```app```文件夹内。

#### 1.2.2 Ubuntu用户

Ubuntu用户请通过命令行安装。

``` bash
sudo snap install mathpix-snipping-tool
```

> 官方地址：https://mathpix.com/

**如果可以把上述两个软件结合使用，那么在写论文的背景知识的过程中，写公式效率可以提升10倍左右！**

> 友情提示，本库的 app 文件夹里提供的是 1.0 版本的 MathPix 软件，如果你想用新版，那么需要花钱订阅。目前新版的 MathPix 软件必须订阅才能使用。macOS 的可以禁止自动升级，但是 Windows 的会自己升级，而且无法禁止。目前来看，并没有很好的解决方案。

## 2. 为什么不用MathType等插件？

### 2.1 收费软件

价格很昂贵，而且盗版体验很差，注意⚠️：免费的永远是最贵的！

其他的诸如Axmath之类的小众软件，输出效果不错，不过输出的PDF是不可选中、不可搜索版本，格式应该是某种矢量图（放大之后可以明显看到不光滑的边界）。

### 2.2 Office 365 内置功能原生、优秀

Office 365 的内置公式比较强大。渲染之后与原文档锲合度最高。

虽然365也是付费软件（淘宝家庭版拆分装，仅 50 RMB / 年），不过在当下中国的大学，没有微软的 Word 还真的是玩不转，不如弃暗投明。用好 Word，一样能做出漂亮的文稿。这里就不谈 Word 与 LaTeX 的优劣了。

> **365 内置的公式，支持段落调节，而 MathType 等插件生成的公式，不支持自动调节，在某些情况下很是难看。**

### 3. 安装字体

要使用下面这个demo方案，需要安装一款字体：```Latin Modern Math```。本 Repository 已经给出，直接切换到```01. Latin Modern Math/otf/```文件夹下，找到latinmodern-math.otf文件，右键->安装即可。macOS用户自己对照摸索，非常简单。

这个字体相对比较好看，不过这里也提供了其他一些解决方案。

### 4. Demo

在 Windows Office 365 Word 里面（PPT不支持）：

- Step 1 ```<ALT> + <=>```   调出公式输入框
- Step 2 ```<CTRL> + <SHIFT> + <=>```  将公式转为线性，同时在**公式选项卡**里把公式切换为 LaTeX ⚠️
- Step 3 复制黏贴这段代码到公式输入框：
```
\left(x+a\right)^n=\sum_{k=1}^{n}\int_{t_1}^{t_2}{\binom{n}{k}{f(x)}^ka^{n-k}}\box(24&dx)
```
- Step 4 ```<CTRL> + <=>``` 渲染公式

![sample code](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/sample%20code.png)

![fomula](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/fomula.png)

Just enjoy it.

![images](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/figure/2019-05-12%2000.23.05.gif)

## 5. 其他字体方案

要想更换内置公式的数学字体，字体必须支持Opentype Math

**重要说明**：尽管Word中支持更改这些字体，但是Office本身局限性，自带pdf输出只支持 **Cambria Math** 和 **Asana Math** 转换为矢量文本，并不支持其他数学字体转换公式为矢量文本，而是强制转换为位图导致模糊，所以必须依赖于强大的第三方Adobe Acrobat DC Pro的Word插件 **PDFMaker** 来嵌入数学字体集

### 5.1 Latin Modern Math，TeX Live自带默认的数学字体

[下载地址](http://www.gust.org.pl/projects/e-foundry/lm-math/download)

![Latin Modern Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Latin%20Modern%20Math.png)

### 5.2 STIX

TeX Live中自带，全称是Scientific and Technical Information Exchange font，这个字体是一套比较大的也是历史比较长的字体，这个字体包含正文字体和数学字体。这个字体风格类似Times，所以很多刊物会用到的。

[项目主页](http://www.stixfonts.org/

下载地址)https://sourceforge.net/projects/stixfonts/

![STIX](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/STIX.png)

### 5.3 XITS Math

基于STIX的一套数学字体，TeX Live中自带，比STIX多了一些数学扩展。类似于Times New Roman.

[下载地址](https://github.com/khaledhosny/xits-math/downloads)

![XITS Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/XITS%20Math.png)

### 5.4 Bonum Math、Pagella Math、Schola Math、Termes Math一系列字体

[项目主页](http://www.gust.org.pl/projects/e-foundry/tg-math)

[下载地址]( http://www.ctan.org/tex-archive/fonts/tex-gyre-math)

![Bonum Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Bonum%20Math.png)

![Pagella Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Pagella%20Math.png)

![Schola Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Schola%20Math.png)

![Termes Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Termes%20Math.png)


### 5.5 Neo Euler

这个字体需要单独安装。

[下载地址](https://github.com/khaledhosny/euler-otf)

![Neo Euler](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Neo%20Euler.png)

### 5.6 Cambria Math

Office公式默认字体。

![Cambria Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Cambria%20Math.png)

### 5.7 Asana Math

TeX Live自带数学字体

[下载地址](http://ctan.org/pkg/asana-math)

注意：很遗憾，Acrobat DC Pro 的 Word 插件 PDFMaker 不支持 Asana Math 字体转换为 pdf 文档，不过有趣的是，该字体和 Cambria Math 一样支持 Word 直接转换 pdf 而不会被强制转换为位图。

## 6. 输出 Word 为 PDF 文档

书写论文、一般文档的重要一步就是将 docx 导出为  PDF，嵌入了所需字体的 PDF 文件会以精准的方式呈现文档的原貌。

这里的原则是：**尽可能使用 Word (Office 365) 的原生功能，而不是借助第三方的插件。**

### 6.1 Windows 10 平台

Windows 10 自带的导出功能并不完善，对于我们最常用的数学字体 Latin Modern Math 的支持不好，如果强行使用 Word 的导出功能，会使得输出的 PDF 中的数学公式为位图形式，锯齿感严重。之前的解决办法是安装 Adobe 的 PDF Maker 插件，这款插件是 Acrobat Pro 自带的一个 Word 插件，该插件的导出功能比较强大。后经 @invisprints 的提醒，发现有更加简单的方法。

![microsoft_print_to_pdf](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/figure/print_to_pdf.png)

如上图，【文件】- 【打印】 - <选择打印机>，使用 Word for Windwos 自带的打印功能，其中选择打印机为 **Microsoft Print to PDF** 这款虚拟打印机，然后点击打印，即可完美实现 PDF 输出。

### 6.2 macOS 平台

macOS 平台的输出比较简单，只需要 `Command Shift C` ，另存为 PDF ，即可实现完美输出。
