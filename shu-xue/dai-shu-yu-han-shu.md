# 代数与函数

### 基础函数&#x20;

$$
指数函数 \\
\begin{aligned}
y &= a^x, \quad a>0, a \neq 1 \\
a^m \cdot a^n &= a^{m+n} \\
\dfrac{a^m}{a^n} &= a^{m-n} \\
(a^m)^n &= a^{mn} \\
a^{-n} &= \dfrac{1}{a^n}
\end{aligned}
\\
对数函数\\
\begin{aligned}
y &= \log_a x, \quad a>0, a \neq 1, x>0 \\
\log_a(MN) &= \log_a M + \log_a N \\
\log_a\left(\dfrac{M}{N}\right) &= \log_a M - \log_a N \\
\log_a(M^k) &= k \cdot \log_a M \\
\log_a b &= \dfrac{\log_c b}{\log_c a}
\end{aligned}
$$

$$
三角函数公式\\
基本关系\\
\sin^2 x + \cos^2 x = 1 \\
1 + \tan^2 x = \sec^2 x \\
1 + \cot^2 x = \csc^2 x \\
\tan x = \frac{\sin x}{\cos x}, \quad \cot x = \frac{\cos x}{\sin x} \\
\sec x = \frac{1}{\cos x}, \quad \csc x = \frac{1}{\sin x} \\

诱导公式\\
\sin(-x) = -\sin x, \quad \cos(-x) = \cos x \\
\tan(-x) = -\tan x, \quad \cot(-x) = -\cot x \\
\sin(\pi - x) = \sin x, \quad \cos(\pi - x) = -\cos x \\
\tan(\pi - x) = -\tan x, \quad \cot(\pi - x) = -\cot x \\
\sin(\pi + x) = -\sin x, \quad \cos(\pi + x) = -\cos x \\
\tan(\pi + x) = \tan x, \quad \cot(\pi + x) = \cot x \\
\sin\Big(\frac{\pi}{2} - x\Big) = \cos x, \quad \cos\Big(\frac{\pi}{2} - x\Big) = \sin x \\
\tan\Big(\frac{\pi}{2} - x\Big) = \cot x, \quad \cot\Big(\frac{\pi}{2} - x\Big) = \tan x \\

和差公式\\
\sin(a \pm b) = \sin a \cos b \pm \cos a \sin b \\
\cos(a \pm b) = \cos a \cos b \mp \sin a \sin b \\
\tan(a \pm b) = \frac{\tan a \pm \tan b}{1 \mp \tan a \tan b} \\

倍角公式\\
\sin 2x = 2 \sin x \cos x \\
\cos 2x = \cos^2 x - \sin^2 x = 2\cos^2 x - 1 = 1 - 2\sin^2 x \\
\tan 2x = \frac{2\tan x}{1 - \tan^2 x} \\

半角公式\\
\sin^2 \frac{x}{2} = \frac{1 - \cos x}{2} \\
\cos^2 \frac{x}{2} = \frac{1 + \cos x}{2} \\
\tan \frac{x}{2} = \frac{1 - \cos x}{\sin x} = \frac{\sin x}{1 + \cos x} \\

积化和差公式\\
\sin a \sin b = \frac{1}{2}[\cos(a - b) - \cos(a + b)] \\
\cos a \cos b = \frac{1}{2}[\cos(a - b) + \cos(a + b)] \\
\sin a \cos b = \frac{1}{2}[\sin(a + b) + \sin(a - b)] \\

和差化积公式\\
\sin a + \sin b = 2 \sin \frac{a + b}{2} \cos \frac{a - b}{2} \\
\sin a - \sin b = 2 \cos \frac{a + b}{2} \sin \frac{a - b}{2} \\
\cos a + \cos b = 2 \cos \frac{a + b}{2} \cos \frac{a - b}{2} \\
\cos a - \cos b = -2 \sin \frac{a + b}{2} \sin \frac{a - b}{2} \\

反三角函数\\
\sin(\arcsin x) = x, \quad \cos(\arccos x) = x, \quad \tan(\arctan x) = x \\
\arcsin(-x) = -\arcsin x, \quad \arccos(-x) = \pi - \arccos x, \quad \arctan(-x) = -\arctan x \\
$$

### 方程、不等式

$$
一元一次方程\\
ax + b = 0 \Rightarrow x = -\frac{b}{a} \\

一元二次方程\\
ax^2 + bx + c = 0 \Rightarrow x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \\
判别式: \Delta = b^2 - 4ac \\
\Delta > 0: \text{两不等实根}, \quad \Delta = 0: \text{重根}, \quad \Delta < 0: \text{无实根} \\

分式方程\\
\frac{f(x)}{g(x)} = 0 \Rightarrow f(x) = 0, \quad g(x) \neq 0 \\

含绝对值方程\\
|f(x)| = a \Rightarrow f(x) = a \text{ 或 } f(x) = -a, \quad a \ge 0 \\
|f(x)| = |g(x)| \Rightarrow f(x) = g(x) \text{ 或 } f(x) = -g(x) \\

一元一次不等式\\
ax + b > 0 \Rightarrow x > -\frac{b}{a}, \quad (a > 0) \\
ax + b < 0 \Rightarrow x < -\frac{b}{a}, \quad (a > 0) \\
\text{注意乘以负数时，不等号反向} \\

一元二次不等式\\
ax^2 + bx + c > 0 \Rightarrow \text{用判别式分析符号变化} \\
ax^2 + bx + c \ge 0 \Rightarrow \text{求根后确定区间} \\

绝对值不等式\\
|f(x)| < a \Rightarrow -a < f(x) < a \\
|f(x)| > a \Rightarrow f(x) > a \text{ 或 } f(x) < -a \\

分式不等式\\
\frac{f(x)}{g(x)} > 0 \Rightarrow f(x) \cdot g(x) > 0, \quad g(x) \neq 0 \\
\frac{f(x)}{g(x)} < 0 \Rightarrow f(x) \cdot g(x) < 0, \quad g(x) \neq 0 \\

基本解题步骤\\
1. 化简方程或不等式 \\
2. 分析定义域，排除无效解 \\
3. 对二次、多项式、不等式使用因式分解或判别式 \\
4. 对绝对值问题，拆分讨论情况 \\
5. 最终合并解集，注意符号及区间表示
$$

### 数列与级数

$$
数列：是按一定规律排列的一列数，记作a_1, a_2, ... a_n \\
通项公式a_n：表示数列第 n 项的表达式，可以直接求任意项，不需要从头数到第 n 项。 \\

等差数列\\
相邻两项的差是固定值 d 的数列 \\
通项公式：a_n = a_1 + (n-1)d d为与前一项差值的规律值 \\
前 n 项和：S_n = \frac{n}{2}(a_1 + a_n) = \frac{n}{2}[2a_1 + (n-1)d] \\

等比数列\\
相邻两项的比值固定的数列，记作公比r(当前项与前一项的比值) \\ 
通项公式：a_n = a_1 \cdot r^{n-1} \\
前 n 项和：S_n = a_1 \frac{1 - r^n}{1 - r}, \quad (r \neq 1) \\
无限等比数列和：S_{\infty} = \frac{a_1}{1 - r}, \quad (|r|<1) \\

特殊数列\\
平方数列：1, 4, 9, ... \quad 前 n 项和：S_n = \frac{n(n+1)(2n+1)}{6} \\
立方数列：1, 8, 27, ... \quad 前 n 项和：S_n = \left(\frac{n(n+1)}{2}\right)^2 \\

级数\\
算术级数和：S_n = \sum_{k=1}^{n} a_k \\
几何级数和：S_n = \sum_{k=0}^{n-1} a_1 r^k = a_1 \frac{1-r^n}{1-r} r为公比\\

无穷级数\\
几何无穷级数：\sum_{k=0}^{\infty} a_1 r^k = \frac{a_1}{1-r}, \quad (|r|<1) \\
调和级数：\sum_{k=1}^{\infty} \frac{1}{k}, \quad 发散 \\
p 级数：\sum_{k=1}^{\infty} \frac{1}{k^p}, \quad 收敛条件：p>1 \\

常用公式与性质\\
\sum_{k=1}^{n} k = \frac{n(n+1)}{2} \\
\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6} \\
\sum_{k=1}^{n} k^3 = \left(\frac{n(n+1)}{2}\right)^2 \\
\sum_{k=0}^{n} r^k = \frac{1 - r^{n+1}}{1 - r}, \quad r \neq 1 \\
\sum_{k=0}^{\infty} r^k = \frac{1}{1-r}, \quad |r|<1 \\

数列极限\\
\lim_{n \to \infty} a_n = A \Rightarrow 数列收敛 \\
\lim_{n \to \infty} a_n \text{不存在} \Rightarrow 数列发散 \\

级数收敛性判断\\
必要条件：\lim_{n \to \infty} a_n = 0 \\
常用判别法：比较判别法、比值判别法、根判别法、交错级数判别法 \\
$$

