---
title: 《CPS》
tags:
	- Reading
	- Experience
	- Story
categories:
	- Read
date: 2017-12-21 16:04:01
---

{% blockquote —— 《论语·子路》%}
子曰：“君子和而不同，小人同而不和。”
{% endblockquote %}

<!-- more -->

## 插图
{% img /gallery/book/0016-cpsXiaYiDaiAI.png 300 CPS %}
<p align="center"><b>CPS</b></p>

-----

# 《CPS：新一代人工智能》

Cyber—PhysicalSystem（CPS）,是美国科学基金会（NSF）在 2006 年提出的新技术方向(Initiative)，并将此项技术体系作为新一代技术革命的突破点。同时，德国的“工业 4.0”战略也将 Cyber-Physical Production System(CPPS) (信息-物理生产系统)作为核心技术，实质是 CPS 在生产系统中的应用体系。无论是德国工业 4.0 战略还是美国 CPS 计划，都将 CPS 作为实施的核心技术，并据此设定各自的战略转型目标，那么究竟 CPS 是什么？今晚我将从工业界的需求角度、技术内涵、应用体系三个方面为大家解释 CPS 的定义。

从生产力发展的需求来看CPS的根本目标

前三次工业革命发展的过程给我们的启示是，每一次科技革命的根本原因在于原有技术体系下的生产要素已经无法满足生产力的发展要求，在这种需求的推动下，新的使能技术的诞生帮助人们突破了限制生产力发展的瓶颈，同时伴随着新的基础设施的发展使新技术的红利得以快速普及。遵循这个规律，我们可以对前三次工业革命进行如下的总结：

而在第四次科技革命中，我们认为需要解决的生产力瓶颈在于技术要素的不可见部分，即人的知识产生和利用效率已经不能满足生产系统的要求，依靠人的知识和经验去驱动生产系统已经达到了生产力的边界，难以使其以最优的效率运行和协同。受人的经验和知识的限制，以人的决策为驱动生产系统中有很大一部分的价值并没有被释放出来。这主要体现在对知识获取的速度、能力的深度、应用的规模化三个方面的瓶颈。因此，如果 CPS 能够成为新工业革命的使能技术，它将必须实现以下两个目标：

1) 提升知识作为核心生产要素的生产力边界，使知识的产生、利用、和传承过程中的效率化和规模化，从而获得本质的提升。

2) 重新优化生产组织要素的价值链关系，使得整个产业链中的各个环节围绕最终用户的价值以高效的协同方式为其提供服务。

以知识为核心使生产要素发挥最大的能力，归根结底是在精确的状态评估 的前提下，对管理和控制活动进行实时的决策优化 ，并协同和调度相关的活动参与者高效率执行的过程。

其中的三个关键词分别是“状态评估”、“决策优化” 、和“协同执行” ，也是实现上述能力中最大的挑战：

1）状态评估，要了解活动相关的个体和环境的实时状态，其中许多状态是不可测量的，需要利用建模的手段从可测的相关参数中进行预测，更重要的是还要对个体之间的相互影响关系进行精确的评估和预测；

2）决策优化，要在对状态的精确掌握的基础上，对各种可能的决策所带来的影响进行精确的分析推演，并在多目标并存的环境下充分考虑之间的trade-off，实现整体目标价值的最大化；

3）协同执行的过程，则要考虑决策的分发与实施的层级关系、时间尺度、和顺序相关性，并且要有一定的容错能力。

## CPS的狭义与广义技术内涵

2006年美国国家科学基金会（NSF）举办了第一届 CPS 研讨会，会议中对 CPS 的定义第一次进行了阐述：CPS 是网络环境（Cyber Space）中的通信（Communication）、计算(Computation)、和控制(Control)与实体系统在所有尺度内的深度融合。这个定义给出了 CPS 的三个基本元素，也就是我们最常提到的 3C 技术要素。NSF 从功能性的角度阐述了 CPS 的内涵，即实体系统里 面的物理规律以信息的方式来表达。我们的这本书从更加广义的角度赋予了 CPS 新的内涵：对实体系统内变化性、相关性、和参考性规律的建模 、预测 、优化 、和管理。

除了功能层面的‘3C’要素，CPS 的广义定义还需要从另外的 3 个C 与 3 个 R 的角度去理解：

CPS 对实体系统分析和预测的目的和手段可以概括为“3C” ：

- Comparison（比较性）：从比较过程中获取洞察，既包括比较相似性，也包括比较差异性。比较的维度既可以是在时间维度上与自身状态的比较，也可以是在集群维度上与其他个体的比较。这种比较分析能够帮助我们将庞大的个体信息进行分类，为接下来寻找相似中的普适性规律和差异中的因果关系奠定基础。

- Correlation (相关性)：如果说物联网是可见世界的连接，那么所连接对象之间的相关性就是不可见世界的连接。对相关性的挖掘是形成记忆和知识的基础，简单的将信息存储下来并不能称之为记忆，通过信息之间的关联性对信息进行管理和启发式的联想才是记忆的本质。相关性同时也促进了人脑在管理和调用信息的效率，我们在回想起一个画面或是情节的时候，往往并不是去回忆每一个细节，而是有一个如线头一样的线索，你去牵它一下就能够引出整个场景。这样的类似记忆式的信息管理方式运用在工业智能中，就是一种更加灵活高效的数据管理方式。

- Consequence (因果性)：数据分析的重要目的是进行决策支持，在制定一个特定的决策时，其所带来的结果和影响应该被同等地分析和预测。这是以往的控制系统所不具备的特性，也是智能化的本质。工业系统中的大部分活动都具有很强的目的性，就是把目标精度最大化，把破坏度最小化的“结果管理”。结果管理的基础是预测，例如在现在的制造系统中，如果我们可以预测到设备的衰退对质量的影响，以及对下一个工序质量的影响，就可以在制造过程中对质量风险进行补偿和管理，制造系统的弹性和坚韧性就会增加。

这 3 个 C 分别对应了实体空间中的对象、环境、与任务的运转基础，又可以用 3 个R 来概括：

- Resource（来源）：数据来源可以从历史的数据、传感器的数据、或是人的经验数据，这些数据都可以用一种逻辑的方式形成一种知识模型。同时，Resource也是比较性的基础。

- Relationship（ 关系）：基于比较和相关性的分析，挖掘显性和隐性的关系。例如，半导体的过程监测中有上百个传感器数据，但是从历史报警的信息，可以利用贝叶斯网络建立传感器的关系图谱，最后上百个传感器与5个传感器有强相关性，只用这 5 个传感器的组合就可以管理所以传感器数据所代表的状态。又比如，在了解发动机运行过程中气压和空气密度与燃烧温度和转速之间的关系后，GE 航空的发动机通过建模优化能够降低 1%的燃油效率。

- Reference （参 考 ）：参考性有两个方面，一个是比较的参考，另一个是执行的参考。也分为主动的参考和被动的参考，同时，参考也是记忆的基础。如果是以结果作为参考，那么目的就是去定义其发生的根原因；如果是以过程作为参考，那么目的就是去寻找避免问题的途径。古语有云：“以铜为鉴,可以正衣冠;以古为鉴,可以知兴替;以人为鉴,可以明得失” ，这句话充满了深刻的哲理，也总结了参考性的三个维度，即以传感器（铜）所反映的自身状态为参考、以历史数据中的相关性和因果性为参考，还有以集群中的其他个体作为参考。

CPS 的技术基础包括物联网、普适计算、和执行机构，它们定义了实体系统的功能性。Cyber 空间中的来源（Resource）、关系（Relationship）、和参考（Reference）构成了实体系统运行的基础，是 CPS 在赛博空间中的管理目标。建立面向实体空间内的比较性(Comparison)、关系性（Correlation）、和目的性（Consequence）的对称性管理是核心的分析手段。而 CPS 的最终目标，是在赛博空间中对实体空间中 3V 的精确管理，即可视性（Visualization）、差异性（Variation）和价值性（Value）.

## CPS的实体空间与赛博空间

实体空间是构成真实世界的各类要素和活动，包括环境、设备、系统、集群、社区、人员活动等。而 Cyber 赛博空间是对上述要素和活动的精确同步和建模，以实时数据驱动的镜像模型动态反映实体状态，通过个体空间、群体空间、环境空间、活动空间与推演空间的建立，模拟个体之间、群体之间和与环境之间的关系，记录实体空间随时间的变化，并结合活动目标，可以对实体空间的活动进行模拟、评估、推演与预测，形成决策知识。

在上图的 CPS 空间相互指导与相互映射过程中，以下 4 个空间是其运行的基础：- 个体空间：在实体空间获取对象机理数据，根据机理关联对象，通过使用数据建立定量化的分析模型，以较小的成本解决多样性和个体差异性的问题；

- 群体空间：在实体空间获取集群运行数据，从大量对象在不同环境下的使用数据中挖掘普适性规律，在原有控制、信息、管理等传统系统的基础上实现预测性和协同性的决策机制；

- 环境空间：在实体空间获取内外环境数据，根据不同环境下的使用数据，建立环境与个体/群体效能之间的量化关系，解决任务多样性和环境复杂性；

- 活动空间：在实体空间获取任务活动数据，针对对象在环境中的活动状态，提取群体对象中的活动特征并进行关联，面向多层级、多维度的任务目标，实现个体/群体在环境中活动的优化协同；

- 推演空间：结合个体空间、群体空间、环境空间与活动空间之间的关系模型，面向多模型空间协作目标，根据内外部需求，以对不同决策造成结果（consequence）的预测与评估为基础，形成多模型协同知识推演规则，实现有效的认知与决策执行支持。

因此，实体空间与赛博空间的关系可以概括为：

通过对实体空间中对象、环境、活动数据的采集、建模、分析、预测、优化和协同，产生与实体空间深度融合、实时交互、互相耦合、互相更新的赛博空间（包括个体空间、环境空间、群体空间、活动空间与推演空间等的结合），通过赛博空间知识的综合利用指导实体空间的具体活动，实现知识的积累、组织、应用与分享；

{% img /gallery/book/0016-cpsXiaYiDaiAIDemo.png 600 CPS %}
<p align="center"><b>CPS技术体系</b></p>

## CPS的技术应用体系

CPS 是一个具有清晰架构和使用流程的技术体系，针对工业大数据的特点和分析要求，能够实现对数据进行收集、汇总、解析、排序、分析、预测、决策、分发的整个处理流程，对实体系统进行流水线式的实时分析能力，并在分析过程中充分考虑机理逻辑、流程关系、活动目标、商业活动等特征和要求。

CPS 技术体系框架包括了 5 个层次的构建模式：智能感知层（Connection）、信息挖掘层（Conversion）、网络层（Cyber）、认知层（Cognition）、和配置执行层（Configuration）。这个 5C 的分析构架设计的目的是为了满足实体空间与赛博空间相互映射和相互指导过程中的分析和决策要求，其特征主要体现在以下几个方面：

1)智能感知（Connection）：从信息来源、采集方式、和管理方式上保证了数据的质量和全面性，建立支持 CPS 上层建筑的数据环境基础。除了建立互联的环境和数据采集的通道，智能感知的另一核心在于按照活动目标和信息分析的需求自主地进行选择性和有所侧重的数据采集。

2)信息挖掘层（conversion）：从低价值密度的数据到高价值密度信息的转换过程，可以对数据进行特征提取、筛选、分类、和优先级排列，保证了数据的可解读性。包括了对数据的分割、分解、分类和分析过程。

3)网络层（Cyber）：重点在于网络环境中信息的融合和赛博空间的建模，将机理、环境与群体有机结合，构建能够指导实体空间的建模分析环境，包括精确同步、关联建模、变化记录、分析预测等。

4)认知层（Cognition）：在复杂环境与多维度参考条件下面向动态目标，根据不同的评估需求进行多源化数据的动态关联、评估、预测结果，实现对实体系统运行规律的认知，以及物、环境、活动三者之间的关联、影响分析与趋势判断，形成“自主认知”的能力。同时结合数据可视化工具和决策优化算法工具为用户提供面向其活动目标的决策支持。

5)配置执行层（Configuration）：根据活动目标和认知层中分析结果的参考，对运行决策进行优化，并将优化结果同步到系统的执行机构，以保障信息利用的时效性和系统运行的协同性。

## CPS实现工业智能的本质

总结而言，CPS 实现工业系统智能化的本质可以概括为：通过对实体系统和人的知识在赛博系统中进行对称建模管理，使人与实体系统通过赛博空间建立认知与交互。进而通过赋予实体系统自省性和自预测能力实现面向状态的智能、自比较与自组织能力实现面向集群的智能、自适应与自调整能力实现面向环境的智能、自重构与自协同能力实现面向任务的智能。最后，通过对实体系统中关系性的认知与建模实现知识的自成长，使知识得以可持续和规模化地利用。

自主地获得知识和高效地利用知识是智能化的本质，这里面包括了工业系统中 5 个维度的知识：

1）知道是什么的知识（Know What），即关于事实方面的知识；

2）知道为什么的知识（Know Why），关于原理和规律方面的知识；

3）知道何时的知识（Know When）：关于时机和趋势方面的知识；

4）知道怎么做的知识（Know How）：关于技艺和策略方面的知识；

5）知道是谁的知识（Know Who）：关于能力和管理方面的知识。

知识并不是独立存在的，需要存在于某种“载体”中，且什么样的载体决定了知识的产生和应用的效率边界。在日本的制造文化中，知识大多是以人的经验和管理制度为载体，通过对人的训练和持续改善的文化进行传承。在德国的制造文化中，知识大多被生产装备和集成制造系统为载体，通过将知识固化成为控制指令和系统组织逻辑来传承。

而 CPS 将成为工业智能时代中新的知识载体，知识可以通过数据和模型进行应用和传承，并通过不断从实体系统运行过程产生的数据中挖掘新的关系和规律来协助人更加快速地获得新的知识。为了使 CPS 成为知识的新载体，就必须让其具备和人一样的产生和应用知识的智慧，即需要具备以下几个重要的能力：

1）感知能力：即具有能够感知外部世界、获取外部信息的能力，这是产生智能活动的前提条件和必要条件；

2）记忆和思维能力：即能够存储感知到的外部信息及由思维产生的知识，同时能够利用知识对信息进行分析、计算、比较、判断、联想、决策；

3）学习能力和自适应能力：即通过与环境的相互作用，不断学习积累知识，使自己的知识和能力不断成长，来适应环境变化；

4）行为决策能力：即对外界的刺激作出反应，形成决策并传达相应的信息。我们在书中所描述的 CPS 技术理念和就是围绕着构建以上 4 种能力而设计的，即

以多源数据的建模为基础，以智能连接（Connection）、智能分析（Conversion）、智能网络（Cyber）、智能认知（Cognition）和智能配置与执行（Configuration）的 5C 体系为构架，建立对实体系统要素和活动之间关系性、因果性和风险性的对称管理，持续优化决策系统的可追踪性、预测性、精确性和强韧性（Resilience），实现赛博空间与实体空间之间的相互映射和相互指导。中国制造最重要的瓶颈在于制造知识的缺失与传承 ，因此CPS 的发展与落地，将在中国未来的工业转型与智能化发展中获得难得的应用机会。

Ref: http://www.sohu.com/a/145690041_488209