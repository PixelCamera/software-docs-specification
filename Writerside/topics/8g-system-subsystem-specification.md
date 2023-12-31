# 系统/子系统需求规格说明（SSS）

> **说明**
> 1. SSS 为一个系统或子系统指定需求和指定保证每个需求得到满足所使用的方法。
     与系统或子系统外部接口相关的需求可在 SSS 中或在该 SSS 引用到的一个或多个《接口需求规格说明》（IRS）中给出。
> 2. 这个SSS，可能还要用《接口需求规格说明》（IRS）加以补充，是构成系统或子系统设计与合格性测试的基础。
     贯穿本文的术语“系统”，如果适用的话，也可解释为“子系统”。
     所形成的文档应冠名为“系统需求规格说明”或“子系统需求规格说明”。

系统/子系统需求规格说明的正文的格式如下：

## 1 引言

本章分为以下几条。

### 1.1 标识

本条应包含本文档适用的系统和软件的完整标识，（若适用）包括标识号、标题、缩略词语、版本号和发行号。

### 1.2 系统概述

本条应简述本文档适用的系统和软件的用途，它应描述系统和软件的一般特性；
概述系统开发、操作和维护的历史；
标识项目的投资方、需方、用户、开发方和支持机构；
标识当前和计划中的运行现场；
列出其他有关的文档。

### 1.3 文档概述

本条应概括本文档的用途和内容，并描述与其使用有关的保密性和私密性要求。

## 2 引用文件

本章应列出本文档所引用所有文档的编号、标题、修订版本和日期，本章也应标识不能通过正常的供货渠道获得的所有文档的来源。

## 3 需求

本章分条详述系统需求，是指功能、业务（包括接口、资源、性能、可靠性、安全性、保密性等）和数据需求。
也就是，构成系统验收条件的系统特性。
给每个需求指定项目唯一标识符以支持测试和可追踪性。
并以一种可以定义客观测试的方式来陈述需求。
对每个需求都应说明相关合格性方法（见第 4 章），如果是子系统，则还要给出从该需求至系统需求的可追踪性（见 5.a 条）。
描述的详细程度遵循以下规则：应包含构成系统验收条件的那些系统特性，需方愿意推迟到设计时留给开发方说明的那些特性。
如果在给定条中没有需求可说明的话，应如实陈述。
如果某个需求在多条中出现，可以只陈述一次而在其他条中引用之。

### 3.1 要求的状态和方式

如果要求系统在多种状态和方式下运行，且不同状态和方式具有不同的需求的话，则要标识和定义每一状态和方式。
状态和方式的例子包括：空闲、就绪、活动、事后分析、训练、降级、紧急情况和后备等。
状态和方式的区别是任意的，可以仅用状态描述系统，也可以仅用方式、方式中的状态、状态中的方式或其他有效的方式描述。
如果不需要多个状态和方式，不需人为加以区分，应如实陈述；
如果需要多个状态和/或方式，还应使本规格说明中的每个需求或每组需求与这些状态和方式相关联，关联可在本条或本条引用的附录中用表格或其他的方法表示，也可在需求出现的地方加以注解。

### 3.2 需求概述

#### 3.2.1 系统总体功能和业务结构

描述系统总体功能和业务的结构。

#### 3.2.2 硬件系统的需求

说明对硬件系统的需求。

#### 3.2.3 软件系统的需求

说明对软件系统的需求。

#### 3.2.4 接口需求

说明硬件系统和软件系统之间的接口。

### 3.3 系统能力需求

本条应分条详细描述与系统每一能力相关联的需求。
“能力”被定义为一组相关的需求。
可以用“功能”、“性能”、“主题”、“目标”或其他适合用来表示需求的词来替代“能力”。

#### 3.3.x（系统能力）

本条应标识必需的每一系统能力，并详细说明与该能力有关的需求。
如果该能力可以更清晰地分解成若干子能力，则应分条对子能力进行说明。
该需求应指出所需的系统行为，包括适用的参数，如响应时间、吞吐时间、其他时限约束、序列、精度、容量（大小/多少）、优先级别、连续运行需求和基本运行条件下的允许的偏差；
（若适用）需求还应包括在异常条件、非许可条件或越界条件下所需的行为，错误处理需求和任何为保证在紧急时刻运行的连续性而引入到系统中的规定。
在确定与系统所接收的输入和系统所产生的输出有关的需求时，应考虑在本文档 3.4.x 给出要考虑的主题列表。

### 3.4 系统外部接口需求

本条应分条描述关于系统外部接口的需求（如有的话）。
本条可引用一个或多个接口需求规格说明（IRS）或包含这些需求的其他文档。

#### 3.4.1 接口标识和接口图

本条应标识所需的系统外部接口。
（若适用）每个接口标识应包括项目唯一标识符，并应用名称、序号、版本和引用文件指明接口的实体（系统、配置项和用户等）。
该标识应说明哪些实体具有固定的接口特性（因而要对这些接口实体强加接口需求），哪些实体正被开发或修改（从而接口需求已被施加于它们）。
可用一个或多个接口图表来描述这些接口。

#### 3.4.x（接口的项目唯一标识符）

本条（从3.4.2开始）应通过项目唯一标识符标识系统的外部接口，简单地标识接口实体，根据需要可分条描述为实现该接口而强加于系统的需求。
该接口所涉及的其他实体的接口特性应以假设、或“当（未提到实体）这样做时，系统将……”的形式描述，而不描述为其他实体的需求。
本条可引用其他文档（如：数据字典、通信协议标准和用户接口标准）代替在此所描述的信息。
（若适用）需求应包括下列内容，它们以任何适合于需求的顺序提供，并从接口实体的角度说明这些特性的区别（如对数据元素的大小、频率或其他特性的不同期望）：

1. 系统必须分配给接口的优先级别；
2. 要实现的接口的类型的需求（如：实时数据传送、数据的存储和检索等）；
3. 系统必须提供、存储、发送、访问、接收的单个数据元素的特性，如：
    1. 名称/标识符；
        1. 项目唯一标识符；
        2. 非技术（自然语言）名称；
        3. 标准数据元素名称；
        4. 技术名称（如代码或数据库中的变量或字段名称）；
        5. 缩写名或同义名；
    2. 数据类型（字母数字和整数等）；
    3. 大小和格式（如：字符串的长度和标点符号）；
    4. 计量单位（如：米、元、秒）；
    5. 范围或可能值的枚举（如：0～99）；
    6. 准确度（正确程度）和精度（有效数字位数）；
    7. 优先级别、时序、频率、容量、序列和其他的约束条件，如：数据元素是否可被更新、业务规则是否适用；
    8. 保密性和私密性的约束；
    9. 来源（设置/发送实体）和接收者（使用/接收实体）；
4. 系统必须提供、存储、发送、访问和接收的数据元素集合体（记录、消息、文件、数组、显示和报表等）的特性，如：
    1. 名称/标识符；
        1. 项目唯一标识符；
        2. 非技术（自然语言）名称；
        3. 技术名称（如代码或数据库的记录或数据结构）；
        4. 缩写名或同义名；
    2. 数据元素集合体中的数据元素及其结构（编号、次序和分组）；
    3. 媒体（如盘）和媒体中数据元素/数据元素集合体的结构；
    4. 显示和其他输出的视听特性（如：颜色、布局、字体、图标和其他显示元素、蜂鸣声和亮度等）；
    5. 数据元素集合体之间的关系。如排序/访问特性；
    6. 优先级别、时序、频率、容量、序列和其他的约束条件，如：数据元素集合体是否可被修改，业务规则是否适用；
    7. 保密性和私密性约束；
    8. 来源（设置/发送实体）和接收者（使用/接收实体）；
5. 系统必须规定接口使用的通信方法所要求的特性。如：
    1. 项目唯一标识符；
    2. 通信链接/带宽/频率/媒体及其特性；
    3. 消息格式化；
    4. 流控制（如：序列编号和缓冲区分配）；
    5. 数据传送速率，周期性/非周期性，传输间隔；
    6. 路由、寻址和命名约定；
    7. 传输服务，包括：优先级别和等级；
    8. 安全性/保密性/私密性方面的考虑，如：加密、用户鉴别、隔离和审核等；
6. 系统必须规定接口使用的协议所要求的特性，如：
    1. 项目唯一标识符；
    2. 协议的优先级别/层次；
    3. 组，包括：分段和重组、路由和寻址；
    4. 合法性检查、错误控制和恢复过程；
    5. 同步，包括：连接的建立、保持和终止；
    6. 状态、标识、任何其他的报告特征；
7. 其他所需的特性，如：接口实体的物理兼容性（尺寸、公差、负荷、电压和接插件兼容性等）。

### 3.5 系统内部接口需求

本条应指明系统内部接口的需求。
如果所有内部接口留到设计时或在系统成分的需求规格说明中规定，那么必须如实说明。
如果实施这样的需求，则可考虑本文档的 3.4 列出的主题。

### 3.6 系统内部数据需求

本条应指明分配给系统内部数据的需求（若有），包括对系统中数据库和数据文件的需求。
如果所有有关内部数据的决策都留待设计时或留待系统部件的需求规格说明中给出，则需在此如实说明。
如果要强加这种需求，则可考虑在本文档的 3.4.x.c 和 3.4.x.d 列出的主题。

### 3.7 适应性需求

（若有）本条应指明要求系统提供的、与安装有关的数据（如：现场的经纬度）和要求系统使用的、根据运行需要可能变化的运行参数（如：表示与运行有关的目标常量或数据记录的参数）。

### 3.8 安全性需求

（若有）本条应描述有关防止对人员，财产、环境产生潜在的危险或把此类危险减少到最低的系统需求，包括：危险物品使用的限制；
为运输、操作和存储的目的而对爆炸物品进行分类；异常中止/异常出口规定；气体检测和报警设备；电力系统接地；排污；防爆（若适用）。
描述还应包括有关系统核部件（若有）的需求，如：部件设计、意外爆炸的预防以及与核安全规则保持一致。

### 3.9 保密性和私密性需求

（若有）本条应指明维持保密性和私密性的系统需求，包括：系统运行的保密性/私密性环境、提供的保密性或私密性的类型和程度，系统必须经受的保密性/私密性的风险、减少此类危险所需的安全措施、系统必须遵循的保密性/私密性政策、系统必须提供的保密性/私密性审核以及保密性/私密性必须遵循的确认/认可准则。

### 3.10 操作需求

说明本系统在常规操作、特殊操作以及初始化操作和恢复操作等方面的要求。

### 3.11 可使用性、可维护性、可移植性、可靠性和安全性需求

说明本系统在可使用性、可维护性、可移植性、可靠性和安全性等方面的要求。

### 3.12 故障处理需求

说明本系统在发生可能的软硬件故障时，对故障处理的要求。

#### 3.12.1 软件系统出错处理

说明属于软件系统的问题；
给出发生错误时的错误信息；
说明发生错误时可能采取的补救措施。

#### 3.12.2 硬件系统冗余措施的说明

说明哪些问题可以由硬件设计解决，并提出可采取的冗余措施；
对硬件系统采取的冗余措施加以说明。

### 3.13 系统环境需求

（若有）本条应指明系统运行必须的与环境有关的需求。
对软件系统而言，运行环境包括支持系统运行的计算机硬件和操作系统（其他有关计算机资源方面的需求在下条描述）。
对硬软件系统而言，运行环境包括系统在运输、存储和操作过程中必须经受的环境条件，如：自然环境条件（风、雨、温度、地理位置）、诱导环境（运动、撞击、噪音、电磁辐射）和对抗环境（爆炸、辐射）。

### 3.14 计算机资源需求

本条应分条进行描述。
根据系统性质，在以下各条中所描述的计算机资源应能够组成系统环境（对应软件系统）或系统部件（对应硬软件系统）。

#### 3.14.1 计算机硬件需求

本条应描述系统使用的或引入到系统中的计算机硬件需求，（若适用）包括：各类设备的数量、处理器、存储器、输入/输出设备、辅助存储器、通信/网络设备、其他所需的设备的类型、大小、能力（容量）及其他所要求的特征。

#### 3.14.2 计算机硬件资源利用需求

本条应描述系统的计算机硬件资源利用方面的需求，如：最大许可使用的处理器能力、存储器容量、输入/输出设备能力、辅助存储器容量和通信/网络设备能力。
这些要求（如每个计算机硬件资源能力的百分比）还包括测量资源时所要求具备的条件。

#### 3.14.3 计算机软件需求

本条应描述系统必须使用或引入系统的计算机软件的需求，例如包括：操作系统、数据库管理系统、通信/网络软件、实用软件、输入和设备模拟器、测试软件和生产用软件。
必须提供每个软件项的正确名称、版本和引用文件。

#### 3.14.4 计算机通信需求

本条应描述系统必须使用的或引入系统的计算机通信方面的需求，例如包括：连接的地理位置、配置和网络拓扑结构、传输技术、数据传输速率、网关、要求的系统使用时间、传送/接收数据的类型和容量、传送/接收/响应的时间限制、数据的峰值和诊断功能。

### 3.15 系统质量因素

（若有）本条应描述系统质量因素方面的需求，例如包括：系统的功能性（实现全部所需功能的能力）、可靠性（产生正确、一致结果的能力……如设备故障的平均间隔时间）、可维护性（易于服务、修改、更正的能力）、可用性（需要时进行访问和操作的能力）、灵活性（易于适应需求变化的能力）、软件可移植性（易于适应新环境变化的能力）、可重用性（在多个应用中使用的能力）、可测试性（易于充分测试的能力）、易用性（易于学习和使用的能力）和其他属性等的定量需求。

### 3.16 设计和构造的约束

（若有）本条应描述约束系统设计和构造的那些需求。
对硬软件系统而言，本条应包括强加于系统的物理需求，这些需求可通过引用适当的商用标准和规范来指定。
需求包括：

1. 特殊系统体系结构的使用或对体系结构方面的需求，例如：需要的子系统；标准部件、现有部件的使用；政府/需方提供的资源（设备、信息、软件）的使用；
2. 特殊设计或构造标准的使用；特殊数据标准的使用；特殊编程语言的使用；工艺需求和生产技术；
3. 系统的物理特性（如：重量限制、尺寸限制、颜色、保护罩）；部件的可交换性；从一地运输到另一地的能力；由单人或一组人携带或架设的能力；
4. 能够使用和不能使用的物品；处理有毒物品的需求以及系统产生电磁辐射的允许范围；
5. 铭牌、部件标记、系列号和批次号的标记、其他标识标记的使用；
6. 为支持在技术、威胁和任务等方面预期的增长和变化而必须提供的灵活性和可扩展性。

### 3.17 相关人员需求

（若有）本条应描述与使用或支持系统的人员有关的需求，包括人员的数量、技术等级、责任期、培训需求、其他的信息，如：所提供的工作站数量、内在帮助和培训能力的需求；（若有）还应包括强加于系统的人力行为工程需求。
这些需求包括对人员在能力与局限性方面的考虑；在正常和极端条件下可预测的人为错误；人为错误造成严重影响的特定区域，例如对高度可调的工作站、错误消息的颜色和持续时间、关键指示器或键的物理位置以及听觉信号的使用需求。

### 3.18 相关培训需求

（若有）本条应描述有关培训方面的系统需求。包括：系统中应包括的培训设备和培训材料。

### 3.19 相关后勤需求

（若有）本条应描述有关后勤方面的系统需求，包括：系统维护、软件支持、系统运输方式、补给系统要求、对现有设施的影响、对现有设备的影响。

### 3.20 其他需求

（若有）本条应描述在以上各条中没有涉及到的其他系统需求，包括在其他合同文件中没有涉及的系统文档的需求，如：规格说明、图表、技术手册、测试计划和测试过程以及安装指导材料。

### 3.21 包装需求

（若有）本条应描述需交付的系统及其部件在包装、加标签和处理方面的需求。（如适用）可引用适当的规范和标准。

### 3.22 需求的优先次序和关键程度

（若适用）本条应给出本规格说明中需求的、表明其相对重要程度的优先顺序、关键程度或赋予的权值，如：标识出那些认为对安全性、保密性或私密性起关键作用的需求，以便进行特殊的处理。
如果所有需求具有相同的权值，本条应如实陈述。

## 4 合格性规定

本章定义一组合格性方法，对于第 3 章中每个需求，指定为了确保需求得到满足所应使用的方法。
可以用表格形式表述该信息，也可以在第 3 章的每个需求中注明要使用的方法。合格性方法包括：

1. 演示：依赖于可见的功能操作，直接运行系统或系统的一部分而不需要使用仪器、专用测试设备或进行事后分析。
2. 测试：使用仪器或其他专用测试设备运行系统或系统的一部分，以便采集数据供事后分析使用。
3. 分析：对从其他合格性方法中获得的积累数据进行处理，例如测试结果的归约、解释或推断。
4. 审查：对系统部件、文档等进行可视化检查。
5. 特殊的合格性方法。系统的任何特殊合格性方法，如：专用工具、技术、过程、设施、验收限制，标准样例的使用和生成等。

## 5 需求可追踪性

对系统级的规格说明，本章不适用；对子系统级的规格说明，本章应包括：

1. 从本规格说明中每个子系统需求到其涉及的系统需求的可追踪性。（该可追踪性也可以通过对第3章中的每个需求进行注释的方法加以描述。）
    - 注：每一层次的系统改进可能导致对更高层次的需求不能直接进行追踪。例如：建立两个子系统的系统体系结构设计可能会产生有关子系统接口的需求，而这些接口需求在系统需求中并没有被覆盖，这样的需求可以被追踪到诸如“系统实现”这样的一般需求，或被追踪到导致它们产生的系统设计决策上。
2. 从分配给被本规格说明所覆盖的子系统的每个系统需求到所涉及的子系统需求的可追踪性。分配给子系统的所有系统需求都应加以说明。追踪到接口需求规格说明（IRS）中所包含的子系统需求时，可引用
   IRS。

## 6 非技术性需求

本章应包括：

1. 交付日期；
2. 里程碑点。

## 7 尚未解决的问题

如需要，可说明系统需求中的尚未解决的遗留问题。

## 8 注解

本章应包含有助于理解本文档的一般信息（例如背景信息、词汇表、原理）。
本章应包含为理解本文档所需要的术语和定义，所有缩略语和它们在文档中的含义的字母序列表。

## 附录

附录可用来提供那些为便于文档维护而单独出版的信息（例如图表、分类数据）。
为便于处理，附录可单独装订成册。附录应按字母顺序（A，B等）编排。