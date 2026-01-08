# 数学公式支持示例 / Math Formula Support Example

本博客使用 MathJax 3 支持 LaTeX 数学公式渲染。/ This blog uses MathJax 3 for LaTeX formula rendering.

## 行内公式 / Inline Formulas

行内公式使用 `$...$` 或 `\(...\)`：/ Inline formulas use `$...$` or `\(...\)`:

- 二次方程 / Quadratic equation: $ax^2 + bx + c = 0$
- 圆的面积 / Circle area: $A = \pi r^2$
- 欧拉恒等式 / Euler's identity: $e^{i\pi} + 1 = 0$
- 正弦函数 / Sine function: $\sin(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$

## 块级公式 / Block Formulas

块级公式使用 `$$...$$` 或 `\[...\]`：/ Block formulas use `$$...$$` or `\[...\]`:

### 麦克斯韦方程组 / Maxwell's Equations

$$
\begin{aligned}
\nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \mathbf{B} &= 0 \\
\nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
\nabla \times \mathbf{B} &= \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}
\end{aligned}
$$

### 傅里叶变换 / Fourier Transform

$$
\mathcal{F}[f(t)] = F(\omega) = \int_{-\infty}^{\infty} f(t) e^{-i\omega t} dt
$$

### 矩阵表示 / Matrix Representation

$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}
=
\begin{bmatrix}
b_1 \\
b_2 \\
b_3
\end{bmatrix}
$$

### 极限与积分 / Limits and Integrals

$$
\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e
$$

$$
\int_0^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$

### 分式与根号 / Fractions and Roots

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

## 常用数学符号 / Common Math Symbols

| 类型 / Type | 符号 / Symbol | 代码 / Code |
|-------------|---------------|-------------|
| 希腊字母 / Greek letters | $\alpha, \beta, \gamma, \pi$ | `\alpha`, `\beta`, `\gamma`, `\pi` |
| 运算符 / Operators | $\sum, \prod, \int, \partial$ | `\sum`, `\prod`, `\int`, `\partial` |
| 关系符 / Relations | $\leq, \geq, \neq, \approx$ | `\leq`, `\geq`, `\neq`, `\approx` |
| 箭头 / Arrows | $\to, \Rightarrow, \iff$ | `\to`, `\Rightarrow`, `\iff` |

## 结语 / Conclusion

MathJax 支持丰富的数学符号和公式，更多用法请参考 [MathJax 文档](https://docs.mathjax.org/)。

MathJax supports rich math symbols and formulas. For more details, refer to the [MathJax Documentation](https://docs.mathjax.org/).
