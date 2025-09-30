# 线性代数

#### 向量与矩阵运算

$$
\textbf{1\ 向量基础} \\
\\
\textbf{1.1\ 向量的表示} \\
\text{向量是具有大小和方向的量，可以用坐标表示为列向量或行向量：} \\
\vec{a} = \begin{bmatrix} a_1 \\ a_2 \\ \dots \\ a_n \end{bmatrix} \\
\vec{b} = \begin{bmatrix} b_1 \\ b_2 \\ \dots \\ b_n \end{bmatrix} \\
\text{说明：}\ \vec{a}, \vec{b}\text{为 n 维向量，列向量在矩阵运算中使用最广泛。} \\
\\
\textbf{1.2\ 向量加减法} \\
\vec{a} + \vec{b} = \begin{bmatrix} a_1 + b_1 \\ a_2 + b_2 \\ \dots \\ a_n + b_n \end{bmatrix} \\
\vec{a} - \vec{b} = \begin{bmatrix} a_1 - b_1 \\ a_2 - b_2 \\ \dots \\ a_n - b_n \end{bmatrix} \\
\text{说明：向量加法满足交换律和结合律。} \\
\\
\textbf{1.3\ 向量数乘} \\
k \vec{a} = \begin{bmatrix} k a_1 \\ k a_2 \\ \dots \\ k a_n \end{bmatrix} \\
\text{说明：改变向量长度，方向不变（若 } k<0 \text{则反向）。} \\
\\
\textbf{1.4\ 向量模（长度）} \\
|\vec{a}| = \sqrt{a_1^2 + a_2^2 + \dots + a_n^2} \\
\text{说明：模表示向量大小，单位向量计算公式为 } \hat{a} = \frac{\vec{a}}{|\vec{a}|}。 \\
\\
\textbf{1.5\ 向量点积（内积）} \\
\vec{a} \cdot \vec{b} = a_1 b_1 + a_2 b_2 + \dots + a_n b_n \\
\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos\theta \\
\text{说明：夹角 }\theta\text{为两向量夹角，点积为零表示垂直。} \\
\\
\textbf{1.6\ 向量叉积（仅三维）} \\
\vec{a} \times \vec{b} = 
\begin{bmatrix} 
a_2 b_3 - a_3 b_2 \\ 
a_3 b_1 - a_1 b_3 \\ 
a_1 b_2 - a_2 b_1 
\end{bmatrix} \\
\text{说明：叉积结果垂直于 }\vec{a}\text{和 }\vec{b}\text{平面，模表示平行四边形面积。} \\
\\
\textbf{2\ 矩阵基础} \\
\\
\textbf{2.1\ 矩阵定义} \\
A = \begin{bmatrix} 
a_{11} & a_{12} & \dots & a_{1n} \\ 
a_{21} & a_{22} & \dots & a_{2n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \dots & a_{mn} 
\end{bmatrix} \\
\text{说明：} A\text{为 } m \times n \text{矩阵， } a_{ij}\text{表示第 i 行第 j 列元素。} \\
\\
\textbf{2.2\ 矩阵加减法} \\
A + B = \begin{bmatrix} 
a_{11}+b_{11} & \dots & a_{1n}+b_{1n} \\ 
\vdots & \ddots & \vdots \\ 
a_{m1}+b_{m1} & \dots & a_{mn}+b_{mn} 
\end{bmatrix} \\
A - B = \begin{bmatrix} 
a_{11}-b_{11} & \dots & a_{1n}-b_{1n} \\ 
\vdots & \ddots & \vdots \\ 
a_{m1}-b_{m1} & \dots & a_{mn}-b_{mn} 
\end{bmatrix} \\
\text{说明：矩阵加减要求维度相同。} \\
\\
\textbf{2.3\ 矩阵数乘} \\
kA = \begin{bmatrix} 
k a_{11} & \dots & k a_{1n} \\ 
\vdots & \ddots & \vdots \\ 
k a_{m1} & \dots & k a_{mn} 
\end{bmatrix} \\
\\
\textbf{2.4\ 矩阵乘法} \\
C = AB, \quad C_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj} \\
\text{说明：} A \text{为 } m \times n, B \text{为 } n \times p, C \text{为 } m \times p. \text{不满足交换律。} \\
\\
\textbf{2.5\ 转置与逆矩阵} \\
A^T = \begin{bmatrix} 
a_{11} & a_{21} & \dots & a_{m1} \\ 
a_{12} & a_{22} & \dots & a_{m2} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{1n} & a_{2n} & \dots & a_{mn} 
\end{bmatrix} \\
AA^{-1} = A^{-1}A = I \\
\text{说明：单位矩阵 } I \text{，逆矩阵存在条件：方阵且行列式非零。} \\
\\
\textbf{3\ 向量与矩阵的运用} \\
\\
\textbf{3.1\ 向量投影} \\
\text{proj}_{\vec{b}} \vec{a} = \frac{\vec{a} \cdot \vec{b}}{|\vec{b}|^2} \vec{b} \\
\\
\textbf{3.2\ 矩阵行列式} \\
\det(A) = \sum_{j=1}^{n} (-1)^{1+j} a_{1j} \det(A_{1j}) \\
\text{说明：} A_{1j} \text{为去掉第1行第 j 列的子矩阵，行列式为零表示不可逆。} \\
\textbf{4.\ 对角矩阵} \\
定义:一个n×n 方阵D，如果除了主对角线上的元素外，其余位置全是 0 \\
D = \begin{bmatrix}  
d_{11} & 0      & 0      & \cdots & 0 \\
0      & d_{22} & 0      & \cdots & 0 \\
0      & 0      & d_{33} & \cdots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0      & 0      & 0      & \cdots & d_{nn}
\end{bmatrix}
$$

转置: 行和列互换

向量投影:  向量a在向量b上的投影所产生的向量

矩阵行列式: 矩阵的一种应用 用到再学

#### 线性方程组、秩、逆矩阵

$$
\textbf{1\ 线性方程组} \\
\\
\text{线性方程组的一般形式：} \\
\begin{cases} 
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1 \\ 
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = b_2 \\ 
\vdots \\ 
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = b_m 
\end{cases} \\
\text{矩阵形式：} \quad A\vec{x} = \vec{b},\quad 
A = \begin{bmatrix} 
a_{11} & a_{12} & \dots & a_{1n} \\ 
a_{21} & a_{22} & \dots & a_{2n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \dots & a_{mn} 
\end{bmatrix},\quad \vec{x} = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix},\quad \vec{b} = \begin{bmatrix} b_1 \\ b_2 \\ \vdots \\ b_m \end{bmatrix} \\
\text{说明：线性方程组有三种情况：无解、唯一解、无穷多解。} \\
\\
\textbf{2\ 矩阵秩} \\
\\
\text{矩阵秩定义：矩阵中最大线性无关行（列）的个数。} \\
\text{符号表示：} \text{rank}(A) \\
\\
\text{性质：} \\
\text{(1) rank(A) } \le \min(m,n) \\
\text{(2) 对于矩阵方程 } A\vec{x} = \vec{b}, \text{若 } \text{rank}(A) = \text{rank}([A|\vec{b}]), \text{则有解。} \\
\text{(3) 若 rank(A) = n，则方阵可逆，方程有唯一解。} \\
\\
\textbf{3\ 逆矩阵} \\
\\
\text{定义：方阵 } A \text{存在矩阵 } A^{-1} \text{使 } AA^{-1} = A^{-1}A = I \\
\\
\text{求逆矩阵方法（仅方阵）：} \\
\text{(1) 伴随矩阵法：} \quad A^{-1} = \frac{1}{\det(A)} \text{adj}(A) \\
\text{(2) 初等行变换法：将 } [A|I] \text{化为 } [I|A^{-1}] \\
\\
\text{说明：} \\
\text{(1) 逆矩阵存在的充分必要条件：方阵且 }\det(A) \neq 0 \\
\text{(2) 方程组 } A\vec{x} = \vec{b} \text{若 } A^{-1} \text{存在，则唯一解 } \vec{x} = A^{-1}\vec{b} \\

\textbf{4.\ 矩阵相似变换} \\
1\ 定义：矩阵相似变换  \\
\text{若 } A, B \in \mathbb{R}^{n \times n} \text{，存在可逆矩阵 } P \in \mathbb{R}^{n \times n} \text{，使得} \\
B = P^{-1} A P \\
\text{则称矩阵 } A \text{ 与 } B \text{ 相似，记作 } A \sim B 。 \\

2\ 直观理解 \\
\text{矩阵 } A \text{ 表示一个线性变换 } x \mapsto Ax 。 \\
\text{相似变换 } B = P^{-1} A P \text{ 相当于在新坐标系下观察同一线性变换}。 \\
\text{其中 } P \text{ 是从旧坐标系到新坐标系的变换矩阵}。 \\

3\ 相似矩阵的重要性质 \\
\text{设 } A \sim B ，则有： \\
\text{(1) 特征值不变： } \text{eig}(A) = \text{eig}(B) \\
\text{(2) 行列式不变： } \det(A) = \det(B) \\
\text{(3) 迹不变： } \mathrm{tr}(A) = \mathrm{tr}(B) \\
\text{(4) 秩不变： } \mathrm{rank}(A) = \mathrm{rank}(B) \\
$$

线性无关行: 矩阵每一行为一个线性方程 如果该方程经化简后 变量xn可被消掉 则为无关行 因为此xn可以为任意数

行列式的迹: 行列式主对角线元素之和

#### 特征值与特征向量

$$
\textbf{1\ 特征值与特征向量定义} \\
\\
\text{设 } A \text{是 } n \times n \text{方阵，如果存在非零向量 } \vec{v} \neq 0 \text{ 和标量 } \lambda \text{使得：} \\
A \vec{v} = \lambda \vec{v} \\
\text{则称 } \lambda \text{为矩阵 } A \text{的特征值，} \vec{v} \text{为对应的特征向量。} \\
\text{说明：特征向量不为零，特征值可以相同对应多个线性无关向量。} \\
\\
\textbf{2\ 特征方程} \\
\\
\text{将方程 } A \vec{v} = \lambda \vec{v} \text{改写为} (A - \lambda I)\vec{v} = 0 \\
\text{非零解存在条件：} \det(A - \lambda I) = 0 \\
\text{此式称为特征方程，其解 } \lambda_1, \lambda_2, \dots, \lambda_n \text{即为特征值。} \\
\\
\textbf{3\ 特征向量求法} \\
\\
\text{已知特征值 } \lambda, \text{求解 } \vec{v} \text{需满足：} \\
(A - \lambda I)\vec{v} = 0 \\
\text{得到非零解集合即为对应特征向量的空间。} \\
\\
\textbf{4\ 特征值性质} \\
\\
\text{(1) } n \times n \text{矩阵最多有 } n \text{个特征值（代数重数计数）。} \\
\text{(2) 若 } A \text{可对角化，则存在可逆矩阵 } P \text{使 } P^{-1}AP = \Lambda, \text{其中 } \Lambda \text{为对角矩阵。} \\
\text{(3) 对角矩阵的特征值即为对角元素。} \\
\text{(4) 相似矩阵具有相同特征值。} \\
\text{(5) 若 } A \text{为实对称矩阵，则特征值为实数，特征向量可正交化。} \\
\\
\textbf{5\ 矩阵对角化} \\
\\
\text{若矩阵 } A \text{有 } n \text{个线性无关的特征向量 } \vec{v}_1, \vec{v}_2, \dots, \vec{v}_n, \text{则可以构造矩阵 } P = [\vec{v}_1, \vec{v}_2, \dots, \vec{v}_n] \\
\text{使得 } P^{-1} A P = \Lambda = \begin{bmatrix} \lambda_1 & 0 & \dots & 0 \\ 0 & \lambda_2 & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & \lambda_n \end{bmatrix} \\
\text{说明：对角化可简化矩阵幂运算及指数运算。} \\
$$

#### 正交化、对角化

$$
\textbf{1\ 正交化} \\
\\
\text{正交化是将一组线性无关向量变为互相正交(即垂直)的向量集合。常用方法：Gram-Schmidt正交化。} \\
\\
\textbf{1.1\ Gram-Schmidt 正交化} \\
\text{设有线性无关向量组 } \{\vec{v}_1, \vec{v}_2, \dots, \vec{v}_n\} \\
\text{构造正交向量组 } \{\vec{u}_1, \vec{u}_2, \dots, \vec{u}_n\} \text{如下：} \\
\vec{u}_1 = \vec{v}_1 \\
\vec{u}_2 = \vec{v}_2 - \frac{\vec{v}_2 \cdot \vec{u}_1}{\vec{u}_1 \cdot \vec{u}_1} \vec{u}_1 \\
\vec{u}_3 = \vec{v}_3 - \frac{\vec{v}_3 \cdot \vec{u}_1}{\vec{u}_1 \cdot \vec{u}_1} \vec{u}_1 - \frac{\vec{v}_3 \cdot \vec{u}_2}{\vec{u}_2 \cdot \vec{u}_2} \vec{u}_2 \\
\vdots \\
\vec{u}_n = \vec{v}_n - \sum_{k=1}^{n-1} \frac{\vec{v}_n \cdot \vec{u}_k}{\vec{u}_k \cdot \vec{u}_k} \vec{u}_k \\
\text{说明：得到的向量组正交，可进一步单位化得到正交单位向量组 } \hat{u}_i = \frac{\vec{u}_i}{|\vec{u}_i|}。 \\
\\
\textbf{2\ 矩阵对角化} \\
\\
\text{矩阵对角化是将矩阵通过相似变换化为对角矩阵。} \\
\\
\textbf{2.1\ 对角化条件} \\
\text{矩阵 } A \text{可对角化，当且仅当 } A \text{有 } n \text{个线性无关特征向量。} \\
\\
\textbf{2.2\ 对角化方法} \\
\text{设 } \vec{v}_1, \vec{v}_2, \dots, \vec{v}_n \text{为 } A \text{的线性无关特征向量，特征值为 } \lambda_1, \dots, \lambda_n \\
\text{构造矩阵 } P = [\vec{v}_1, \vec{v}_2, \dots, \vec{v}_n] \\
\text{则 } P^{-1} A P = \Lambda = \begin{bmatrix} \lambda_1 & 0 & \dots & 0 \\ 0 & \lambda_2 & \dots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & \lambda_n \end{bmatrix} \\
\\
\textbf{2.3\ 实对称矩阵的对角化} \\
\text{若 } A \text{为实对称矩阵，则存在正交矩阵 } Q \text{使 } Q^T A Q = \Lambda \\
\text{说明：特征向量可选为正交单位向量，且 } Q^{-1} = Q^T。 \\
\text{这种对角化称为正交对角化。} \\
$$

#### 奇异值分解（SVD）

$$
\textbf{1\ SVD基础} \\
1\ 定义（代数角度）\\
对任意 m \times n 矩阵 A，SVD 将其分解为三个矩阵的乘积：\\
A = U \Sigma V^\top \\

U \in \mathbb{R}^{m \times m} \text{ 是正交矩阵，表示输出空间的正交基} \\ 
V \in \mathbb{R}^{n \times n} \text{ 是正交矩阵，表示输入空间的正交基} \\ 
\Sigma \in \mathbb{R}^{m \times n} \text{ 是对角矩阵，对角线元素为奇异值（非负，按大小排列）} \\

\text{注意：}\Sigma \text{ 不一定是方阵，但对角线上的数值都} \ge 0 \\

2\ 几何直观理解\\
\text{把 } A \text{ 看作一个线性变换： } x \mapsto Ax \\

\text{SVD 相当于把这个变换分成三个步骤：} \\

\text{(1) 旋转/反射 } V^\top \text{：把输入向量 } x \text{ 投影到新的正交坐标系} \\ 
\text{(2) 缩放 } \Sigma \text{：沿每个坐标轴按奇异值 } \sigma_i \text{ 拉伸或压缩} \\ 
\text{(3) 旋转/反射 } U \text{：把变换后的向量映射到输出空间} \\

\text{所以，SVD 实际上把复杂的变换拆解成“旋转 → 缩放 → 旋转”的过程} \\

3\ 奇异值的意义\\
\text{奇异值 } \sigma_i \text{ 描述了矩阵在不同方向上的“伸缩强度”} \\ 
\text{矩阵的秩 = 非零奇异值的个数} \\ 
\text{最大奇异值 = 变换的最大放大倍数} \\

4\ 小例子（二维）\\
\text{设 } A = \begin{bmatrix}3 & 1 \\ 0 & 2\end{bmatrix} \text{，SVD 分解后可能得到：} \\

U = \begin{bmatrix} u_1 & u_2 \end{bmatrix}, \quad 
\Sigma = \begin{bmatrix} \sigma_1 & 0 \\ 0 & \sigma_2 \end{bmatrix}, \quad
V^\top = \begin{bmatrix} v_1^\top \\ v_2^\top \end{bmatrix} \\

\text{几何上就是：} \\ 
V^\top \text{ 旋转输入空间} \\ 
\Sigma \text{ 沿 } v_1, v_2 \text{ 方向拉伸} \\ 
U \text{ 再旋转到输出空间} \\
\textbf{1\ SVD定义} \\
\\
\text{设 } A \text{为 } m \times n \text{矩阵，则存在单位正交矩阵 } U (m \times m), V (n \times n) \text{以及对角矩阵 } \Sigma (m \times n) \text{使得：} \\
A = U \Sigma V^T \\
\\
\text{说明：} \\
\text{(1) } U = [\vec{u}_1, \vec{u}_2, \dots, \vec{u}_m],\quad V = [\vec{v}_1, \vec{v}_2, \dots, \vec{v}_n] \text{分别为左右奇异向量矩阵。} \\
\text{(2) } \Sigma = \text{diag}(\sigma_1, \sigma_2, \dots, \sigma_r, 0, \dots, 0),\quad \sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_r > 0 \text{为奇异值。} \\
\text{(3) } r = \text{rank}(A) \text{为矩阵秩。} \\
\\
\textbf{2\ SVD性质} \\
\\
\text{(1) } A^T A = V \Sigma^T \Sigma V^T, \quad A A^T = U \Sigma \Sigma^T U^T \\
\text{(2) 奇异值 } \sigma_i = \sqrt{\lambda_i} \text{，其中 } \lambda_i \text{为 } A^T A \text{或 } A A^T \text{的非零特征值} \\
\text{(3) SVD 可用于任何矩阵（方阵或非方阵），不同于特征值分解仅限方阵。} \\
\text{(4) 对应于非零奇异值 } \sigma_i \text{的 } \vec{u}_i, \vec{v}_i \text{分别为 } AA^T \text{和 } A^T A \text{的特征向量。} \\
\\
\textbf{3\ SVD应用} \\
\\
\text{(1) 矩阵压缩/降维：低秩近似 } A \approx \sum_{i=1}^k \sigma_i \vec{u}_i \vec{v}_i^T, \quad k < r \\
\text{(2) 求广义逆 } A^+ = V \Sigma^+ U^T, \text{其中 } \Sigma^+ = \text{diag}(\sigma_1^{-1}, \dots, \sigma_r^{-1}, 0, \dots, 0) \\
\text{(3) 数据分析：主成分分析(PCA)可通过 SVD 计算协方差矩阵特征向量} \\
\text{(4) 求解最小二乘问题 } \min \|A\vec{x} - \vec{b}\|_2 \text{时可用 SVD。} \\
$$

压缩矩阵: 将矩阵中差异大的列提取出来(即主成分分析) 然后将提取出来的列重新组成一个矩阵

$$
\textbf{1\ 最小二乘法} \\
1\ 问题背景\\
\text{设线性模型为：}\\
y = X \beta + \varepsilon\\
y \in \mathbb{R}^m \text{ ：观测值向量}\\
X \in \mathbb{R}^{m \times n} \text{ ：设计矩阵}\\
\beta \in \mathbb{R}^n \text{ ：待求参数向量}\\
\varepsilon \text{ ：误差}\\
\text{当方程组过定或存在噪声时，一般没有精确解}\\

2\ 最小二乘法思想\\
\hat{\beta} = \arg\min_{\beta} \|y - X\beta\|_2^2\\
\|y - X\beta\|_2^2 = \sum_{i=1}^m (y_i - (X\beta)_i)^2\\
\text{即选择 } \beta \text{ 使得预测值 } X\beta \text{ 与观测值 } y \text{ 差异最小}\\

3\ 求解公式\\
\frac{\partial}{\partial \beta} \|y - X\beta\|_2^2 = -2 X^\top (y - X\beta) = 0\\
X^\top X \hat{\beta} = X^\top y \quad \text{(正规方程)}\\
\text{如果 } X^\top X \text{ 可逆，则解为：}\\
\hat{\beta} = (X^\top X)^{-1} X^\top y\\

4\ 几何理解\\
\text{所有可能的 } X\beta \text{ 构成列空间（Column Space）}\\
\text{最小二乘法就是把 } y \text{ 投影到列空间上}\\
X\hat{\beta} \text{ 是最接近 } y \text{ 的向量}\\
\text{投影误差与列空间正交：}\\
X^\top (y - X\hat{\beta}) = 0\\

5\ SVD 视角\\
X = U \Sigma V^\top \\
\text{列空间由 } U \text{ 的前 } r \text{ 列生成， } r = \text{rank}(X)\\
\hat{\beta} = V \Sigma^{-1} U^\top y \quad \text{(保留非零奇异值)}\\
\text{几何上沿列空间方向找到最佳投影}\\

6\ 总结\\
\text{最小二乘 = 找一个参数向量，使预测向量 } X\beta \text{ 尽量接近观测值 } y\\
\text{误差平方和最小，几何上就是把 } y \text{ 投影到 } X \text{ 的列空间}
$$

### 待补充

&#x20;
