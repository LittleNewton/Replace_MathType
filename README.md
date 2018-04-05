# Replace_MathType

## 1. 基于Microsoft Office 365

本库的基础软件是Office 365（下称365），一般的Office 2016可行性未知。365会给与最新的软件支持，所以在兼容性与新特性上面会有相当大的优势。

下图显示了365的公式菜单，可以看到，已经官方支持LaTeX语法了！

![demo](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/README%20figures/Word%20menu.png)

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

![LaTeX代码](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/README%20figures/sample%20code.png)

![渲染效果](https://raw.githubusercontent.com/LittleNewton/Replace_MathType/master/README%20figures/fomula.png)

Just enjoy it.
