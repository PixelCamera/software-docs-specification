# 软件测试说明（STD）

> **说明**
> 1. STD 描述执行计算机软件配置项 CSCI、系统或子系统合格性测试所用到的测试准备、测试用例及测试过程。
> 2. 通过 STD 需方能够评估所执行的合格性测试是否充分。

软件测试说明的正文的格式如下：

## 1 引言

本章应分成以下几条。

### 1.1 标识

本条应包含本文档适用的系统和软件的完整标识，（若适用）包括标识号、标题、缩略词语、版本号、发行号。

### 1.2 系统概述

本条应简述本文档适用的系统和软件的用途。
它应描述系统与软件的一般性质；
概述系统开发、运行和维护的历史；
标识项目的投资方、需方、用户、开发方和支持机构；
标识当前和计划的运行现场；
并列出其他有关文档。

### 1.3 文档概述

本条应概述本文档的用途与内容，并描述与其使用有关的保密性与私密性要求。

## 2 引用文件

本章应列出本文档引用的所有文档的编号、标题、修订版本和日期。
本章还应标识不能通过正常的供货渠道获得的所有文档的来源。

## 3 测试准备

本章应分以下几条，（若适用）应包括用“警告”或“注意”标记的安全提示和保密性与私密性考虑。

### 3.x（测试的项目唯一标识符）

本条应用项目唯一标识符标识一个测试并提供简要说明，应分为以下几条。
当所需信息与前面为另一测试所指出的信息重复时，此处可作引用而无需重复。

#### 3.x.1 硬件准备

本条应描述为进行测试工作需要做的硬件准备过程。有关这些过程可以引用已出版的操作手册。
（若适用）应提供以下内容：

1. 要使用的特定硬件，用名字和（若适用）编号标识；
2. 任何用于连接硬件的开关设置和电缆；
3. 说明硬件、互联控制和数据路径的一个或多个图示；
4. 使硬件处于就绪状态的分步指令。

#### 3.x.2 软件准备

本条应描述为测试准备被测项和其他有关软件，包括用于测试的数据的必要过程。
有关这些过程，可以引用已出版的软件手册。
（若适用）应提供下述信息：

1. 测试中要使用的特定软件；
2. 被测项的存储媒体（如磁带、盘）；
3. 任何相关软件（如模拟器、测试驱动程序、数据库）的存储媒体；
4. 加载软件的指令，包括所需的顺序；
5. 多个测试用例共同使用的软件初始化指令。

#### 3.x.3 其他测试前准备

本条应描述进行测试前所需的其他人员活动、准备或过程。

## 4 测试说明

本章应分为以下几条。
（若适用）应包括用“警告”或“注意”标记的安全提示和保密性与私密性考虑。

### 4.x（测试的项目唯一标识符）

本条应用项目唯一标识符标识一个测试，并分为以下几条。
当所需信息与以前提供的信息重复时，此处可作引用而无需重复。

#### 4.x.y（测试用例的项目唯一标识符）

本条应用项目唯一标识符标识一个测试用例，说明其目的并提供简要描述。
下述各条提供测试用例的详细说明。

##### 4.x.y.1 涉及的需求

本条应标识测试用例所涉及的 CSCI 需求或系统需求（此信息亦可在 5.a 中提供）。

##### 4.x.y.2 先决条件

本条应标识执行测试用例前必须建立的先决条件，（若适用）应讨论以下内容：

1. 软、硬件配置；
2. 测试开始之前需设置或重置的标志、初始断点、指针、控制参数或初始数据；
3. 运行测试用例所需的预置硬件条件或电气状态；
4. 计时度量所用的初始条件；
5. 模拟环境的条件；
6. 测试用例特有的其他特殊条件。

##### 4.x.y.3 测试输入

本条应描述测试用例所需的测试输入，（若适用）应提供以下内容：

1. 每一测试输人的名称、用途和说明（如值的范围、准确度）；
2. 测试输入的来源与用于选择测试输入的方法；
3. 测试输入是真实的还是模拟的；
4. 测试输入的时间或事件序列；
5. 控制输人数据的方式：
    1. 用最小/合理数量的数据类型和值测试各项；
    2. 对过载、饱和及其他“最坏情况”影响，用各种有效数据类型和值试验被测各项；
    3. 对非常规输入处理用无效数据类型和值试验被测各项；
    4. 如需要允许再测试。

##### 4.x.y.4 预期测试结果

本条应标识测试用例的所有预期测试结果。
（若适用）应提供中间结果和最终结果。

##### 4.x.y.5 评价结果的准则

本条应标识用于评价测试用例的中间和最终测试结果的准则。
（若适用）应对每一测试结果提供以下信息：

1. 输出可能变化但仍能接受的范围或准确度；
2. 构成可接受的测试结果的输入和输出条件的最少组合或选择；
3. 用时间或事件数表示的最大/最小允许的测试持续时间；
4. 可能发生的中断、停机或其他系统故障的最大数目；
5. 允许的处理错误的严重程度；
6. 当测试结果不明确时执行重测试的条件；
7. 把输出解释为“指出在输入测试数据、测试数据库/数据文件或测试过程中的不规则性”的条件；
8. 允许表达测试的控制、状态和结果的指示方式，以及表明下一个测试用例（或许是辅助测试软件的输出）准备就绪的指示方式；
9. 以上未提及的其他准则。

##### 4.x.y.6 测试过程

本条应定义测试用例的测试过程。
测试过程应被定义为以执行步骤顺序排列的、一系列单独编号的步骤。
为便于文档维护，可以将测试过程作为附录并在此引用。
每个测试过程的适当详细程度依赖于被测试软件的类型。
对于某些软件，每次键击可以是一个单独的测试过程步骤；
而对于大多数软件，每一步骤可以包括逻辑相关的一串键击或其他动作。
适当的详细程度应该有利于规定预期结果并把它们与实际结果进行比较。
（若适用）每一测试过程应提供：

1. 每一步骤所需的测试操作员的动作和设备操作，（若适用）包括以下方面的命令：
    1. 初始化测试用例并运用测试输入；
    2. 检查测试条件；
    3. 执行测试结果的临时评价；
    4. 记录数据；
    5. 暂停或中断测试用例；
    6. 如果需要，请求数据转储或其他帮助；
    7. 修改数据库/数据文件；
    8. 如果不成功，重复测试用例；
    9. 根据该测试用例的要求，应用替代方式；
    10. 终止测试用例。
2. 对每一步骤的预期结果与评价准则
3. 如果测试用例涉及多个需求，需标识出哪一个（些）测试过程步骤涉及哪些需求。（亦可在第 5 章中提供）
4. 程序停止或指示的错误发生后要采取的动作，如：
    1. 为便于引用，根据指示器记录关键的数据；
    2. 暂停或中止对时间敏感的测试支持软件和测试仪器；
    3. 收集与测试结果有关的系统记录和操作员记录。
    4. 归约和分析测试结果所采用的过程，（若适用）应完成下述各项：
        1. 检测是否已产生了输出；
        2. 标识由测试用例所产生数据的媒体和位置；
        3. 评价输出，作为继续测试序列的基础；
        4. 与所需的输出对照，评价测试输出。

##### 4.x.y.7 假没和約束

本条应标识所做的任何假设，以及在描述测试用例中由于系统或测试条件而引入的约束或限制，如时间、接口、设备、人员与数据库/数据文件的限制。
如果对指定的限制和参数放弃或例外得到批准的话，应对它们加以标识，并且本条应指出它们对测试用例的影响与冲击。

## 5 需求的可追踪性

本章应包括：

1. 从本文中的每个测试用例到它所涉及的系统或 CSCI 需求的可追踪性。如果测试用例涉及多个需求，应包含从每一组测试过程步骤到所涉及的需求的可追踪性（此可追踪性亦可在
   4.x.y.1 中提供）
2. 从本文所提及的每个系统或 CSCI 需求到涉及它们的测试用例的可追踪性。对于 CSCI 测试，是从 CSCI
   软件需求规格说明（SRS）和有关接口需求规格说明（IRS）中的 CSCI 需求到涉及它们的测试用例的可追踪性。对于系统测试，是从在系统的系统/子系统规格说明（SSS）及有关
   IRS 中的每个系统需求到涉及它们的测试用例的可追踪性。如果测试用例涉及多个需求，则可追踪性应指明涉及每一个需求的具体测试过程步骤。

## 6 注解

本章应包含有助于理解本文档的一般信息（例如背景信息、词汇表、原理）。
本章应包含为理解本文档需要的术语和定义，所有缩略语和它们在文档中的含义的字母序列表。

## 附录

附录可用来提供那些为便于文档维护而单独出版的信息（例如图表、分类数据）。
为便于处理，附录可单独装订成册。
附录应按字母顺序（A，B等）编排。
