---
output:
  html_document: default
  pdf_document: default
---

# 分布函数 {#chapter:distribution-function}



## 随机变量

### 随机变量概念

1. 一般使用大写字母X,Y,Z表示。

   - 离散型随机变量：有限个、无限可列个。
   - 非离散型：连续型。

2. 一个事件的概率记做$P\lbrace X=a\rbrace$。

:::: {.rmdnote data-latex="{注意}"}
在概率中，X（大写）表示变量，x（小写）表示变量的取值。
::::

## 分布函数

$F(x)=P(X\leq x)$，分布函数是一个普通的实函数。

   - X取值不超过x的概率。大写的X为一个随机变量，小写的x为一个实数值（与$F(x)$中的x相同）。
   - $x\in(-\infty,\infty)$。
   - $F(x)\in[0,1]$
   
### 几何分布

事件第k次时是首次发生，前k-1次未发生，则

$$
\begin{align}
   P\lbrace X = k\rbrace=(1-p)^{k-1}
   (\#eq:geom-dist)
\end{align}
$$

### 二项分布 {#sec:binomial-distr}

二项分布是0-1分布的扩展版。

事件A发生的概率为P（$P(A)=p$），做n次实验，则事件A发生了k次的概率公式如下，记做$X \sim B(n,p) $

$$
\begin{align}
   P\lbrace X=k\rbrace=({C_n^k} {p^k}) {(1-p)^{n-k}}, k=0,1,2,...,n
   (\#eq:binomial-distr)
\end{align}
$$
### 泊松分布 {#sec:poisson-dist}

二项分布在具体计算时，过程比较复杂。我们通常采用泊松分布进行近似计算。泊松分布的计算公式如下（记做$X \sim P(\lambda)$）：

$$
\begin{align}
   P \lbrace X=k \rbrace = \frac{\lambda}{k!}e^{-\lambda}(\lambda>0), k=0,1,2,3,...
   (\#eq:poisson-dist)
\end{align}
$$

::: {.rmdtip data-latex="{提示}"}
1. 泊松分布的参数$\lambda$是单位时间(或单位面积)内随机事件的平均发生次数。

2. 泊松分布适合于描述单位时间内随机事件发生的次数。

3. 泊松分布的值通常通过查表得到。表中分别定义了不同$\lambda$和$k$值所对应的泊松分布值。

4. 如果二项分布中n比较大（$n \geq 100$），np比较适中（$np\leq10$）时，可以使用泊松分布近似计算二项分布。
:::

