# 组合数学 1.1 (2017.9.5)


## 加法原理
## 乘法原理
## 排列与组合


@定义 一些符号  

$$P_{n,m}=n(n-1)\cdots(n-m+1)$$  
$${n \choose k}=\frac{n!}{m!(n-m)!}$$
$${n \choose m}=0 (m>n)$$  
@


@定理
原有概念的推广

$${-1 \choose n}=\frac{(-1)(-2)\cdots(-n)}{n!}=(-1)^{n}$$ 
$${\frac{1}{2} \choose n}=\frac{\frac{1}{2} (\frac{1}{2}-1) \cdots (\frac{1}{2}-n+1)}{n!}=\frac{(-1)^{n-1} (2n-2)!} {2^{2n-1} n!(n-1)!}=\frac{(-1)^{n-1} {2n-1 \choose n-1}}{2^{2n-1} n}$$  
$$(x+y)^{n}=\sum_{i=0}^{n}{n \choose i}x^{n-i}y^{i}$$  
$$(1+x)^{n}=\sum_{i=0}^{n}{n \choose i}x^{i}=\sum_{i\ge0}^{}{n \choose i}x^{i}$$  
$$(1+x)^{-1}=1-x+x^{2}-x^{3}+\cdots=\sum_{i\ge0}^{}(-1)^{i}x^{i}=\sum_{i\ge0}^{}{-1 \choose i}x^{i}$$ 
@

@例
推广

$$(1+x)^a=\sum_{i\ge 0}{a\choose i}x^i\quad(|x|<1)$$(a任意)

@

### 应用1

$${n\choose 0}+{n\choose 1}+...+{n\choose n}=(1+1)^n=2^{n}$$

$${n\choose 0}-{n\choose 1}+...+{n\choose n}=(1-1)^n=0$$

$${n\choose 0}+{n\choose 2}+...+{n\choose 2*\lfloor n\rfloor}=2^{n-1}$$

$${n\choose 1}+{n\choose 3}+...+{n\choose 2*\lfloor n\rfloor}=2^{n-1}$$

### 应用2

$$\sum_(i\ge 0){n\choose 3i}$$

考虑1的三次单位根 1  $\quad\omega1 \quad \omega2$

其中

$$\omega1=e^{\pi*2i/3} \quad \omega2=e^{\pi*4i/3}$$

$$\omega1^3=1$$

于是可以展开$(1+\omega)^n,(1+\omega^2)^n,(1+1)^n$

由($1+\omega+\omega^2=0$)得

$$\sum_{i\ge0}{n\choose3i}=\frac{(1+\omega)^n+(1+\omega^2)^n+(1+1)^n}{3}$$

>练习: 化简上式

## Vandermonde恒等式

### 求和 $\sum_{i\ge0}^{}i{n \choose i}={n \choose 1}+2{n \choose 2} +\cdots+n{n \choose n}= ?$
对$(1+x)^{n}=\sum_{i\ge0}{n \choose i}x^{i}$求导得到

$$n(1+x)^{n-1}=\sum_{i\ge0}^{}i{n \choose i}x^{i-1}={n \choose 1}+2{n \choose 2}x+\cdots+n{n \choose n}x^{n-1}$$  
令$x=1$得到

$$\sum_{i\ge0}^{}i{n \choose i}={n \choose 1}+2{n \choose 2}+\cdots+n{n \choose n}=n\cdot2^{n-1}$$  

### $(1+x)^{n}(1+x)^{m}=(1+x)^{m+n}$
$(\sum_{i\ge0}^{}{n \choose i}x^{i})(\sum_{j\ge0}^{}{m \choose j}x^{j})=(\sum_{k\ge0}^{}{n+m \choose k}x^{k})$ 
$\underbrace{\Rightarrow\sum_{i=0}^{k}{n \choose i}{m \choose k-i}={n+m \choose k}}_{Vandermonde \quad formula}$  
令$m=n=k$可得

$${n \choose 0}^{2}+{n \choose 1}^{2}+\cdots+{n \choose n}^{2}={2n \choose n}^{2}=2^{2n}-2\sum_{i=0}^{n-1}{2n \choose i}$$



写成公式形式：

$${k\choose k}+{k+1 \choose k}+{k+2\choose k}+...+{n\choose k}={n+1\choose k+1}$$

## 组合数的多项式性质

考察

$$1^2+2^2+3^2+...+n^2=\frac{n*(n(+1)*(2n-1)}{6}$$

其可用组合数的性质证明如下：

$$ \sum{k\choose 2}=\sum\frac{k(k+1)}{2}=\sum(k^2/2-k/2)$$(1)
$$\sum_{k=1}^{n}k^2=2\sum_{k=1}^{n}{k\choose 2}+\sum_{k=1}^n k$$(2)

>练习: $1^3+2^3+3^3+...+n^3=?$

Tips: 

$$x^2=x(x-1)+x=2{x\choose 2}+{x\choose 1}$$(1)

$$x^3=6{x\choose 3}+2{x\choose 2}+{x\choose 1}$$(2)

$$x^k==?{x\choose n}+...+?{x\choose 1}$$(3)

可以发现

$${x\choose n},...,{x\choose 1}$$(4)

是一组线性无关的基.

思考：见作业1