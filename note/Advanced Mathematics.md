# 高等数学II-1 

胡小兵 <iamhxb@cqu.edu.cn>  
助教：熊若兰 tel: 13872442250 <ruolanx100@163.com>  

Sep. 30th, 2024 课程介绍、微积分的一些基本问题  

> 成绩构成：  
> 期中 $20\%+$ 期末 $55\%+$ 考勤 $5\%+$ 作业 $10\%+$ Easylearning助学平台 $10\%$  

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
  $S_n=(\frac{1}{n})^2\cdot\frac{1}{n}+(\frac{2}{n})^2\cdot\frac{1}{n}+\cdots+(\frac{n-1}{n})^2\cdot\frac{1}{n}+(\frac{n}{n})^2\cdot\frac{1}{n}=\frac{1}{n^3}[1^2+2^2+\cdots+(n-1)^2+n^2]=\frac{1}{6}(1+\frac{1}{n})(2+\frac{1}{n})$  
  
  $S=\lim\limits_{n\to\infty}S_n=\lim\limits_{n\to\infty}\frac{1}{6}(1+\frac{1}{n})(2+\frac{1}{n})=\frac{1}{3}$

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
余集 $C_BA=A\backslash B\,(A\subset B)$
### 函数的几种特性