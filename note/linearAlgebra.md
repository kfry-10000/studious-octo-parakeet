# 线性代数  

copyright@kfry-10000  
若发现该笔记存在问题请联系<20241340@stu.cqu.edu.cn>  

主讲：张谋  
<https://sakai.cqu.edu.cn>  

## 行列式

### 预备知识

引进行列式的概念，讨论行列式性质，计算行列式值

二元线性方程组  
$\begin{cases}
    a_{11}x_1+a_{12}x_2=b_1\qquad(1)\\a_{21}x_1+a_{22}x_2=b_2\qquad(2)\end{cases}$  
$\begin{matrix}
    (1)\times a_{22}-(2)\times a_{12}:&(a_{11}a_{22}-a_{12}a_{21})x_1=b_1a_{22}-b_2a_{12}\\(2)\times a_{11}-(1)\times a_{21}:&(a_{11}a_{22}-a_{12}a_{21})x_2=b_2a_{11}-b_1a_{21}
\end{matrix}$  
若 $a_{11}a_{22}-a_{12}a_{21}\not ={0}$ ,  
则 $x_1=\dfrac{b_1a_{22}-b_2a_{12}}{a_{11}a_{22}-a_{12}a_{21}},\ x_2=\dfrac{b_2a_{11}-b_1a_{21}}{a_{11}a_{22}-a_{12}a_{21}}$  
消元法解多元线性方程组不方便  

定义 $\begin{vmatrix}
    a&b\\c&d
\end{vmatrix}=ad-bc$ ，称之为二阶行列式  
$x_1=\frac{D_1}{D}$, $x_2=\frac{D_2}{D}$  
其中 $D=\begin{vmatrix}
    a_{11}&a_{12}\\a_{21}&a_{22}
\end{vmatrix}$ (称为系数行列式), $D_1=\begin{vmatrix}
    b_1&a_{12}\\b_2&a_{22}
\end{vmatrix}$ ， $D_2=\begin{vmatrix}
    a_{11}&b_1\\a_{21}&b_2
\end{vmatrix}$  
类似可得三阶行列式以及三元线性方程组解法

把 $n$ 个不同的元素排成一列，叫做 $n$ 个元素的全排列，简称排列  
排列数 $P_n=n!$  
一般地，规定从小到大的排列为标准顺序（标准排列或自然排列）
在排列 $S_1S_2\cdots S_i\cdots S_j\cdots S_n$ 中, $\exist S_i>S_j$ 就说它们形成了一个**逆序（或反序）**，一个排列中所有逆序的总数称作这个排列的**逆序数**，记作 $t[S_1\cdots S_n]$
逆序数为奇数称作**奇排列**，偶数称作**偶排列**，最大为$\frac{1}{2}n(n-1)$ ，最小为 $0$
对换 相邻对换

> 一个排列中的任何两元素，无论与其它元素做怎样的对换，只要前后次序没有发生变化，则两者的逆序不变  

证明：  
相邻对换  
$a_1\cdots a_labb_1\cdots b_m\rightarrow a_1\cdots a_lbab_1\cdots b_m$  

- 易知经过相邻对换后，$a_1\cdots a_l,\ b_1\cdots b_m$中的任何两个元素都没发生变化  
- 同时 $a,b$ 两个元素与元素 $a_1\cdots a_l,\ b_1\cdots b_m$ 形成的逆序总个数也没发生变化  
  
仅 $ab$本身之间的逆序发生了变化，奇偶性发生了变化  

非相邻对换  
$$\begin{matrix}
    a_1\cdots a_lab_1\cdots b_mbc_1\cdots c_n&\Longrightarrow a_1\cdots a_lbb_1\cdots b_mac_1\cdots c_n\\
    a_1\cdots a_lab_1\cdots b_mbc_1\cdots c_n&\stackrel{b经过m+1次相邻对换}{\longrightarrow}a_1\cdots a_lbab_1\cdots b_mc_1\cdots c_n\\&\stackrel{a经过m次相邻对换}{\longrightarrow}a_1\cdots a_lbb_1\cdots b_mac_1\cdots c_n
\end{matrix}$$  
- 共经过 $2m+1$ 次相邻对换，所以前后两个排列的奇偶性相反
  
> 推论：奇排列调成标准排列的对换次数为奇数，偶排列调成标准排列的对换次数为偶数  
### 行列式的定义  
#### $n$ 阶行列式的定义  
三阶行列式的定义为  
$$\begin{vmatrix}
    a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}
\end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}$$  
1. 等式右端是 $6$ 项之和，每项都是位于不同行不同列的 $3$ 个元素的乘积，即同一项中不可能有两个元素来自同一行同一列  
2. 每一项各元素的行标排列成自然排列，因此右端的任意一项除符号外可写成$a_{1p_1}a_{2p_2}a_{3p_3}$ ，其中 $p_1p_2p_3$ 为 $123$ 的某个排列
3. 正项列标排列逆序数为偶数，负项列标排列逆序数为奇数  
假设 $p_1p_2p_3$ 的逆序数为 $t$ ，则三阶行列式可定义为  
$$\begin{matrix}
\begin{vmatrix}
    a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}
\end{vmatrix}=|a_{ij}|_{3\times3}&=\sum\limits_{(p_1p_2p_3)}(-1)^ta_{1p_1}a_{2p_2}a_{3p_3}\\&=\sum\limits_{(p_1p_2p_3)}(-1)^ta_{p_11}a_{p_22}a_{p_33}\\&=\vartriangle(a_{ij})=\det(a_{ij})\end{matrix}$$

> 定义： $n^2$ 个数排列成 $n$ 行 $n$ 列的一个表
$$\begin{vmatrix}
    a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\cdots&\cdots&\cdots&\cdots\\a_{n1}&a_{n2}&\cdots&a_{nn}
\end{vmatrix}=D$$
>注： $n$ 阶行列式有 $n!$ 项，正负各一半，每项都是 $n$ 个来自于不同行不同列的元素之积， $t$ 是行标为自然排列，列标的逆序数。  

并按下值计算：  
$$D=\sum\limits_{(p_1p_2\cdots p_n)}(-1)^ta_{1p_1}a_{2p_2}\cdots a_{np_n}=\sum\limits_{(p_1p_2\cdots p_n)}(-1)^ta_{p_11}a_{p_22}\cdots a_{p_nn}$$  
其中 $t=t[p_1\cdots p_n]$ ， $p_1\cdots p_n$ 为 $1,2,3,\cdots,n$ 的全排列，  
则称 **$D$为$n$阶行列式** 。  

对角行列式的值=对角元之积  
反对角行列式  

双阶乘  
$(2k)!!=2\times4\times\cdots\times{2k}\\(2k+1)!!=1\times3\times\cdots\times{2k+1}$  
### 行列式的性质  
> 性质1  $D=D^T$ (行列式与其转置行列式相等)

证明：记$D=\det(a_{ij}),D^T=\det(b_{ij})$ 则 $b_{ij}=a{ji}$  
$$D^T=\det(b_{ij})=\sum\limits_{p_1\cdots p_n}(-1)^tb_{1p_1}\cdots b_{np_n}=\sum\limits_{p_1\cdots p_n}(-1)^ta_{p_11}\cdots a_{p_nn}$$

> 性质2 互换行列式的两行或两列，行列式改变符号

证明：记　$D=\vartriangle\!(a_{ij})$ ，交换 $D$ 中的 $i,j$ 两行得到的行列式记为 $D_1=\vartriangle\!(b_{ij})$ ，即  
$D=\begin{vmatrix}
    a_{11}&a_{12}&\cdots&a_{1n}\\\cdots&&\cdots&\cdots\\a_{i1}&a_{i2}&\cdots&a_{in}\\\cdots&&\cdots&\cdots\\a_{j1}&a_{j2}&\cdots&a_{jn}\\\cdots&&\cdots&\cdots\\a_{n1}&a_{n2}&\cdots&a_{nn}
\end{vmatrix}=\sum\limits_{p_1\cdots p_n}a_{1p_1}\cdots a_{np_n}\quad D_1=\begin{vmatrix}
    a_{11}&a_{12}&\cdots&a_{1n}\\\cdots&&\cdots&\cdots\\a_{j1}&a_{j2}&\cdots&a_{jn}\\\cdots&&\cdots&\cdots\\a_{i1}&a_{i2}&\cdots&a_{in}\\\cdots&&\cdots&\cdots\\a_{n1}&a_{n2}&\cdots&a_{nn}
\end{vmatrix}=\begin{vmatrix}
    b_{11}&b_{12}&\cdots&b_{1n}\\\cdots&&\cdots&\cdots\\b_{i1}&b_{i2}&\cdots&b_{in}\\\cdots&&\cdots&\cdots\\b_{j1}&b_{j2}&\cdots&b_{jn}\\\cdots&&\cdots&\cdots\\b_{n1}&b_{n2}&\cdots&b_{nn}
\end{vmatrix}$  
$b_{kp}=a_{kp}\ k\not ={i,j}\qquad b_{ip}=a_{jp},b_{jp}=a_{ip}$  
$\begin{matrix}
    D_1&=\sum\limits_{p_1\cdots p_n}(-1)^{t[p_1\cdots p_i\cdots p_j\cdots p_n]}b_1p_1\cdots b_ip_i\cdots b_jp_j\cdots b_np_n\\&=\sum\limits_{p_1\cdots p_n}(-1)^{t[p_1\cdots p_i\cdots p_j\cdots p_n]}a_{1p_1}\cdots a_{jp_i}\cdots a_{ip_j}\cdots a_{np_n}\\&=\sum\limits_{p_1\cdots p_n}(-1)^{t[p_1\cdots p_j\cdots p_i\cdots p_n]}a_{1p_1}\cdots a_{ip_i}\cdots a_{jp_j}\cdots a_{np_n}\\&=-\sum\limits_{p_1\cdots p_n}(-1)^{t[p_1\cdots p_i\cdots p_j\cdots p_n]}a_{1p_1}\cdots a_{ip_i}\cdots a_{jp_j}\cdots a_{np_n}\\&=-D
\end{matrix}$  
> 推论 如果行列式有两行（列）的元素完全相同，则此行列式的值为0  
$D=-D=0$

 > 性质3 行列式的某一行（列）中所有元素都乘以同一数k,等于用k乘以此行列式。  
   推论1 行列式中某一行（列）的所有元素的公因子可以提到行列式外面  
   推论2 行列式中某一行（列）的所有元素全为0，则此行列式等于0。  
   推论3  行列式中如果有两行（列）元素成比例，则此行列式等于0。  
   推论4 行列式中如果某一行（列）的元素都是两数之和  
   $D=\begin{vmatrix}
    a_{11}&\cdots&a_{1j}+a^\prime_{1j}&\cdots&a_{1n}\\&&\cdots&&\\a_{i1}&\cdots&a_{ij}+a^\prime_{ij}&\cdots&a_{in}\\&&\cdots&&\\a_{n1}&\cdots&a_{nj}+a^\prime_{nj}&\cdots&a_{nn}
 \end{vmatrix}=\begin{vmatrix}
    a_{11}&\cdots&a_{1j}&\cdots&a_{1n}\\&&\cdots&&\\a_{i1}&\cdots&a_{ij}&\cdots&a_{in}\\&&\cdots&&\\a_{n1}&\cdots&a_{nj}&\cdots&a_{nn}
 \end{vmatrix}+\begin{vmatrix}
    a_{11}&\cdots&a^\prime_{1j}&\cdots&a_{1n}\\&&\cdots&&\\a_{i1}&\cdots&a^\prime_{ij}&\cdots&a_{in}\\&&\cdots&&\\a_{n1}&\cdots&a^\prime_{nj}&\cdots&a_{nn}
 \end{vmatrix}=D_1+D_2$  
   证明：$D=\sum(-1)^ta_{p_11}\cdots (a_{ij}+a^\prime_{ij})\cdots a_{p_nn}=\sum(-1)^ta_{p_11}\cdots a_{ij}\cdots a_{p_nn}+\sum(-1)^ta_{p_11}\cdots a^\prime_{ij}\cdots a_{p_nn}$

> 性质5 吧行列式的某一行（列）的各元素乘以同一数后加到另一行（或列）对应元素上，行列式不变。  

例🖋️  
$\begin{vmatrix}
    3&1&-1&2\\-5&1&3&-4\\2&0&1&-1\\1&-5&3&-3
\end{vmatrix}\xlongequal{c_1\leftrightarrow c_2}\begin{vmatrix}
    1&3&-1&2\\1&-5&3&-4\\0&2&1&-1\\-5&1&3&-3
\end{vmatrix}\xlongequal{r_2-r_1}\begin{vmatrix}
    1&3&-1&2\\0&-8&4&-6\\0&2&1&-1\\-5&1&3&-3
\end{vmatrix}\xlongequal{r_4+5r_1}\begin{vmatrix}
    1&3&-1&2\\0&-8&4&-6\\0&2&1&-1\\0&16&-2&7
\end{vmatrix}\xlongequal{r_2\leftrightarrow r_3}\begin{vmatrix}
    1&3&-1&2\\0&2&1&-1\\0&-8&4&-6\\0&16&-2&7
\end{vmatrix}\xlongequal{r_3+4r_2}\begin{vmatrix}
    1&3&-1&2\\0&2&1&-1\\0&0&8&-10\\0&16&-2&7
\end{vmatrix}\xlongequal{r_4-8r_2}\begin{vmatrix}
    1&3&-1&2\\0&2&1&-1\\0&0&8&-10\\0&0&-10&15
\end{vmatrix}=\cdots$ 把行列式化为上三角行列式  

例🖋️  
$\begin{vmatrix}
    3&1&1&1\\1&3&1&1\\1&1&3&1\\1&1&1&3
\end{vmatrix}=\begin{vmatrix}
    6&6&6&6\\1&3&1&1\\1&1&3&1\\1&1&1&3
\end{vmatrix}=6\begin{vmatrix}
    1&1&1&1\\1&3&1&1\\1&1&3&1\\1&1&1&3
\end{vmatrix}=6\begin{vmatrix}
    1&1&1&1\\0&2&0&0\\0&0&2&0\\0&0&0&2
\end{vmatrix}=48$

例🖋️  
$\begin{vmatrix}
    a&b&c&d\\a&a+b&a+b+c&a+b+c+d\\a&2a+b&3a+2b+c&4a+3b+2c+d\\a&3a+b&6a+3b+c&10a+6b+3c+d
\end{vmatrix}=\begin{vmatrix}
    a&0+b&c&d\\a&a+b&a+b+c&a+b+c+d\\a&2a+b&3a+2b+c&4a+3b+2c+d\\a&3a+b&6a+3b+c&10a+6b+3c+d
\end{vmatrix}=\begin{vmatrix}
    a&0&c&d\\a&a&a+b+c&a+b+c+d\\a&2a&3a+2b+c&4a+3b+2c+d\\a&3a&6a+3b+c&10a+6b+3c+d
\end{vmatrix}+\begin{vmatrix}
    a&b&c&d\\a&b&a+b+c&a+b+c+d\\a&b&3a+2b+c&4a+3b+2c+d\\a&b&6a+3b+c&10a+6b+3c+d
\end{vmatrix}=\begin{vmatrix}
    a&0&c&d\\a&a&a+b+c&a+b+c+d\\a&2a&3a+2b+c&4a+3b+2c+d\\a&3a&6a+3b+c&10a+6b+3c+d
\end{vmatrix}+0$  
$\begin{matrix}
    原式&=a\begin{vmatrix}
    1&b&c&d\\1&a+b&a+b+c&a+b+c+d\\1&2a+b&3a+2b+c&4a+3b+2c+d\\1&3a+b&6a+3b+c&10a+6b+3c+d
\end{vmatrix}\\&=a\begin{vmatrix}
    1&0&0&0\\1&a&a+b&a+b+c\\1&2a&3a+2b&4a+3b+2c\\1&3a&6a+3b&10a+6b+3c
\end{vmatrix}\\&=a^2\begin{vmatrix}
    1&0&0&0\\1&1&a+b&a+b+c\\1&2&3a+2b&4a+3b+2c\\1&3&6a+3b&10a+6b+3c
\end{vmatrix}\\&\xlongequal[c_4-c\cdot c_2]{c_3-b\cdot c_2}a^3\begin{vmatrix}
    1&0&0&0\\1&1&1&a+b\\1&2&3&4a+3b\\1&3&6&10a+6b
\end{vmatrix}\xlongequal{c_4-b\cdot c_3}a^4\begin{vmatrix}
    1&0&0&0\\1&1&1&1\\1&2&3&4\\1&3&6&10
\end{vmatrix}
\end{matrix}$

例🖋️  
$\begin{vmatrix}
    1+a&1&1&1\\1&1-a&1&1\\1&1&1+b&1\\1&1&1&1-b
\end{vmatrix}\xlongequal{r_1-r_2,r_3-r_4}\begin{vmatrix}
    a&a&0&0\\1&1-a&1&1\\0&0&b&b\\1&1&1&1-b
\end{vmatrix}=ab\begin{vmatrix}
    1&1&0&0\\1&1-a&1&1\\0&0&1&1\\1&1&1&1-b
\end{vmatrix}\xlongequal[c_3-c_4]{c_1-c_2}ab\begin{vmatrix}
    0&1&0&0\\a&1-a&0&1\\0&0&0&1\\0&1&b&1-b
\end{vmatrix}=a^2b^2\begin{vmatrix}
    0&1&0&0\\1&1&0&1\\0&0&0&1\\0&1&1&1
\end{vmatrix}$
### 行列式的展开  
$$\begin{vmatrix}
    a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}
\end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}\\=a_{11}(a_{22}a_{33})-a_{12}(a_{21}a_{33}-a_{23}a_{31})+a_{13}(a_{21}a_{32}-a_{22}a_{31})\\=a_{11}\begin{vmatrix}
    a_{22}&a_{23}\\a_{32}&a_{33}
\end{vmatrix}-a_{12}\begin{vmatrix}
    a_{21}&a_{23}\\a_{31}&a_{33}
\end{vmatrix}+a_{13}\begin{vmatrix}
    a_{21}&a_{22}\\a_{31}&a_{32}
\end{vmatrix}$$  

在 $n$ 阶行列式中，把元素 $a_{ij}$ 所在的第 $i$ 行与第 $j$ 列划去后留下来的 $n-1$ 阶行列式叫做元素 $a_{ij}$ 的**余子式**，记作 $M_{ij}$ 。而 $A_{ij}=(-1)^{i+j}M_{ij}$ 叫做 $a_{ij}$ 的**代数余子式**。  
注：行列式中某元素的(代数)余子式与该元素的大小无关，只与元素的位置有关。  
> 定理 一个 $n$ 阶行列式，如果其中第 $i$ 行所有元素除 $a_{ij}$ 外都为 $0$ ，则这个行列式等于 $a_{ij}$ 与它的代余子式的乘积。即  
> $D=\vartriangle\!(a_{ij})=\begin{vmatrix}
    a_{11}&\cdots&a_{1j-1}&a_{1j}&a_{1j+1}&\cdots&a_{1n}\\&\cdots&&\cdots&&\cdots&\\a_{i-1,1}&\cdots&a_{i-1,j-1}&a_{i-1,j}&a_{i-1,j+1}&\cdots&a_{i-1,n}\\0&\cdots&0&a_{ij}&0&\cdots&0\\a_{i+1,1}&\cdots&a_{i+1,j-1}&a_{i+1,j}&a_{i+1,j+1}&\cdots&a_{i+1,n}\\&\cdots&&\cdots&&\cdots&\\a_{n,1}&\cdots&a_{n,j-1}&a_{n,j}&a_{n,j+1}&\cdots&a_{n,n}
\end{vmatrix}=a_{ij}A_{ij}=a_{ij}A_{ij}$

> 性质6 $A=\begin{vmatrix}
    D_k&0\\*&D_r
\end{vmatrix}=|D_k||D_r|$
$\begin{vmatrix}
    a_{11}&a_{12}&\cdots&a_{1m}&0&\cdots&0\\a_{21}&a_{22}&\cdots&a_{2m}&0&\cdots&0\\\vdots&\vdots&&\vdots&\vdots&&\vdots\\a_{m1}&a_{m2}&\cdots&a_{mm}&0&\cdots&0\\&&&&b_{11}&\cdots&b_{1r}\\&&*&&\vdots&&\vdots\\&&&&b_{r1}&\cdots&b_{rr}
\end{vmatrix}$  

数学归纳法证明

> 推论  
$\begin{vmatrix}
    0&D_m\\D_n&*
\end{vmatrix}=(-1)^{mn}|D_m|\cdot|D_n|=\begin{vmatrix}
    *&D_m\\D_n&0
\end{vmatrix}$

例  
$\begin{vmatrix}
    a&&&&&&&b\\&a&&&&&b&\\&&\cdots&&&\cdots&&\\&&&a&b&&&\\&&&c&d&&&\\
\end{vmatrix}$  

例  
证明范德蒙行列式
$\begin{vmatrix}
    1&1&\cdots&1\\x_1&x_2&\cdots&x_n\\{x_1}^2&{x_2}^2&\cdots&{x_n}^2\\\vdots&\vdots&&\vdots\\{x_1}^{n-2}&{x_2}^{n-2}&\cdots&{x_n}^{n-2}\\{x_1}^{n-1}&{x_2}^{n-1}&\cdots&{x_n}^{n-1}
\end{vmatrix}$  

$\begin{vmatrix}
    1&1&\cdots&1\\x_1&x_2&\cdots&x_n\\{x_1}^2&{x_2}^2&\cdots&{x_n}^2\\\vdots&\vdots&&\vdots\\{x_1}^{n-2}&{x_2}^{n-2}&\cdots&{x_n}^{n-2}\\{x_1}^{n-1}&{x_2}^{n-1}&\cdots&{x_n}^{n-1}
\end{vmatrix}=\begin{vmatrix}
    1&1&\cdots&1\\x_1&x_2&\cdots&x_n\\{x_1}^2&{x_2}^2&\cdots&{x_n}^2\\\vdots&\vdots&&\vdots\\{x_1}^{n-2}&{x_2}^{n-2}&\cdots&{x_n}^{n-2}\\0&{x_2}^{n-2}(x_2-x_1)&\cdots&{x_n}^{n-2}(x_n-x_1)
\end{vmatrix}=\begin{vmatrix}
    1&1&\cdots&1\\x_1&x_2&\cdots&x_n\\{x_1}^2&{x_2}^2&\cdots&{x_n}^2\\\vdots&\vdots&&\vdots\\0&{x_2}^{n-3}(x_2-x_1)&\cdots&{x_n}^{n-3}(x_n-x_1)\\0&{x_2}^{n-2}(x_2-x_1)&\cdots&{x_n}^{n-2}(x_n-x_1)
\end{vmatrix}=\begin{vmatrix}
    1&1&\cdots&1\\0&{x_2-x_1}&\cdots&{x_n-x_1}\\0&{x_2}(x_2-x_1)&\cdots&{x_n}(x_n-x_1)\\\vdots&\vdots&&\vdots\\0&{x_2}^{n-3}(x_2-x_1)&\cdots&{x_n}^{n-3}(x_n-x_1)\\0&{x_2}^{n-2}(x_2-x_1)&\cdots&{x_n}^{n-2}(x_n-x_1)
\end{vmatrix}$  

## 矩阵  

### 矩阵的概念  

> 定义 有 $m\times n$ 个数 $a_{ij}$ 排成 $m$ 行 $n$ 列的一个数表
$\begin{bmatrix}
    a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\vdots&&&\vdots\\&&&a_{mn}
\end{bmatrix}$  

### 一些特殊的矩阵
#### 对角阵 数量阵 单位阵
$\Lambda=\Lambda^T$

#### 三角阵

#### 伴随阵
由方阵 $A$ 中各元素的代数余子式所组成的矩阵  
$A^*=\begin{bmatrix}
    A_{11}
\end{bmatrix}$  
1. $AA^*=A^*A=|A|E$  
2. $(kA)^*=k^{n-1}A^*$  
3. x`$(A^T)^*=(A^*)^T$

#### 对称阵与反对称阵  
> 对称阵 若 $A=A^T$ ，则称 $A$ 为对称阵  
> 记 $A=(a_{ij})_{n\times n}$ ，则 $A^T=(a_{ji})_{n\times n}$ ，由 $A=A^T$ 易知 $a_{ij}=a_{ji}$  
> 从形式上看，对称阵以对角线为对称轴的对应元素相同  
>
> 反对称阵 若 $A=-A^T$ ，则称 $A$ 为反对称阵  
> $-A=-\begin{bmatrix}
    a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}
\end{bmatrix}=A^T=\begin{bmatrix}
    a_{11}&a_{21}&a_{31}\\a_{12}&a_{22}&a_{32}\\a_{13}&a_{23}&a_{33}
\end{bmatrix}\Rightarrow a_{ij}=-a{ji}(a_{ii}=0)$  
 从形式上看，对称阵以对角线为对称轴的对应元素反号且对角线元素全为 $0$

1. 若 $A,B$ 均为对称阵，则 $AB$ 为对称阵的充要条件是 $AB=BA$  
2. 若 $A,B$ 均为反对称阵，则 $AB$ 为对称阵的充要条件是 $AB=BA$
3. 若 $A$ 均为对称阵， $B$为 反对称阵，则 $AB$ 为反对称阵的充要条件是 $AB=BA$  

#### 正交阵

> 正交阵 设 $A$ 为方阵，若 $AA^T=E$ 或 $A^TA=E$ 则称 $A$ 是一个正交阵  
> 各个行向量或列向量均为单位向量且正交
>
$\xi\xi^T$

### 矩阵的运算

#### 矩阵的加法  

> 定义 如果 $A=(a_{ij})$ ， $B=(b_{ij})$ 都是 $m\times n$ 矩阵，则矩阵 $A+B=(a_{ij}+b_{ij})$  
> 定义 数 $\lambda$ 与矩阵 $A=(a_{ij})$ 的乘积记为 $\lambda A=(\lambda a_{ij})$  
> 定义 设 $A=(a_{ij})_{m\times s},\qquad B=(b_{ij})_{s\times n}$ 则 $AB=C=(c_{ij})_{m\times n}$ 其中 $c_{ij}=\sum\limits_{k=1}^{s}a_{ik}b_{kj}$  

矩阵乘法不满足交换律  
> 矩阵的方幂
>
单位阵与任何矩阵可换，任意两个对角阵显然可换  
零因子  
> 定义 若 $A\not ={B}$  

若 $AB=BA$ 则  
$A^2-B^2=(A+B)(A-B)=(A-B)(A+B)$  

秩

#### 矩阵的转置  

> 定义 把矩阵 $A$ 的行（列）换成同序数的行（列）而得到的新矩阵，叫做 $A$ 的**转置矩阵**记为 $A^T$  
> 一般地 $A^T\not ={A}$  
> 满足一下运算规律：  
>

#### 方阵的行列式  

> 定义 由 $n$ 阶方阵 $A$ 的元素位置不变所构成的行列式，叫做方阵 $A$ 的行列式，记为 $|A|$ 或 $\det A$  
> 行列式是一个数，矩阵仅是一个数表  
> 满足一下运算规律（ $A,B$ 均为 $n$ 阶方阵）：  
> $|A|=|A^T|,|\lambda A|=\lambda^n|A|，$  
> 当 $|A|\not ={0}$ 时，称  
>
#### 共轭矩阵  

> 定义 $A=(a_{ij})$ 为复矩阵
>

### 分块矩阵
用几条纵线和横线把一个矩阵分成若干小块，每一小块称为原矩阵的一个子矩阵（或子块），以子矩阵为原矩阵的一个元素，就得到分块矩阵。  
#### 分块矩阵的运算
1. 加法
2. 数与分块矩阵的乘法
3. 分块矩阵与分块矩阵的乘法：为了使 $A$ 的子块与 $B$ 的子块能相乘，分块时必须要求矩阵 $A$ 的列数的分法于 $B$ 的行数的分法一致
4. 分块矩阵的转置
证明：
$\det\begin{bmatrix}
    A&0\\0&B
\end{bmatrix}=$  

#### 特殊分块矩阵
1. 分块对角阵
2. 分块三角阵  
$A=\begin{bmatrix}
    B_{mm}&D\\0&C_{nn}
\end{bmatrix}$ $|A|=|B_{mm}||C_{nn}|$  
$A=\begin{bmatrix}
    0&C_{nn}\\B_{mm}&D
\end{bmatrix}$ $|A|=(-1)^{mn}|B_{mm}||C_{nn}|$  

### 矩阵的秩
> 定义 在 $m\times n$ 中，取 $k$ 行 $k$ 列交叉点处的  $k^2$ 个元素，按原来的相对位置，得到一个 $k$ 阶行列式，称为矩阵 $A$ 的一个 $k$ 阶子式，在 $m\times n$ 矩阵中共有 $C^k_mC^k_n$ 个 $k$ 阶子式  
> 定义 如果矩阵 $A$ 有一个 $r$ 阶子式 $D\not ={0}$ ，并且  

1. $A$ 为满秩矩阵  $\Leftrightarrow$  

### 初等变换与初等方阵  

> 定义 如果一个矩阵经过有限次初等变化，等价  
>
等价的性质  
1. 反身性 $A\sim A$  
2. 对称性 $A\sim B\Rightarrow B\sim A$
3. 传递性 $A\sim B,B\sim C\Rightarrow A\sim C$  

> 定理 若 $A\sim B$ ，则 $R(A)=R(B)$ ，即矩阵的初等变换不改变矩阵的秩  
>
化为行阶梯型  
$A=\begin{bmatrix}
    1&-1&0&2&1\\-3&3&0&-7&0\\1&-1&2&3&2\\2&-2&2&5&3
\end{bmatrix}\stackrel{\begin{matrix}
    r_2+3r_1\\r_3-r_1\\r_4-2r_1
\end{matrix}}{\longrightarrow}
\begin{bmatrix}
    1&-1&0&2&1\\0&0&0&-1&3\\0&0&2&1&1\\0&0&0&0&0
\end{bmatrix}\stackrel{r_2\leftrightarrow r_3}{\longrightarrow}
\begin{bmatrix}
    1&-1&0&2&1\\0&0&2&1&1\\0&0&0&-1&3\\0&0&0&0&0
\end{bmatrix}\stackrel{变换为行最简}{\longrightarrow}
\begin{bmatrix}
    1&-1&0&2&1\\0&0&1&0&2\\0&0&0&1&-3\\0&0&0&0&0
\end{bmatrix}$  

> **谋曰：要习惯于只做行变换，解方程组时列变换会对结果产生影响**

例🖋️ $A=\begin{bmatrix}
    a&b&b&b&b\\b&a&b&b&b\\b&b&a&b&b\\b&b&b&a&b\\b&b&b&b&a
\end{bmatrix}$ ，求 $R(A)$  
$$A\rightarrow\begin{bmatrix}
    a&b&b&b&b\\b-a&a-b&0&0&0\\b-a&0&a-b&0&0\\b-a&0&0&a-b&0\\b-a&0&0&0&a-b
\end{bmatrix}\rightarrow\begin{bmatrix}
    a+4b&b&b&b&b\\0&a-b&0&0&0\\0&0&a-b&0&0\\0&0&0&a-b&0\\0&0&0&0&a-b
\end{bmatrix}$$  
1. $a-b=0,a+4b=0\Leftrightarrow a=b=0$ ，此时 $R(A)=0$
2. $a-b\not ={0},a+4b\not ={0}\Leftrightarrow$ ，此时 $R(A)=5$
3. $a-b=0,a+4b\not ={0}\Leftrightarrow a=b\not ={0}$ ，此时 $R(A)=1$
4. $a-b\not ={0},a+4b=0\Leftrightarrow$ ，此时 $R(A)=4$

初等变换  

1. $|E(i,j)|=-1,|E(i(k))|=k,E(j(k),i)=1$  
2. 因初等方阵的行列式均不等于 $0$ ，故初等方阵是满秩矩阵
3. 初等方阵的转置仍为同类初等方阵

> 定理 对一个 $m\times n$ 的矩阵 $A$ 作初等变换就相当于在 $A$ 的左边乘上相应的 $m\times m$ 的初等方阵。对 $A$ 做初等列变换就相当于在 $A$ 的右边乘上相应的 $n\times n$ 的初等方阵。
>
> 定理 $A$ 为满秩矩阵 $\Leftrightarrow$ $A$ 能表示成一些初等方阵的乘积  
> 证 "$\Rightarrow$" $A$ 满秩，则 $A\sim E$ ，也有 $E\sim A$  
> $\therefore$ 存在初等方阵 $P_1\cdots R_rP_{r+1}\cdots R_l$ 使  
> $P_1\cdots P_rEP_{r+1}\cdots P_l=A$  
>
> 推论1 两个 $m\times n$ 矩阵 $A,B$ 等价 $\Leftrightarrow$ 存在 $m$ 阶的满秩矩阵 $P$ 及 $n$ 阶的满秩矩阵 $Q$ 使 $PAQ=B$ 。  
> $R(PAQ)=R(PA)=R(AQ)=R(A)\quad(P,Q为满秩矩阵)$
>

### 方阵的逆  

> 定义 对于 $n$ 阶方阵 $A$ ，如果存在一个 $n$ 阶方阵 $B$ 使 $AB=BA=E$ ，则称 $A$ 是可逆的，并称 $B$ 为 $A$ 的逆，记为 $B=A^{-1}$ 带回得 $AA^{-1}=A^{-1}A=E$ 。  
>
> 结论 初等方阵的逆仍为初等方阵
> $0$ 矩阵没有逆， $\begin{bmatrix}
    1&0\\0&0
\end{bmatrix}$ 没有逆。  

例🖋️ 设 $A_{3\times3}$ 可逆，把 $A$ 的第 $2$ 行 的 $(-3)$ 加到第 $1$ 行得 $B$ ，再将 $B$ 的第 $1$ 列的 $3$ 倍加到第 $2$ 列得 $C$ ，记 $P=\begin{bmatrix}
    1&-3&0\\0&1&0\\0&0&1
\end{bmatrix}$  
$PA=B$  
$BP^{-1}=C$  

> 性质1 若 $A$ 可逆，则 $A$ 的逆唯一  
> 性质2 若 $A$ 可逆，则 $A^{-1}$ 也可逆，且 $(A^{-1})^{-1}=A$  
> 性质3 若 $A$ 可逆， $\lambda\not ={0}$ ，则 $\lambda A$ 也可逆，且 $(\lambda A)^{-1}=\dfrac{1}{\lambda}A^{-1}$  
> 性质4 若 $A,B$ 是同阶可逆方阵，则 $AB$ 可逆，且 $(AB)^{-1}=B^{-1}A^{-1}$  
> 性质5 若 $A$ 可逆，则 $A^T$ 也可逆，且 $(A^T)^{-1}=(A^{-1})^T$  
> 定理 $A可逆\Leftrightarrow|A|\not ={0}$ 。当可逆时， $A^{-1}=\dfrac{1}{|A|}A^*$ 。 $|A^{-1}|=\dfrac{1}{|A|}=|A|^{-1}$

负方幂  

例🖋️ 若 $A$ 满列秩，则 $R(AB)=R(B)$ ；若 $A$ 满行秩，则 $R(BA)=R(B)$  
证：由已知 $A\sim [\dfrac{E}{0}]$  

例🖋️ 设
$Q^{-1}AQ=\begin{bmatrix}
    3&&\\&0&\\&&0
\end{bmatrix}$
， $Q$ 为 $3$ 阶可逆矩阵，则

## 向量

### $n$ 维向量

#### $n$ 维向量的概念及运算

> 定义 $n$ 个有序数所组成的数组 $(a_1,a_2,a_3,\cdots,a_n)=\vec{a}$ 称为 $n$ 维向量或行矩阵，称向量
> $\vec{a}=\begin{bmatrix}
    a_1\\a_2\\\vdots\\a_n
\end{bmatrix}$
> 为 $n$ 维列向量或列矩阵。 $a_i$ 称为向量 $\vec{a}$ 的第 $i$ 分量，分量全为实数的向量称实向量，分量为复数的向量称为复向量。  
> 零向量  
> 复向量  
> 向量的相等
>
> 线性运算  

#### 向量的内积（数量积，点积）

> 定义 设有行向量 $\vec{\alpha}=(a_1,a_2,\cdots,a_n),\beta=(b_1,b_2,\cdots,b_n)$ 令 $[\vec{\alpha},\vec{\beta}]=a_1b_1+a_2b_2+\cdots+a_nb_n=\vec{\alpha}\vec{\beta}^T$ ，称 $[\vec{\alpha},\vec{\beta}]$ 为向量 $\vec{\alpha}$ 与 $\vec{\beta}$ 的内积。

具有以下性质

1. $[\vec{\alpha},\vec{\beta}]=[\vec{\beta},\vec{\alpha}]$
2. $\lambda[\vec{\alpha},\vec{\beta}]=[\lambda\vec{\alpha},\lambda\vec{\beta}]$

> 定义 令 $\|\vec{\alpha}\|=\sqrt{[\vec{\alpha},\vec{\alpha}]}=\sqrt{{a_1}^2+{a_2}^2+\cdots+{a_n}^2}$

3. 三角 不等式 $\|\vec{\alpha}+\vec{\beta}\|\le\|\vec{\alpha}\|+\|\vec{\beta}\|$

许瓦兹不等式 $|[\vec{\alpha},\vec{\beta}]|\le\|\vec{\alpha}\|\cdot\|\vec{\beta}\|$

向量夹角

> 定义 当 $[\vec{\alpha},\vec{\beta}]=0$ 时，称向量 $\vec{\alpha},\vec{\beta}$ 正交，记作 $\vec{\alpha}\perp\vec{\beta}$

### 向量组的线性相关与线性无关

> 定义 对于向量 $\vec{\alpha},\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$
>
> 定义1 若向量组中某一向量是其余向量的线性组合，则称这组向量**线性相关**，否则就不线性相关，称为**线性无关**。  
> 定义2 设有 $n$ 维向量组 $\vec{\alpha},\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ ，如果 存在一组不全为 $0$ 的数 $\lambda_1,\lambda_2,\cdots,\lambda_m$ ，使得 $\vec{\alpha}=\lambda_1\vec{\alpha_1}+\lambda_2\vec{\alpha_2}+\cdots+\lambda_,\vec{\alpha_m}$  
>
> 定理 向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}(m\ge2)$ 线性相关 $\Leftrightarrow$ 向量组中至少有一个向量能由其余的 $m-1$ 向量线性表示
>
> 结论 当向量的个数与维数一致时，向量组所组成的行列式不等于 $0$ $\Leftrightarrow$ 向量组线性无关  
>
> 定理 设向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ 线性无关，而向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m},\vec{\beta}$ 线性相关，则向量 $\vec{\beta}$ 一定能由向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ 线性表示且表示式唯一。  
>
> 定理 若 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 线性相关，则 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r},\vec{\alpha_{r+1}},\cdots,\vec{\alpha_m}$ 也线性相关  
> 推论 含有 $\vec{0}$ 向量的向量组必线性相关  
> 推论 无关向量组减少向量仍线性无关或整体无关必部分无关
>
> 定理 设有两个向量组：  
> $$\vec{\alpha_j}=\begin{bmatrix}
    a_{1j}\\a_{2j}\\\vdots\\a_{rj}
\end{bmatrix},\quad\vec{\beta_j}=\begin{bmatrix}
    a_{1j}\\a_{2j}\\\vdots\\a_{rj}\\a_{r+1j}
\end{bmatrix},j=1,2,\cdots,m$$
> 若 $r$ 维向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ 线性无关，则 $r+1$ 维向量组 $\vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_m}$ 仍线性无关。（无关组增加分量仍无关）  
> 推论 相关组减少分量仍相关
> 当然 无关组减少分量仍无关
>
> 定理 任意 $n+1$ 个 $n$ 维向量线性相关
> 推论 任意 $m$ 个 $n$ 维向量线性相关 $(m>n)$

### 向量组的最大线性无关组与秩

> 定义 记
$A=\begin{bmatrix}
    a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\cdots&\cdots&\cdots&\cdots\\a_{m1}&a_{m2}&\cdots&a_{mn}
\end{bmatrix}$
$=\begin{bmatrix}
    \vec{\alpha_1}\\\vec{\alpha_2}\\\vdots\\\vec{\alpha_m}
\end{bmatrix}$
$=\begin{bmatrix}
    \vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_n}
\end{bmatrix}$  
称向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ 是矩阵 $A$ 的行向量


推论2 等价线性无关向量组所含向量的个数相等

定义 设 $T$ 是 $n$ 维向量所组成的向量组，在 $T$ 中选取 $r$ 个向量 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ ，如果满足：
1.  $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 线性无关；
2. $\forall\vec{\alpha}\in T,\quad\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r},\vec{\alpha}$ 线性相关 $\Leftrightarrow$ $\forall\vec{\alpha}\in T,\vec{\alpha}$ 可由 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 线性表示；

则称向量组  $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 为向量组 $T$ 的一个**最大（极大）线性无关组**，简称**最大(极大)无关组**  

两两无关不能推出整体无关

$R^n$ 是全体 $n$ 维向量所组成的向量组，则 $n$ 维单位坐标向量是 $R^n$ 的一个最大无关组，  
但任意 $n$ 个线性无关的 $n$ 维向量均是 $R^n$ 的一个最大无关组

定义 向量组的最大无关组所含向量的个数称为这个向量组的**秩**

已知 $R(\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_s})=r$ ，则 $R(\vec{\alpha_{i1}},\vec{\alpha_{i2}},\cdots,\vec{\alpha_{ir}})=r$ ，向量组 $\vec{\alpha_{i1}},\vec{\alpha_{i2}},\cdots,\vec{\alpha_{ir}}$ 线性无关，任意 $r$ 个线性无关的向量都构成它的一个最大无关组

定理 矩阵 $A$ 的秩等于矩阵 $A$ 行向量的秩，也等于矩阵 $A$ 的列向量的秩。

两个矩阵乘积的秩不会增大（乘可逆矩阵不变）

> 定理 若矩阵 $A$ 经过有限次初等行变换变成 $B$ ，则 $A$ 的行向量组与 $B$ 的行向量组等价；而 $A$ 的任意 $k$ 个列向量与 $B$ 中对应的 $k$ 个列向量有相同的线性相关性  
> $\exist P$ 可逆，使 $B=PA,\;A=P^{-1}B$ ，即 $A,B$ 的行向量能相互线性表示，故 $A$ 的行向量组与 $B$ 的行向量组等价

注1； 若 $\{\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_s}\}\sim\{\vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_t}\}$ ，则 $R(\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_s})=R(\vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_t})$ ，反之不成立  
2 若 $R(\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_s})=R(\vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_t})=R(\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_s},\vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_t})=k$ ，则 $\{\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_s}\}\sim\{\vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_t}\}$

设列向量组 $I$ 组成的矩阵为 $A$ ，列向量组 $II$ 组成的矩阵为 $B$ ，于是列向量组 $III$ 组成的矩阵为 $A|B$ ；则  
$$max\{R(A),R(B)\}\le R(A|B)\le R(A)+R(B)$$  

### 正交向量组

> 定义 一组两两正交的非 $0$ 向量，称为正交向量组，即  
> $$[\vec{\alpha}_i,\vec{\alpha}_j]\stackrel{看成列向量}{\longrightarrow}fvghjjjkk'mn $$

斯密特标准正交化方法

### 向量空间

> 定义 设 $V$ 为 $n$ 维向量构成的非空集合，若满足：
> 1. 对向量的加法封闭： $\forall\vec{\alpha},\vec{\beta}\in V\Rightarrow\vec{\alpha}+\vec{\beta}\in V$
> 2. 对向量的数乘封闭 $\forall\vec{\alpha},\lambda\in R\Rightarrow\lambda\vec{\alpha}\in V$
>
> 则称 $V$ 为实数域 $R$ 上的**向量空间**

注：若 $V$ 中的 $n$ 维向量是数组组成的向量，只须满足加法及数乘封闭，即 $V$ 为向量空间

$R^n=\{n维向量\}$ 向量空间  

$V_3=\{\lambda_1\vec{\alpha_1}+\lambda_2\vec{\alpha_2}+\cdots+\lambda_m\vec{\alpha_m}|\lambda_1,\cdots,\lambda_m\in R\}$ 构成向量空间，并称由 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ 生成的向量空间， $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_m}$ 称为向量空间的**生成元**

子空间
> 定义 若 $V_1,V_2$ 是两个向量空间,且 $V_1\subset V_2$ 则称 $V_1$ 是 $V_2$ 的**子空间**

#### 向量的基与坐标

> 定义 如果向量 $V$ 空间中的 $r$ 个 $n$ 维向量 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 满足
> 1. $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 线性无关；
> 2. $\forall\vec{\alpha}\in V,\vec{\alpha}$ 可由 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 线性表示；
>
> 则称向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 为向量空间的一个基，数 $r$ 称为向量空间的**维数**，并称 $V$ 是 $n$ 维空间。

注：
1. 定义中把“向量空间”改为“向量组”，上述定义即是最大无关组的定义。
2. 含有非 $0$ 向量的空间都有基，基只要存在，则一般不唯一；单独一个 $0$ 向量可以构成向量空间，它没有基，其维数为 $0$ 。
3.  $r$ 维向量空间中任意 $r$ 个线性无关向量均为它的基。

$V=V_1\cap V_2$  
$$\forall\vec{\alpha},\vec{\beta}\in V\Rightarrow$$

> 定义 设 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 是向量空间的一个基， $\vec{\alpha}$ 是 $V$ 中一向量，若 $\vec{\alpha}=x_1\vec{\alpha_1}+x_2\vec{\alpha_2}+\cdots+x_r\vec{\alpha_r}$ ，则称有序数组 $(x_1,x_2,\cdots,x_r)$ 为向量 $\vec{\alpha}$ 在基 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 下的**坐标**  
> 向量在单位坐标向量下的坐标与向量的坐标一致，否则不一致

#### 基变换与坐标变换

> 定义 设列向量组 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_n}$ 及 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_n}$ 是 $n$ 维向量空间 $V$ 中的两个基，记 $A=(\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_n}),B=\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_n}$ ，则 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 可由 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 表示可表为 $B=AP$ ，称为基变换公式，矩阵 $P$ 称为由基 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 到基 $\vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_r}$ 的**过渡矩阵**。

更详细的表示
$$\begin{align}
    \left\{\begin{aligned}
        &\vec{\beta_1}=p_{11}\vec{\alpha_1}+p_{12}\vec{\alpha_2}+\cdots+p_{1n}\vec{\alpha_n}\\
        &\vec{\beta_2}=p_{21}\vec{\alpha_1}+p_{22}\vec{\alpha_2}+\cdots+p_{2n}\vec{\alpha_n}\\
        &\cdots\,\cdots\\
        &\vec{\beta_n}=p_{n1}\vec{\alpha_1}+p_{n2}\vec{\alpha_2}+\cdots+p_{nn}\vec{\alpha_n}\\
    \end{aligned}\right.
\end{align}$$

记
$P=\begin{bmatrix}
    p_{11}&\cdots&p_{1n}\\
    \vdots&&\vdots\\p_{n1}&\cdots&p_{nn}
\end{bmatrix}$  
即
$$\begin{bmatrix}
    \vec{\alpha_1},\vec{\alpha_2},\cdots,\vec{\alpha_n}
\end{bmatrix}P=\begin{bmatrix}
    \vec{\beta_1},\vec{\beta_2},\cdots,\vec{\beta_n}
\end{bmatrix}$$

坐标变换

### 一般向量空间简介

将“数”推广为一般的元素“非数”：函数、矩阵等任意元素。

> 定义1 
> 1. 对定义的加法、数乘运算封闭
> 2. 四条加法公理  
> 3. 四条数乘公理
>
> 满足上面的向量空间也称实数域 $R$ 上为**线性空间(实线性空间)**

#### 内积

对称性 可加性 齐次性 性  
规定了内积的向量空间是一个欧几里得空间

#### 线性变换

## 线性方程

### 克莱姆法则(Cramer's Rule)

设有 $n$ 个未知数 $x_1,x_2,\cdots,x_n$ 的 $m$ 个线性方程组组成的方程为  
$\begin{cases}
    a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1\\a_{21}x_1+a_{22}x_2+\cdots+a_{1n}x_n=b_2\\\vdots\\a_{m1}x_1+a_{m2}x_2+\cdots+a_{1n}x_n=b_m
\end{cases}\Leftrightarrow
\begin{bmatrix}
    a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\cdots&&\cdots&\\a_{m1}&a_{m2}&\cdots&a_{mn}
\end{bmatrix}
\begin{bmatrix}
    x_1\\x_2\\\vdots\\x_n
\end{bmatrix}=
\begin{bmatrix}
    b_1\\b_2\\\vdots\\b_n
\end{bmatrix}\Leftrightarrow A\bold{X}=\bold{B}$

### 齐次线性方程组


$$\begin{cases}
    A\vec{x_0}=0\\B\vec{x_0}=0
\end{cases}\Leftrightarrow\begin{bmatrix}
    A\\B
\end{bmatrix}\vec{x_0}=0$$

### 非齐次线性方程组

> 性质1 非齐次方程的任意两解之差是对应齐次方程的解  
> 性质2 齐次的解加非齐次的解仍是非齐次的解

齐次方程通解结构定理

$A\vec{x}=\vec{\beta}$ 有解 $\Leftrightarrow$ 向量

称为方程的**表示矩阵**或**增广矩阵**

## 矩阵的相似对角化

### 方阵的特征值和特征向量

> 定义 设 $A$ 为 $n$ 阶方阵，如果数 $n$ 和 $n$ 维非零向量 $\vec{x}$ 使关系式 $A\vec{x}=\lambda\vec{x}$ 成立，则称 $\lambda$ 为 $A$ 的**特征值**， $\vec{x}$ 称为 $A$ 的对应于(属于) $\lambda$ 特征值的**特征向量**

求法

非 $0$ 向量 $\vec{x}$ 使 $A\vec{x}=\lambda\vec{x}\Leftrightarrow(A-\lambda E)\vec{x}=\vec{0}$ 有非 $0$ 解 $\Leftrightarrow|A-\lambda E|=0$  
方程 $|A-\lambda E|=0$ 是关于 $\lambda$ 的一元 $n$ 次方程，称为 $A$ 的**特征方程**  
$f(\lambda)=|A-\lambda E|$ 是一个关于 $\lambda$ 的 $n$ 阶多项式，称为 $A$ 的**特征多项式**

$A^2-2A=E\Rightarrow\lambda^2-2\lambda-1=0$   
即  
$\varphi(A)=0\Rightarrow\varphi(\lambda)=0$

1. $\lambda_1+\lambda_2+\cdots+\lambda_n=a_{11}+a_{22}+\cdots+a_{nn}=\operatorname{tr}A(称为A迹)$
2. $\lambda_1\cdot\lambda_2\cdot\cdots\cdot\lambda_n=|A|$

$A\vec{p}=\lambda\vec{p}\Rightarrow\vec{p}=\lambda A^{-1}\vec{p}\Rightarrow\dfrac{1}{\lambda}=A^{-1}\vec{p}$  
$|A-\lambda E|=0\Rightarrow|A||E-\lambda A^{-1}|=0\Rightarrow(-1)^n|\dfrac{1}{\lambda}E-A^{-1}|=0$

> 定理 设 $\lambda_1,\lambda_2,\cdots,\lambda_n$ 是方阵 $A$ 的特征根， $\vec{p_1},\vec{p_2},\cdots,\vec{p_n}$ 是与之对应的特征向量，如果 $\lambda_1,\lambda_2,\cdots,\lambda_n$ 互不相等，则 $\vec{p_1},\vec{p_2},\cdots,\vec{p_n}$ 线性无关

> 推广 设 $\vec{p_{i1}},\vec{p_{i2}},\cdots,\vec{p_{it_i}}$ 是方阵 $A$ 对应于特征值 $\lambda_i$ 的 $t_i$ 个线性无关的特征向量 $(i=1,2,\cdots,m)$ ，且 $\lambda_1,\lambda_2,\cdots,\lambda_m$ 互不相等，则 $\vec{p_{11}},\vec{p_{12}},\cdots,\vec{p_{1t_1}},\vec{p_{21}},\vec{p_{22}},\cdots,\vec{p_{2t_2}},\cdots,\vec{p_{m1}},\vec{p_{m2}},\cdots,\vec{p_{mt_m}}$ 线性无关 

### 相似矩阵

$\exist P^{-1}$ ，使 $P^{-1}AP=B\Rightarrow A=(p^{-1})^{-1}BP^{-1}=Q^{-1}BQ$  
称 $P^{-1}AP$ 为对 $A$ 做**相似变换**，可逆矩阵 $P$ 为**相似变化阵**

性质：  
1. 反身性： $A$ 与 $A$ 相似 （因 $E^{-1}AE=A$）
2. 对称性： $A$ 与 $B$ 相似，则 $B$ 与 $A$ 相似
3. 传递性： $A$ 与 $B$ 相似， $B$ 与 $C$ 相似，则 $A$ 与 $C$ 相似

Conclusion：
1. $A$ 与 $B$ 相似，则 $R(A)=R(B),|A|=|B|$
2. $A$ 与 $B$ 相似，则 $kA$ 与 $kB$ 相似， $A^m$ 与 $B^m$ 相似（ $k$ 为实数， $m$ 为正整数）
3. $A$ 与 $B$ 相似，且 $A$ 可逆，则 $A^{-1}$ 与 $B^{-1}$ 也相似，$A^*$ 与 $B^*$ 也相似
4. $A$ 与 $B$ 相似， $f(x)$ 为任意多项式，则 $f(A)$ 与 $f(B)$ 相似

> 定理 设 $A$ 与 $B$ 相似，则 $A$ 与 $B$ 有相同的特征多项式，从而 $A$ 与 $B$ 有相同的特征值，进一步，有相同的迹  
> 即若 $A$ 与 $B$ 相似，则 $|\lambda E-A|=|\lambda E-B|,\operatorname{tr}A=\operatorname{tr}B$

Conclusion2

讨论：对于 $\forall A_{n\times n}$ 如何寻找可逆阵 $P$ ，使 $P^{-1}AP=\Lambda$  
证明：  
$P^{-1}AP=\Lambda$  
$\Rightarrow AP=P\Lambda$  
$\Leftrightarrow A(\vec{p_1}\cdots\vec{p_n})=(\vec{p_1}\cdots\vec{p_n})\begin{bmatrix}
    \lambda_1&&&\\&\lambda_2&&\\&&\cdots&\\&&&\lambda_n
\end{bmatrix}$

> 定理 $n$ 阶方阵 $A$ 与对角阵相似（可对角化） $\Leftrightarrow$ $A$ 有 $n$ 个线性无关的特征向量

将 $A$ 对角化的步骤：  
1. 求出特征值
2. 求出 $n$ 个线性无关的特征向量
3. 构造 $P$
4. 结果

### 实对称阵的相似对角化

> 定理 实对称阵的特征值为实数，特征向量也为实向量

证明：设 $\lambda$ 为实对称阵 $A$ 的特征值， $\vec{x}$ 为对应的特征向量

$A\vec{x}=\lambda\vec{x}$
> 定理
>

证明：

> **二重根求特征向量时可直接选择两正交向量**

## 二次型

### 二次型及其标准型

> 定义 含有 $n$ 个变量 $x_1,x_2,\cdots,x_n$ 的二次**齐次函数**  
> $$f(x_1,x_2,\cdots,x_n)=\sum\limits_{i,j=1}^na_{ij}x_ix_j$$  
> 称为 $n$ 元二次型， $a_ij$ 为实数称为实二次型， $a_ij$ 为复数称为复二次型。本教材只讨论实二次型。  
>
> 齐次函数： 若 $f(tx,ty)=t^kf(x,y)$ ，称 $f(x,y)$ 关于变量 $x,y$ 是 $k$ 次**齐次函数**
>
> 实二次型中最简单的一种是只含平方项，即  
> $$f(y_1,y_2,\cdots,y_n)=k_1{y_1}^2+k_2{y_2}^2+\cdots+k_n{y_n}^2$$  
> 称二次型的标准型。若标准形中非零的 $k_i=\pm1$ 称为二次型的规范形
>
>