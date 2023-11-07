# 软件（结构）设计说明（SDD）

> **说明**
> 1. SDD 描述了计算机软件配置项（CSCI）的设计。它描述了 CSCI 级设计决策、CSCI 体系结构设计（概要设计）和实现该软件所需的详细设计。
     > SDD 可用接口设计说明 IDD 和数据库（顶层）设计说明 DBDD 加以补充。
> 2. SDD 连同相关的 IDD 和 DBDD 是实现该软件的基础。向需方提供了设计的可视性，为软件支持提供了所需要的信息。
> 3. IDD 和 DBDD 是否单独成册抑或与 SDD 合一份资料视情况繁简而定。

软件（结构）设计说明的正文的格式如下：

## 1 引言

本章应分为以下几条。

### 1.1 标识

本条应包含本文档适用的系统和软件的完整标识。（若适用）包括标识号、标题、缩略词语、版本号、发行号。

### 1.2 系统概述

本条应简述本文档适用的系统和软件的用途。它应描述系统与软件的一般性质；概述系统开发、运行和维护的历史；标识项目的投资方、需方、用户、开发方和支持机构；标识当前和计划的运行现场；并列出其他有关文档。

### 1.3 文档概述

本条应概述本文档的用途与内容，并描述与其使用有关的保密性或私密性要求。

### 1.4 基线

说明编写本系统设计说明书所依据的设计基线。

## 2 引用文件

本章应列出本文档引用的所有文档的编号、标题、修订版本和日期。本章也应标识不能通过正常的供货渠道获得的所有文档的来源。

## 3 CSCI 级设计决策

本章应根据需要分条给出 CSCI 级设计决策，即 CSCI 行为的设计决策（忽略其内部实现，从用户的角度看，它如何满足用户的需求）和其他影响组成该
CSCI 的软件配置项的选择与设计的决策。

如果所有这些决策在CSCI 需求中均是明确的，或者要推迟到 CSCI 的软件配置项设计时指出，本章应如实陈述。
为响应指定为关键性的需求（如安全性、保密性、私密性需求）而作出的设计决策，应在单独的条中加以描述。
如果设计决策依赖于系统状态或方式，则应指出这种依赖性。
应给出或引用理解这些设计所需的设计约定。
CSCI级设计决策的例子如下：

1. 关于 CSCI 应接受的输人和产生的输出的设计决策，包括与其他系统、HWCI、CSCI 和用户的接口（本文的 4.5.x
   标识了本说明要考虑的主题）。如果该信息的部分或全部已在接口设计说明（IDD）中给出，此处可引用。
2. 有关响应每个输人或条件的 CSCI 行为的设计决策，包括该 CSCI 要执行的动作、响应时间及其他性能特性、被模式化的物理系统的说明、所选择的方程式/算法/规则和对不允许的输入或条件的处理。
3. 有关数据库/数据文件如何呈现给用户的设计决策（本文的 4.5.x 标识了本说明要考虑的主题）。如果该信息的部分或全部已在数据库（顶层）设计说明（DBDD）中给出，此处可引用。
4. 为满足安全性、保密性、私密性需求而选择的方法。
5. 对应需求所做的其他CSCI级设计决策，例如为提供所需的灵活性、可用性和可维护性所选择的方法。

## 4 CSCI 体系结构设计

本章应分条描述 CSCI 体系结构设计。
如果设计的部分或全部依赖于系统状态或方式，则应指出这种依赖性。
如果设计信息在多条中出现，则可只描述一次，而在其他条引用。
应给出或引用为理解这些设计所需的设计约定。

### 4.1 体系结构

#### 4.1.1 程序（模块）划分

用一系列图表列出本CSCI 内的每个程序（包括每个模块和子程序）的名称、标识符、功能及其所包含的源标准名。

#### 4.1.2 程序（模块）层次结构关系

用一系列图表列出本CSCI 内的每个程序（包括每个模块和子程序）之间的层次结构与调用关系。

### 4.2 全局数据结构说明

本章说明本程序系统中使用的全局数据常量、变量和数据结构。

#### 4.2.1 常量

包括数据文件名称及其所在目录，功能说明，具体常量说明等。

#### 4.2.2 变量

包括数据文件名称及其所在目录，功能说明，具体变量说明等。

#### 4.2.3 数据结构

包括数据结构名称，功能说明，具体数据结构说明（定义、注释、取值..）等。

### 4.3 CSCI 部件

本条应：

1. 标识构成该 CSCI 的所有软件配置项。应赋予每个软件配置项一个项目唯一标识符。
    - 注：软件配置项是 CSCI 设计中的一个元素，如 CSCI
      的一个主要的分支，该分支的一个组成部分、一个类、对象、模块、函数、例程或数据库。软件配置项可以出现在一个层次结构的不同层次上，并且可以由其他软件配置项组成。设计中的软件配置项与实现它们的代码和数据实体（例程、过程、数据库、数据文件等）或包含这些实体的计算机文件之间，可以有也可以没有一对一的关系。一个数据库可以被处理为一个
      CSCI，也可被处理为一个软件配置项。SDD 可以通过与所采用的设计方法学一致的名字来引用软件配置项。
2. 给出软件配置项的静态关系（如“组成”）。根据所选择的软件设计方法学可以给出多种关系（例如，采用面向对象的设计方法时，本条既可以给出类和对象结构，也可以给出CSCI的模块和过程结构）。
3. 陈述每个软件配置项的用途，并标识分配给它的 CSCI 需求与 CSCI 级设计决策（需求的分配也可在 6.a 中提供）。
4. 标识每个软件配置项的开发状态/类型（如新开发的软件配置项，重用已有设计或软件的软件配置项、再工程的已有设计或软件、为重用而开发的软件等）。对于已有设计或软件，本说明应提供标识信息，如名称、版本、文档引用、库等。
5. 描述 CSCI（若适用，每个软件配置项）计划使用的计算机硬件资源（例如处理器能力、内存容量、输入/输出设备能力、辅存容量和通信/网络设备能力）。这些描述应覆盖该
   CSCI 的资源使用需求中提及的、影响该CSCI 的系统级资源分配中提及的、以及在软件开发计划的资源使用度量计划中提及的所有计算机硬件资源。如果一给定的计算机硬件资源的所有使用数据出现在同一个地方，如在一个
   SDD 中，则本条可以引用它。针对每一计算机硬件资源应包括如下信息：
    1. 得到满足的CSCI 需求或系统级资源分配；
    2. 使用数据所基于的假设和条件（例如，典型用法、最环情况用法、特定事件的假设）；
    3. 影响使用的特殊考虑（例如虚存的使用、覆盖的使用、多处理器的使用或操作系统开销、库软件或其他的实现开销的影响）；
    4. 所使用的度量单位（例如处理器能力百分比、每秒周期、内存字节数、每秒千字节）；
    5. 进行评估或度量的级别（例如软件配置项、CSCI 或可执行程序）。
6. 指出实现每个软件配置项的软件放置在哪个程序库中。

### 4.4 执行概念

本条应描述软件配置项间的执行概念。
为表示软件配置项之间的动态关系，即 CSCI 运行期间它们如何交互的，本条应包含图示和说明，
（若适用）包括执行控制流、数据流、动态控制序列，状态转换图、时序图、配置项之间的优先关系、中断处理、时间/序列关系、异常处理、并发执行、动态分配与去分配、对象/进程/任务的动态创建与删除和其他的动态行为。

### 4.5 接口设计

本条应分条描述软件配置项的接口特性，既包括软件配置项之间的接口，也包括与外部实体，如系统、配置项及用户之间的接口。
如果这些信息的部分或全部已在接口设计说明（IDD）、本文的第5章或其他地方说明的话，可在此处引用。

#### 4.5.1 接口标识与接口图

本条应陈述赋予每个接口的项目唯一标识符，（若适用）并用名字、编号、版本和文档引用等标识接口实体（软件配置项、系统、配置项、用户等）。
接口标识应说明哪些实体具有固定接口特性（从而把接口需求强加给接口实体），哪些实体正在开发或修改（因而已把接口需求分配给它们）。
（若适用）应该提供一个或多个接口图以描述这些接口。

#### 4.5.x（接口的项目唯一标识符）

本条（从 4.5.2 开始编号）应用项目唯一标识符标识接口，应简要标识接口实体，并且应根据需要划分为几条描述接口实体的单方或双方的接口特性。
如果一给定的接口实体本文没有提到（例如，一个外部系统），但是其接口特性需要在本 SDD
描述的接口实体时提到，则这些特性应以假设、或“当［未提到实体］这样做时，［提到的实体］将……”的形式描述。
本条可引用其他文档（例如数据字典、协议标准、用户接口标准）代替本条的描述信息。本设计说明应包括以下内容，（若适用）它们可按适合于要提供的信息的任何次序给出，并且应从接口实体角度指出这些特性之间的区别（例如数据元素的大小、频率或其他特性的不同期望）。

1. 由接口实体分配给接口的优先级；
2. 要实现的接口的类型（例如实时数据传输、数据的存储与检索等）；
3. 接口实体将提供、存储、发送、访问、接收的单个数据元素的特性，例如：
    1. 名称/标识符；
        1. 项目唯一标识符；
        2. 非技术（自然语言）名称；
        3. 标准数据元素名称；
        4. 缩写名或同义名；
    2. 数据类型（字母数字、整数等）；
    3. 大小与格式（例如字符串的长度与标点符号）；
    4. 计量单位（如米、元、纳秒等）；
    5. 范围或可能值的枚举（如0~99）；
    6. 准确度（正确程度）与精度（有效数位数）；
    7. 优先级、时序、频率、容量、序列和其他约束，如数据元索是否可被更新，业务规则是否适用；
    8. 保密性与私密性约束；
4. 接口实体将提供、存储、发送、访问、接收的数据元素集合体（记录、消息、文件、数组、显示、报表等）的特性，例如：
    1. 名称/标识符；
        1. 项目唯一标识符；
        2. 非技术（自然语言）名称；
        3. 技术名称（如代码或数据库中的记录或数据结构名）；
        4. 缩写名或同义名；
    2. 数据元素集合体中的数据元素及其结构（编号、次序、分组）；
    3. 媒体（如盘）及媒体上数据元素/集合体的结构；
    4. 显示和其他输出的视听特性（如颜色、布局、字体、图标及其他显示元素、蜂鸣声、亮度等）；
    5. 数据集合体之间的关系，如排序/访问特性；
    6. 优先级、时序、频率、容量、序列和其他约束，如数据集合体是否可被更新，业务规则是否适用；
    7. 保密性与私密性约束；
    8. 来源（设置/发送实体）与接收者（使用/接收实体）。
5. 接口实体为该接口使用通信方法的特性，例如：
    1. 项目唯一标识符；
    2. 通信链路/带宽/频率/媒体及其特性；
    3. 消息格式化；
    4. 流控制（如序列编号与缓冲区分配）；
    5. 数据传输率、周期或非周期和传送间隔；
    6. 路由、寻址及命名约定；
    7. 传输服务，包括优先级与等级；
    8. 安全性/保密性/私密性考虑，如加密、用户鉴别、隔离、审核等。
6. 接口实体力该接口使用协议的特性，例如：
    1. 项目唯一标识符；
    2. 协议的优先级/层；
    3. 分组，包括分段与重组、路由及寻址；
    4. 合法性检查、错误控制、恢复过程；
    5. 同步，包括连接的建立、保持、终止；
    6. 状态、标识和其他报告特性。
7. 其他特性，如接口实体的物理兼容性（尺寸、容限、负荷、电压、接插件的兼容性等）。

## 5 CSCI 详细设计

本章应分条描述CSCI 的每个软件配置项。
如果设计的部分或全部依赖于系统状态或方式，则应指出这种依赖性。
如果该设计信息在多条中出现，则可只描述一次，而在其他条引用。
应给出或引用为理解这些设计所需的设计约定。
软件配置项的接口特性可在此处描述，也可在第 4 章或接口设计说明（IDD）中描述。
数据库软件配置项，或用于操作/访问数据库的软件配置项，可在此处描述，也可在数据库（顶层）设计说明（DBDD）中描述。

### 5.x（软件配置项的项目唯一标识符或软件配置项组的指定符）

本条应用项目唯一标识符标识软件配置项并描述它。（若适用）描述应包括以下信息。
作为一种变通，本条也可以指定一组软件配置项，并分条标识和描述它们。
包含其他软件配置项的软件配置项可以引用那些软件配置项的说明，而无需在此重复。

1. （若有）配置项设计决策，诸如（如果以前未选）要使用的算法；
2. 软件配置项设计中的约束、限制或非常规特征；
3. 如果要使用的编程语言不同于该 CSCI 所指定的语言，应该指出，并说明使用它的理由；
4. 如果软件配置项由过程式命令组成或包含过程式命令（如数据库管理系统（DBMS）中用于定义表单与报表的菜单选择、用于数据库访问与操纵的联机
   DBMS 查询、用于自动代码生成的图形用户接口（GUI）构造器的输人、操作系统的命令或 shell 脚本），应有过程式命令列表和解释它们的用户手册或其他文档的引用；
5. 如果软件配置项包含、接收或输出数据，（若适用）应有对其输入、输出和其他数据元素以及数据元素集合体的说明。（若适用）本文的
   4.5.x 提供要包含主题的列表。软件配置项的局部数据应与软件配置项的输入或输出数据分开来描述。如果该软件配置项是一个数据库，应引用相应的数据库（顶层）设计说明（DBDD）；接口特性可在此处提供，也可引用本文第4章或相应接口设计说明。
6. 如果软件配置项包含逻辑，给出其要使用的逻辑，（若适用）包括：
    1. 该软件配置项执行启动时，其内部起作用的条件；
    2. 把控制交给其他软件配置项的条件；
    3. 对每个输入的响应及响应时间，包括数据转换、重命名和数据传送操作；
    4. 该软件配置项运行期间的操作序列和动态控制序列，包括：
        1. 序列控制方法；
        2. 该方法的逻辑与输入条件，如计时偏差、优先级赋值；
        3. 数据在内存中的进出；
        4. 离散输入信号的感知，以及在软件配置项内中断操作之间的时序关系；
    5. 异常与错误处理。

## 6 需求的可追踪性

本章应包括：

1. 从本 SDD 中标识的每个软件配置项到分配给它的 CSCI 需求的可追踪性（亦可在 4.1 中提供）；
2. 从每个 CSCI 需求到它被分配给的软件配置项的可追踪性。

## 7 注解

本章应包含有助于理解本文档的一般信息（例如背景信息、词汇表、原理）。
本章应包含为理解本文档需要的术语和定义，所有缩略语和它们在文档中的含义的字母序列表。

## 附录

附录可用来提供那些为便于文档维护而单独出版的信息（例如图表、分类数据）。
为便于处理，附录可单独装订成册。
附录应按字母顺序（A，B等）编排。