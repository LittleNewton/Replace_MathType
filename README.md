# Replace_MathType

## 1. 基于Microsoft Office 365

### 1.1 Office 365

本库的基础软件是Windows 10 Office 365（下称365），一般的Office 2016可行性未知。365会给与最新的软件支持，所以在兼容性与新特性上面会有相当大的优势。

下图显示了365的公式菜单，可以看到，已经官方支持LaTeX语法了！

![Word menu](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/figure/you_latex.gif)

> 特别注意，macOS版本的Office 365不支持LaTeX语法。如果是苹果用户，推荐使用虚拟机或使用双系统。不过，macOS用户也可以安装本字体以实现预览。

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

## 2. 为什么不用MathType等插件？

### 2.1 收费软件

价格很昂贵，而且盗版体验很差，注意⚠️：免费的永远是最贵的！

其他的诸如Axmath之类的小众软件，输出效果不错，不过输出的PDF是不可选中、不可搜索版本，格式应该是某种矢量图（放大之后可以明显看到不光滑的边界）。

### 2.2 Office 365内置功能原生优秀

365的内置公式比较强大。渲染之后与原文档锲合度最高。

虽然365也是付费软件（淘宝家庭版拆分装，仅售80 RMB / 年），不过在当下中国的大学，没有微软的Word还真的是玩不转，不如弃暗投明。用好Word，一样能做出漂亮的文稿。这里就不谈Word与LaTeX的优劣了。

> **365内置的公式，支持段落调节，而MathType等插件生成的公式，不支持自动调节，在某些情况下很是难看。**

### 3. 安装字体

要使用下面这个demo方案，需要安装一款字体：```Latin Modern Math```。本Repository已经给出，直接切换到```01. Latin Modern Math/otf/```文件夹下，找到latinmodern-math.otf文件，右键->安装即可。macOS用户自己摸索。

这个字体相对比较好看，不过这里也提供了其他一些解决方案。

### 4. Demo

在365 Word里面（PPT不支持）：

- Step 1 ```<ALT> + <=>```   调出输入栏
- Step 2 ```<CTRL> + <SHIFT> + <=>```  将公式转为线性
- Step 3 复制黏贴这段代码：
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

注意：很遗憾，Acrobat DC Pro的Word插件PDFMaker不支持Asana Math字体转换为pdf文档，不过有趣的是，该字体和Cambria Math一样支持Word直接转换pdf而不会被强制转换为位图。

好了，就这么些常用的数学公式字体，由于数学符号的特殊性，所以支持Opentype Math的字体并不多，但已经基本能满足需求了，同时转换成通用格式pdf时，推荐使用Adobe Acrobat DC Pro的Word插件(安装后升级补丁就有)，能够输出比Word更加优质高质量的pdf文档(很明确地告诉你，想要更改为这些数学字体后输出矢量文本pdf文档，必须使用PDFMaker)。

![PDFMaker](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/PDF%20Maker.png)

此外，最好设置为高质量印刷来输出pdf，点击 首选项>转换设置>高质量打印。

![Print Quality](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Print%20Quality.png)
