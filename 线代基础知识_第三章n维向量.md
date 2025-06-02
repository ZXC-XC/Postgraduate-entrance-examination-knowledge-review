

# 第三章 n维向量

# **第三章 $n$ 维向量——难点，加油**

## **一、知识结构网络图**

### **运算**
- 加法，数乘，内积
- 如果 $\beta=k_1\alpha_1+\cdots+k_n\alpha_n$

### **概念**
- 称 $\beta$ 可由 $\alpha_1,\cdots,\alpha_n$线性表出
- 方程组 $x_1\alpha_1+\cdots+x_n\alpha_n=\beta$ 有解
- $r(\alpha_1,\cdots,\alpha_n)=r(\alpha_1,\cdots,\alpha_n,\beta)$

### **判定**
- $\alpha_1,\cdots,\alpha_n$ 无关，则 $\alpha_1,\cdots,\alpha_n,\beta$ 相关

### **等价**
- 若 $\alpha_1,\cdots,\alpha_n$ 与 $\beta_1,\cdots,\beta_n$ 可互相线性表出

### **线性相关**

#### **概念**
- 若在 $n$ 个分量 $k_1,\cdots,k_n$ 中，至少有一个 $k_1,\cdots,k_n\neq 0$
- $k_1\alpha_1+\cdots+k_n\alpha_n = 0$ 有非零解
- 充分条件——$r(\alpha_1,\alpha_2,\cdots,\alpha_n)<n$
- 若 $\alpha_i$ 可由 $\alpha_1,\cdots,\alpha_{i-1},\alpha_{i+1},\cdots,\alpha_n$ 线性表出

#### **充分条件**
- $n+1$ 个 $n$ 维向量必相关

### **线性无关**

#### **概念**
- 如果 $k_1\alpha_1+\cdots+k_n\alpha_n=0$，则必有 $k_1=0,\cdots,k_n=0$
- $k_1\alpha_1+\cdots+k_n\alpha_n=0$ 只有零解
- $r(\alpha_1,\cdots,\alpha_n)=n$

#### **判定**
- 阶梯形同向量组

### **极大线性无关组**

#### **概念**

#### **求法**

### **向量维数的秩**
- 向量组的秩

### **向量空间**

#### **概念**
- 解空间

#### **坐标**
- 过渡矩阵
- 规范正交基

### **基础内容**

## **二、基本内容与重要结论**

### **基础知识**

$n$ 个数 $a_{i1},a_{i2},\cdots,a_{in}$ 所组成的有序数组
$\alpha_i = (a_{i1},a_{i2},\cdots,a_{in})^T$ 或 $\alpha_i = (a_{i1},a_{i2},\cdots,a_{in})$

称为 $n$ 维向量。其中 $a_{i1},a_{i2},\cdots,a_{in}$ 称为向量 $\alpha_i$（或 $\alpha_i$）的分量，前一个表示式称为列向量，后者称为行向量。

设 $n$ 维向量 $\alpha = (a_1,a_2,\cdots,a_n)^T$，$\beta = (b_1,b_2,\cdots,b_n)^T$，

#### **加法**
$\alpha + \beta = (a_1+b_1,a_2+b_2,\cdots,a_n+b_n)^T$

#### **数乘向量**
$k\alpha = (ka_1,ka_2,\cdots,ka_n)^T$

#### **内积**
$(\alpha,\beta) = a_1b_1+a_2b_2+\cdots+a_nb_n$

### **【评注】**
（1）对于 $\alpha = (a_1,a_2,\cdots,a_n)^T$ 的长度
$\|\alpha\| = \sqrt{(\alpha,\alpha)} = \sqrt{a_1^2+a_2^2+\cdots+a_n^2}$

例如：$\alpha = (1,2,3)^T$，则 $(\alpha,\alpha) = 1^2+2^2+3^2 = 14$，因此向量 $\alpha$ 的长度为 $\|\alpha\| = \sqrt{14}$。

另 $\frac{\alpha}{\|\alpha\|} = \frac{1}{\sqrt{14}}(1,2,3)^T$ 是单位向量。

（2）若 $\alpha = 0$ 即 $a_1^2+a_2^2+\cdots+a_n^2 = 0 \Leftrightarrow \alpha = 0$。

（3）若 $(\alpha,\beta)=0$，则称 $\alpha$ 与 $\beta$ 正交，此时若 $\alpha \neq 0$，$\beta \neq 0$，则称 $\alpha$ 与 $\beta$ 垂直，记为 $\alpha \perp \beta$。

### **定义3.1** 设 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 是 $n$ 个向量，$k_1,k_2,\cdots,k_n$ 是一组数，称 $k_1\alpha_1+k_2\alpha_2+\cdots+k_n\alpha_n$ 是 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 的线性组合。

### **定义3.2** 对 $n$ 个向量 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 而言，若存在不全为零的数 $k_1,k_2,\cdots,k_n$ 使得
$k_1\alpha_1+k_2\alpha_2+\cdots+k_n\alpha_n=0$

则称向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 的线性相关，或者说向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 线性相关（简记为相关）。

例如：$\alpha_1 = (1,0)^T$，$\alpha_2 = (2,1)^T$，$\alpha_3 = (1,-1)^T$，$\beta = (3,2)^T$，则 $\alpha_1 + \alpha_2 + \alpha_3 = \beta$。

又如：$\alpha_1 = (2,0,0)^T$，$\alpha_2 = (0,2)^T$，$\beta = (0,4,3)^T$，则 $\alpha_1 + 2\alpha_2 \neq \beta$。

明显由于 $\alpha_1,\alpha_2,\alpha_3$ 线性无关，且表示法不唯一。

又如：$\alpha_1 = (1,1)^T$，$\alpha_2 = (2,0)^T$，$\beta = (3,3)^T$，则 $\beta = \alpha_1 + \alpha_2$ 且 $\beta = 3\alpha_1 - 3\alpha_2$。

### **定义3.3** 对 $n$ 个向量 $\alpha_1,\alpha_2,\cdots,\alpha_n$，如果存在不全为零的数 $k_1,k_2,\cdots,k_n$ 使得
$k_1\alpha_1+k_2\alpha_2+\cdots+k_n\alpha_n=0$

则称向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 线性相关，否则，称向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 线性无关。

# **$n$维向量线性相关示例**

（也就是说，当且仅当 $k_1 = k_2 = \cdots = k_n = 0$ 时，$k_1\alpha_1 + k_2\alpha_2 + \cdots + k_n\alpha_n = 0$ 才能成立，或者说，只要 $k_1,k_2,\cdots,k_n$ 不全为零，则 $k_1\alpha_1 + k_2\alpha_2 + \cdots + k_n\alpha_n \neq 0$）。

例如，对于下列向量组的线性相关关系皆容易判别：

（1）$\alpha_1 = (1,2,3)^T$，$\alpha_2 = (2,3,4)^T$，$\alpha_3 = (0,0,0)^T$，
因为 $\alpha_3 = 0$，
组合系数 $0,0,1$ 不全为零，故向量组 $\alpha_1,\alpha_2,\alpha_3$ 线性相关。

（2）$\alpha_1 = (1,2,3)^T$，$\alpha_2 = (2,4,6)^T$，$\alpha_3 = (3,0,5)^T$，
因为 $2\alpha_1 - \alpha_2 = 0$，
组合系数 $2,-1,0$ 不全为零，故向量组 $\alpha_1,\alpha_2,\alpha_3$ 线性相关。

（3）$\alpha_1 = (1,2,3)^T$，$\alpha_2 = (2,3,4)^T$，$\alpha_3 = (3,5,7)^T$，
因为 $\alpha_1 + \alpha_2 - \alpha_3 = 0$，
组合系数 $1,1,-1$ 不全为零，故向量组 $\alpha_1,\alpha_2,\alpha_3$ 线性相关。

（4）$\alpha_1 = (1,2,3)^T$，$\alpha_2 = (0,4,5)^T$，$\alpha_3 = (0,0,6)^T$，
如果 $k_1\alpha_1 + k_2\alpha_2 + k_3\alpha_3 = 0$，按分量写出，有
$$\begin{cases}
k_1 &= 0, \\
4k_2 &= 0, \\
3k_1 + 5k_2 + 6k_3 &= 0.
\end{cases}$$

故 $k_1 = 0,k_2 = 0,k_3 = 0$，

所以 $\alpha_1,\alpha_2,\alpha_3$ 线性无关。

### **定义3.4** 设有两个 $n$ 维向量组（Ⅰ）$\alpha_1,\alpha_2,\cdots,\alpha_s$ 和（Ⅱ）$\beta_1,\beta_2,\cdots,\beta_t$，若（Ⅱ）中的每个向量 $\beta_i$（$i = 1,2,\cdots,t$）都可由（Ⅰ）中的向量 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性表示，则称向量组（Ⅰ）可以线性表出向量组（Ⅱ），记为 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性表出 $\beta_1,\beta_2,\cdots,\beta_t$。

如果（Ⅰ）（Ⅱ）这两个向量组可以互相线性表出，则称这两个向量组等价向量组。

（1）$\alpha_1 = (1,0,0)^T$，$\alpha_2 = (0,1,0)^T$，$\alpha_3 = (0,0,1)^T$ 与 $\beta_1 = (1,1,1)^T$，$\beta_2 = (1,1,0)^T$，$\beta_3 = (1,0,0)^T$，

由
$$\beta_1 = \alpha_1 + \alpha_2 + \alpha_3,$$
$$\beta_2 = \alpha_1 + \alpha_2,$$
$$\beta_3 = \alpha_1,$$

知向量组 $\alpha_1,\alpha_2,\alpha_3$ 可由向量组 $\beta_1,\beta_2,\beta_3$ 线性表出，

而
$$\alpha_1 = \beta_3,$$
$$\alpha_2 = \beta_2 - \beta_3,$$
$$\alpha_3 = \beta_1 - \beta_2,$$

知向量组 $\alpha_1,\alpha_2,\alpha_3$ 与 $\beta_1,\beta_2,\beta_3$ 可以相互线性表出，所以这两个向量组是等价向量组。

（2）$\alpha_1 = (1,0,0)^T$，$\alpha_2 = (1,2,0)^T$ 与 $\beta_1 = (2,1,1)^T$，$\beta_2 = (0,1,1)^T$，

由
$$\alpha_1 = \frac{1}{2}\beta_1 - \frac{1}{2}\beta_2,\; \alpha_2 = -\frac{1}{2}\beta_1 + \frac{5}{2}\beta_2 + 2\beta_3,$$

知向量组 $\alpha_1,\alpha_2$ 由向量组 $\beta_1,\beta_2,\beta_3$ 线性表出，但是明显 $\beta_1,\beta_2,\beta_3$ 不能由 $\alpha_1,\alpha_2$ 线性表出，因为 $\alpha_1,\alpha_2$ 都在 $xOy$ 平面内，所以向量组 $\beta_1,\beta_2,\beta_3$ 不能由向量组 $\alpha_1,\alpha_2$ 线性表出。这两个向量组不等价。


# **$n$维向量线性无关概念**

### **定义3.5** 在向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 中，若存在 $r$ 个向量 $\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_r}$ 线性无关，且向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 中任何 $r+1$ 个向量都线性相关，则称向量组 $\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_r}$ 是向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 的一个极大线性无关组。

### **定义3.6** 向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 的秩是其线性无关向量的最大个数，即极大线性无关组的向量个数。

例如，向量组 $\alpha_1 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$，$\alpha_2 = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$，$\alpha_3 = \begin{bmatrix} 2 \\ 4 \end{bmatrix}$，$\alpha_4 = \begin{bmatrix} 3 \\ 6 \end{bmatrix}$，$\alpha_5 = \begin{bmatrix} 4 \\ 8 \end{bmatrix}$，

$\alpha_2 = 0$ 与其他任一向量线性无关；$\alpha_3 = 2\alpha_1$，$\alpha_4 = 3\alpha_1$，$\alpha_5 = 4\alpha_1$，

所以向量组 $\alpha_1,\alpha_2,\alpha_3,\alpha_4,\alpha_5$ 线性相关；且任何两个向量组成的向量组线性无关，如 $\alpha_1,\alpha_2$。

故向量组的秩 $r(\alpha_1,\alpha_2,\alpha_3,\alpha_4,\alpha_5) = 2$。

注意向量组的极大线性无关组不一定唯一，但如 $\alpha_1,\alpha_2$ 也是极大线性无关组，则向量组 $\alpha_1,\alpha_2,\alpha_3,\alpha_4,\alpha_5$ 的一个极大线性无关组。

另外，向量组的秩 $r(\alpha_1,\alpha_2,\alpha_3,\alpha_4,\alpha_5) = 2$。

## **重要定理**

### **定理3.1** 向量 $\beta$ 可由向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性表示
$\Leftrightarrow$ 非齐次线性方程组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ $\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{bmatrix} = \beta$ 有解

$\Leftrightarrow$ 秩 $r(\alpha_1,\alpha_2,\cdots,\alpha_s) = r(\alpha_1,\alpha_2,\cdots,\alpha_s,\beta)$。

### **定理3.2** 向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性相关
$\Leftrightarrow$ 齐次线性方程组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ $\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{bmatrix} = 0$ 有非零解

$\Leftrightarrow$ 向量组的秩 $r(\alpha_1,\alpha_2,\cdots,\alpha_s) < s$。

### **推论1** $r$ 个 $n$ 维向量 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 线性相关的充分必要条件是其行列式为零。

### **推论2** $n+1$ 个 $n$ 维向量一定线性相关。

### **定理3.3** 任何向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 则必 $\exists$ 部分组 $\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_r}$（$r\leq s$）线性无关，且 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 可由 $\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_r}$ 线性表出，反之不成立。

向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 及 $\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_r}$（$1\leq i_1<i_2<\cdots<i_r\leq s$）称 $\alpha_{i_1},\alpha_{i_2},\cdots,\alpha_{i_r}$ 是 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 的极大线性无关组。

### **定理3.4** $\alpha_1,\alpha_2,\cdots,\alpha_r$ 线性无关 $\Rightarrow$ 延伸组 $\alpha_1,\alpha_2,\cdots,\alpha_r,\beta$ 线性无关；
$\alpha_1,\alpha_2,\cdots,\alpha_r$ 线性相关 $\Rightarrow$ 缩短组 $\alpha_1,\alpha_2,\cdots,\alpha_{r-1}$ 线性无关，反之均不成立。

向量组 $\alpha_1 = (a_{11},a_{21},\cdots,a_{n1})^T$，$\alpha_2 = (a_{12},a_{22},\cdots,a_{n2})^T$，$\cdots$，$\alpha_s = (a_{1s},a_{2s},\cdots,a_{ns})^T$ 称为 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 的一个标准正交组，若

1. $\alpha_1,\alpha_2,\cdots,\alpha_s$ 两两正交；
2. $\|\alpha_1\| = \|\alpha_2\| = \cdots = \|\alpha_s\| = 1$。

则 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 是标准单位向量组。

### **定理3.5** 如果 $\alpha_1,\alpha_2,\cdots,\alpha_r$（$r \geq 2$）线性相关，则其中有一个向量可用其余向量线性表出；反之，若有一个向量可由其余向量线性表出，则 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 线性相关。

### **定理3.6** 若向量组 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 与 $\beta_1,\beta_2,\cdots,\beta_s$ 等价，则 $r=s$，且是由 $C$ 表示如下：

$$\begin{bmatrix} \beta_1,\beta_2,\cdots,\beta_s \end{bmatrix} = \begin{bmatrix} \alpha_1,\alpha_2,\cdots,\alpha_r \end{bmatrix}C,$$

其中 $C$ 为方阵且行列式 $|C| \neq 0$。

### **定理3.7** 如果向量组 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 可由向量组 $\beta_1,\beta_2,\cdots,\beta_s$ 线性表示，且 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 线性无关，则 $r \leq s$，且向量组 $\beta_1,\beta_2,\cdots,\beta_s$ 也线性无关，则 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 与 $\beta_1,\beta_2,\cdots,\beta_s$ 等价。

### **推论** 如果 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 线性无关，且它可由 $\beta_1,\beta_2,\cdots,\beta_r$ 线性表出，则 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 与 $\beta_1,\beta_2,\cdots,\beta_r$ 等价。

### **定理3.8** 设 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 可由 $\beta_1,\beta_2,\cdots,\beta_s$ 线性表出，则 $r(\alpha_1,\alpha_2,\cdots,\alpha_r) \leq r(\beta_1,\beta_2,\cdots,\beta_s)$。

### **推论** 若向量组（Ⅰ）及（Ⅱ）是两个等价的向量组，则 $r$（Ⅰ）$= r$（Ⅱ）。

### **定理3.9** 如果 $r(A) = r$，则 $A$ 中有 $r$ 个线性无关的列向量，并且这些向量组成一个线性无关的向量组合，也就是 $r(A) = r$ 的秩等于 $A$ 的列秩。

### **定理3.10** $r(A) = r$ 则行秩 $= r$。

# **向量空间与标准正交基**

### **定理3.7** 全体 $n$ 维向量组成的加法和数乘运算合起来称为 $n$ 维向量空间。

### **定义3.8** 设 $W$ 是 $n$ 维向量的非空集合，如果满足
（1）$\forall \alpha,\beta \in W$，则有 $\alpha + \beta \in W$；
（2）$\forall \alpha \in W$ 及任意数 $k$，都有 $k\alpha \in W$；
则称 $W$ 是 $n$ 维向量空间的子空间。

### **定义3.9** 如果向量空间 $V$ 中的 $n$ 个向量 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 满足
（1）$\alpha_1,\alpha_2,\cdots,\alpha_n$ 线性无关；
（2）$V$ 中任意向量 $\beta$ 均可由向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 线性表出，即
$\beta = x_1\alpha_1 + x_2\alpha_2 + \cdots + x_n\alpha_n = \beta$。

则称 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 为向量空间 $V$ 的一个基（底）。其中所含向量的个数 $n$ 称为向量空间 $V$ 的维数（简称维数），$x_1,x_2,\cdots,x_n$ 称为向量 $\beta$ 在基 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 下的坐标。

### **定义3.10** 设 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 是向量空间的一组基，如它们满足
$$(\alpha_i,\alpha_j) = \begin{cases} 1, & i = j, \\ 0, & i \neq j. \end{cases}$$

则称 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 为标准正交基。

特别地，若 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 为单位向量，且 $A\alpha_i = 0$ 的解，则 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 为齐次线性方程组 $Ax = 0$ 的解所构成的向量空间，即解空间。

例如：$A = \begin{bmatrix} 1 & 0 & -1 \\ 0 & 1 & 0 \\ 1 & 0 & 1 \end{bmatrix}$，则方程 $Ax = 0$ 的基础解系是
$$\gamma_1 = (0,0,1,0)^T,\gamma_2 = (0,-1,0,1)^T$$

是解空间的基，零空间的维数是 $n-r(A) = 4-2 = 2$。

### **定义3.11** 在 $n$ 维向量空间定两组基
（Ⅰ）$\alpha_1,\alpha_2,\cdots,\alpha_n$；
（Ⅱ）$\beta_1,\beta_2,\cdots,\beta_n$。

若
$$\beta_1 = c_{11}\alpha_1 + c_{12}\alpha_2 + \cdots + c_{1n}\alpha_n,$$
$$\beta_2 = c_{21}\alpha_1 + c_{22}\alpha_2 + \cdots + c_{2n}\alpha_n,$$
$$\cdots\cdots\cdots\cdots$$
$$\beta_n = c_{n1}\alpha_1 + c_{n2}\alpha_2 + \cdots + c_{nn}\alpha_n,$$

即
$$[\beta_1,\beta_2,\cdots,\beta_n] = [\alpha_1,\alpha_2,\cdots,\alpha_n] \mathbf{C},$$

其中
$$\mathbf{C} = \begin{bmatrix} c_{11} & c_{12} & \cdots & c_{1n} \\ c_{21} & c_{22} & \cdots & c_{2n} \\ \vdots & \vdots & & \vdots \\ c_{n1} & c_{n2} & \cdots & c_{nn} \end{bmatrix}.$$

则称矩阵 $\mathbf{C}$ 为由基 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 到基 $\beta_1,\beta_2,\cdots,\beta_n$ 的过渡矩阵。

### **定理3.12** 如果 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 与 $\beta_1,\beta_2,\cdots,\beta_n$ 是 $n$ 维向量空间的两个基，且 $\gamma$ 在基底 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 的坐标为 $y_1,y_2,\cdots,y_n$，则在基底 $\beta_1,\beta_2,\cdots,\beta_n$ 的坐标为 $x_1,x_2,\cdots,x_n$，则标准变换公式为
$$\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = \mathbf{C} \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix}, 或 \mathbf{x} = \mathbf{C}\mathbf{y},$$

其中 $n$ 阶矩阵 $\mathbf{C}$ 是由基底 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 到基底 $\beta_1,\beta_2,\cdots,\beta_n$ 的过渡矩阵。

关系：
$[\beta_1,\beta_2,\cdots,\beta_n] = [\alpha_1,\alpha_2,\cdots,\alpha_n]\mathbf{C}$，其中 $\mathbf{C}$ 为过渡矩阵。

### **定理3.13** 若 $\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n$ 是施密特正交化，设
$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n] = [\alpha_1,\alpha_2,\cdots,\alpha_n]\mathbf{C}$，

则 $\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n$ 是规范正交基当且仅当矩阵 $\mathbf{C}$ 为正交矩阵。

## **【注释】** 线性无关的判定

若想判断向量组是否线性无关，通常可以采用定义或定理来分析判断。

（1）用定义判断 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性无关的根据是：
设 $k_1\alpha_1 + k_2\alpha_2 + \cdots + k_s\alpha_s = 0$

$\Downarrow$ 检查方程
$$k_1 = 0,k_2 = 0,\cdots,k_s = 0.$$

（2）用秩 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性无关
$\Leftrightarrow [\alpha_1,\alpha_2,\cdots,\alpha_s] $ $\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{bmatrix} = 0$ 只有零解
$\Leftrightarrow$ 秩 $r(\alpha_1,\alpha_2,\cdots,\alpha_s) = s$。

系数矩阵 $A$ 的 $r(A) = A$ 的列秩 $= A$ 的行秩，$r(AB) \leq \min(r(A),r(B))$。

若 $A$ 可逆，则 $r(AB) = r(B)$，$r(BA) = r(B)$。

若 $A$ 是 $m \times n$ 矩阵，$B$ 是 $n \times s$ 矩阵且 $AB = 0$，则 $r(A) + r(B) \leq n$。

（3）应用：

### **【例3.20】** 设向量组（Ⅰ）可由向量组（Ⅱ）线性表出，且秩 $r$（Ⅰ）$= r$（Ⅱ），证明向量组（Ⅰ）与（Ⅱ）等价。

设 $A$ 是 $m \times r$ 矩阵，$B$ 是 $n \times s$ 矩阵，证明秩
$r(AB) \leq \min(r(A),r(B))$。

### **【例3.25】** 证明：（1）$r(A+B) \leq r(A) + r(B)$；
（2）$\begin{bmatrix} A & B \\ O & B \end{bmatrix} = r(A) + r(B)$。
