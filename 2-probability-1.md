---
output:
  html_document: default
  pdf_document: default
---

# 概率-Part1 {#chapter:probability-1}



## 事件的概率 {#sec:prob}

### 古典概率模型

古典概率模型需要满足的条件：

   - 样本空间中有有限个样本点。
   - 所有的样本点出现的可能性相同-等可能性。
   
### 排列组合

1. 加法原理：几类方案。乘法原理：一个方案分几步。

### 排列 {#sec:P}

1. 不重复排列，从n个不同元素中取出m个不同的排列的个数：

$$
\begin{align}
   P_n^m=n(n-1)(n-2)...(n-m+1)=\frac{n!}{(n-m)!}
   (\#eq:permutation)
\end{align}
$$ 

:::: {.rmdnote data-latex="{注意}"}
全排列。$0! =1$。
::::

2. 重复排列，从n个不同元素中取出m个排列（可以相同）的个数，为$n^m$。

3. 组合，从n个不同元素中取出m个个不同的元素（不用排队）。

$$
\begin{align}
   C_n^m&=\frac{P_n^m}{m!}=\frac{n!}{m!(n-m)!} \\
   C_n^m&=C_n^{n-m} \\
   C_n^0&=C_n^n=1
   (\#eq:combination)
\end{align}
$$ 

## 频率与概率 {#sec:freq-prob}

1. n次试验，事件A发生了m次，则A发生的频率为$\frac{m}{n}$，使用$\omega_n(m)$表示。

   - 性质1：非负性，$0\leq\omega_n(m)\leq1$
   - 性质2：规范性，$\omega_n(\Omega)=1$，$\omega_n(\Phi)=0$
   - 性质3：可加性，两两互不相容事件集的频率等于每个事件频率之和。
   
2. 频率的稳定值无限接近于统计概率。

## 公理化 {#sec:axiomatic}

:::: {.rmdnote data-latex="{注意}"}
- 公理1：非负性

- 公理2：规范性

- 公理3：完全可加性，事件$A_1,A_2,...$不相容，则$P(A_1+A_2+...)=P(A_1)+P(A_2)+...$。*事件相加的概率等于事件概率的相加。*
::::

:::: {.rmdtip data-latex="{提示}"}
- 性质1：$P(\Phi)=0$。

- 性质2：有限可加性，事件$A_1,A_2,...,A_n$不相容，则$P(A_1+A_2+...+A_n)=P(A_1)+P(A_2)+...P(A_n)$

- 性质3：$P(\bar{A})=1-P(A)$

- 性质4：

   - 1) $P(A-B)=P(A)-P(AB)$ 
   - 2) 如果$A\supset B$，则$P(A-B)=P(A)-P(B)，且P(A)\geq P(B)$。

- **性质5（重要）**：加法公式，$P(A+B)=P(A)+P(B)-P(AB)$
::::

## 条件概率 {#sec:conditional-prob}

1. 定义：$\Omega$为样本空间，A、B为两个事件，$P(B)>0$，在B已经发生的条件下A发生的概率即为A对B的条件概率，记做$P(A|B)$。计算公式为有如下几种：

- 公式1：
   
$$
\begin{align}
  P(A|B)=\frac{n_{AB}}{n_B}
  (\#eq:con-prob-1)
\end{align}
$$

- 公式2：
   
$$
\begin{align}
  P(A|B)=\frac{P(AB)}{P(B)}
  (\#eq:con-prob-2)
\end{align}
$$

:::: {.rmdnote data-latex="{注意}"}
条件概率的样本空间发生了变化，从$\Omega$变成了B
::::


### 乘法公式

1. 两个事件的乘法公式。

$$
\begin{align}
  P(AB)&=P(B)P(A|B) \\
  P(AB)&=P(A)P(B|A)
  (\#eq:n-multiplication-1)
\end{align}
$$

2. 多个事件的乘法公式（三个事件）：

$$
\begin{align}
  P(ABC)&=P(A)P(B|A)P(C|AB)
  (\#eq:n-multiplication-2)
\end{align}
$$

::: {.rmdtip data-latex="{提示}"}
公式\@ref(eq:n-multiplication-2)可以通过按步骤进行的方式直观理解：

步骤1：事件A发生，概率为P(A)。

步骤2：事件A发生的前提下，事件B发生，概率为P(B|A)。

步骤3：事件A、B同时发生的前提下，事件C发生，概率为P(C|AB)。

步骤4：将以上三步的结果相乘，得到事件A、B、C同时发生的概率。
:::
