# 优化理论

#### 凸函数与凸优化

$$
\textbf{1 凸函数（Convex Function）} \\
\text{说明：凸函数是定义在凸集上的函数，其函数值不会高于连接两点的线段。} \\
\text{定义：设 } f: \mathbb{R}^n \to \mathbb{R}, \text{若对于任意 } x,y \in \mathrm{dom}(f), \, \theta \in [0,1], \\
f(\theta x + (1-\theta)y) \leq \theta f(x) + (1-\theta)f(y), \\
\text{则称 } f(x) \text{ 为凸函数。若不等式严格成立，则称为严格凸函数。} \\

\text{常见判别方法：} \\
1. \text{单变量函数：若 } f''(x) \geq 0 \text{ 对所有 } x \text{ 成立，则 } f(x) \text{ 为凸函数。} \\
2. \text{多变量函数：若 Hessian 矩阵 } \nabla^2 f(x) \succeq 0 \text{，则 } f(x) \text{ 为凸函数。} \\

\text{性质：} \\
1. \text{凸函数的局部极小点必为全局极小点。} \\
2. \text{凸函数的非负加权和仍为凸函数。} \\

\\
\textbf{2 凸优化（Convex Optimization）} \\
\text{说明：凸优化问题是在凸集上最小化凸函数，具有良好的理论性质和高效的算法。} \\
\text{标准形式：} \\
\min_{x \in \mathbb{R}^n} f(x) \\
\text{s.t. } g_i(x) \leq 0, \; i = 1, \dots, m \\
\quad \; h_j(x) = 0, \; j = 1, \dots, p \\
\text{其中 } f(x) \text{ 和 } g_i(x) \text{ 为凸函数，} h_j(x) \text{ 为仿射函数。} \\

\text{性质：} \\
1. \text{可解性好：局部极小解一定是全局极小解。} \\
2. \text{对偶理论：凸优化问题常可通过对偶问题求解。} \\
3. \text{算法：梯度下降、牛顿法、内点法等在凸优化中表现稳定。} \\

\text{应用：} \\
1. \text{机器学习：如 SVM、Lasso 回归。} \\
2. \text{信号处理、运筹学、控制理论等领域。} \\
$$

#### Lagrange 乘子法

$$
\textbf{1 问题背景} \\
\text{在优化问题中，如果存在约束条件，常用 Lagrange 乘子法将约束纳入目标函数进行求解。} \\

\\
\textbf{2 基本形式} \\
\text{约束优化问题：} \\
\min f(x) \\
\text{s.t. } g_i(x) = 0, \quad i = 1, 2, \dots, m \\

\text{构造 Lagrangian 函数：} \\
\mathcal{L}(x, \lambda) = f(x) + \sum_{i=1}^m \lambda_i g_i(x) \\
\text{其中 } \lambda_i \text{ 为 Lagrange 乘子。} \\

\\
\textbf{3 一阶必要条件（KKT 条件的等式约束部分）} \\
\frac{\partial \mathcal{L}(x, \lambda)}{\partial x} = 0 \\
\frac{\partial \mathcal{L}(x, \lambda)}{\partial \lambda_i} = g_i(x) = 0, \quad i=1,2,\dots,m \\

\text{解此方程组可得到候选极值点。} \\

\\
\textbf{4 推广：含不等式约束的情况（KKT 条件）} \\
\min f(x) \\
\text{s.t. } g_i(x) \leq 0, \; i=1,\dots,m; \quad h_j(x)=0, \; j=1,\dots,p \\

\text{Lagrangian：} \\
\mathcal{L}(x, \
$$

#### 梯度下降、牛顿法

$$
\textbf{1 梯度下降法（Gradient Descent）} \\
\text{说明：梯度下降是一种一阶优化方法，通过沿负梯度方向迭代更新变量以最小化目标函数。} \\
\text{迭代公式：} \\
x_{k+1} = x_k - \eta \nabla f(x_k) \\
\text{其中 } \eta > 0 \text{ 为学习率（步长）。} \\

\text{性质与特点：} \\
1. \text{若 } f(x) \text{ 为凸函数，则梯度下降法收敛到全局最优解。} \\
2. \text{学习率过大会导致震荡，过小则收敛缓慢。} \\
3. \text{常见改进：动量法、随机梯度下降（SGD）、自适应学习率方法（Adam、RMSProp 等）。} \\

\\
\textbf{2 牛顿法（Newton's Method）} \\
\text{说明：牛顿法是一种二阶优化方法，利用 Hessian 矩阵信息加速收敛。} \\
\text{迭代公式：} \\
x_{k+1} = x_k - [\nabla^2 f(x_k)]^{-1} \nabla f(x_k) \\
\text{其中 } \nabla^2 f(x_k) \text{ 为 Hessian 矩阵。} \\

\text{性质与特点：} \\
1. \text{在目标函数二次可微且 Hessian 正定时，牛顿法具有二次收敛速度。} \\
2. \text{相比梯度下降，牛顿法每次迭代计算代价更高（需计算并求逆 Hessian）。} \\
3. \text{若 Hessian 不正定，需使用修正方法（如拟牛顿法 BFGS）。} \\

\text{对比：} \\
- \text{梯度下降：依赖一阶导数，计算简单但收敛较慢。} \\
- \text{牛顿法：利用二阶信息，收敛快但计算复杂。} \\
$$

#### KKT 条件与约束优化

$$
\textbf{1 约束优化问题（Constrained Optimization）} \\
\text{一般形式：} \\
\min_{x \in \mathbb{R}^n} f(x) \\
\text{s.t. } g_i(x) \leq 0, \quad i=1,\dots,m \\
\quad\quad h_j(x) = 0, \quad j=1,\dots,p \\

\text{其中：} \\
- f(x) \text{ 为目标函数} \\
- g_i(x) \text{ 为不等式约束} \\
- h_j(x) \text{ 为等式约束} \\

\\
\textbf{2 拉格朗日函数（Lagrangian Function）} \\
L(x, \lambda, \mu) = f(x) + \sum_{i=1}^m \lambda_i g_i(x) + \sum_{j=1}^p \mu_j h_j(x) \\
\text{其中：} \lambda_i \geq 0 \text{ 为不等式约束的拉格朗日乘子，} \mu_j \in \mathbb{R} \text{ 为等式约束的拉格朗日乘子。} \\

\\
\textbf{3 KKT 条件（Karush–Kuhn–Tucker Conditions）} \\
\text{若 } x^* \text{ 是约束优化问题的最优解，则存在 } \lambda^*, \mu^* \text{ 使得：} \\

(1)\ \ \nabla_x L(x^*, \lambda^*, \mu^*) = 0 \quad \text{(驻点条件)} \\
(2)\ \ g_i(x^*) \leq 0, \quad h_j(x^*) = 0 \quad \text{(可行性条件)} \\
(3)\ \ \lambda_i^* \geq 0 \quad \text{(乘子非负性)} \\
(4)\ \ \lambda_i^* g_i(x^*) = 0, \quad \forall i \quad \text{(互补松弛条件)} \\

\\
\textbf{4 性质与说明} \\
1. \text{KKT 条件是约束优化的必要条件（在某些正则条件下）。} \\
2. \text{若问题为凸优化问题（目标函数凸，约束为凸集），则 KKT 条件也是充分条件。} \\
3. \text{通过 KKT 条件，可以转化约束优化为无约束问题（拉格朗日对偶）。} \\

\\
\textbf{5 对比：无约束优化 vs 约束优化} \\
- \text{无约束优化：最优解满足 } \nabla f(x^*) = 0。 \\
- \text{约束优化：需满足 KKT 条件（梯度 + 约束 + 互补条件）。} \\
$$

