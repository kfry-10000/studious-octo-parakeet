# 线性代数
张谋  
<https://sakai.cqu.edu.cn>  
Oct. 8th, 2024
# 行列式  
## 预备知识 
引进行列式的概念，讨论行列式性质，计算行列式值  
二元线性方程组  
$\begin{cases}
    a_{11}x_1+a_{12}x_2=b_1\\a_{21}x_1+a{22}x_2=b_2\end{cases}$  
消元法解不通用  
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
## 行列式的定义  
### $n$ 阶行列式的定义  
三阶行列式的定义为  
$$\begin{vmatrix}
    a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}
\end{vmatrix}=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}$$  
1. 等式右端是 $6$ 项之和，每项都是位于不同行不同列的 $3$ 个元素的乘积，即同一项中不可能有两个元素来自同一行同一列  
2. 每一项各元素的航标排列成自然排列，因此右端的任意一项除符号外可写成$a_{1p_1}a_{2p_2}a_{3p_3}$ ，其中 $p_1p_2p_3$ 为 $123$ 的某个排列
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
则称 **$D$为$n$阶行列式** 

对角行列式的值=对角元之积  
反对角行列式  


双阶乘  
$(2k)!!=2\times4\times\cdots\times{2k}\\(2k+1)!!=1\times3\times\cdots\times{2k+1}$  
## 行列式的性质  
> 性质1  $D=D^T$ (行列式与其转置行列式相等)

证明：记$D=\det(a_{ij}),D^T=\det(b_{ij})$ 则 $b_{ij}=a{ji}$  
$$D^T=\det(b_{ij})=\sum\limits_{p_1\cdots p_n}(-1)^tb_{1p_1}\cdots b_{np_n}=\sum\limits_{p_1\cdots p_n}(-1)^ta_{p_11}\cdots a_{p_nn}$$ 

> 性质2 互换行列式的两行或两列，行列式改变符号

