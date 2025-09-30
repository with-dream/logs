# 高等线性代数

#### 向量范数、矩阵范数

$$
\textbf{1\ 向量范数（Vector Norm）} \\
\\
\text{向量范数用于度量向量的长度或大小。常用的 p-范数（Lp-norm）定义为：} \\
\text{设 } \mathbf{x} = (x_1, x_2, \dots, x_n)^T \in \mathbb{R}^n, \quad \|\mathbf{x}\|_p = \left( \sum_{i=1}^{n} |x_i|^p \right)^{1/p}, \quad p \ge 1 \\
\\
\text{常用范数：} \\
\text{1-范数（曼哈顿范数）: } \|\mathbf{x}\|_1 = \sum_{i=1}^{n} |x_i| \\
\text{2-范数（欧几里得范数）: } \|\mathbf{x}\|_2 = \sqrt{\sum_{i=1}^{n} x_i^2} \\
\infty\text{-范数（最大范数）: } \|\mathbf{x}\|_\infty = \max_{1 \le i \le n} |x_i| \\
\\
\text{性质：} \\
\|\mathbf{x}\| \ge 0, \quad \|\mathbf{x}\| = 0 \iff \mathbf{x} = 0 \\
\|\alpha \mathbf{x}\| = |\alpha| \|\mathbf{x}\| \\
\|\mathbf{x} + \mathbf{y}\| \le \|\mathbf{x}\| + \|\mathbf{y}\| \ (\text{三角不等式}) \\
\\
\textbf{2\ 矩阵范数（Matrix Norm）} \\
\\
\text{矩阵范数用于度量矩阵的大小或“伸缩能力”。常用定义包括算子范数和Frobenius范数。} \\
\\
\text{2.1 Frobenius 范数（平方和范数）：} \\
\|\mathbf{A}\|_F = \sqrt{\sum_{i=1}^{m} \sum_{j=1}^{n} |a_{ij}|^2} \\
\text{等价于 } \|\mathbf{A}\|_F = \sqrt{ \text{trace}(A^T A) } \\
\\
\text{2.2 p-算子范数（Induced Norm / Operator Norm）：} \\
\|\mathbf{A}\|_p = \sup_{\mathbf{x} \neq 0} \frac{\|\mathbf{A} \mathbf{x}\|_p}{\|\mathbf{x}\|_p} \\
\\
\text{常用算子范数：} \\
\text{谱范数（2-范数）: } \|\mathbf{A}\|_2 = \sqrt{\lambda_{\max}(A^T A)} = \sigma_{\max}(A), \text{最大奇异值} \\
1\text{-范数: } \|\mathbf{A}\|_1 = \max_{1 \le j \le n} \sum_{i=1}^{m} |a_{ij}| \ (\text{列和最大}) \\
\infty\text{-范数: } \|\mathbf{A}\|_\infty = \max_{1 \le i \le m} \sum_{j=1}^{n} |a_{ij}| \ (\text{行和最大}) \\
\\
\text{性质：} \\
\|\alpha A\| = |\alpha| \|A\| \\
\|A + B\| \le \|A\| + \|B\| \\
\|A B\| \le \|A\| \|B\| \ (\text{次乘性}) \\
$$

#### 正定矩阵、Gram 矩阵

$$
\textbf{1 正定矩阵（Positive Definite Matrix）} \\
\text{说明：正定矩阵是线性代数中非常重要的矩阵类型，用于判断二次型的正性、优化问题中的凸性等。} \\
\text{定义：} \\
\text{设 } A \in \mathbb{R}^{n \times n} \text{ 是对称矩阵，如果对任意非零向量 } x \in \mathbb{R}^n \text{ 有 } x^T A x > 0 \\
\text{则称 } A \text{ 为正定矩阵。} \\
\text{性质：} \\
1. \text{所有特征值 } \lambda_i > 0 \\
2. \text{矩阵 A 可分解为 } A = L L^T \text{（Cholesky 分解），其中 } L \text{ 为下三角矩阵} \\
3. \text{正定矩阵的主子矩阵也都是正定矩阵} \\
\text{判定方法：} \\
\text{(1) 所有主子式 } \Delta_k = \det(A_k) > 0, \quad k=1,2,\dots,n \\
\text{(2) 所有特征值 } \lambda_i > 0 \\
\\
\textbf{2 Gram 矩阵（Gram Matrix）} \\
\text{说明：Gram 矩阵用于描述向量组之间的内积关系，常用于信号处理、最小二乘法、核方法等。} \\
\text{定义：} \\
\text{设 } v_1, v_2, \dots, v_n \in \mathbb{R}^m \text{ 为向量，则它们的 Gram 矩阵定义为} \\
G = \begin{bmatrix}  
v_1^T v_1 & v_1^T v_2 & \dots & v_1^T v_n \\  
v_2^T v_1 & v_2^T v_2 & \dots & v_2^T v_n \\  
\vdots & \vdots & \ddots & \vdots \\  
v_n^T v_1 & v_n^T v_2 & \dots & v_n^T v_n \\  
\end{bmatrix} \\
\text{性质：} \\
1. \text{Gram 矩阵总是对称的 } G = G^T \\
2. \text{Gram 矩阵总是半正定的，即 } x^T G x \ge 0, \quad \forall x \in \mathbb{R}^n \\
3. \text{如果向量组线性无关，则 Gram 矩阵正定} \\
\text{与正定矩阵的关系：} \\
\text{如果 } v_1, \dots, v_n \text{ 线性无关，则 Gram 矩阵 } G \text{ 是正定矩阵} \\
$$

#### 特征分解与 PCA

$$
\textbf{1 特征分解（Eigen Decomposition）} \\
\text{说明：特征分解是线性代数中将矩阵分解为特征向量和特征值的形式，用于理解矩阵的结构、简化计算等。} \\
\text{定义：} \\
\text{设 } A \in \mathbb{R}^{n \times n} \text{，如果存在非零向量 } v \in \mathbb{R}^n \text{ 和标量 } \lambda \in \mathbb{R} \text{ 使得} \\
A v = \lambda v \\
\text{则称 } \lambda \text{ 为矩阵 } A \text{ 的特征值，} v \text{ 为对应的特征向量。} \\
\text{矩阵特征分解形式（对称矩阵 A）：} \\
A = V \Lambda V^T \\
\text{其中 } V = [v_1, v_2, \dots, v_n] \text{ 为特征向量构成的正交矩阵，} \Lambda = \text{diag}(\lambda_1, \dots, \lambda_n) \text{ 为特征值对角矩阵。} \\
\text{性质：} \\
1. \text{对称矩阵总是可以特征分解，且特征向量正交} \\
2. \text{矩阵的秩等于非零特征值的个数} \\
3. \text{幂次矩阵可以通过特征分解简化计算： } A^k = V \Lambda^k V^T \\

\\
\textbf{2 主成分分析（PCA, Principal Component Analysis）} \\
\text{说明：PCA 是一种降维方法，用于将高维数据投影到低维空间，同时保留数据的主要方差方向。} \\
\text{步骤：} \\
1. \text{数据中心化：} X_c = X - \bar{X} \\
2. \text{计算协方差矩阵：} \Sigma = \frac{1}{n} X_c^T X_c \\
3. \text{对协方差矩阵进行特征分解：} \Sigma = V \Lambda V^T \\
4. \text{选择前 k 个最大特征值对应的特征向量构成投影矩阵 } W = [v_1, \dots, v_k] \\
5. \text{降维后的数据：} Z = X_c W \\
\text{性质与说明：} \\
1. \text{PCA 最大化投影后的方差，保证信息尽可能保留} \\
2. \text{特征向量对应的特征值越大，其方向上的方差越大} \\
3. \text{PCA 可以理解为协方差矩阵的特征分解应用} \\
$$























