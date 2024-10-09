# 高等数学II-1 

胡小兵 <iamhxb@cqu.edu.cn>  
助教：熊若兰 tel: 13872442250 <ruolanx100@163.com>  

Sep. 30th, 2024 课程介绍、微积分的一些基本问题  

> 成绩构成：  
> 期中 $20\%+$ 期末 $55\% +$ 考勤 $5\% +$ 作业 $10\% +$ Easylearning助学平台 $10\%$  

Oct. 9th, 2024  切换为学堂在线  
成绩构成变化  
期中 $20\%+$ 期末 $55\% +$ 考勤 $10\% +$ 作业 $10\% +$ 学堂在线 $5\%$  


# 极限论     
## 微积分的一些基本问题
### 面积问题
- 多边形（正 $n$ 边形）的面积 $A_6=6\cdot\frac{1}{2}ah=\frac{1}{2}l_6h$
- 圆面积、割圆术——用内接正 $n$ 边形的面积来逼近圆的面积  
  $A=\lim\limits_{n\to\infty}A_n=\pi r^2$
- 曲边三角形的面积  用矩形面积近似取代曲边梯形面积  
  在区间 $[0,1]$ 上等距插入 $n-1$ 个点，将它等分成 $n$ 个小区间：  

  $[0,\frac{1}{n}],[\frac{1}{n},\frac{2}{n}],\cdots,[\frac{n-1}{n},1]$  

  区间长： $\vartriangle\!x=\frac{1}{n}$  
  第 $i$ 个矩形的高： $h_i=(\frac{i}{n})^2$
  第 $i$ 个矩形的面积： $s_i=(\frac{i}{n})^2\frac{1}{n}\qquad i=1,2,\cdots,n$  
  $$\begin{align*}S_n&=(\frac{1}{n})^2\cdot\frac{1}{n}+(\frac{2}{n})^2\cdot\frac{1}{n}+\cdots+(\frac{n-1}{n})^2\cdot\frac{1}{n}+(\frac{n}{n})^2\cdot\frac{1}{n}\\&=\frac{1}{n^3}[1^2+2^2+\cdots+(n-1)^2+n^2]\\&=\frac{1}{6}(1+\frac{1}{n})(2+\frac{1}{n})\end{align*}$$  
  
  $$S=\lim\limits_{n\to\infty}S_n=\lim\limits_{n\to\infty}\frac{1}{6}(1+\frac{1}{n})(2+\frac{1}{n})=\frac{1}{3}$$

### 切线问题  
- 圆的切线  
- 曲线的切线 曲线在 $P$ 的切线 $k=\lim\limits_{Q\to P}k_{QP}$
### 变速直线运动的瞬时速度问题  
$s(t)=\frac{1}{2}gt^2$  
考虑在 $[t_0,t_0+\vartriangle \! t]$ 时间内的运动
$\overline{v}=\dfrac{\vartriangle\!s}{\vartriangle\!t}$  
作业1-1
## 函数
### 函数的概念  
#### 集合
集合简称集 元素简称元  
记作 $a\in M$  
$Q=\{ x|x=\frac{p}{q},\;p,q\in Z \}$  
并集 $A\cup B$  
交集 $A\cap B$  
差集 $A\backslash B=\{ x|x\in A \ \&\ x\notin B \}$  
余集 $B^c_A=\complement_AB=A\backslash B\,(B\subset A)$  
直积 $A\times B =\{(x,y)|\;x\in A,\,y\in B\}$  
**特例** $R\times R\overset{简记}{=}R^2$ 为平面上的全体点集  
#### 区间与邻域  
开区间 闭区间 半开区间 有限区间 无限区间  
##### 邻域  
> 设 $a$ 与 $\delta$ 是两个实数，且 $\delta>0$ ，数集 $\{x|\left|x-a\right|<\delta\}$ 称为点 $a$ 的 $\delta$ 邻域，点 $a$ 叫做邻域的中心， $\delta$ 叫做邻域的半径  
> 
$U(a,\delta)=\{x|a-\delta<x<a+\delta\}$  
点 $a$ 的 $\delta$ 去心邻域  
$U^0(a,\delta)=\{x|0<|x-a|<\delta\}$  
点 $a$ 的 $\delta$ 左邻域  $\{x|a-\delta<x<a\}$  
点 $a$ 的 $\delta$ 右邻域  $\{x|a<x<a+\delta\}$ 
> 
#### 绝对值  
运算性质  
$||a|-|b||\le|a\pm b|\le|a|+|b|$  

#### 函数的概念  
> 定义：设 $X,Y$ 是两个数集，如果 $\forall x\in X,\exist y\in Y$ 按照法则 $f$ 与之对应，则称 $y$ 是 $x$ 的函数，记作  
$$y=f(x),x\in X$$  
定义域（Domain）记作 $D_f$  
值域（Range） 记作  $R_f=f(X)=\{y|y=f(x),x\in X\}$  
函数两要素：定义域 对应法则  
> 如果自变量在定义域内任取一个数值时，对应的函数值总是只有一个，这种函数叫做**单值函数**，否则叫**多值函数**  
> 如果两个函数的定义域和对应关系完全一样，则我们就称两个函数相等  
> 注：使函数有意义的自变量的全体称为函数的自然定义域，简称**定义域**
#### 函数的三种表示法  
解析法 表格法 图示法
#### 几个特殊的函数  
符号函数
$y=\operatorname{sgn} x=\begin{cases}
  1&x>0\\0&x=0\\-1&x<0
\end{cases}\qquad\forall x\in R,\;x=\operatorname{sgn}x\cdot|x|$  
取整函数
$y=[x]\qquad[x]$ 表示不超过 $x$ 的最大整数  
狄利克雷函数
$y=D(x)=\begin{cases}
  1&当x是有理数时\\0&当x是无理数时
\end{cases}$
### 函数的几种特性  
#### 函数的有界性  
> 设 $f(x)$ 在数集 $X$ 上有定义，若 $\exist M>0, \forall x\in X$ ，使 $|f(x)|\le M$ 成立，则称函数 $f(x)$ 在 $X$ 上有界，否则称无界  
#### 函数的单调性  
单调增加 严格单调增加  
单调减少 严格单调减少  
#### 函数的奇偶性  
> 设数集 $X$ 关于 **原点对称** ，对于 $\forall x\in X$ ，有 $f(-x)=f(x)$ ，称 $f(x)$ 为偶函数  
> 设数集 $X$ 关于 **原点对称** ，对于 $\forall x\in X$ ，有 $f(-x)=-f(x)$ ，称 $f(x)$ 为奇函数
#### 函数的周期性  
> $\exist T \not ={0},\forall x,x+T\in X$ ，恒有 $f(x+T)=f(x)$ 则称 $f(x)$ 为周期函数， $T$ 称为 $f(x)$ 的周期  
### 函数的延拓  
> 一般的，如果 $D_g\subset D_f$ ，当 $x\in D_g$ 时，有 $f(x)=g(x)$ ，则称 $f(x)$ 是函数 $g(x)$ 的延拓。  
### 反函数  
> 对于函数 $y=f(x)$ ，若变量 $y$ 在函数的值域内任取一值 $y_0$ 时，变量 $x$ 在函数的定义域内必有唯一的 $x_0$ 与之对应，即 $f(x_0)=y_0$ ，那么变量 $x$ 就是变量 $y$ 的函数。  
> 这个函数用 $x=f^{-1}(y)$ 表示，称为函数 $y=f(x)$ 的
反函数。  

$y=f(x)\quad(x\in D)$ 的反函数 $x=f^{-1}(y)$ 记为  
$$y=f^{-1}(x)\qquad(x\in f(D))$$  
> 定理 设 $y=f(x)$ 在 $X$ 上严格单调增加（或减少），则必存在反函数 $x=f^{-1}(y)$ ，它在 $f(X)$ 上也严格单调增加（或减少）。  

> 注1 函数严格单调仅是存在反函数的充分条件，而不是必要条件。  
> 注2 函数存在反函数与否跟讨论的定义区间有关。  

#### 函数及其反函数的图像  
> $y=f(x)$ 与 $y=f^{-1}(x)$ 的图像关于直线 $y=x$ 互相对称。  

若点 $M(x,y)$ 在曲线 $y=f(x)$ （即 $x=f^{-1}(y)$ ）上，则点 $M'(y,x)$ 在反函数 $y=f^{-1}(x)$ 上。
### 复合函数  
> 定义 设 $y=f(u)$ 是 $u$ 的函数，而 $u=\varphi(x)$ 又是 $x$ 的函数，且 $\varphi(x)$ 的值域的全部或部分在 $f(u)$ 的定义域内，那么 $y$ 通过 $u$ 的联系也是 $x$ 的函数，我们称 $y$ 关于 $x$ 的函数是由 $y=f(u)$ 及 $u=\varphi(x)$ 复合而成的函数,简称复合函数. 记作 $y=f[\varphi(x)]$ ， $u$ 为中间变量。

> 注1 $f(u)$ 与 $\varphi(x)$ 可以复合的条件是：  
> $R_\varphi\subseteq D_f$ ，即 $u=\varphi(x)$ 的值域包含在 $y=f(u)$ 的定义域内。