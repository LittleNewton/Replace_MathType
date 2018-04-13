# Replace_MathType

## 1. 基于Microsoft Office 365

本库的基础软件是Office 365（下称365），一般的Office 2016可行性未知。365会给与最新的软件支持，所以在兼容性与新特性上面会有相当大的优势。

下图显示了365的公式菜单，可以看到，已经官方支持LaTeX语法了！

![Word menu](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Word%20menu.png)

## 2. 为什么不用MathType？

收费软件，体验很差！诸如Axmath之类的小众软件，输出效果不错，不过输出的PDF是不可选中版本，格式应该是某种矢量图（放大之后可以明显看到不光滑的边界）

虽然365也是付费软件，不过在当下中国的大学，没有微软的Word还真的是玩不转，不如弃暗投明。用好Word，一样能做出漂亮的文稿。这里就不谈Word与LaTeX的优劣了。

## 3. 安装字体

要使用这个方案，需要安装一款字体。Latin Modern Math字体，已经给出，直接安装即可。MacOS用户自己摸索。

这个字体相对比较好看，其余的一律比较丑。

## 4. Demo

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

## 5. 其他字体方案

要想更换内置公式的数学字体，字体必须支持Opentype Math

重要说明：尽管Word中支持更改这些字体，但是Office本身局限性，自带pdf输出只支持Cambria Math和Asana Math转换为矢量文本，并不支持其他数学字体转换公式为矢量文本，而是强制转换为位图导致模糊，所以必须依赖于强大的第三方Adobe Acrobat DC Pro的Word插件PDFMaker来嵌入数学字体集

### 5.1 Latin Modern Math，TeX Live自带默认的数学字体
[下载地址](http://www.gust.org.pl/projects/e-foundry/lm-math/download)

![Latin Modern Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Latin%20Modern%20Math.png)

### 5.2 STIX

TeX Live中自带，全称是Scientific and Technical Information Exchange font，这个字体是一套比较大的也是历史比较长的字体，这个字体包含正文字体和数学字体。这个字体风格类似Times，所以很多刊物会用到的。
项目主页：http://www.stixfonts.org/
下载地址：https://sourceforge.net/projects/stixfonts/

![STIX](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/STIX.png)

### 5.3 XITS Math

基于STIX的一套数学字体，TeX Live中自带，比STIX多了一些数学扩展。类似于Times New Roman.

下载地址：https://github.com/khaledhosny/xits-math/downloads

![XITS Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/XITS%20Math.png)

### 5.4 Bonum Math、Pagella Math、Schola Math、Termes Math一系列字体

项目主页: http://www.gust.org.pl/projects/e-foundry/tg-math
下载地址: http://www.ctan.org/tex-archive/fonts/tex-gyre-math

![Bonum Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Bonum%20Math.png)

![Pagella Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Pagella%20Math.png)

![Schola Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Schola%20Math.png)

![Termes Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Termes%20Math.png)


5.Neo Euler，这个字体需要单独安装下载地址： https://github.com/khaledhosny/euler-otf

![Neo Euler](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Neo%20Euler.png)

6 Cambria Math， Office公式默认字体

![Cambria Math](https://raw.githubusercontent.com/LittleNewton/LittleNewton_Figures_References/master/Replace_MathType/Cambria%20Math.png)

7.Asana Math， TeX Live自带数学字体
下载地址：http://ctan.org/pkg/asana-math

注意：很遗憾，Acrobat DC Pro的Word插件PDFMaker不支持Asana Math字体转换为pdf文档，不过有趣的是，该字体和Cambria Math一样支持Word直接转换pdf而不会被强制转换为位图。
好了，就这么些常用的数学公式字体，由于数学符号的特殊性，所以支持Opentype Math的字体并不多，但已经基本能满足需求了，同时转换成通用格式pdf时，推荐使用Adobe Acrobat DC Pro的Word插件(安装后升级补丁就有)，能够输出比Word更加优质高质量的pdf文档(很明确地告诉你，想要更改为这些数学字体后输出矢量文本pdf文档，必须使用PDFMaker)。

此外，最好设置为高质量印刷来输出pdf，点击首选项>转换设置>高质量打印。
