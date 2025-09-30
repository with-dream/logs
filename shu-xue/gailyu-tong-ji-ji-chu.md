# 概率与统计基础

#### 随机变量与分布（正态、二项、泊松、指数等）

$$
\textbf{1\ 随机变量概念} \\
\\
\text{随机变量（Random Variable, RV）是一个函数，将样本空间 } \Omega \text{ 的结果映射到实数 } \mathbb{R}.\\
\text{它将不确定的事件用数值表示，便于分析概率与统计特性。} \\
\text{常用符号： } X, Y, Z\\
\text{分类：} \text{离散型（Discrete）——取有限或可数值；连续型（Continuous）——取连续值} \\
\\
\textbf{1.1\ 概率质量函数（PMF, 离散型）} \\
P(X = x_i) = p_i, \quad \sum_i p_i = 1\\
\text{直观理解：每个可能取值的概率，概率之和为 1；它告诉你离散事件发生的可能性。} \\
\\
\textbf{1.2\ 概率密度函数（PDF, 连续型）} \\
f_X(x) \ge 0, \quad \int_{-\infty}^{\infty} f_X(x) dx = 1\\
P(a \le X \le b) = \int_a^b f_X(x) dx\\
\text{直观理解：PDF 描述连续变量在某个区间的“概率密度”，单点概率为 0，概率通过积分计算。} \\
\\
\textbf{1.3\ 期望与方差} \\
E[X] = \sum_i x_i p_i \ (\text{离散}) \quad \text{或} \quad E[X] = \int_{-\infty}^{\infty} x f_X(x) dx \ (\text{连续})\\
Var(X) = E[(X - E[X])^2] \\
\text{直观理解：期望是随机变量的“中心”或长期平均，方差衡量随机变量偏离中心的程度。} \\
\text{简化公式： } Var(X) = E[X^2] - (E[X])^2 \\
\\
\textbf{2\ 二项分布 Binomial} \\
\\
\text{描述：固定次数独立实验中成功次数的分布，每次实验只有成功/失败两种结果。} \\
X \sim \text{Bin}(n, p), \quad n \text{次独立试验，每次成功概率 } p\\
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}, \quad k = 0,1,\dots,n\\
\text{公式理解：} \\
\text{(1) } \binom{n}{k} = \frac{n!}{k!(n-k)!} \text{ 表示选出 k 个成功位置的组合数} \\
\text{(2) } p^k \text{ 表示这 k 次成功的概率} \\
\text{(3) } (1-p)^{n-k} \text{ 表示剩下 n-k 次失败的概率} \\
E[X] = np, \quad Var(X) = np(1-p) \\
\text{直观理解：期望 = 成功次数平均值，方差 = 成功次数波动大小} \\
\\
\textbf{3\ 泊松分布 Poisson} \\
\\
\text{描述：单位时间或空间内随机事件发生次数的分布，事件独立，平均发生率固定。} \\
X \sim \text{Poisson}(\lambda), \quad \lambda > 0\\
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad k = 0,1,2,\dots\\
E[X] = \lambda, \quad Var(X) = \lambda\\
\text{直观理解：告诉你在固定时间段内事件出现 k 次的概率；泊松分布是二项分布在大 n 小 p 下的极限情况。} \\
\\
\textbf{4\ 正态分布 Normal} \\
\\
\text{描述：连续型随机变量最常见的分布，呈钟形对称，适合自然现象或测量误差。} \\
X \sim N(\mu, \sigma^2), \quad \mu \text{均值}, \sigma^2 \text{方差}\\
f_X(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}\\
E[X] = \mu, \quad Var(X) = \sigma^2\\
\text{标准正态：} Z = \frac{X-\mu}{\sigma} \sim N(0,1)\\
\text{性质：正态分布加法仍为正态，平均值为各均值之和，方差为各方差之和。} \\
\\
\textbf{5\ 指数分布 Exponential} \\
\\
\text{描述：连续型随机变量，描述事件发生的等待时间，短时间内发生概率大，长时间发生概率小。} \\
X \sim \text{Exp}(\lambda), \quad \lambda > 0\\
f_X(x) = \lambda e^{-\lambda x}, \quad x \ge 0\\
E[X] = \frac{1}{\lambda}, \quad Var(X) = \frac{1}{\lambda^2}\\
\text{无记忆性：} P(X > s+t \mid X > s) = P(X > t) \\
\text{直观理解：事件发生时间的延迟越长，概率密度越低，但累计概率随时间增长而增加。} \\
\\
\textbf{6\ 分布总结表} \\
\\
\begin{array}{|c|c|c|c|}
\hline
\text{分布} & \text{PMF/PDF} & E[X] & Var(X) \\
\hline
\text{二项} & \binom{n}{k} p^k (1-p)^{n-k} & np & np(1-p) \\
\text{泊松} & \frac{\lambda^k e^{-\lambda}}{k!} & \lambda & \lambda \\
\text{正态} & \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} & \mu & \sigma^2 \\
\text{指数} & \lambda e^{-\lambda x}, x\ge0 & 1/\lambda & 1/\lambda^2 \\
\hline
\end{array} \\
\\
\text{附加理解：} \\
\text{(1) PMF 与 PDF 区别：离散 vs 连续，概率直接给 vs 积分求概率} \\
\text{(2) 期望：随机变量的长期平均 / 分布重心} \\
\text{(3) 方差：随机变量的离散程度 / 波动大小} \\
\text{(4) 指数分布等待时间：短等待概率大，长等待概率小；累计概率随时间增加而升高} \\
\text{(5) 二项分布公式 \(\binom{n}{k}p^k(1-p)^{n-k}\) 分解理解：组合数 × 成功概率 × 失败概率} \\
$$

#### 期望、方差、协方差、相关系数

$$
\textbf{1\ 期望（Expectation）} \\
\\
\text{期望是随机变量的平均值或数学期望，描述随机变量的中心位置。} \\
\\
\text{离散型随机变量 } X: E[X] = \sum_i x_i P(X = x_i) \\
\text{连续型随机变量 } X: E[X] = \int_{-\infty}^{\infty} x f_X(x) dx \\
\\
\text{性质：} \\
E[aX + b] = a E[X] + b, \quad E[X + Y] = E[X] + E[Y] \\
\\
\textbf{2\ 方差（Variance）} \\
\\
\text{方差描述随机变量的离散程度或波动性。} \\
Var(X) = E[(X - E[X])^2] \\
\text{计算公式：} Var(X) = E[X^2] - (E[X])^2 \\
\\
\text{性质：} \\
Var(aX + b) = a^2 Var(X), \quad Var(X + Y) = Var(X) + Var(Y) + 2 Cov(X,Y) \\
\\
\textbf{3\ 协方差（Covariance）} \\
\\
\text{协方差描述两个随机变量的线性关系方向和程度。} \\
Cov(X,Y) = E[(X - E[X])(Y - E[Y])] \\
\text{性质：} \\
Cov(X,X) = Var(X), \quad Cov(X,Y) = Cov(Y,X), \quad Cov(aX+b, cY+d) = ac \, Cov(X,Y) \\
\\
\textbf{4\ 相关系数（Correlation Coefficient）} \\
\\
\text{相关系数衡量两个随机变量线性关系强弱，取值范围 } [-1,1]。 \\
\rho_{XY} = \frac{Cov(X,Y)}{\sqrt{Var(X) Var(Y)}} \\
\\
\text{性质：} \\
\rho_{XY} = 1 \ (\text{完全正相关}), \quad \rho_{XY} = -1 \ (\text{完全负相关}) \\
\rho_{XY} = 0 \ (\text{不存在线性相关}) \\
\\
\textbf{5\ 常用公式总结} \\
\\
E[aX + bY] = a E[X] + b E[Y] \\
Var(aX + bY) = a^2 Var(X) + b^2 Var(Y) + 2ab Cov(X,Y) \\
Cov(aX + b, cY + d) = ac Cov(X,Y) \\
\rho_{XY} = \frac{Cov(X,Y)}{\sigma_X \sigma_Y}, \quad \sigma_X = \sqrt{Var(X)}, \sigma_Y = \sqrt{Var(Y)} \\
$$

#### 大数定律与中心极限定理

$$
\textbf{1\ 大数定律（Law of Large Numbers, LLN）} \\
\\
\text{大数定律描述独立同分布随机变量的样本平均数收敛于期望。} \\
在大量重复实验中，随机现象的平均结果会趋近于它的期望 \\
\\
\text{设 } X_1, X_2, \dots, X_n \text{为独立同分布（i.i.d）随机变量，期望 } E[X_i] = \mu \\
\text{样本平均数：} \bar{X}_n = \frac{1}{n} \sum_{i=1}^{n} X_i \\
\\
\text{弱大数定律（收敛于概率）：} \\
\bar{X}_n \xrightarrow{P} \mu, \quad n \to \infty \\
\text{即对任意 } \epsilon > 0, \quad \lim_{n\to\infty} P(|\bar{X}_n - \mu| > \epsilon) = 0 \\
\\
\text{强大数定律（几乎处处收敛）：} \\
\bar{X}_n \xrightarrow{a.s.} \mu, \quad n \to \infty \\
\\
\textbf{2\ 中心极限定理（Central Limit Theorem, CLT）} \\
\\
\text{中心极限定理描述独立同分布随机变量和的标准化极限分布为正态分布。} \\
\\
\text{设 } X_1, X_2, \dots, X_n \text{为 i.i.d 随机变量，期望 } E[X_i] = \mu, Var(X_i) = \sigma^2 \\
S_n = \sum_{i=1}^{n} X_i \\
\text{标准化和：} Z_n = \frac{S_n - n \mu}{\sigma \sqrt{n}} \\
\\
\text{则当 } n \to \infty: \quad Z_n \xrightarrow{d} N(0,1) \\
\text{即 } \lim_{n\to\infty} P(a \le Z_n \le b) = \int_a^b \frac{1}{\sqrt{2\pi}} e^{-x^2/2} dx \\
\\
\text{说明：CLT 是大数定律的补充，描述样本平均数的波动分布趋近正态分布。} \\
\\
\textbf{3\ 应用与公式总结} \\
\\
\text{样本平均的近似分布：} \bar{X}_n \approx N(\mu, \sigma^2/n), \quad n \text{大} \\
\text{二项分布近似正态：} B(n,p) \approx N(np, np(1-p)), \quad n \text{大} \\
\text{泊松分布近似正态：} Poisson(\lambda) \approx N(\lambda, \lambda), \quad \lambda \text{大} \\
$$

独立同分布: 独立即离散值 如抛硬币  同分布即每次实验遵循相同的概率分布

#### 参数估计、假设检验、置信区间

$$
\textbf{1\ 参数估计（Parameter Estimation）} \\
\\
\text{参数估计用于根据样本数据估计总体分布的未知参数（如均值、方差）。} \\
\\
\text{1.1 点估计（Point Estimation）：} \\
\text{使用样本统计量作为总体参数的估计值。} \\
\text{例：样本均值 } \bar{X} = \frac{1}{n} \sum_{i=1}^n X_i \text{估计总体均值 } \mu \\
\text{样本方差 } S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i - \bar{X})^2 \text{估计总体方差 } \sigma^2 \\
\\
\text{1.2 区间估计（Interval Estimation）/置信区间：} \\
\text{为未知参数提供一个区间，使其以一定置信水平包含真实值。} \\
\text{例：总体均值 } \mu \text{置信区间（已知 } \sigma \text{）:} \\
\bar{X} \pm z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \\
\text{若 } \sigma \text{未知，用样本标准差 } S \text{替代，并使用 t 分布 } t_{\alpha/2,n-1} \\
\\
\textbf{2\ 假设检验（Hypothesis Testing）} \\
\\
\text{假设检验用于判断样本数据是否支持某个总体假设。} \\
\\
\text{2.1 原假设与备择假设：} \\
H_0: \text{原假设（如 } \mu = \mu_0\text{）} \\
H_1: \text{备择假设（如 } \mu \neq \mu_0 \text{）} \\
\\
\text{2.2 检验统计量（Test Statistic）：} \\
\text{已知 } \sigma: Z = \frac{\bar{X} - \mu_0}{\sigma/\sqrt{n}} \sim N(0,1) \\
\text{未知 } \sigma: t = \frac{\bar{X} - \mu_0}{S/\sqrt{n}} \sim t(n-1) \\
\\
\text{2.3 拒绝域与显著性水平：} \\
\text{设显著性水平 } \alpha \text{，根据 } Z \text{或 } t \text{值判断是否拒绝 } H_0 \\
\text{双侧检验：拒绝 } H_0 \text{当 } |Z| > z_{\alpha/2} \text{或 } |t| > t_{\alpha/2,n-1} \\
\\
\textbf{3\ 置信区间（Confidence Interval, CI）} \\
\\
\text{置信区间给出参数的可能取值范围，置信水平为 } 1-\alpha \\
\\
\text{3.1 总体均值（已知 } \sigma \text{）：} \\
CI = \bar{X} \pm z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \\
\\
\text{3.2 总体均值（未知 } \sigma \text{）：} \\
CI = \bar{X} \pm t_{\alpha/2,n-1} \frac{S}{\sqrt{n}} \\
\\
\text{3.3 总体比例 } p \text{置信区间：} \\
CI = \hat{p} \pm z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} \\
\\
\text{说明：置信区间与假设检验密切相关，置信区间包含 } \mu_0 \text{时 } H_0 \text{不被拒绝} \\
$$

**假设检验理解:**\
假设检验的法庭比喻\
假设检验就像审判案件，我们用样本数据作为“证据”，来判断零假设 H0H0​（被告无罪）是否应该被拒绝。

| 法庭概念     | 统计概念                 | 解释                    |
| -------- | -------------------- | --------------------- |
| 被告无罪     | H0H0​ 为真（无效应）        | 默认情况：没有效应或差异          |
| 检察官提出指控  | H1H1​（有效应）           | 我们怀疑有差异，想证明 H0H0​ 是假的 |
| 证据足够就判有罪 | 拒绝 H0H0​             | 数据显示效应显著，我们认为零假设不成立   |
| 证据不足维持无罪 | 不拒绝 H0H0​            | 数据没有提供足够证据反对零假设       |
| 错判无罪     | 第二类错误（Type II error） | H1H1​ 真，但我们没有拒绝 H0H0​ |
| 错判有罪     | 第一类错误（Type I error）  | H0H0​ 真，但我们错误地拒绝了它    |

***

直观理解

1. **零假设 H0H0​** 是“默认立场”，比如“药物无效”或“被告无罪”。
2. **备择假设 H1H1​** 是我们怀疑的情况，比如“药物有效”或“被告有罪”。
3. 根据样本数据判断证据是否足够：
   * **足够** → 拒绝 H0H0​（认定有效应/有罪）
   * **不足** → 不拒绝 H0H0​（无法确定）
4. **错误的可能性**：
   * 第一类错误：误判无效为有效（拒绝真实的 H0H0​）
   * 第二类错误：误判有效为无效（未拒绝假的 H0H0​）

> 核心区别：不拒绝 H0H0​ 并不意味着 H0H0​ 一定为真，只是证据不足。



