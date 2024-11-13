# 高等数学II-1

胡小兵 <iamhxb@cqu.edu.cn>  
助教：熊若兰 tel: 13872442250 <ruolanx100@163.com>  

Sep. 30th, 2024 课程介绍、微积分的一些基本问题  

> 成绩构成：  
> 期中 $20\%+$ 期末 $55\% +$ 考勤 $5\% +$ 作业 $10\% +$ Easylearning助学平台 $10\%$  

Oct. 9th, 2024  切换为学堂在线  
成绩构成变化  
期中 $20\%+$ 期末 $55\% +$ 考勤 $10\% +$ 作业 $10\% +$ 学堂在线 $5\%$  

## 极限论

### 微积分的一些基本问题

#### 面积问题

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

#### 切线问题  

- 圆的切线  
- 曲线的切线 曲线在 $P$ 的切线 $k=\lim\limits_{Q\to P}k_{QP}$

#### 变速直线运动的瞬时速度问题  

$s(t)=\frac{1}{2}gt^2$  
考虑在 $[t_0,t_0+\vartriangle \! t]$ 时间内的运动
$\overline{v}=\dfrac{\vartriangle\!s}{\vartriangle\!t}$  
作业1-1

### 函数

#### 函数的概念  

##### 集合

集合简称集 元素简称元  
记作 $a\in M$  
$Q=\{ x|x=\frac{p}{q},\;p,q\in Z \}$  
并集 $A\cup B$  
交集 $A\cap B$  
差集 $A\backslash B=\{ x|x\in A \ \&\ x\notin B \}$  
余集 $B^c_A=\complement_AB=A\backslash B\,(B\subset A)$  
直积 $A\times B =\{(x,y)|\;x\in A,\,y\in B\}$  
**特例** $R\times R\overset{简记}{=}R^2$ 为平面上的全体点集  

##### 区间与邻域  

开区间 闭区间 半开区间 有限区间 无限区间  

###### 邻域  
>
> 设 $a$ 与 $\delta$ 是两个实数，且 $\delta>0$ ，数集 $\{x|\left|x-a\right|<\delta\}$ 称为点 $a$ 的 $\delta$ 邻域，点 $a$ 叫做邻域的中心， $\delta$ 叫做邻域的半径  
>
$U(a,\delta)=\{x|a-\delta<x<a+\delta\}$  
点 $a$ 的 $\delta$ 去心邻域  
$U^0(a,\delta)=\{x|0<|x-a|<\delta\}$  
点 $a$ 的 $\delta$ 左邻域  $\{x|a-\delta<x<a\}$  
点 $a$ 的 $\delta$ 右邻域  $\{x|a<x<a+\delta\}$
>
##### 绝对值  

运算性质  
$||a|-|b||\le|a\pm b|\le|a|+|b|$  

##### 函数概念  

> 定义：设 $X,Y$ 是两个数集，如果 $\forall x\in X,\exist y\in Y$ 按照法则 $f$ 与之对应，则称 $y$ 是 $x$ 的函数，记作  
$$y=f(x),x\in X$$  
定义域（Domain）记作 $D_f$  
值域（Range） 记作  $R_f=f(X)=\{y|y=f(x),x\in X\}$  
函数两要素：定义域 对应法则  
> 如果自变量在定义域内任取一个数值时，对应的函数值总是只有一个，这种函数叫做**单值函数**，否则叫**多值函数**  
> 如果两个函数的定义域和对应关系完全一样，则我们就称两个函数相等  
> 注：使函数有意义的自变量的全体称为函数的自然定义域，简称**定义域**
>
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

#### 函数的几种特性  

##### 函数的有界性  
>
> 设 $f(x)$ 在数集 $X$ 上有定义，若 $\exist M>0, \forall x\in X$ ，使 $|f(x)|\le M$ 成立，则称函数 $f(x)$ 在 $X$ 上有界，否则称无界  
>
##### 函数的单调性  

单调增加 严格单调增加  
单调减少 严格单调减少  

##### 函数的奇偶性  

> 设数集 $X$ 关于 **原点对称** ，对于 $\forall x\in X$ ，有 $f(-x)=f(x)$ ，称 $f(x)$ 为偶函数  
> 设数集 $X$ 关于 **原点对称** ，对于 $\forall x\in X$ ，有 $f(-x)=-f(x)$ ，称 $f(x)$ 为奇函数

##### 函数的周期性  

> $\exist T \not ={0},\forall x,x+T\in X$ ，恒有 $f(x+T)=f(x)$ 则称 $f(x)$ 为周期函数， $T$ 称为 $f(x)$ 的周期  

#### 函数的延拓  

> 一般的，如果 $D_g\subset D_f$ ，当 $x\in D_g$ 时，有 $f(x)=g(x)$ ，则称 $f(x)$ 是函数 $g(x)$ 的延拓。  

#### 反函数  

> 对于函数 $y=f(x)$ ，若变量 $y$ 在函数的值域内任取一值 $y_0$ 时，变量 $x$ 在函数的定义域内必有唯一的 $x_0$ 与之对应，即 $f(x_0)=y_0$ ，那么变量 $x$ 就是变量 $y$ 的函数。  
> 这个函数用 $x=f^{-1}(y)$ 表示，称为函数 $y=f(x)$ 的
反函数。  

$y=f(x)\quad(x\in D)$ 的反函数 $x=f^{-1}(y)$ 记为  
$$y=f^{-1}(x)\qquad(x\in f(D))$$  
> 定理 设 $y=f(x)$ 在 $X$ 上严格单调增加（或减少），则必存在反函数 $x=f^{-1}(y)$ ，它在 $f(X)$ 上也严格单调增加（或减少）。  
> 注1 函数严格单调仅是存在反函数的充分条件，而不是必要条件。  
> 注2 函数存在反函数与否跟讨论的定义区间有关。  

##### 函数及其反函数的图像  

> $y=f(x)$ 与 $y=f^{-1}(x)$ 的图像关于直线 $y=x$ 互相对称。  

若点 $M(x,y)$ 在曲线 $y=f(x)$ （即 $x=f^{-1}(y)$ ）上，则点 $M'(y,x)$ 在反函数 $y=f^{-1}(x)$ 上。

#### 复合函数  

> 定义 设 $y=f(u)$ 是 $u$ 的函数，而 $u=\varphi(x)$ 又是 $x$ 的函数，且 $\varphi(x)$ 的值域的全部或部分在 $f(u)$ 的定义域内，那么 $y$ 通过 $u$ 的联系也是 $x$ 的函数，我们称 $y$ 关于 $x$ 的函数是由 $y=f(u)$ 及 $u=\varphi(x)$ 复合而成的函数,简称复合函数. 记作 $y=f[\varphi(x)]$ ， $u$ 为中间变量。  
> 注1 $f(u)$ 与 $\varphi(x)$ 可以复合的条件是：  
  $R_\varphi\subseteq D_f$ ，即 $u=\varphi(x)$ 的值域包含在 $y=f(u)$ 的定义域内。

#### 基本初等函数  

##### 反三角函数  

反正弦函数 $y=\arcsin x\quad D=[-1,1],R=[-\dfrac{\pi}{2},\dfrac{\pi}{2}]$ 单调递增  
反余弦函数 $y=\arccos x\quad D=[-1,1],R=[0,\pi]$ 单调递减  
反正切函数 $y=\arctan x\quad D=R,R=[-\dfrac{\pi}{2},\dfrac{\pi}{2}]$ 单调递增  

##### 双曲函数  

双曲正弦 $\sh x=\sinh x=\dfrac{e^x-e^{-x}}{2}\quad D=(-\infty,+\infty)$ 奇函数，单调递增  
双曲余弦 $\ch x=\cosh x=\dfrac{e^x+e^{-x}}{2}\quad D=(-\infty,+\infty)$ 偶函数  
$y=\frac{1}{2}e^x,y=\frac{1}{2}e^x$ 渐近线  
双曲正切函数 $\th x=\tanh x=\dfrac{\sh x}{\ch x}=\dfrac{e^x-e^{-x}}{e^x+e^{-x}}\quad D$ 奇函数，有界函数  
$y=\pm1$ 渐近线

> 凡是由常数和基本初等函数经过**有限次四则运算**及**有限次的函数复合**所构成并可用**一个式子表示**的函数，称为**初等函数**。  

### 数列的极限  

#### 数列极限的定义  

##### 数列

> 数列是按次序排列的一列无穷多个数  
> 数列是定义在正整数集 $N^+$ 上的函数

考察数列 $\left\{1+\dfrac{(-1)^{n-1}}{n}\right\}$  
定量分析 $\left\{1+\dfrac{(-1)^{n-1}}{n}\right\}$ 无限接近 $1$  
当 $n$ 充分大时$\left|1+\dfrac{(-1)^{n-1}}{n}-1\right|$ 能任意小，即 $\dfrac{1}{n}$ 能任意小  
对 $\forall\epsilon>0$ ，总 $\exist N=\left[\dfrac{1}{\epsilon}\right]$ ，当 $n>N$ 时，满足$\left|1+\dfrac{(-1)^{n-1}}{n}-1\right|<\epsilon$ ，则称 $1$ 为数列 $\left\{1+\dfrac{(-1)^{n-1}}{n}\right\}$ 的极限

一般化
> 数列极限定义 设数列 $\{x_n\}$ ， $a$ 是实数，若对 $\forall\epsilon>0$ 总 $\exist正整数N$ ，当 $n>N$ 时，便有 $|x_n-a|<\epsilon$ ，则称数列 $\{x_n\}$ 存在极限 $a$ ，或称 $\{x_n\}$ 收敛于 $a$  
> 记为  

即  
$\lim\limits_{n\rightarrow\infty}x_n=a\Leftrightarrow\forall\epsilon>0,\exist N,当n>N时，有|x_n-a|<\epsilon$

利用 $\epsilon\text{-}N$ 定义证明 $\lim\limits_{n\rightarrow\infty}\dfrac{n+(-1)^{n-1}}{n}=1$  
证： $|x_n-1|=\left|\dfrac{n+(-1)^{n-1}}{n}-1\right|=\dfrac{1}{n}$  
任给 $\epsilon>0$ ，要 $|x_n-1|<\epsilon$ ，只要 $\dfrac{1}{n}<\epsilon$ ，解得 $n>\dfrac{1}{\epsilon}$

$\lim\limits_{n\rightarrow\infty}\sqrt[n]{a}=1\ (a>0)$  
证：分三种情况证明  

1. 当 $a>1$ 时  
   - $\sqrt[n]{a}$
   令 $\sqrt[n]{a}=1+\alpha_n\ (\alpha_n>0)$ ，则  
   - $a=(1+\alpha_n)^n>1+n\alpha_n$ ，得 $\alpha_n<\dfrac{a-1}{n}$  
   $|\sqrt{a}-1|=\alpha_n<\dfrac{a-1}{n}<\epsilon$
2. 当 $0<a<1$ 时，令 $\dfrac{1}{a}=b>1$ ，有 $\lim\limits_{n\rightarrow\infty}\sqrt[n]{b_n}=1$
3. 当  $a=1$ 时，对 $\forall n,\sqrt[n]{a}=1$

##### 数列极限的几何解释  

对邻域 $U(a,\epsilon)$ ，总存在项 $x_N$ 使第 $N$ 项以后的所有项 $x_{N+1},x_{N+2},\cdots$ 全部位于邻域外

$\lim\limits_{x\rightarrow\infty}x_n=a$  
$\Leftrightarrow$ 对于 $\forall$ 邻域 $U(a,\epsilon)$ ，总 $\exist N$ ，当 $n>N$ 时，有 $x_n\in U(a,\epsilon)$  
$\Leftrightarrow$ 对于 $\forall\epsilon>0$ ，只有有限项 $x_n$ 位于邻域 $U(a,\epsilon)$ 外  

例  
$\lim\limits_{n\rightarrow\infty}\sqrt[n]{n}=1$  
证：令 $\sqrt[n]{n}-1=h_n$ ，即 $\sqrt[n]{n}=1+h_n$ ，则  
$n=(1+h_n)^n=1+nh_n+\dfrac{n(n-1)}{2!}h_n^2+\cdots+h_n^n>1+\dfrac{n(n-1)}{2!}h_n^2\quad(n\ge2)$

#### 收敛数列的性质  

> 定理 收敛数列的极限唯一  
>
证：用反证法，假设 $\lim\limits_{n\rightarrow\infty}x_n=a$ 及 $\lim\limits_{n\rightarrow\infty}x_n=a$ 且 $a<b$  
取 $\epsilon=\frac{b-a}{2}$ ，因 $\lim\limits_{n\rightarrow\infty}x_n=a$ ，故 $\exist N_1$ ，使当 $n>N_1$ 时， $|x_n-a|<\frac{b-a}{2}$ ，从而 $x_n<\frac{a+b}{2}$  
同理，因 $\lim\limits_{n\rightarrow\infty}x_n=b$ ，故 $\exist N_2$ ，使当 $n>N_2$ 时， $|x_n-b|<\frac{b-a}{2}$ ，从而 $x_n>\frac{a+b}{2}$  

> 数列有界定义 对数列 $\{x_n\}$ ，若 $\exist M\in R$ ，使 $x_n\le M\quad n=1,2,3,\cdots$ 则称 $M$ 为数列 $\{x_n\}$ 的上界；若 $\exist M\in R$ ，使 $x_n\ge M\quad n=1,2,3,\cdots$ 则称 $M$ 为数列 $\{x_n\}$ 的下界。  
> 定理 **收敛数列一定有界**  

aaa

> 定理 **收敛数列的比较性质**  

若 $\lim\limits_{n\rightarrow\infty}x_n=a,$  

>推论1（保号性） 若$\lim\limits_{n\rightarrow\infty}x_n=a\quad a>0$ ，则 $\exist$ 正整数 $N$ ，当 $n>N$ 时，有 $x_n>0$ 。  
证：令 $y_n=0\quad n=1,2,\cdots$  
推论2 若$\lim\limits_{n\rightarrow\infty}x_n=a\quad\lim\limits_{n\rightarrow\infty}y_n=b$ ，且  

#### 子数列（子列）  

在数列 $\{x_n\}$ 中任意取无限多项，并保持这些项在原数列 $\{x_n\}$ 中的次序，由此得到的数列称为 $\{x_n\}$ 的子列，记为$\{x_{n_k}\}$  
> 注： $x_{n_k}$ $\{x_{n—_k}\}$ 中的第 $k$ 项，是 $\{x_n\}$ 中的第 $n_k$ 项
> 定理 收敛数列的任一子列收敛于同一极限

证  

#### 数列极限的运算性质  

定理 若 $\lim\limits_{n\rightarrow\infty}x_n=a,\ \lim\limits_{n\rightarrow\infty}y_n=b$ 则  

1. $\lim\limits_{n\rightarrow\infty}(x_n\pm y_n)=\lim\limits_{n\rightarrow\infty}x_n\pm\lim\limits_{n\rightarrow\infty}y_n=a\pm b$  
2. $\lim\limits_{n\rightarrow\infty}(x_n\cdot y_n)=\lim\limits_{n\rightarrow\infty}x_n\cdot\lim\limits_{n\rightarrow\infty}y_n=a\cdot b$
3. $\lim\limits_{n\rightarrow\infty}\dfrac{x_n}{y_n}=\dfrac{\lim\limits_{n\rightarrow\infty}x_n}{\lim\limits_{n\rightarrow\infty}y_n}=a\pm b$  

#### 数列极限夹逼准则  

> 定理 若数列 $\{x_n\},\{y_n\},\{z_n\}$ 满足下列条件：  
>
> 1. $\exist N\in N^+$ ，当 $n>N_0$ 时，有： $y_n\le x_n\le z_n$  
> 2. $\lim\limits_{n\rightarrow\infty}y_n=\lim\limits_{n\rightarrow\infty}z_n=a$  
>
> 则数列 $x_n$ 的极限存在，且 $\lim\limits_{n\rightarrow\infty}x_n=a$

#### 单调有界准则  

> 定理 单调有界数列必有极限  
> 定义（上确界）： 给定一个实数集 $E$ ，如果 $\exist$ 实数 $M$ 满足：  
>
> 1. $\forall x\in E$ ，都有 $x\le M$  
> 2. $\forall\epsilon>0,\quad\exist y\in E$ ，使得 $y>M-\epsilon$  
>
> 则称M为集合 $E$ 的上确界  
> 定理 若实数集 $E$ 有上界，则必有**上确界**  

### 函数的极限  

#### 自变量趋于某个值时

> 设 $f(x)$ 在 $x_0$
>
> 单侧极限  
>
> 定理
> $\lim\limits_{x\rightarrow x_0}f(x)=A\Leftrightarrow\lim\limits_{x\rightarrow x_0^-}f(x)=\lim\limits_{x\rightarrow x_0^+}f(x)=A$  
>
> 1. 若 $\lim\limits_{x\rightarrow x_0^-}f(x)$ 和 $\lim\limits_{x\rightarrow x_0^+}f(x)$ 中至少一个不存在，则 $\lim\limits_{x\rightarrow x_0}f(x)$ 不存在
> 2. 若 $\lim\limits_{x\rightarrow x_0^-}f(x)\not ={}\lim\limits_{x\rightarrow x_0^+}f(x)$ ，则 $\lim\limits_{x\rightarrow x_0}f(x)$ 不存在  

#### 自变量趋向无穷大时函数的极限  

##### 正无穷  

> 定义 设 $f(x)$ 在 $x>a\quad a>0$ 使有定义，对于 $\forall\epsilon>0,\quad\exist X>0$ ，当 $x>X$ 时，恒有 $|f(x)-A|<\epsilon$
>
> 几何意义  
> 对于 $\forall\epsilon>0,\quad\exist X>0$ ，当 $x>X$ 使，函数 $y=f(x)$ 的图形完全落在以直线 $y=A$ 未中心线，宽为 $2\epsilon$ 的带型区域内  

##### 负无穷

> 定义 设 $f(x)$ 在 $x>a\quad a>0$ 使有定义，对于 $\forall\epsilon>0,\quad\exist X>0$ ，当 $x<-X$ 时，恒有 $|f(x)-A|<\epsilon$
>
> 几何意义  
> 对于 $\forall\epsilon>0,\quad\exist X>0$ ，当 $x<-X$ 使，函数 $y=f(x)$ 的图形完全落在以直线 $y=A$ 未中心线，宽为 $2\epsilon$ 的带型区域内  
>
##### 无穷大  

> 定义 设 $f(x)$ 在 $x>a\quad a>0$ 使有定义，对于 $\forall\epsilon>0,\quad\exist X>0$ ，当 $|x|>X$ 时，恒有 $|f(x)-A|<\epsilon$
>
> 几何意义  
> 对于 $\forall\epsilon>0,\quad\exist X>0$ ，当 $|x|>X$ 使，函数 $y=f(x)$ 的图形完全落在以直线 $y=A$ 未中心线，宽为 $2\epsilon$ 的带型区域内  
>
> 定理
> $\lim\limits_{x\rightarrow\infty}f(x)\Leftrightarrow\lim\limits_{x\rightarrow+\infty}f(x),\lim\limits_{x\rightarrow-\infty}f(x)$  
>

##### 水平渐近线  

> 如果 $\lim\limits_{x\rightarrow+\infty}f(x)=c$ 或 $\lim\limits_{x\rightarrow-\infty}f(x)=c$ ，则称直线 $y=c$ 是函数 $y=f(x)$ 的图形的水平渐近线  
>

#### 函数极限的性质

##### 唯一性

> 若函数 $f(x)$ 的极限存在，则该极限是唯一的
>

##### 局部有界性

> 定理 若 $\lim\limits_{x\rightarrow x_0}f(x)$ 存在，则函数 $f(x)$ 在点 $x_0$ 的某个去心邻域内有界。  
>

##### 局部保号性  

> 定理 设函数 $f(x)$ 在 $\mathring{U}(x_0,\delta_1)$ 内有定义，且 $\lim\limits_{x\rightarrow x_0}f(x)=A>0$ （或 $A<0$ ），则 $\exist\delta_1>\delta>0$  
> 当 $0<|x-x_0|<\delta$ 时，有 $f(x)>0$ （或 $f(x)<0$ ）  
>
> 推论1 设函数 $f(x),g(x)$ 在 $\mathring{U}(x_0,\delta_1)$ 内有定义， $\lim\limits_{x\rightarrow x_0}f(x)=A,\lim\limits_{x\rightarrow x_0}g(x)=b$ 且 $A>B$ 则 $\exist\delta>0$ ，当 $0<|x-x_0|<\delta$ 时，有 $f(x)>g(x)$  
> 推论2 设在 $x_0$ 的某去心邻域内， $f(x)\ge g(x)$ 且 $\lim\limits_{x\rightarrow x_0}f(x)=A,\lim\limits_{x\rightarrow x_0}g(x)=B$ ，则 $A\ge B$  
>
> 定理（复合函数的极限定理） 设 $\lim\limits_{u\rightarrow u_0}f(u)=f(u_0),u=f(x)$ 且 $u_0=\lim\limits_{x\rightarrow x_0}g(x)$ ，则 $\lim\limits_{x\rightarrow x_0}f[g(x)]=f[\lim\limits_{x\rightarrow x_0}g(x)]=f(u_0)$  

##### 函数极限夹逼准则

#### 函数极限与数列极限的关系

#### 函数极限的运算性质  

四则运算

#### 两个重要极限  

1. $\lim\limits_{x\rightarrow0}\dfrac{\sin x}{x}=1$  
 设单位圆 $O$ ，圆心角 $AOB=x$ ， $(0<x<\dfrac{\pi}{2})$ ，过 $A$ 点做单位圆的切线，得 $\vartriangle\!ACO$ 。  
 扇形 $OAB$ 的圆心角为 $x$ ， $\vartriangle\!OAB$ 的高为 $BD$ ，则 $S_{\vartriangle OAB}<S_{扇形OAB}<S_{\vartriangle OAC}\Rightarrow\frac{1}{2}\sin x<\frac{1}{2}x<\frac{1}{2}\tan x\Rightarrow\cos x<\dfrac{\sin x}{x}<1(0<|x|<\dfrac{\pi}{2})$  
 $\lim\limits_{x\rightarrow0}\cos x=1,\lim\limits_{x\rightarrow0}=1\Rightarrow\lim\limits_{x\rightarrow0}\dfrac{\sin x}{x}=1$
2. $\lim\limits_{x\rightarrow\infty}(1+\dfrac{1}{x})^x=e$  
  先证 $\lim\limits_{x\rightarrow+\infty}(1+\dfrac{1}{x})^x=e$  
  当 $x\in R^+$ 时，总 $\exist n\in N^+$ ，满足： $n\le x<n+1$  
  当 $x\ge1$ 时，$(1+\dfrac{1}{n+1})<(1+\dfrac{1}{x})\le(1+\dfrac{1}{n})$
  再证； $\lim\limits_{x\rightarrow-\infty}(1+\dfrac{1}{x})^x=e$  
  令 $t=-x$ 则 $\lim\limits_{x\rightarrow-\infty}(1+\dfrac{1}{x})^x=\lim\limits_{t\rightarrow+\infty}(1-\dfrac{1}{t})^{-t}=\lim\limits_{t\rightarrow+\infty}(\dfrac{t}{t-1})^t=\lim\limits_{t\rightarrow+\infty}(1+\dfrac{1}{t-1})^t=\lim\limits_{t\rightarrow+\infty}(1+\dfrac{1}{t-1})^{t-1}(1+\dfrac{1}{t-1})=\lim\limits_{t\rightarrow+\infty}(1+\dfrac{1}{t-1})^{t-1}\cdot\lim\limits_{t\rightarrow+\infty}(1+\dfrac{1}{t-1})=e$  
  综上
  $$\lim\limits_{x\rightarrow\infty}\left(1+\dfrac{1}{x}\right)^x=e$$  
  推广 $\lim\limits_{x\rightarrow x_0}\left(1+\dfrac{1}{\varPhi(x)}\right)^{\varPhi(x)}=e$ 其中 $\lim\limits_{x\rightarrow x_0}\varPhi(x)=\infty$  
  令 $t=\dfrac{1}{x}$
  $$\lim\limits_{x\rightarrow0}(1+x)^\frac{1}{x}=e$$  
  推广 $\lim\limits_{x\rightarrow x_0}(1+\varPhi(x))^\frac{1}{\varPhi(x)}=e$ 其中 $\lim\limits_{x\rightarrow x_0}\varPhi(x)=0$

### 无穷大量与无穷小量

#### 无穷小量

> 定义 在自变量的某一变化过程中，极限为0的函数或者数列，称为**无穷小量**，简称无穷小。
>
> 1. 如果 $\forall\epsilon>0,\quad\exist\delta=\delta(\epsilon)>0$ ，当 $0<|x-x_0|<\epsilon$ 时
> 2. 如果 $\forall\epsilon>0,\quad X=X(\epsilon)>0$ ，当 $|x|>X$ 时，恒有  
> $$|f(x)|<\epsilon$$  
> 则称函数 $f(x)$ 为当 $x\rightarrow\infty$ 时的无穷小量。
>
##### 无穷小量与极限的关系  

> 定理 $\lim\limits_{x\rightarrow x_0}f(x)=A\Leftrightarrow f(x)=A+\alpha$ 其中， $\alpha$ 是当 $x\rightarrow x_0$ 时的无穷小量。  
>
> 定理 有限个无穷小量的和仍是无穷小量
>
> 定理 有界变量与无穷小量的乘积仍是无穷小量

#### 无穷大量  

在自变量的某一变化过程中，函数的绝对值无线变大的量，称为**无穷大量**，简称**无穷大**。  
> 定义 如果对于任意给定的整数 $M,\;\exist\delta>0$  
>
> 定义 垂直/铅直渐近线

#### 无穷小与无穷大的关系

> 定理 在自变量的同一个变化过程中：  
>
> 1. 若 $f(x)$ 是无穷小量，且 $f(x)\not ={0}$ ，则 $1/f(x)$ 是无穷大量  
> 2. 若 $f(x)$ 是无穷大量，则 $1/f(x)$ 是无穷小量  

证明无穷大量，可以先证明这个量的倒数为无穷小量  

一般有以下结论  
$$\lim\limits_{x\rightarrow\infty}\dfrac{a_0x^m+a_1x^{m-1}+\cdots+a_m}{b_0x^n+b_1x^{n-1}+\cdots+b_n}=\begin{cases}
  \dfrac{a_0}{b_0}&n=m\\0&n>m\\\infty&n<m
\end{cases}$$  

#### 无穷小量的比较

> 定义 设 $\alpha(x),\beta(x)$ 是同一过程中的两个无穷小，且 $\alpha(x)\not ={0}$  
> 1. 如果 $\lim\dfrac{\beta(x)}{\alpha(x)}$  
> 1. 如果 $\lim\dfrac{\beta(x)}{\alpha(x)}$
> 1. 如果 $\lim\dfrac{\beta(x)}{\alpha(x)}$
> 4. 如果 $\lim\dfrac{\beta(x)}{\alpha(x)}=1$ ，则称 $\beta(x)$ 与 $\alpha(x)$ 是**等价无穷小**，记作 $\alpha(x)\sim\beta(x)$
> 5. 如果 $\lim\dfrac{\beta(x)}{\alpha(x)^k}=C(C\not ={0},k>0)$ ，则称 $\beta(x)$ 与 $\alpha(x)$ 是 $k$ 阶无穷小
>
> 定理 等价无穷小替换定理 设 $\alpha(x),\beta(x)$ 是同一过程中的两个无穷小，且 $\alpha(x)\not ={0}$ 如果 $\alpha(x)\sim\alpha^\prime(x),\beta(x)\sim\beta^\prime(x)$ 且 $\lim\dfrac{\beta^\prime(x)}{\alpha^\prime(x)}$ 存在，则 $\lim\dfrac{\beta(x)}{\alpha(x)}=\lim\dfrac{\beta^\prime(x)}{\alpha^\prime(x)}$  
> 证 $\lim\dfrac{\beta(x)}{\alpha(x)}=\lim\left(\dfrac{\beta(x)}{\beta^\prime(x)}\cdot\dfrac{\beta^\prime(x)}{\alpha^\prime(x)}\cdot\dfrac{\alpha^\prime(x)}{\alpha(x)}\right)$

### 函数的连续性

#### 连续函数的概念

##### 函数的增量

设函数 $f(x)$ 在 $U(x_0,\delta)$ 内有定义， $\forall x\in U(x_0,\delta),\varDelta x=x-x_0$ 称为自变量 $x$ 在点 $x_0$ 的增量， $\varDelta y=f(x)-f(x_0)=f(x_0+\varDelta x)-f(x_0)$ 称为  

#### 函数连续的定义

> 定义1 设函数 $f(x)$ 在点 $x_0$
>
> 定义2 设函数 $f(x)$ 在点 $x_0$ 的某一个领域内有定义，如果  
> $$\lim\limits_{x\rightarrow x_0}f(x)=f(x_0)$$  
> 那么就称函数 $y=f(x)$ 在点 $x_0$ 连续
>
> 定义3 函数 $f(x)$ 在点 $x_0$ 连续 $\Leftrightarrow$ $\forall x$  

函数 $f(x)$ 在点 $x_0$ 处连续必须满足的三个条件
1. $f(x)$ 在点 $x_0$ 处有定义
2. $\lim\limits_{x\rightarrow x_0}f(x)$ 存在
3. $\lim\limits_{x\rightarrow x_0}f(x)=f(x_0)$

如果上述三个条件中只有有一个不满足，则函数 $f(x)$ 在点 $s_0$ 处不连续（间断）  

##### 单侧连续  

> 定义 若函数 $f(x)$ 在 $x_0-\delta<x\le x_0$ 内有定义，且 $\lim\limits_{x\rightarrow{x_0}^-}f(x)=f(x_0)$ ，则称 $f(x)$ 在点 $x_0$ 处左连续
>
> 定定义 若函数 $f(x)$ 在 $x_0\le x<x_0+\delta$ 内有定义，且 $\lim\limits_{x\rightarrow{x_0}^+}f(x)=f(x_0)$ ，则称 $f(x)$ 在点 $x_0$ 处右连续  
> 定义 若函数 $f(x)$ 在 $x_0\le x<x_0+\delta$ 内有定义， $f(x)$ 在点 $x_0$ 处右连续 $\Leftrightarrow$ $\forall\epsilon>0,\exist\delta>0$  
>
> 定义 函数 $f(x)$ 在 $x_0$ 处连续的充分必要条件是函数 $f(x)$ 在 $x_0$ 处**既左连续又右连续**

##### 连续函数与连续区间

#### 连续函数的运算与初等函数的连续性

##### 连续函数的四则运算

> 定理 若函数 $f(x),g(x)$ 在点 $x_0$ 处连续，则 $f(x)\pm g(x),f(x)\cdot g(x),\dfrac{f(x)}{g(x)}$ 均在点 $x_0$ 处连续
>
##### 反函数的连续性

> 严格单调连续的函数必有连续的反函数

##### 初等函数的连续性

三角函数及反三角函数在他们的定义域内是连续的。  
指数函数 $y=a^x\quad(a>0,a\not ={0})$ 在其定义域内是单调连续的。  

> 定理 基本初等函数在定义域内是连续的  
> 定理 一切初等函数在其**定义区间**内是连续的  
> 定义区间  

例🖋️ 求 $\lim\limits_{x\rightarrow1}\sin\sqrt{e^2-1}$

例🖋️ 求 $\lim\limits_{x\rightarrow0}\dfrac{\sqrt{1+x^2-1}}{x}$  

例🖋️ 考察函数 $f(x)=\lim\limits_{n\rightarrow\infty}\sqrt[n]{1+x^{2n}}$ 在其定义域内的连续性  
解  
当 $|x|=1$ 时， $f(x)=\lim\limits_{n\rightarrow\infty}\sqrt[n]{2}=1$  
当 $0<|x|<1$ 时， $f(x)=\lim\limits_{n\rightarrow\infty}(1+x^{2n})^\frac{1}{n}=\lim\limits_{n\rightarrow\infty}(1+x^{2n})^{\frac{1}{x^{2n}}\frac{x^{2n}}{n}}=\left[\lim\limits_{n\rightarrow\infty}(1+x^{2n})^\frac{1}{x^{2n}}\right]^{\lim\limits_{n\rightarrow\infty}\frac{x^{2n}}{n}}=e^0=1$

#### 函数的间断点

函数 $f(x)$ 在点 $x_0$ 处连续必须满足的三个条件：  

如果上述三个条件有一个不满足，称函数间断

##### 第一类间断点

设点 $x_0$ 为函数 $f(x)$ 的间断点。如果 $f(x)$ 在点 $x_0$ 处的左右极限都存在，则称 $x_0$ 为函数 $f(x)$ 的第一类间断点

可去间断点 如果 $f(x)$ 在点 $x_0$ 处的极限存在，但 $\lim\limits_{x\rightarrow x_0}f(x)\not ={f(x_0)}$ ，或 $f(x)$ 在点 $x_0$ 处无定义，则称点 $x_0$ 为函数 $f(x)$ 的可去间断点
注意 可去间断点只要改变或者补充间断点处函数的定义，则可使其变为连续点。

跳跃间断点 如果 $f(x)$ 在点 $x_0$ 处的左右极限都存在，但 $\lim\limits_{x\rightarrow {x_0}^-}f(x)\not ={\lim\limits_{x\rightarrow {x_0}^+}f(x)}$

##### 第二类间断点

如果 $f(x)$ 在点 $x_0$ 处的左右极限至少有一个不存在，则称点 $x_0$ 为函数 $f(x)$ 的**第二类间断点**

无穷型

震荡型

#### 闭区间上连续函数的性质

> 定义 设函数 $f(x)$ 在区间 $I$ 上有定义，如果 $\exist x_0\in I$ ，使得 $\forall x\in I$ 都有 $f(x)\le f(x_0)$
>
定理 最大值和最小值定理  
> 符号 $C[a,b]$ 表示：  
> > 闭区间 $[a,b]$ 上所有连续函数构成的集合  
>
> $f(x)\in C[a,b]$ 表示；  
> > $f(x)$ 是 $[a,b]$ 上的连续函数
>
> 定理 在闭区间上连续的函数一定有最大值和最小值

若 $f(x)\in C[a,b]$ ，则 $\exist\xi_1,\xi_2\in[a,b]$ ，使得 $\forall x\in[a,b]$ ，有 $f(x)\le f(\xi_1),f(x)\ge f(\xi_2)$  

注意：  
1. 若区间是开区间，定理不一定成立；
2. 若区间内有间断点，定理不一定成立。

> 定理（有界性定理） 在闭区间上连续的函数一定在该区间上有界。

> 定义 如果 $f(x_0)=0$ ，则 $x_0$ 称为函数 $f(x)$ 的**零点**  
> 定理（零点定理） 设函数 $f(x)$ 在闭区间 $[a,b]$ 上连续，且 $f(a)\cdot f(b)<0$ ，则 $\exist\xi\in(a,b)$ ，使得 $f(\xi)=0$  
> 几何解释 连续曲线 $y=f(x)$ 的两个端点位于 $x$ 轴的不同侧，则曲线于 $x$ 轴至少有一个交点。  
>
> 定理（介值定理） 设函数 $f(x)$ 在闭区间 $[a,b]$ 上连续，且 $f(a)\not ={f(b)}$ ，对于介于 $f(a)$ 于 $f(b)$ 之间的任意常数 $c$ ， $\exist\xi\in(a,b)$ ，使得 $f(\xi)=c$  
> 推论 在闭区间上连续的函数必取得介于最大值 $M$ 与最小值 $m$ 之间的任何值  

例🖋️ 设函数 $f(x)$ 在区间 $[a,b]$ 上连续，且 $a\le f(x)\le b$ 。证明在 $[a,b]$ 上至少存在一点 $\xi$ ，使得 $f(\xi)=\xi$ 。  
证  
令 $F(x)=f(x)-x$ ，则 $F(x)$ 在 $[a,b]$ 上连续，  
而 $F(a)=f(a)-a\ge0,\quad F(b)=f(b)-b\le0$ ，  

例🖋️ 设函数 $f(x)\in C[0,1]$ ，且 $f(0)=f(1)$ ，  
证明 $\exist\xi\in[0.\frac{2}{3}]$ ，使得 $f(\xi+\frac{1}{3})=f(\xi)$ 。  
证  
令 $F(x)=f(x+\frac{1}{3})-f(x),\quad\forall x\in[0,\frac{2}{3}],F(x)\in C[0,\frac{2}{3}]$  
$\because F(0)=f(\frac{1}{3})-f(0),F(\frac{1}{3})=f(\frac{2}{3})-f(\frac{1}{3}),F(\frac{2}{3})=f(1)-f(\frac{2}{3})=f(0)-f(\frac{2}{3})$  
$\therefore$

## 导数与微分

### 导数（derivative）的定义

> 定义 设函数 $y=f(x)$ 在点 $x_0$ 的某个领域 $U(x_0,\delta)$ 内有定义，且 $x_0+\vartriangle\!x\in U(x_0,\delta)$ ，若 $\lim\limits_{\vartriangle\!x\rightarrow0}\dfrac{f(x_0+\vartriangle\!x)-f(x_0)}{\triangle\!x}$ 存在

对于人艺 $x\in I$ ，都对应着 $f(x)$ 的

单侧导数
1. 左导数 $f^\prime_-(x_0)=\lim\limits_{\vartriangle\!x\rightarrow0^-}\dfrac{f(x_0+\vartriangle\!x)-f(x_0)}{\vartriangle\! x}=\lim\limits_{x\rightarrow{x_0}^-}\dfrac{f(x)-f(x_0)}{x-x_0}$
2. 右导数 $f^\prime_-(x_0)=\lim\limits_{\vartriangle\!x\rightarrow0^+}\dfrac{f(x_0+\vartriangle\!x)-f(x_0)}{\vartriangle\! x}=\lim\limits_{x\rightarrow{x_0}^+}\dfrac{f(x)-f(x_0)}{x-x_0}$  

> 定理 函数 $f(x)$ 在 $x_0$ 处可导 $\Leftrightarrow$ 左导数 $f^\prime_-(x_0)$ 与右导数 $f^\prime_+(x_0)$ 均存在且相等
>
> 定义 如果 $f(x_0)$ 在开区间 $(a,b)$ 内可导，且 $f^\prime_+(a)$ 和$f^\prime_-(b)$ 都存在，则说 $f(x)$ 在闭区间 $[a,b]$ 上都可导

### 由定义求导数

步骤
1. 求增量 $\vartriangle\!y=f(x+\vartriangle\!x)-f(x)$
2. 算比值 $\dfrac{\vartriangle\!y}{\vartriangle\!x}=\dfrac{f(x+\vartriangle\!x)-f(x)}{\vartriangle\!x}$
3. 求极限 $y^\prime=\lim\limits_{\vartriangle\!x\rightarrow0}\dfrac{\vartriangle\!y}{\vartriangle\!x}$

### 导数的几何意义

$f^\prime(x_0)$ 表示曲线 $y=f(x)$ 在点 $M(x_0,f(x_0))$ 处的切线的斜率，即  
$$f^\prime(x_0)=\tan\alpha\quad(\alpha为倾角)$$  
切线方程 $y=f^\prime(x_0)(x-x_0)+f(x_0)$  
法线方程 $y=-\dfrac{1}{f^\prime(x_0)}(x-x_0)+f(x_0)$

### 可导与连续的关系

> 定理 凡可导函数都是连续函数

### 求导法则

#### 导数的四则运算法则

> 定理 如果函数 $u(x),v(x)$ 在点 $x$ 处可导，则他们的和、差、积、商（分母不为 $0$ ）在点 $x$ 处也可导，且
>
> 1. $[u(x)\pm v(x)]^\prime=u^\prime(x)\pm v^\prime(x)$
> 2. $[u(x)v(x)]^\prime=u^\prime(x)v(x)+u(x)v^\prime(x)$
> 3. $\left[\dfrac{u(x)}{v(x)}\right]^\prime=\dfrac{u^\prime(x)v(x)-u(x)v^\prime(x)}{(v(x))^2}$

#### 反函数的求导法则

> 定理 如果函数 $x=\varPhi(y)$ 在区间 $I_y$ 内单调可导且 $\varPhi^\prime(y)\not ={0}$ ，那么它的反函数 $y=$

#### 复合函数的求导法则

> 定理 如果函数 $u=\varPhi(x)$ 在点 $x$ 可导，而 $y=f(u)$ 在点 $u=\varPhi(x)$ 可导，则复合函数 $y=f[\varPhi(x)]$ 在点 $x$ 可导，其导数为  
> $$\{f[\varPhi(x)]\}^\prime=f^\prime(u)\cdot\varPhi^\prime(x)$$
> $$\dfrac{\mathrm{d}y}{\mathrm{d}x}=\dfrac{\mathrm{d}y}{\mathrm{d}u}\cdot\dfrac{\mathrm{d}u}{\mathrm{d}x}$$
> 链式法则

#### 隐函数的求导法则

> 定义 由方程 $F(x,y)=0$ 所确定的 $y$ 关于 $x$ 的函数称为**隐函数**  
> $y=f(x)$ 形式称为**显函数**  
> $F(x,y)=0\Rightarrow y=f(x)$ 隐函数的显化  
> 用复合函数求导法则直接对方程两边求导

#### 对数求导法

#### 参数方程求导

### 高阶导数

#### 高阶导数的定义

> 定义 如果函数 $f(x)$ 的导数 $f^\prime(x)$ 在点 $x$ 处可导，即  
> $$[f^\prime(x)]^\prime=\lim\limits_{\vartriangle\!x\rightarrow0}\dfrac{f^\prime(x+\vartriangle\!x)-f^\prime(x)}{\vartriangle\!x}$$
>
一般地，函数 $f(x)$ 的 $n-1$ 阶导数的导数称为函数 $f(x)$ 的 $n$ 阶导数，记作 $f^{(n)}f(x),y^{(n)},\dfrac{\mathrm{d}^ny}{\mathrm{d}x^n},\dfrac{\mathrm{d}^nf(x)}{\mathrm{d}x^n}$  
即 $y^{(n)}=(y^{(n-1)})^\prime=\dfrac{\mathrm{d}}{\mathrm{d}x}\left(\dfrac{\mathrm{d}^{(n-1)}y}{\mathrm{d}x^{n-1}}\right)$  
二阶和二阶以上的导数统称为**高阶导数**。  
相应的， $f(x)$ 称为零阶导数； $f^\prime(x)$ 称为一阶导数。  

#### 高阶导数求法举例

##### 直接法

由高阶导数的定义逐步求高阶导数

莱布尼兹公式  
$$(u\cdot v)^{(n)}=u^{(n)}v+nu^{n-1}v^\prime+\cdots+\dfrac{n(n-1)}{2!}u^{(n-2)}v^n+$$

### 微分

#### 微分的定义

> 定义 设函数 $y=f(x)$ 在某区间内有定义， $x_0$ 及 $x_0+\vartriangle\!x$ 在这区间内，如果  
> $$\vartriangle\!y=f(x_0+\vartriangle\!x)-f(x_0)=A\cdot\vartriangle\!x+o(\vartriangle\!x)$$  
> 成立（其中 $A$ 是与 $\vartriangle\!x$ 无关的常数），则称函数 $y=$  

#### 可微的条件

> 定理 函数 $f(x)$ 在点 $x_0$ 可微的充要条件是 $f(x)$ 在点 $x_0$ 可导，且 $A=f^\prime(x_0)$

导数也叫**微商**

#### 微分的几何意义

#### 微分的求法

$$\mathrm{d}y=f^\prime(x)\mathrm{d}x$$
