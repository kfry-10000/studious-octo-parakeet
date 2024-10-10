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
\end{vmatrix}=a_{ij}A_{ij}$
