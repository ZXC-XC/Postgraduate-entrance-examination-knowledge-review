- [第三章 $n$ 维向量——难点](#第三章-n-维向量难点)
  - [一、知识结构网络图](#一知识结构网络图)
  - [二、基本内容与重要结论](#二基本内容与重要结论)
    - [基础知识](#基础知识)
    - [重要定理](#重要定理)
  - [向量空间](#向量空间)


# 第三章 $n$ 维向量——难点

## 一、知识结构网络图


**n维向量**

- 运算  
  加法、数乘、内积  - Schmidt正交化

- 线性表示  
  - 概念  
    如果 $\beta = k_1a_1 + k_2a_2 + \cdots + k_na_n$，称 $\beta$ 可由 $a_1, a_2,\cdots, a_n$ 线性表示  
  
  - 判定
     $\Leftrightarrow$ 方程组  $x_1a_1 + x_2a_2 + \cdots + x_na_n = 0$ 有解    
      $\Leftrightarrow$ $r(\alpha_1,\cdots,\alpha_s,\beta)=r(\alpha_1,\cdots,\alpha_s)$
      $\Leftarrow$ $\alpha_1,\cdots,\alpha_s$无关，$\alpha_1,\cdots,\alpha_s,\beta$相关 
  - 等价
    若 $\alpha_{1}, \cdots, \alpha_{s}$ 与 $\beta_{1}, \cdots, \beta_{s}$ 可互相线性表出。

- 线性相关  
  - 概念  
     存在不全为0的 $k_1, k_2, \cdots, k_n$，使 $k_1a_1 + k_2a_2 + \cdots + k_na_n = 0$
  - 判定  
      $\Leftrightarrow$ $[a_1, \cdots, a_s]x=0$ 只有零解
      $\Leftrightarrow$ $r(a_1, \cdots, a_s)=s$
      $\Leftrightarrow$ $\forall i, a_i$ 不能由其余的向量表示
      $\Leftarrow$ 阶梯形向量组

- 极大线性无关组  
  - 概念  
  - 求法  

- 向量组的秩  
  - 矩阵的秩  

- 向量空间  
  - 概念  
    解空间  
  - 基  
    - 坐标  
    - 过渡矩阵  
    - 单位正交基  

## 二、基本内容与重要结论

### 基础知识

$n$ 个数 $a_{1},a_{2},\cdots,a_{n}$ 所组成的有序数组
$$(a_1, a_2, \cdots, a_n)^T  \text{ 或 } a = (a_1, a_2, \cdots, a_n)$$

称为 **$n$ 维向量**。其中 $a_{1},a_{2},\cdots,a_{n}$ 称为向量 $\alpha$的**分量**或（**坐标**），前一个表示式称为列向量，后者称为行向量。

设 $n$ 维向量 $\alpha = (a_1,a_2,\cdots,a_n)^T$，$\beta = (b_1,b_2,\cdots,b_n)^T$，

**向量加法**
$\alpha + \beta = (a_1+b_1,a_2+b_2,\cdots,a_n+b_n)^T$

**数乘向量**
$k\alpha = (ka_1,ka_2,\cdots,ka_n)^T$

**向量内积**
$$(\alpha, \beta) = \alpha^T \beta = \beta^T \alpha = a_1b_1 + a_2b_2 + \cdots + a_n b_n$$

**【评注】**
（1）对于 $\alpha = (a_1,a_2,\cdots,a_n)^T$ 的长度
$\|\alpha\| = \sqrt{(\alpha^T,\alpha)} = \sqrt{a_1^2+a_2^2+\cdots+a_n^2}$

---

（2）若 $\alpha = 0$ 即 $a_1^2+a_2^2+\cdots+a_n^2 = 0 \Leftrightarrow \alpha = 0$。

（3）若 $(\alpha,\beta)=0$，则称 $\alpha$ 与 $\beta$ 正交，此时若 $\alpha \neq 0$，$\beta \neq 0$，则称 $\alpha$ 与 $\beta$ 垂直，记为 $\alpha \perp \beta$。

**定义3.1** 设 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 是 $n$ 个向量，$k_1,k_2,\cdots,k_n$ 是一组实数，称 $$k_1\alpha_1+k_2\alpha_2+\cdots+k_n\alpha_n$$是 $\alpha_1,\alpha_2,\cdots,\alpha_n$ 的**线性组合**。

**定义 3.2** 对 $n$ 维向量 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 和 $\beta$, 若存在实数 $k_{1}, k_{2}, \cdots, k_{s}$ 使得 $$k_{1} \alpha_{1} + k_{2} \alpha_{2} + \cdots + k_{s} \alpha_{s} = \beta$$, 则称 $\beta$ 是 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 的线性组合, 或说 $\beta$ 可由 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ **线性表出 (示)**。

**定义3.3** 对 $n$ 个向量 $\alpha_1,\alpha_2,\cdots,\alpha_n$，如果存在不全为零的数 $k_1,k_2,\cdots,k_n$ 使得
$k_1\alpha_1+k_2\alpha_2+\cdots+k_n\alpha_n=0$

则称向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ **线性相关**，否则，称向量组 $\alpha_1,\alpha_2,\cdots,\alpha_n$ **线性无关**。


（也就是说，当且仅当 $k_1 = k_2 = \cdots = k_n = 0$ 时，$k_1\alpha_1 + k_2\alpha_2 + \cdots + k_n\alpha_n = 0$ 才能成立，或者说，只要 $k_1,k_2,\cdots,k_n$ 不全为零，则 $k_1\alpha_1 + k_2\alpha_2 + \cdots + k_n\alpha_n \neq 0$）。


**定义 3.4** 设有两个 $n$ 维向量组 (I) $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$; (II) $\beta_{1}, \beta_{2}, \cdots, \beta_{t}$; 如果 (I) 中每个向量 $\alpha_{i}(i=1,2, \cdots, s)$ 都可由 (II) 中的向量 $\beta_{1}, \beta_{2}, \cdots, \beta_{t}$ 线性表出, 则称向量组 (I) 可由向量组 (II) **线性表出**。

如果 (I) (II) 这两个向量组可以互相线性表出, 则称这两个**向量组等价**。

**定义 3.5** 在向量组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 中, 若存在 $r$ 个向量 $\alpha_{i_{1}}, \alpha_{i_{2}}, \cdots, \alpha_{i_{r}}$ 线性无关, 再加进任一个向量 $\alpha_{j}(j=1,2, \cdots, s)$, 向量组 $\alpha_{i_{1}}, \alpha_{i_{2}}, \cdots, \alpha_{i_{r}}, \alpha_{j}$ 就线性相关, 则称 $\alpha_{i_{1}}, \alpha_{i_{2}}, \cdots, \alpha_{i_{r}}$ 是向量组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 的一个**极大线性无关组**。

**定义 3.6** 向量组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 的极大线性无关组中所含向量的个数 $r$ 称为这个向量组的**秩**。


### 重要定理

**定理3.1** 向量 $\beta$ 可由向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性表示
$\Leftrightarrow$ 非齐次线性方程组 $[\alpha_1,\alpha_2,\cdots,\alpha_s]$ $\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{bmatrix} = \beta$ 有解

$\Leftrightarrow$ 秩 $r(\alpha_1,\alpha_2,\cdots,\alpha_s) = r(\alpha_1,\alpha_2,\cdots,\alpha_s,\beta)$。

**定理3.2** 向量组 $\alpha_1,\alpha_2,\cdots,\alpha_s$ 线性相关
$\Leftrightarrow$ 齐次线性方程组 $[\alpha_1,\alpha_2,\cdots,\alpha_s]$ $\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_s \end{bmatrix} = 0$ 有非零解

$\Leftrightarrow$ 向量组的秩 $r(\alpha_1,\alpha_2,\cdots,\alpha_s) < s$。

**推论 1** $n$ 个 $n$ 维向量 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 线性相关的充分必要条件是行列式 $\left|\begin{array}{llll}\alpha_{1} & \alpha_{2} & \cdots & \alpha_{n}\end{array}\right|=0$.

**推论 2** $n+1$ 个 $n$ 维向量一定线性相关.

**定理 3.3** 任何部分组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{r}$ 相关 $\Rightarrow$ 整体组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{r}, \cdots, \alpha_{s}$ 相关, 整体组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{r}, \cdots, \alpha_{s}$ 无关 $\Rightarrow$ 任何部分组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{r}$ 无关, 反之都不成立.

**定理3.4** $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 线性无关 $\Rightarrow$ 延伸组 $\widetilde{\alpha}_{1}, \widetilde{\alpha}_{2}, \cdots, \widetilde{\alpha}_{m}$ 线性无关;

$\widetilde{\alpha}_{1}, \widetilde{\alpha}_{2}, \cdots, \widetilde{\alpha}_{m}$ 线性相关 $\Rightarrow$ 缩短组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 线性相关, 反之均不成立。

**定理 3.5** 如果 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}(s \geqslant 2)$ 线性相关, 则其中必有一个向量可用其余的向量线性表出; 反之, 若有一个向量可用其余的 $s-1$ 个向量线性表出, 则这 $s$ 个向量必线性相关。

**定理 3.6** 如果 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 线性无关, $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}, \beta$ 线性相关, 则 $\beta$ 可由 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 线性表出, 且表示法唯一。


**定理3.7** 如果向量组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 可由向量组 $\beta_{1}, \beta_{2}, \cdots, \beta_{t}$ 线性表出, 而且 $s > t$, 那么 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 线性相关。即如果多数向量能用少数向量线性表出, 那么多数向量一定线性相关。

**推论** 如果 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 线性无关, 且它可由 $\beta_{1}, \beta_{2}, \cdots, \beta_{t}$ 线性表出, 则 $s \leqslant t$.


**定理3.8** 设 $\alpha_1,\alpha_2,\cdots,\alpha_r$ 可由 $\beta_1,\beta_2,\cdots,\beta_s$ 线性表出，则 $r(\alpha_1,\alpha_2,\cdots,\alpha_r) \leq r(\beta_1,\beta_2,\cdots,\beta_s)$。

**推论** 若向量组（Ⅰ）及（Ⅱ）是两个等价的向量组，则 $r$（Ⅰ）$= r$（Ⅱ）。

**定理3.9** 
 如果 $r(A) = r$, 则 $A$ 中有 $r$ 个线性无关的列向量, 而其他列向量是这 $r$ 个线性无关列向量的线性组合, 也就是 $r(A) = A$ 的列秩。

一般地, $r(A) = A$ 的行秩 $= A$ 的列秩。

**【评注】** **线性无关的判定**

若向量的坐标没有给出, 通常用定义法或用秩的理论来分析判断论证, 也要有反证法的构思。

(1) 用定义法证 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 线性无关的框图是:

设 $k_{1} \alpha_{1} + k_{2} \alpha_{2} + \cdots + k_{s} \alpha_{s} = 0$

$\downarrow$ 恒等变形 $\stackrel{\text {}}{}$ （乘或重组）

$k_{1} = 0, k_{2} = 0, \cdots, k_{s} = 0$.

(2) 用秩 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}$ 线性无关

$\Leftrightarrow\left[\begin{array}{llll}\alpha_{1} & \alpha_{2} & \cdots & \alpha_{s}\end{array}\right]\left[\begin{array}{c}x_{1} \\x_{2} \\\vdots \\x_{s}\end{array}\right]=0$ 只有零解

$\Leftrightarrow$ 秩 $\left(\alpha_{1}, \alpha_{2}, \cdots, \alpha_{s}\right) = s$.

要注意公式: $r(A) = A$ 的列秩 $= A$ 的行秩, $r(AB) \leqslant \min(r(A), r(B))$. 
若 $A$ 可逆, 则 $r(AB) = r(B), r(BA) = r(B)$.

若 $A$ 是 $m \times n$ 矩阵, 且$r(A) = n$,则$r(AB) = r(B)$

若 $A$ 是 $m \times n$ 矩阵, $B$ 是 $n \times s$ 矩阵且 $AB = O$, 则 $r(A) + r(B) \leqslant n$.

(3) 反证法。

**补充**

设 $A$ 是 $m \times n$ 矩阵, $B$ 是 $n \times s$ 矩阵, 证明秩 $r(AB) \leqslant \min(r(A), r(B))$.

 $r(A + B) \leqslant r(A, B) \leqslant r(A) + r(B)$;

$r\left[\begin{array}{cc}A & B \\O & B\end{array}\right]=r(A)+r(B)$.

## 向量空间

**定义 3.7** 全体 $n$ 维向量连同向量的加法和数乘运算合称为 $n$ **维向量空间**。

**定义 3.8** 设 $W$ 是 $n$ 维向量的非空集合, 如果满足

(1) $\forall \alpha, \beta \in W$, 必有 $\alpha + \beta \in W$;

(2) $\forall \alpha \in W$ 及任一实数 $k$, 必有 $k \alpha \in W$,

则称 $W$ 是 $n$ 维向量空间的子空间。

**定义 3.9** 如果向量空间 $V$ 中的 $m$ 个向量 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 满足

(1) $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 线性无关;

(2) $V$ 中任意向量 $\beta$ 均可由向量组 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 线性表出, 即

$x_{1} \alpha_{1} + x_{2} \alpha_{2} + \cdots + x_{m} \alpha_{m} = \beta$,

则称 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 为向量空间 $V$ 的一个**基底 (或基)**。基中所含向量的个数 $m$ 称为向量空间 $V$ 的**维数**, 记作 $\operatorname{dim} V = m$, 并称 $V$ 是 $m$ 维向量空间。向量 $\beta$ 的表示系数 $x_{1}, x_{2}, \cdots, x_{m}$ 称为向量 $\beta$ 在基底 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{m}$ 下的**坐标**。

**定义 3.10** 设 $e_{1}, e_{2}, \cdots, e_{n}$ 是向量空间的一组基, 如果它们满足

$(e_{i}, e_{j})=\left\{\begin{array}{ll}1, & i=j, \\0, & i \neq j\end{array}\right.$

则称 $e_{1}, e_{2}, \cdots, e_{n}$ 为**规范正交基**。

设齐次方程组 $A x = 0$ 的解向量的集合为 $W$, 由解的性质知:

若 $\alpha, \beta$ 是 $A x = 0$ 的解, 则 $\alpha + \beta, k \alpha$ 仍是 $A x = 0$ 的解, 所以 $W$ 是 $n$ 维向量空间的子空间, 通常称为**解空间**。


**定义3.11** 在 $n$ 维向量空间定两组基
（Ⅰ）$\alpha_1,\alpha_2,\cdots,\alpha_n$；
（Ⅱ）$\beta_1,\beta_2,\cdots,\beta_n$。

$$
\beta_1 = c_{11} \alpha_1 + c_{21} \alpha_2 + \cdots + c_{n1} \alpha_n，
$$

$$
\beta_2 = c_{12} \alpha_1 + c_{22} \alpha_2 + \cdots + c_{n2} \alpha_n，
$$

$$
\cdots \cdots \cdots \cdots
$$

$$
\beta_n = c_{1n} \alpha_1 + c_{2n} \alpha_2 + \cdots + c_{nn} \alpha_n，
$$

即  
$$
【\beta_1，\beta_2，\cdots，\beta_n】 = 【\alpha_1，\alpha_2，\cdots，\alpha_n】C，
$$

其中  

$C=\left[\begin{array}{cccc}c_{11} & c_{12} & \cdots & c_{1 n} \\c_{21} & c_{22} & \cdots & c_{2 n} \\\vdots & \vdots & & \vdots \\c_{n 1} & c_{n 2} & \cdots & c_{n n}\end{array}\right]$,

则称矩阵 $C$ 为由基 $\alpha_1，\alpha_2，\cdots，\alpha_n$ 到基 $\beta_1，\beta_2，\cdots，\beta_n$ 的**过渡矩阵**。

**定理 3.10** 如果 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 与 $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$ 是 $n$ 维向量空间的两个基底, 则由基 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 到基 $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$ 的过渡矩阵 $C$ 是可逆矩阵。

**定理 3.11** 如果向量 $\gamma$ 在基底 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 的坐标为 $x_{1}, x_{2}, \cdots, x_{n}$, 向量 $\gamma$ 在基底 $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$ 的坐标为 $y_{1}, y_{2}, \cdots, y_{n}$, 则坐标变换公式为

$\left[\begin{array}{c}x_{1} \\x_{2} \\\vdots \\x_{n}\end{array}\right]=C\left[\begin{array}{c}y_{1} \\y_{2} \\\vdots \\y_{n}\end{array}\right] \quad$ 或 $\quad x=C y$,

其中 $n$ 阶矩阵 $C$ 是由基底 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 到基底 $\beta_{1}, \beta_{2}, \cdots, \beta_{n}$ 的过渡矩阵。

**定理 3.12** 若 $n$ 维向量 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 非零且两两正交, 则 $\alpha_{1}, \alpha_{2}, \cdots, \alpha_{n}$ 线性无关。

**定理 3.13** 若 $e_{1}, e_{2}, \cdots, e_{n}$ 是规范正交基, 设

$\left[\varepsilon_{1}, \varepsilon_{2}, \cdots, \varepsilon_{n}\right]=\left[e_{1}, e_{2}, \cdots, e_{n}\right] C$,

则 $\varepsilon_{1}, \varepsilon_{2}, \cdots, \varepsilon_{n}$ 是规范正交基的充分必要条件是 $C$ 为正交矩阵。
