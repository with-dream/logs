# 概率论与数理统计

#### 联合分布、条件分布、贝叶斯公式

$$
\textbf{1 联合分布（Joint Distribution）} \\
\text{说明：联合分布刻画多个随机变量同时发生时的概率分布情况。} \\
\text{若随机变量 } X, Y \text{ 的联合概率分布函数为：} \\
P(X = x, Y = y) \\
\text{则称其为联合分布。对于连续型随机变量，联合概率密度函数为：} \\
f_{X,Y}(x,y) \\

\text{性质：} \\
1. \text{边缘分布：} P(X=x) = \sum_y P(X=x, Y=y) \quad (\text{离散型}) \\
\quad f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x,y) dy \quad (\text{连续型}) \\
2. \text{联合分布完全刻画了随机变量之间的关系} \\

\\
\textbf{2 条件分布（Conditional Distribution）} \\
\text{说明：条件分布表示在已知一个随机变量取值的情况下，另一个随机变量的分布。} \\
\text{离散型：} \\
P(X=x \mid Y=y) = \frac{P(X=x, Y=y)}{P(Y=y)} \\
\text{连续型：} \\
f_{X \mid Y}(x \mid y) = \frac{f_{X,Y}(x,y)}{f_Y(y)} \\
\text{条件分布描述了在 } Y=y \text{ 已知时， } X \text{ 的分布规律。} \\

\\
\textbf{3 贝叶斯公式（Bayes' Theorem）} \\
\text{说明：贝叶斯公式用于在已知条件概率的情况下，推导反向条件概率，是贝叶斯统计的基础。} \\
\text{公式：} \\
P(A \mid B) = \frac{P(B \mid A) \, P(A)}{P(B)} \\
\text{其中：} \\
P(B) = \sum_i P(B \mid A_i) P(A_i) \quad \text{（离散情形，全概率公式）} \\
\text{意义：} \\
1. \text{将“结果已知时的原因概率”转换为“原因已知时的结果概率”} \\
2. \text{在机器学习、统计推断、模式识别等领域应用广泛} \\
$$

#### 随机向量与协方差矩阵

$$
\textbf{1 随机向量（Random Vector）} \\
\text{说明：随机向量是由多个随机变量组成的向量，用于描述多维随机现象。} \\
\text{定义：设 } X_1, X_2, \dots, X_n \text{ 为随机变量，随机向量定义为：} \\
X = \begin{bmatrix} X_1 \\ X_2 \\ \vdots \\ X_n \end{bmatrix} \in \mathbb{R}^n \\
\text{其分布由联合分布函数 } F_X(x) = P(X_1 \leq x_1, \dots, X_n \leq x_n) \text{ 描述。} \\

\text{性质：} \\
1. \text{随机向量的期望：} E[X] = \begin{bmatrix} E[X_1] \\ E[X_2] \\ \vdots \\ E[X_n] \end{bmatrix} \\
2. \text{随机向量的线性变换：若 } Y = AX + b, \text{则 } E[Y] = AE[X] + b \\

\\
\textbf{2 协方差矩阵（Covariance Matrix）} \\
\text{说明：协方差矩阵刻画了随机向量各分量之间的方差和协方差关系。} \\
\text{定义：} \\
\Sigma = \mathrm{Cov}(X) = E\left[ (X - E[X])(X - E[X])^T \right] \\
\text{其中 } \Sigma \in \mathbb{R}^{n \times n}, \text{元素为：} \\
\Sigma_{ij} = \mathrm{Cov}(X_i, X_j) = E[(X_i - E[X_i])(X_j - E[X_j])] \\

\text{性质：} \\
1. \text{协方差矩阵对称：} \Sigma^T = \Sigma \\
2. \text{协方差矩阵半正定：} x^T \Sigma x \geq 0 \quad \forall x \in \mathbb{R}^n \\
3. \text{对角元素为方差：} \Sigma_{ii} = \mathrm{Var}(X_i) \\
4. \text{非对角元素为协方差：} \Sigma_{ij} = \mathrm{Cov}(X_i, X_j) \\
$$

#### 极大似然估计（MLE）、贝叶斯估计

$$
\textbf{1 极大似然估计（Maximum Likelihood Estimation, MLE）} \\
\text{说明：MLE 通过最大化观测数据在给定参数下的似然函数，来估计未知参数。} \\
\text{设样本为 } x_1, x_2, \dots, x_n, \text{其概率密度（或质量）函数为 } f(x \mid \theta)。 \\
\text{似然函数定义为：} \\
L(\theta) = \prod_{i=1}^n f(x_i \mid \theta) \\
\text{对数似然函数（便于计算）：} \\
\ell(\theta) = \ln L(\theta) = \sum_{i=1}^n \ln f(x_i \mid \theta) \\
\text{极大似然估计量定义为：} \\
\hat{\theta}_{MLE} = \arg \max_{\theta} L(\theta) = \arg \max_{\theta} \ell(\theta) \\
\text{性质：} \\
1. \text{在样本量足够大时，MLE 渐近无偏且有效。} \\
2. \text{MLE 仅依赖数据和模型假设，不考虑先验信息。} \\

\\
\textbf{2 贝叶斯估计（Bayesian Estimation）} \\
\text{说明：贝叶斯估计结合了先验分布与观测数据，通过后验分布推断参数。} \\
\text{贝叶斯公式：} \\
p(\theta \mid X) = \frac{p(X \mid \theta) \, p(\theta)}{p(X)} \\
\text{其中：} \\
p(X \mid \theta) \text{ 为似然函数，} \\
p(\theta) \text{ 为先验分布，} \\
p(\theta \mid X) \text{ 为后验分布。} \\
\text{常见贝叶斯估计准则：} \\
1. \text{最大后验估计（MAP）：} \hat{\theta}_{MAP} = \arg \max_{\theta} p(\theta \mid X) \\
2. \text{贝叶斯均值估计：} \hat{\theta}_{Bayes} = E[\theta \mid X] = \int \theta \, p(\theta \mid X) \, d\theta \\
\text{性质：} \\
1. \text{贝叶斯估计考虑了先验信息，适合样本量较小的情况。} \\
2. \text{当先验为均匀分布时，MAP 估计等价于 MLE。} \\
$$

#### 偏差-方差分解

$$
\textbf{1 问题背景} \\
\text{在监督学习中，我们希望模型 } f(x) \text{ 尽可能逼近真实函数 } f^*(x)。 \\
\text{预测误差可以分解为偏差、方差和不可约误差。} \\

\\
\textbf{2 偏差-方差分解公式} \\
\text{设真实模型为 } y = f^*(x) + \epsilon, \quad E[\epsilon] = 0, \quad Var(\epsilon) = \sigma^2。 \\
\text{学习算法得到的模型为 } \hat{f}(x)。 \\
\text{均方误差（MSE）：} \\
MSE(x) = E\big[(\hat{f}(x) - f^*(x))^2\big] \\
\text{分解为：} \\
MSE(x) = \underbrace{(E[\hat{f}(x)] - f^*(x))^2}_{\text{偏差}^2} + \underbrace{E[(\hat{f}(x) - E[\hat{f}(x)])^2]}_{\text{方差}} + \underbrace{\sigma^2}_{\text{噪声}} \\

\\
\textbf{3 各部分解释} \\
1. \text{偏差（Bias）：模型的期望预测与真实值的差距，反映模型拟合能力。} \\
2. \text{方差（Variance）：不同训练集下模型预测的波动性，反映模型的稳定性。} \\
3. \text{噪声（Noise）：数据本身的不可约误差，与模型无关。} \\

\\
\textbf{4 意义} \\
1. \text{高偏差：模型过于简单（欠拟合），难以学习到真实模式。} \\
2. \text{高方差：模型过于复杂（过拟合），对训练数据敏感。} \\
3. \text{偏差-方差权衡：选择合适的模型复杂度，在偏差与方差之间取得平衡。} \\
$$

