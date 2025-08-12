assuming you already find a,b.. i 

Assuming independence: 

$$
P(X=x_{i}, y=y_{i}) = P(X)P(Y)
$$
or 

We know the cond probability 

x = 1 given y=10 is 0.5

does not equal 

P(x=1)=G

Not independent 

Compute the mean is easy after doing part 1

$$
P(x=1)=G
$$
$$
P(x=1)=0.2
$$
$$
P(x=3)= I
$$
$$
\mu_{x}+E(x) = \sum x_{i} P(x=x_{i})
$$
$$
=1 \cdot P(x=1) + 2 \cdot p(x=2)
$$
$$
= ? + 3\cdot P(x=3)
$$
$$
E(x^{2}) = \dots
$$
The variance of x
$$
\sigma_{x}^{2} = E(x^{2}) - \mu_{x}^{2} = ?
$$

$$
E(x | y = 6)
$$
$$
= \sum x_{i}: P(x=x_{i} |y =0)
$$
$$
= 1 \cdot P(x=1|y=6) + 2 \cdot P(x = 2 |y=6) + 3 \cdot P(x=3|y=6)
$$
$$
=?
$$
$$
E(x | y = 6)
$$
$$
E(x |y = 8) 
$$
$$
E(x|y=10)
$$
if these three are the same, then x is mean independent of y

part d: 
if it is mean independence, then the covariance is 0

$$
Cov(x,y) = \sum x_{i} y_{j}
$$

Problem 2:


Define
$$
 x_{i} =\begin{cases}
1 & \text{ if the i'th mussel is good} \\
0 & \text{ if not}
\end{cases}
$$
$$
x_{i} \approx Bernoulli (P)
$$
where 
$$
P=P(X=1) = 0.9
$$
$$
\sum X_{i}  = \text{ The number of good nussels in a sample }
$$

$$
P\left( \sum X_{i} < 6  \right)
$$
$$
= P\left(\frac{ \sum x_{i}-60\cdot P}{\sqrt{ 60 \cdot p\cdot (1-p) }}<\frac{ 6 - 60\cdot p}{\sqrt{ 60 \cdot p \cdot(1-p) }} \right)
$$
$$
\approx P\left( Z<\frac{ 6-60 \cdot p}{\sqrt{ 60 \cdot P(1-P) }} \right)
$$
see photo on phone

Problem #3

N children in small town. 

Define buronelli variable x for cavities or no cavities

$$
i = 1, \dots n
$$

$$
x_{i} \approx^{iid} Bernoulli(P)
$$
when $P=P(X=1)$
Then, 
$n_{1} = \sum(x_{i})$
This is the total number of children with cavities in a sample of size n. 

A: 
is the sample average unbiased?
$$
\frac{n_{1}}{n} = \frac{1}{n} \sum x_{i}
$$
Apply large number thing

$$
E\left( \frac{n_{1}}{n} \right) = E\left( \frac{1}{n} \sum ^{n}_{i=1} x_{i} \right) = P
$$
Not biased 


ask kyle for picture

B: assume total population 200

Sample size 80

Population size is 150/200

true p 
$$
p=\frac{150}{200}
$$
Find probability that more then 55 children have cavities in samp size of 80

$$
P\left( \sum ^{80}_{i=1} x_{i} > 55 \right)
$$
$$
= P\left( \frac{\sum ^{80} x_{i} - 80 \cdot p}{\sqrt{ 80 \cdot p \cdot (1-p) }} > \frac{55-80\cdot P}{\sqrt{ 80\cdot P() }} \right)
$$
See kyle picture 

C: find 90% confidence interval

B and c are not related. We do not know the true proportion, only sample estimate

$$
\left( \hat{P} - Z_{\frac{\alpha}{2}} \cdot \sqrt{ \frac{\hat{p}(1-\hat{p})}{n} } \right)
$$
Where n is 80
$$
\hat{p} + z_{\frac{\alpha}{2}} \cdot \sqrt{ \left( \frac{\hat{p}(1-\hat{p})}{n} \right) }
$$
D :

$$
p=0.75 \ vs \ H_{1} = P \neq 0.75
$$
Under $H_{0}$

$$
z = \frac{\hat{p}-p}{\sqrt{ \hat{p}_{1}-\hat{p} }}
$$
follows approximately standard normal 
$$
N(0,1)
$$
$$
z_{act} = \hat{p}_\text{actual} - p .. 
$$
Problem 3 Revisited:

N is total population of children
n is the sample size (small n)

$n_{1}$ is the number of children that had cavities in the sample size of n students. 

Population proportion is $\propto$ to population mean?

Define 
$$
x = \begin{cases}
 1 & \text{ if child has cavities} \\
0 & \text{otherwise }
\end{cases}
$$
x is a Bernoulli variable with proportion p

p is the proportion of children that have cavities, or the probability that a child has a cavity

Now: 
$$
\sum ^{n}_{i=1} x_{i} = n_{1}
$$

**The mean of the burnoulli random var is equal to P**
**Variance of the bernoulli random variable P(1-P)**

By wigglos large number:

$$
\frac{n_{1}}{n}= \frac{1}{n}\sum ^{n}_{i=1} x_{i} \to p \text{ as } n \to \infty
$$


Unbiased!
as long as $\frac{n_{1}}{n}$ is a sample average by wigglos large number, then it is unbiased

B:
The true proportion is given by $\frac{150}{200} =0.75$
Find the probability that the sample has more then 55 children with cavities

$$
P\left( \sum x_{i} > 55 \right)
$$
Standardize $x_{i}$ by dividing mean by standard deviation 

mean is given by
$$
E\left( \sum ^{80} x_{i} \right) = 80 * p = 80 * 0.75
$$
Variance
$$
Var\left( \sum ^{80} x_{i} \right) = n-p(1-p)
$$
$$
= 80*0.75 (0.25)
$$
=b?


central limit theorem, the lhs of picture follows it

Part C: You dont need the 200

Sample average is $\hat{p} = \frac{n_{1}}{n}$ 

$$
\hat{p} - z_{\frac{\alpha}{2}} \cdot \sqrt{ \frac{\hat{p}(1-\hat{p})}{n} } ,  \ \hat{p} + z_{\frac{\alpha}{2}} \sqrt{ \frac{\hat{p}(1-\hat{p})}{2} }
$$
