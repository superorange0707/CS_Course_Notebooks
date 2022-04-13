# Fuzzy logic and system笔记



## Lecture2

### 1.1 character function

characteristic function: for a given set A, this function assigns a value μA(x) to every x ∈ X, such that  

*μA(x) = 1 iff x ∈ A μA(x) = 0 iff x ∈/ A*



### 1.2 Membership function(隶属度函数)

**分段函数**：完全符合则为1， 完全不符合为0，中间的部分使用**程度**表示，



### 1.3 Notation

#### 1.3.1 Discrete sets(离散集)

A=μ1/x1 +μ2/x2 +μ3/x3 +...+μn/xn



#### 1.3.2 Continuous sets

$$
A =
\int_{x∈X}μ_A(x)/x
$$



### 1.4 *α*-cuts

An *α*-cut of a fuzzy set *A* is a crisp set:


$$
A_a
$$


 ***α*-cuts**:

*A**α* = *{**x* *∈* *X**|**µ**A*(*x*) ***≥*** *α**}*



**strong *α*-cuts**:

*A**α*+ = *{**x* *∈* *X**|**µ**A*(*x*) ***>** α**}*



### 1.5 Support

**defination:** the crisp set of elements where the membership is greater than **0**



### 1.6 Normality

A fuzzy set is normalised if at least one of its elements attains the maximum possible grade if membership grades are in [0*,* 1],

it is normalised when at least one element has height 1.

**归一化：至少有一个元素达到了1，且其他元素都处于[0,1]之间**



### 1.7 Convexity(凸性)：（平滑曲线，先升后降）

μA(λr +(1−λ)s)≥min[μA(r),μA(s)]

 ∀r , s ∈ X and ∀λ ∈ [0, 1]

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318153955542.png" alt="image-20220318153955542" style="zoom:50%;" />





### 1.8 Complement:相反的

$$
µ_ \overline{A} = 1 -µ_A(x)
$$

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318153920231.png" alt="image-20220318153920231" style="zoom:50%;" />



### 1.9  Intersection： A And B: 取A和B中逐个对应，数值小的那个组成新的集合

The fuzzy intersection (AND), A ∩ B of two fuzzy sets A and B, is usually given by μA∩B = min(μA(x), μB(x)).

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318154710537.png" alt="image-20220318154710537" style="zoom:50%;" />



### 1.10 UNION       A OR B: 取A和B中逐个对应，数值大的那个组成新的集合

The fuzzy union (OR), A ∪ B of two fuzzy sets A and B, is usually given by μA∪B = max(μA(x),μB(x)).

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318154726541.png" alt="image-20220318154726541" style="zoom:50%;" />



<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318154916238.png" alt="image-20220318154916238" style="zoom:50%;" />



### 1.11  complement *c*

**A complement c is a function which converts a fuzzy set, A, to another set, A** 

**满足一下四个条件**

#### 1.11.1 Boundary condition（有边界，c(0) = 1 and c(1) = 0）



#### 1.11.2 Monotonic non-increasing （单调不递增）



#### 1.11.3 Continuity（连续的）



#### 1.11.4 Involution（对合的，  c(c(a)) = a, ∀a ∈ [0, 1], 即转两次后依旧是原来的值，对称的）



### 1.12   triangular norms or t-norms



#### 1.12.1 Intersection norms

**A t-norm is a function which takes two arguments in [0*,* 1] and returns a value in [0*,* 1].** 

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318162119216.png" alt="image-20220318162119216" style="zoom:50%;" />



**必须** **满足以下公理 **：   **(1)有边界  （2）可交换  (3)单调性  （4）联想性（可以交叉运算）**

公理 i1: ***i*(1*,* 1) = 1*,* *i*(0*,* 1) = *i*(1*,* 0) = *i*(0*,* 0) = 0** must behave like crisp sets **(boundary conditions)**

公理 i2: ***i(a, b) = i(b,a)*** (**commutative**)

公理i3:***if a* *≤* *a'* *and b* *≤* *b*'*,* *then i*(*a,* *b*) *≤* *i*(*a*',b')**  **(单调性)**

公理i4: ***i*(*i*(*a,* *b*)*,* *c*) = *i*(*a,* *i*(*b*, *c*))** (**associative**)



**可能需要满足以下公理：（1）连续  （2）幂等： i(a,a) = a **



##### 1.12.1.1 Common t-conorms（Intersection）

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318165858125.png" alt="image-20220318165858125" style="zoom: 33%;" />



#### 1.12.2 Union axioms

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318170159053.png" alt="image-20220318170159053" style="zoom: 33%;" />



**必须** **满足以下公理 **：   **(1)有边界  （2）可交换  (3)单调性  （4）联想性（可以交叉运算）**

公理 u1:  ***u(0,0)=0, u(0,1)=u(1,0)=u(1,1)=1*** must behave like crisp sets **(boundary conditions)**

公理 u2: ***u(a, b) = u(b,a)*** (**commutative**)

公理 u3:***if a* *≤* *a'* *and b* *≤* *b*'*,* *then u(*a,* *b*) *≤* *u*(*a*',b')**  **(单调性)**

公理 u4: **u*(*u*(*a,* *b*)*,* *c*) = *u*(*a,* *u*(*b*, *c*))** (**associative**)



**可能需要满足以下公理：（1）连续  （2）幂等： u(a,a) = a **



##### 1.12.2.1 Common t-conorms（Union）

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318170451254.png" alt="image-20220318170451254" style="zoom: 33%;" />





## Lecture3

#### **1.** **语言变量**(linguistic variable)

x:语言变量的名称(如高度) 

 

T (X):一组术语(例如，矮、中、高)，即 X 的语言值 X 的集合 

 

u:给出基本变量 X 的取值范围的论域(域) 

 

g:用于生成术语(例如，非常高，非常高，...)，X，in T (X ) 

 

M:与 T (X)中的每个语言术语 X 相关联的语义规则 ，M(X)，它表示一个模糊集

 

 

#### **2. hedge****（限制语：类似形容词）**

比如：非常，稍微

 

 

#### **3. concentrate****（集中）**

对隶属度函数求平方，使其函数曲线更集中于



#### 4.Terms

术语的数量和形状可能取决于应用

**Alternative Term**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318180650854.png" alt="image-20220318180650854" style="zoom:50%;" />



### 5.Triangular membership functions（三角隶属度函数）

**Three parameters (left, centre, right)**



### 6.Trapezoidal membership functions（梯形隶属度函数）

**Three parameters (left, centre, right) for ‘shoulder’（梯形的肩膀有三个参数）**

**Four parameters for trapezoid (lb, lt, rt, rb)（梯形有四个参数）**



### 7.Gaussian membership functions（高斯隶属度函数）

**Two parameters (standard deviation, centre)（标准偏差，中心））**



### 8.Sigmoid membership functions（S型函数）

**Two parameters (slope, half–point)（斜率、半点））**



### 9. Guildline of Lingustic variable

**（1）the terms should span the universe of discourse**

**（2）the terms should not overlap too much**

**（3）terms should normally overlap at around 0.5 membership**

**（4）the number of terms should be small (*≤* 7)**

**（5）all terms are normal**

**（6）all terms are convex**

**（7）usually odd number of terms**

### 10. Linguistic Truth

***X* = Truth**

***U* = [0, 1]**

***T* = true + not true + very true + somewhat true + defifinitely true\+ . . . + false + not false + very false + somewhat false +defifinitely false + . . .**

So, we can now represent and systematise statements such as

**“that’s not very true!”**



### 11. Level Sets

The term **undefifined** can be defifined as 
$$
θ=\int_{0}^{1}{0/V}
$$
The term **unknown** can be defifined as 
$$
θ=\int_{0}^{1}{1/V}
$$


### 12. Extension Principle

**f is a mapping (function) from *U* to *V*** 

***A* = *µ*1*/u*1 + *. . .* + *µn/un***

Then

***f*(*A*) = *f*(*µ*1*/u*1 + *. . .* + *µn/un*) *≡* *µ*1*/*f*(*u*1) + *. . .* + µn*/f*(*un*)**





## Lecture4

### Inferencing Principles

### 1. If-Then Rules (Fuzzy Logic)

### 1.1 Essential operation

**(1) each of the antecedent(s) is evaluated to a number in [0, 1] and combined into a single number - the truth of the rule premise**

**(2)each of the consequent(s) is considered to be true to the same degree as the premise)(每个结果都被认为在与前提相同的程度上是正确的）)**



#### **Example**：

**IF p THEN q**：

**p is true, hence q is true**

**p is half true, hence q is half true**

**p is not true, hence q is not true!**

**p is FALSE, hence q is FALSE**



### 2.Method

#### 2.1 **Comprises a set of rules of the form:**

**IF *x*1 is *A*1 [AND/OR *x*2 is *B*1 . . . ]       THEN *y* is *C*1**



#### 2.2 Rule的要求

**（1）for each antecedent, evaluate the membership degree of the crisp input value in the fuzzy term（对于每个前件，评估模糊项中清晰输入值的隶属度）**

**（2）combine all membership degrees using appropriate fuzzy operator (e.g. min, prod, max)（使用适当的模糊算子（例如 min、prod、max）组合所有隶属度；）;**

**（3）fifire the rule at the strength (combined degree) to obtain the rule output based on the consequent（在强度（组合度）处触发规则以根据结果获得规则输出。）.**



#### 2.3 Aggregate the output of each rule and interpret in some way  (e.g. defuzzify the fuzzy output to a crisp value)（汇总每个规则的输出并以某种方式进行解释（例如，将模糊输出去模糊化为清晰的值）。）.

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318232337755.png" alt="image-20220318232337755" style="zoom:50%;" />



**（1）将输入条件按每个rule（规则）进行输出，并考虑两个条件的用And**

**（2）将所有条件的输出都得到后，合并每个条件的输出， 使用OR。** 

**（3）合并后得到最后的结果。**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318233135978.png" alt="image-20220318233135978" style="zoom:45%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318233156577.png" alt="image-20220318233156577" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318233218284.png" alt="image-20220318233218284" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318233242278.png" alt="image-20220318233242278" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220318233313140.png" alt="image-20220318233313140" style="zoom:50%;" />



### 3. Operator

Mamdani inference features union and intersection operators：

**Intersection:（当rule的条件需要一起考虑时；对单个rule的结果进行推导时）**

（1）intersection combining antecedents joined by **AND;**
（2）implication operator to derive each consequent

**UOION：（当合并所有rule 的结果时；rule的条件中是OR的情况）**

（1）union combining antecedants joined by **OR;** 

（2）also used to combine all consequents overall



## Mamdani

### 2.1Mamdani Defuzzifification（去模糊化）

**去模糊化原因： Mamdani 推理的结果通常为模糊集**

**输出要求：将模糊输出集转换为数字，这个过程称为去模糊化Defuzzication**

**方法：Centroid以及Centre-Of-Gravity**



### 2.1.1 Type of Defuzzification

#### 2.1.1.1 Numeric Defuzzification（数字化去模糊化）

**often, a single (crisp) number is required as output e.g. fuzzy controller; there are many different options (COG (centroid), mean-of-maxima, centre-of-area)**

**（通常，需要一个（清晰的）数字作为输出，例如模糊控制器；有许多不同的选项（COG（质心）、最大值均值、区域中心））**



#### 2.1.1.2**Linguistic defuzzifification（语言去模糊化）**

**a linguistic term representing the output set is found; some form of similarity or distance metric used**

**（找到表示输出集的语言术语；使用某种形式的相似性或距离度量）**



#### 2.1.2Centre of Gravity（**Centroid：**）

**计算方法**：（**不为0的数乘以✖️后面的数并且整个集合结果相加，（出现重复的只计算一次））/（前面的数相加）**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320103510625.png" alt="image-20220320103510625" style="zoom:50%;" />



#### 2.1.3 Mean of Maxima (MOM)

**The mean of the x which attain the maximal membership grade（隶属度函数中达到最高值得那一段的平均值）**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320104101784.png" alt="image-20220320104101784" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320104145149.png" alt="image-20220320104145149" style="zoom:50%;" />



**找到最大值，找到属于最大值的几个量，将这几个量求平均值**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320105605626.png" alt="image-20220320105605626" style="zoom:50%;" />





#### 2.1.4 Smallest/Largest of Maxima

**属于最大值的部分中，最小的量以及最大的量**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320105723903.png" alt="image-20220320105723903" style="zoom:50%;" />



<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320110025035.png" alt="image-20220320110025035" style="zoom:50%;" />







#### 2.1.5Bisector（最好画个图）

**The value of x which splits the total area into two equal subareas usually very similar result to the centroid.（x 的值将总面积分成两个相等的子面积，通常与质心非常相似。）（即分割后的两边的平均值都相似或相等）**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320111511855.png" alt="image-20220320111511855" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320111529315.png" alt="image-20220320111529315" style="zoom:50%;" />



#### 2.1.6 去模糊化的问题

**信息丢失 - 当减少到单个时这是不可避免的数字**



#### 2.1.7 Metrics

***µg***:**Membership grade at defuzzifification point**

**µh:Maximum membership grade(Height)**

**Normalised Area:**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320115637208.png" alt="image-20220320115637208" style="zoom:50%;" />



**Fuzzy Entropy(模糊熵)：**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320115736751.png" alt="image-20220320115736751" style="zoom:50%;" />





#### 2.1.8 Linguistic Approximation

##### 2.1.8.1 **compute the distance：**

（1）the actual output set

（2）the set of all terms of the linguistic variable

Search to fifind the best term while limiting the complexity to produce comprehensible output (e.g. medium or high may be prefered to not extremely low or fairly medium or fairly high)（搜索以找到最佳术语，同时限制产生可理解输出的复杂性（例如，可能更喜欢中或高而不是极低或相当中等或相当高））



##### 2.1.8.2 **Euclidean distance:**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320120816331.png" alt="image-20220320120816331" style="zoom:50%;" />

 ***ηi*:语言术语的隶属等级**

**Minimum distance =*⇒* best match(最小距离即最佳匹配)**



##### 2.1.8.3 **Degree of overlap:**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320132337449.png" alt="image-20220320132337449" style="zoom:50%;" />

**Maximum overlap =*⇒* best match（最大重叠 =*⇒* 最佳匹配）**





## Lecture5

### 1. Zeroth order  inference models

#### 1.1 Rule Type

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320153853389.png" alt="image-20220320153853389" style="zoom:30%;" />

**A, B, . . . are fuzzy sets in the antecedent（A，B为前缀中的模糊集合），ki表示结果的每一个常量**



**Example:**

IF x is A1 AND/OR y is B1 . . . THEN z is *k*1



### 1.2 

### *wi：*The antecedents are evaluated as per Mamdani to find the fifiring strength (truth) of each rule



**权重*wi*：****与每条规则相关的 ki 的加权平均值给出的总输出**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320163307043.png" alt="image-20220320163307043" style="zoom: 25%;" />



### 1.3 TSK处理rule得到结果的过程：

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320164413814.png" alt="image-20220320164413814" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320164443691.png" alt="image-20220320164443691" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320164834163.png" alt="image-20220320164834163" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320164849973.png" alt="image-20220320164849973" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320164917903.png" alt="image-20220320164917903" style="zoom:50%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320164936203.png" alt="image-20220320164936203" style="zoom:50%;" />





### 2 Camparison

**Mamdani vs Sugeno**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320170448911.png" alt="image-20220320170448911" style="zoom:50%;" />





### 3 First order

#### 3.1 the rule format

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220320170849005.png" alt="image-20220320170849005" style="zoom:45%;" />

***pi, qi and ri are constants（变量）***



#### 3.2  TSK VS Mamdani（Advantages）

**TSK Sugeno advantages:**

computationally effificient

works well with linear techniques (e.g. PID control)

works with optimisation & adaptive techniques

has guaranteed continuity of the output surface

well-suited to mathematical analysis

does not require defuzzifification

**计算效率高**

**适用于线性技术（例如 PID 控制）**

**使用优化和自适应技术**

**保证了输出表面的连续性**

**非常适合数学分析**

**不需要去模糊化**



**Mamdani advantages**

**简单直观**
**已被广泛接受**
**非常适合人工输入**





## Lecture6

### 1.Fuzzy Model

#### 1.1 Two process

**(1) Model identification**

**structure identifification**：**(寻找合适的言语变量的数量以及隶属度函数，规则形式等)**

Example:fifinding the number of linguistic variables, fuzzy terms (membership functions), form of rules, etc





**(2) Model tuning(Optimisation)**

**Parameter Tuning（寻找合适的参数以及规则权重、去模糊化的参数）**

fifinding the exact values of the m.f. parameters, rule weights, defuzzifification parameters, etc.



### 1.2 考察模型以及性能的方法

#### 1.2.1 模型的好坏

**（1）objective function（目标函数）**

**（2）cost function（消耗函数）**

**（3）error measure（错误测量）**



#### 1.2.2 性能测试

**（1）maximise objective functions/performance（最大化目标函数/性能）**

**（2）minimise cost functions/error（最小化消耗函数/错误）**



### 1.3 Direct Objective Function

**Example：**

**考虑餐厅消费**

**输入**：餐厅服务与食物质量

**输出**：小费



**目标函数：**

**最大化小费（for waiter）**

**最小化小费（for customer）**





#### 1.4  Cost Function

#### calculate the cost (e.g. root-mean-squared error) based on model outputs





#### 1.5 FIS Structure(股票投资建议)

**Inputs：**

（1）FTSE index – three terms (m.f.s): falling, stable, rising

（2）Exchange-rate – three terms (m.f.s): down, unchanged, up



**Outputs:**

**advice** – three terms: sell, hold, buy



**Rules:**

Three rules

1. If exchange is falling and ftse is up then advice is buy

2. If exchange is rising and ftse is down then advice is sell

3. If exchange is stable or ftse is unchanged then advice is hold



**Indirect Objective function:**

A suitable indirect objective function can be created by using the advice to buy/sell shares

 

**Methods:**

**Exhaustive Search(穷举)**





### 2. The Monte Carlo algorithm

#### **Process:**（创建随机位置，不断寻找最优位置，如果找到的位置比目前最优位置好则替换它。直到完成迭代（设定迭代次数）。可能找不到全局最优）

（1）generate a random starting position

（2）evaluate the starting position and store it as best

（3）repeat

​	generate a new random position

​	evaluate the new position

​	if the new position is better than the best found so far store  the new position as the best

（4）until we decide to stop (e.g. not improved for 20 goes)

This may or may not fifind the global maximum





### 3. The hill climbing algorithm

**Process：**

**（1）从一个固定或者随机点开始迭代**

**（2）每一次迭代：**

**a.评估每一个方向**

**b.向有最好提升的方向去**

**（3）当下一步的所有方向都比当前的点低时，则终止（即无法产生下一个更优解时）**



**Output：**

**保证找到一个最优解，但如果存在多个最优解则不保证其为全局最优解**



### 4. Stochastic Local Search(随机局部搜索)

**局部爬山的性能非常依赖于景观的形状——如果景观有很多局部最大值，找到全局最大值的机会很小**



#### 4.1 结合蒙特卡洛和爬山

##### 过程：

1. **重复:**

   **a.创建新的初始起点**

   **b.爬山搜寻局部最大值**

   **c.存储局部最大值**

2. **直到达到停止条件**

3. **随机搜索**

4. **在附近移动**





### 5. simulated Annealing（退火算法）

**Process:(SA 算法通常被实现为基本爬山算法)**

**1.初始化温度：T**

##### 1.1 所有的操作（爬山或者退火）都能接受

##### 1.2 搜索是随机的



**2.生成随机解： i**

**3.重复：**
**3.1 生成一个新的（附近的）解决方案，j**
**3.2 如果适应度（j）高于适应度（i）然后接受移动**
**3.3如果适应度（j）低于适应度（i）然后接受移动**

**3.4:for 3.2,3.3:根据随着适应度差异的大小而减小并随着温度T而增加的概率**

**3.5: 降低温度，T**

###### 3.5.1只接受上坡动作

###### 3.5.2 搜索是逐渐爬坡接近（局部最优解）



**Notice:**

**可以让算法在每个 T 重复多次，而不是而不是在每一步之后减少 T**

**长度参数 L 指定在每个温度T要重复执行的步骤数**



**4.直到停止标准**





## Lecture7（**ANFIS**）

### **ANFIS：Adaptive Neuro-Fuzzy Inference System**

#### 1. First-order Sugeno fuzzy model

#### **Structure： 2 inputs (2 mfs), 4 rules**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220321205606939.png" alt="image-20220321205606939" style="zoom:50%;" />





#### 2. Layer

##### 2.1 Layer1 : Inputs

**前提参数:例子中输入为两个参数，且每个参数有两种可能**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220321205901696.png" alt="image-20220321205901696" style="zoom:33%;" />

**m.f.s are Gaussians（隶属度函数通常为高斯函数）**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220321211157069.png" alt="image-20220321211157069" style="zoom:33%;" />



##### 2.2  Layer2: rule Firing 规则触发

**T-norm operator combining  the separate antecedents  into single rule firing strength**

**(T-范数算子将单独的前件组合成单个规则触发强度):即  将条件规则的前置条件互相组合从而达到各个规则的触发条件**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323131850134.png" alt="image-20220323131850134" style="zoom:33%;" />



**对于n个输入，有M^n的规则**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323131915080.png" alt="image-20220323131915080" style="zoom:33%;" />





##### 2.3 Layer3: Normalised Firing(中心化触发)

**layer3的输出是对条件触发强度的中心化**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323132218206.png" alt="image-20220323132218206" style="zoom:33%;" />





**2.4 Layer 4 – Rule Consequents**

**Consequent parameters  (towards defuzzification)（后置参数：去模糊化）** 

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323132417927.png" alt="image-20220323132417927" style="zoom:33%;" />



##### 2.5 Layer5-Defuzzification（去模糊化）

**最终清晰的输出：对每个归一化的求和规则输出**

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323132646354.png" alt="image-20220323132646354" style="zoom:33%;" />





### 3.ANFIS – Zeroth Order

##### 3.1 Zeroth-order Sugeno fuzzy model

**Structure：** 2 inputs (2 mfs), 4 rules

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323134810858.png" alt="image-20220323134810858" style="zoom:33%;" />

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220323134827720.png" alt="image-20220323134827720" style="zoom:33%;" />



**Parameters**：

**Two sets:S1,S2**

**S1:**

1.定义输入的隶属度函数

2.非线性

3.在反向传播中（错误的反向传播)通过使用梯度下降调整算法进行修改



**S2**

1.定义结果函数的参数

2. 线性
3. 在前向传播算法通过使用迭代最小二乘估计进行修改



##### 3.3 ANFIS Learning

##### 3.3.1 Two passes（混合学习步骤的两种方法）

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220412193427063.png" alt="image-20220412193427063" style="zoom:33%;" />



**1.Forward Pass**

###### 1.1 LSE

a. goal:minimise the squared error(最小化方差)

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220412193639144.png" alt="image-20220412193639144" style="zoom:25%;" />

1.A 是第 3 层产生的输出矩阵

2.B 是目标输出的矩阵

3.X 是结果参数的矩阵



b.顺序（迭代）估计算法来估计 X，基本上按照卡尔曼滤波器





**2.Backward Pass**

**2.1 Back Propagation**

a.overall error measure

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220412201132102.png" alt="image-20220412201132102" style="zoom:25%;" />

 *Y**p* are actual outputs and *T**p* are targets



b.

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220412201424570.png" alt="image-20220412201424570" style="zoom:25%;" />

*h*为学习速率，它的表达式为：

<img src="/Users/a13912721110/Library/Application Support/typora-user-images/image-20220413163742690.png" alt="image-20220413163742690" style="zoom:25%;" />



