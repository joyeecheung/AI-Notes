#CH2 Intelligent Agents

##Agents and Environments

###Agent
Anything that:

* perceiving its **environment** through **sensors**
* acting upon that environment through **acuators**

###Percept
The agent's perceptual inputs at any given instant.

###Perspect sequence
The complete history of **everything** the agent has ever perceived.

###Dependence on percept
An agent's choice of action at any given instant can depend on the entire percept sequence observed to date, but **not** on anything it hasn't perceived.

###How to specify the agent's behavior
* Specify the agent's choice of action for every possible percept sequence
* Described by the **agent function** that maps any given percept sequence to action

###Agent function and agent program
* The agent function for an AI is **implemented** by an agent program
* The agent function is an **abstract methematical description**
* The agent program is a concrete implementation, running within some physical system

##Good Behavior: The Concept of Rationality

###Rational agent
For **each possible percept sequence**, a rational agent select an action that is expected to **maximize its performance measure**, given the evidence provided by the percept sequence and whatever built-in knowledge the agent has.

####Performance measure
Evaluates any given sequence of **environment states** and determine if the chosen sequence of actions is **desirable**.

It's **environment states**, not **agent states** -- you can't define your own success.

####Design principle of performance measure
It's better to design permorance according to **what one really wants** in the environment, rather than according to how one thinks the agent **should behave**.

###Rationality
Four factors:

* The **performance measure** that defines the criterion of success
* The agent's **prior knowledge** of the environment
* The **actions** that the agent can perform
* The agent's **percept sequence** to date

###Omnisience
* Knowing the **actual outcome** of its actions and can  act accordingly.
* Impossible -- you can't see the future.
* Rationality != perfection -- Raionality maximize the **expected outcome**, perfection maximize the **actual outcome**
* Rationality depends on the percept sequence **to date**

####Information gathering
* Doing actions in order to modify future percepts e.g. **exploration**
* R.A. gathers information

###Learning
* R.A. learns as much as possible from what it perceives

####a priori
Extreme cases: the environment is completely known

###Autonomy
* The more an agent **relies on the prior knowledge** of its designer rather than its own percepts, the more the agent **lacks autonomy**
* R.A. is autonomous: it learns what it can to compensate for **partial or incorrect** prior knowledge
* After sufficient experience of its environment, the behavior of a R.A can become effectively **independent of its prior knowledge**

##The Nature of environments
###Task environment
Essentially the problems to which rational agents are the solutions.

###Specifying the task environment: PEAS
####Performance measure
What is desired?
####Environment
What will the agent face?
####Acutuators
How can the agent act?
####Sensors
How can the agent perceive?

####Real environment v.s. artificial environment
环境是否真实并不是最重要的，关键在于

* 各个agent的**行为间关系**的复杂度是否足够
* 环境能够生成的**percept sequence**是否足够
* **performance measure**是否合理

###Properties of task environments
####Fully observable v.s. partially observable
* 环境的全貌是否可见？
* **Fully observable** 
	* 传感器能够探测到影响决策的**所有因素**
	* agent不需要在内部（以其他结构）维护世界的状态，因为世界的状态是可以随时通过直接观察得知的。
* **unobservable**
	* agent连传感器都没有

####Single agent v.s. multiagent
* 什么东西可以算作agent
	* 一个agent的行为应当**根据另一个agent的行为最大化自己的performance measure**
* 分类
	* Competitive multiagent environment
		* e.g. 下棋
	* Cooperative multiagent environment
		* e.g. 出租车驾驶
* 可能出现的特殊Rational behavior
	*  **Communications**
	*  **Randomized** behavior

####Deterministic v.s. stochastic
* 是否存在不确定性（uncertainty）？
* 是否能够通过当前状态+agent的行为唯一确定环境会产生什么变化？
	* 其他agent的行为不算作不确定性，因为可以推出
* **uncertain**: not fully observable || not dterministic
* **stochastic**
	* uncertain
	* 有概率的不确定性
* **nonedterministic**
	* characterized by **possible outcomes**
	* 没有可知概率的不确定性
	* performance measure would require the agent to success for **all possible outcomes**

####Episodic v.s. sequential
* 短期行为是否会影响长期环境（所以在决策时需要think ahead）？

####Static v.s. dynamic
* 环境是否会自己改变 -- 随着时间自动改变，无论agent的行为如何？
* **dynamic**
	* e.g. 出租车驾驶
* **semidynamic**
	* 环境不会随着时间改变，但agent的performance score会影响环境
	* e.g.下棋
* **static**
	* e.g. 字谜

####Discrete v.s. continuous
* state/time/percepts/actions
* discrete
	* e.g. 下棋
* continuous
	* e.g. 出租车驾驶

####Known v.s. unknown
* 是否已知每种行为会带来什么后果or不同后果各自的概率？（相关物理法则是否已知？）
* known和observable并没有必然联系
	* known environment可以是partially observable的
		* e.g. 卡牌游戏，知道规则但不知道对手手里的牌
	* unknown environment可以是fully observable的
		* e.g. 电子游戏，屏幕上可以看到世界全景但不知道每个按钮按了会有什么后果

##The Structure of agents

* **agent = architecture + program**
	* architecture: physical devices
	* program: implements the agent function

###Agent programs

###Simple reflex agents

###Model-based reflex agents

###Goal-based agents

###Utility-based agents

###Learing agents

###How the components of agent programs work