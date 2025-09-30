# 微积分

#### 极限与连续

$$
1. 极限的定义（数列极限）\\
\lim_{n \to \infty} a_n = A \\
当 n 趋近于无穷大时，数列 a_n 趋近于某个确定的常数 A\\
A 是数列 a_n 的极限\\

2. 极限的定义（函数极限）\\
\lim_{x \to x_0} f(x) = L \\
当 x 趋近于 x_0 时，函数 f(x) 的值无限接近某个常数 L\\
L 是函数 f(x) 在 x_0 点的极限\\

3. 左极限与右极限\\
\lim_{x \to x_0^-} f(x) = L_1, \quad \lim_{x \to x_0^+} f(x) = L_2 \\
左极限表示 x 从 x_0 的左边趋近时的极限，右极限表示 x 从右边趋近时的极限\\
函数在 x_0 点极限存在的条件：左极限 = 右极限\\

4. 无穷大与无穷小\\
\lim_{x \to \infty} f(x) = \infty, \quad \lim_{x \to \infty} g(x) = 0 \\
当 x 趋近无穷大时，f(x) 无限增大；g(x) 无限接近 0\\
\infty 表示无限大，0 表示无限小\\

5. 极限的运算法则\\
\lim_{x \to x_0} [f(x) \pm g(x)] = \lim_{x \to x_0} f(x) \pm \lim_{x \to x_0} g(x)\\
\lim_{x \to x_0} [f(x) \cdot g(x)] = (\lim_{x \to x_0} f(x)) \cdot (\lim_{x \to x_0} g(x))\\
\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{\lim_{x \to x_0} f(x)}{\lim_{x \to x_0} g(x)}, \quad \lim_{x \to x_0} g(x) \neq 0\\
极限可以进行加减乘除运算（前提除法分母极限不为零）\\

6. 连续的定义\\
f(x) 在 x_0 连续 \Leftrightarrow \lim_{x \to x_0} f(x) = f(x_0)\\
函数连续意味着：函数值 = 极限值\\
连续性要求三条件：函数在 x_0 定义、极限存在、函数值等于极限\\

7. 间断点\\
间断点类型：\\
第一类间断点：可去间断、跳跃间断\\
第二类间断点：无穷间断、振荡间断\\
函数在间断点处极限不存在或不等于函数值\\

8. 初等函数的连续性\\
多项式函数、指数函数、对数函数、三角函数在其定义域内连续\\
常用结论：连续函数在定义域内不会“跳跃”\\
$$

#### 一元微分（导数、偏导、梯度）

$$
1. 导数的定义（函数变化率）\\
f'(x_0) = \lim_{h \to 0} \frac{f(x_0+h) - f(x_0)}{h} \\
导数表示函数在 x_0 点的瞬时变化率，也可以理解为曲线在该点的切线斜率\\

2. 导数的几何意义\\
y = f(x) 曲线在 x_0 点的切线斜率 = f'(x_0)\\
正导数：曲线上升，负导数：曲线下降，导数为零：切线水平\\

3. 基本求导公式\\
\frac{d}{dx} [c] = 0, \quad \frac{d}{dx} [x^n] = n x^{n-1} \\
\frac{d}{dx} [e^x] = e^x, \quad \frac{d}{dx} [\ln x] = \frac{1}{x} \\
\frac{d}{dx} [\sin x] = \cos x, \quad \frac{d}{dx} [\cos x] = -\sin x\\
常用初等函数的导数公式，便于快速求解复合函数\\

4. 导数运算法则\\
(f \pm g)' = f' \pm g' \\
(f \cdot g)' = f' g + f g' \\
\left(\frac{f}{g}\right)' = \frac{f'g - f g'}{g^2}, \quad g \neq 0 \\
(u(v(x)))' = u'(v(x)) \cdot v'(x) \\
导数可以进行加减乘除运算，复合函数使用链式法则\\

5. 偏导数（多元函数）\\
f_x(x_0, y_0) = \frac{\partial f}{\partial x}(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0+h, y_0) - f(x_0, y_0)}{h} \\
f_y(x_0, y_0) = \frac{\partial f}{\partial y}(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0, y_0+h) - f(x_0, y_0)}{h} \\
偏导表示多元函数对某一个自变量的瞬时变化率，固定其他变量\\

6. 梯度向量\\
\nabla f(x, y) = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right) \\
梯度向量的方向表示函数增大最快的方向，大小表示增长最快的速率\\

7. 几何理解（梯度）\\
在二维平面上，梯度方向垂直于等高线（函数值相同的曲线）\\
梯度的模 ||\nabla f|| = \sqrt{(f_x)^2 + (f_y)^2} 表示函数变化最快的速率\\

8. 高阶导数\\
二阶导数：f''(x) = \frac{d}{dx} f'(x) \\
偏二阶导数：f_{xx} = \frac{\partial^2 f}{\partial x^2}, \quad f_{xy} = \frac{\partial^2 f}{\partial x \partial y} \\
用于描述函数的凹凸性、极值等性质\\

9. 导数应用\\
切线方程：y - f(x_0) = f'(x_0)(x - x_0) \\
函数单调性：f'(x) > 0 上升，f'(x) < 0 下降 \\
极值与最值：f'(x) = 0 或 f'(x) 不存在为候选点\\
多元函数极值：梯度 = 0 或边界条件\\
$$

#### 积分（定积分、不定积分）

$$
1. 不定积分（反导数）\\
\int f(x) dx = F(x) + C \\
不定积分表示求函数 f(x) 的原函数 F(x)，加上任意常数 C\\
求积分即是求导数的逆运算\\

2. 基本积分公式\\
\int x^n dx = \frac{x^{n+1}}{n+1} + C, \quad n \neq -1 \\
\int \frac{1}{x} dx = \ln |x| + C \\
\int e^x dx = e^x + C \\
\int a^x dx = \frac{a^x}{\ln a} + C, \quad a>0, a\neq 1 \\
\int \sin x dx = -\cos x + C, \quad \int \cos x dx = \sin x + C \\
\int \sec^2 x dx = \tan x + C, \quad \int \csc^2 x dx = -\cot x + C \\
\int \sec x \tan x dx = \sec x + C, \quad \int \csc x \cot x dx = -\csc x + C \\
常用初等函数的不定积分公式，便于快速求解\\

3. 积分运算法则\\
\int [f(x) \pm g(x)] dx = \int f(x) dx \pm \int g(x) dx \\
\int k \cdot f(x) dx = k \int f(x) dx \\
积分线性性质：加减、常数因子可直接提出\\

4. 定积分（求面积）\\
\int_a^b f(x) dx = F(b) - F(a) \\
定积分表示函数 f(x) 在区间 [a, b] 下曲线与 x 轴之间的净面积\\
F(x) 为 f(x) 的原函数\\

5. 定积分性质\\
\int_a^a f(x) dx = 0 \\
\int_a^b f(x) dx = -\int_b^a f(x) dx \\
\int_a^b [f(x) \pm g(x)] dx = \int_a^b f(x) dx \pm \int_a^b g(x) dx \\
\int_a^b k \cdot f(x) dx = k \int_a^b f(x) dx \\
\int_a^b f(x) dx = \int_a^c f(x) dx + \int_c^b f(x) dx \\
定积分可拆分区间进行计算\\

6. 换元积分法\\
\int f(g(x)) g'(x) dx = \int f(u) du, \quad u = g(x) \\
通过代换，将复杂函数转换为容易积分的形式\\

7. 分部积分法\\
\int u \, dv = u v - \int v \, du \\
适用于两函数乘积的积分，将复杂积分拆分为易处理形式\\

8. 定积分几何意义\\
\int_a^b f(x) dx 表示曲线 y=f(x) 从 x=a 到 x=b 与 x 轴之间的面积\\
曲线在 x 轴下方的部分积分为负，净面积为正负相抵后的值\\

9. 常用结论\\
定积分可用于求面积、弧长、体积、平均值等\\
\text{平均值}：f_{\text{avg}} = \frac{1}{b-a} \int_a^b f(x) dx \\
$$

#### 多元微积分（偏导数、重积分、雅可比矩阵）

$$
1. 多元函数与偏导数\\
多元函数：函数的自变量不止一个，如 f(x, y), f(x, y, z)\\
偏导数：在多元函数中，对某一个自变量求导，其他变量固定\\
\frac{\partial f}{\partial x} = \lim_{h \to 0} \frac{f(x+h, y) - f(x, y)}{h} \\
\frac{\partial f}{\partial y} = \lim_{h \to 0} \frac{f(x, y+h) - f(x, y)}{h} \\
偏导数表示函数对某一方向的瞬时变化率\\

2. 高阶偏导数与混合偏导\\
二阶偏导数：f_{xx} = \frac{\partial^2 f}{\partial x^2}, \quad f_{yy} = \frac{\partial^2 f}{\partial y^2} \\
混合偏导数：f_{xy} = \frac{\partial^2 f}{\partial x \partial y}, \quad f_{yx} = \frac{\partial^2 f}{\partial y \partial x} \\
若函数连续且二阶偏导连续，则 f_{xy} = f_{yx}（克莱罗定理）\\

3. 梯度向量\\
\nabla f(x, y) = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right) \\
梯度方向：函数值增大最快的方向\\
梯度模：||\nabla f|| = \sqrt{(f_x)^2 + (f_y)^2} 表示变化最快的速率\\

4. 多元函数的极值与驻点\\
驻点条件：\nabla f(x, y) = 0 或梯度不存在的点\\
二阶判别法（二维情况）：\\
H = \begin{vmatrix} f_{xx} & f_{xy} \\ f_{yx} & f_{yy} \end{vmatrix} \\
H > 0, f_{xx} > 0 \Rightarrow \text{局部最小值} \\
H > 0, f_{xx} < 0 \Rightarrow \text{局部最大值} \\
H < 0 \Rightarrow \text{鞍点} \\
H = 0 \Rightarrow 判别法失败，需要进一步分析\\

5. 重积分（双重积分、三重积分）\\
双重积分：\iint_D f(x, y) d\sigma \\
表示在区域 D 上函数 f(x, y) 的积分，可理解为“体积”或“累积量”\\
积分顺序可交换（在连续可积条件下）：\iint_D f(x, y) dx dy = \iint_D f(x, y) dy dx\\
三重积分：\iiint_\Omega f(x, y, z) dV \\
表示三维空间区域 \Omega 内函数 f(x, y, z) 的积分\\

6. 重积分计算方法\\
直角坐标法：\iint_D f(x, y) dx dy 或 dy dx，根据区域边界决定积分顺序\\
极坐标法（二维）：x = r \cos \theta, y = r \sin \theta, dx dy = r dr d\theta\\
柱面坐标（三维）：x = r \cos \theta, y = r \sin \theta, z = z, dV = r dr d\theta dz\\
球坐标（三维）：x = \rho \sin \phi \cos \theta, y = \rho \sin \phi \sin \theta, z = \rho \cos \phi, dV = \rho^2 \sin \phi d\rho d\phi d\theta\\
选择合适坐标系可简化积分计算\\

7. 雅可比矩阵与变量替换\\
n 元函数 \mathbf{F}(x_1, ..., x_n) = (f_1, ..., f_m) 的雅可比矩阵：\\
J = \frac{\partial(f_1, ..., f_m)}{\partial(x_1, ..., x_n)} = 
\begin{bmatrix}
\frac{\partial f_1}{\partial x_1} & \cdots & \frac{\partial f_1}{\partial x_n} \\
\vdots & \ddots & \vdots \\
\frac{\partial f_m}{\partial x_1} & \cdots & \frac{\partial f_m}{\partial x_n}
\end{bmatrix} \\
雅可比行列式（det J）用于变量替换求重积分：dx_1 ... dx_n = |\det J| du_1 ... du_n\\
保证积分区域在坐标变换下体积保持比例\\

8. 多元微积分常用结论\\
梯度方向垂直于等值面或等高线\\
重积分可用不同坐标系简化计算\\
雅可比矩阵提供变量替换和局部线性变换信息\\
偏导、梯度、雅可比在优化问题、物理建模、概率统计中广泛应用\\
$$



### 待整理

1 偏二阶导数 及如何描述函数的凹凸性、极值  2 梯度方向垂直等高线\
3 切线方程 4 多元函数极值 5 不定积分没理解  6 导数并没有十分理解
