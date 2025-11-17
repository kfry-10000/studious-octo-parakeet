# 高等数学II-2

## 向量代数

### 第一节 向量及其加减法 向量与数的乘法

#### 向量的概念

向量：既有大小又有方向的量  
向量表示 $\vec{a}$ 或 $\overrightarrow{M_1M_2}$  
以
向量的摸： $|\vec{a}|$  
单位向量：模长为 $1$ 的向量 $\vec{a^0}$
零向量： $\vec{0}$  
自由向量：不考虑起点位置
相等向量：大小且方向相等  
复向量：大小相等但方向相反 $-\vec{a}$  
向径：将向量的起点移到坐标原点，则该向量为向径

#### 向量的加减法

1. 加法 $\vec{a}+\vec{b}=\vec{c}$  
   三角形法则，平行四边形法则  
   特殊的：若 $\vec{a}\parallel\vec{b}$ ，分为**同向**和**反向**  
   三角形法则可推广至多个向量相加
   **向量的加法符合以下运算规则：**
   1. 交换律： $\vec{a}+\vec{b}=\vec{b}+\vec{c}$
   2. 结合律： $(\vec{a}+\vec{b})+\vec{c}=\vec{a}+(\vec{b}+\vec{c})$
   3. $\vec{a}+(-\vec{a})=\vec{0}$
2. 减法 $\vec{a}-\vec{b}=\vec{a}+(-\vec{b})$

#### 向量与数的乘法

设 $\lambda$ 是一个数，向量 $\vec{a}$ 与 $\lambda$ 的乘积 $\lambda\vec{a}$ 规定为：  
1. $\lambda>0$ ， $\lambda\vec{a}$ 与 $\vec{a}$ 同向， $|\lambda\vec{a}|=\lambda|\vec{a}|$
2. $\lambda=0$ ， $\lambda\vec{a}=\vec{0}$
3. $\lambda<0$ ， $\lambda\vec{a}$ 与 $\vec{a}$ 反向， $|\lambda\vec{a}|=-\lambda|\vec{a}|$

数与向量的乘积符合下列运算规律：
1. 结合律： $\lambda(\mu\vec{a})=\mu(\lambda\vec{a})=(\lambda\mu)\vec{a}$
2. 分配律： $(\lambda+\mu)\vec{a}=\lambda\vec{a}+\mu\vec{a}\qquad\lambda(\vec{a}+\vec{b})$

两个向量的平行关系
> 定理 设向量 $\vec{a}\not ={0}$ ，那么向量 $\vec{b}\parallel\vec{a}\Leftrightarrow\exist唯一\lambda\in\reals,\ \vec{b}=\lambda\vec{a}$

#### 向量在轴上的投影

空间两向量的夹角的概念： 
$\vec{a}\not ={0},\quad\vec{b}\not ={0}$ ，向量 $\vec{a}$ 与向量 $\vec{b}$ 的夹角 $\varphi=(\widehat{\vec{a},\vec{b}})=(\widehat{\vec{b},\vec{a}})\quad(0\le\varphi\le\pi)$  
类似地，可定义向量与一轴或空间两轴的夹角  
特殊地，当两个向量中**有一个零向量**时，规定它们的夹角可在 $0$ 与 $\pi$ 之间任意取值

空间一点在轴上的投影

空间一向量在轴上的投影

记为 $\Pr j_u$

注意，向量在轴上的投影**是一个数**

定理2（投影定理）：
> 两个向量的和在轴上的投影等于两个向量在该轴上的投影之和

#### 小结 思考题

### 第一节 空间直角坐标系

三个坐标轴的正方向符合右手系

八个卦限

#### 空间点的直角坐标

有序数组 $(x,y,z)$

#### 空间两点间的距离

$\sqrt{(x_1-x_2)^2+(y_1-y_2)^2+(z_1-z_2)^2}$

#### 向量的空间表示

空间中的点与向径为一一对应关系

#### 小结 思考题 

### 第二节 向量的乘法运算

#### 两向量的数量积

> 定义 设向量 $\vec{a}$ 与 $\vec{b}$ 的夹角为 $\theta$ 则称 $|\vec{a}||\vec{b}|\cos\theta$ 为向量 $\vec{a}$ 与 $\vec{b}$ 的数量积，记为 $\vec{a}\cdot\vec{b}$ ，即  
> 
> $$\vec{a}\cdot\vec{b}=|\vec{a}||\vec{b}|\cos\theta$$
> 数量积也称为“**点积**”、“**内积**”

#### 向量的向量积

#### 向量的混合积

> 定义 设已知三个向量 $\vec{a},\vec{b},\vec{c}$ ，数量 $(\vec{a}\times\vec{b})\cdot\vec{c}$ 称为这三个向量的混合积
> $$\left[\vec{a}\vec{b}\vec{c}\right]=(\vec{a}\times\vec{b})\cdot\vec{c}=\begin{vmatrix}
   a_x&a_y&a_z\\b_x&b_y&b_z\\c_x&c_y&c_z
\end{vmatrix}$$

1. 混合积的几何意义 以向量 $\vec{a},\vec{b},\vec{c}$ 为棱的平行六面体的体积
2. $\left[\vec{a}\vec{b}\vec{c}\right]=(\vec{a}\times\vec{b})\cdot\vec{c}=(\vec{b}\times\vec{c})\cdot\vec{a}=(\vec{c}\times\vec{a})\cdot\vec{b}$

### 平面及其方程

#### 点法式方程

点 $(x_0,y_0,z_0)$ ，法向量 $(A,B,C)$

$$A(x-x_0)+B(y-y_0)+C(z-z_0)=0$$

#### 三点式方程

过三点 $M_1(x_1,y_1,z_1),M_2(x_2,y_2,z_2),M_3(x_3,y_3,z_3)$ 的平面方程  

$$\begin{vmatrix}
   x-x_1&y-y_1&z-z_1\\x-x_2&y-y_2&z-z_2\\x-x_3&y-y_3&z-z_3
\end{vmatrix}=0$$

#### 平面的一般方程

$$Ax+By+Cz+D=0$$

#### 平面的截距式方程

$$\dfrac{x}{a}+\dfrac{y}{b}+\dfrac{z}{c}=1$$y2

#### 两平面的夹角

> 定义 两平面**法向量**之间的夹角称为两平面的夹角（通常取锐角）

两平面位置特征
1. $\Pi_1\perp\Pi_2\iff A_1A_2+B_1B_2+C_1C_2=0$
2. $\Pi_1\parallel\Pi_2\iff $

### 直线

#### 空间直线的一般方程

> 定义 空间直线可看成两平面的交线

$$\begin{cases}
   \Pi_1:\\\Pi_2: w 
\end{cases}$$  

> 定义 平行定直线 $l$ 

### 空间的曲线及其方程

#### 空间曲线的一般方程

空间曲线可视为两曲面的**交线**，其一般方程为  
$$\begin{cases}
   F(x,y,z)=0\\G(x,y,z)=0
\end{cases}$$
特点：
1. 曲线上的点的坐标都满足该方程组
2. 不在曲线上的点都不满足该方程组

### 二次曲面

> 三元二次方程 $Ax^2+By^2+Cz^2+Dxy+Eyz+Fzx+Gx+Hy+Iz+J=0$  

#### 平面点集

### 偏导数

#### 偏导数及其计算

> 令 $f_{xx}(x_0,y_0)=A\quad f_{xy}(x_0,y_0)=B\quad f_{yy}(x_0,y_0)=C$ 
> 1. $AC-B^2>0$ 时有极值  
>    当 $A<0$ 时有**极大值**，当 $A>0$ 时有**极小值**
> 2. $AC-B^2<0$ 时没有极值
> 3. $AC-B^2=0$ 时可能有极值，也可能无极值

