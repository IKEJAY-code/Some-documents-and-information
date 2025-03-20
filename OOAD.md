<center>

# 面向对象分析与设计

</center>

### 1.1.1 序言
&emsp;&emsp;本文档是《面向对象分析与设计》的学习笔记，主要内容包括面向对象分析与设计的基本概念、方法、技术和工具等。本文档的目的是帮助读者更好地理解面向对象分析与设计的基本概念、方法、技术和工具，提高读者的面向对象分析与设计能力。

### 1.2.1 课程的定义
- 有各种思维,例如：Object-oriented
- 学习面向对象的思维方式
- 利用面向对象的思维方式去思考实际问题
- UML: 统一建模语言
- C++, Python: 面向对象设计语言

### 1.3.1 面向对象思想的起源
- 艾伦·凯的成就:
  - SmallTalk语言之父
  - 面向对象的思想的奠基人   

### 1.4.1 面向对象的基本概念
- **类 (Class)**
- **对象 (Object)**
- 定义: 用对象来定义类、用类来产生对象
- 有的时候在表达概念的时候可以通用

#### 1. 问题:
- What is a Class, Object?
  - A class is a description of a set of objects that share the same attributes, operations, relationships, and semantics.
  - An object is an instance of a class.
  - 1) 类、定义了实例的行为和信息结构
  - 2) 对象的当前状态取决于作用该状态的属性

#### 2. 类的构成、对象的构成
- 属性 == 数据 == 状态 == 信息
- 操作 == 方法 == 行为 == 职责
- 对象 == 实例

#### 3. 软件的过程是如何完成的?
- **类:**
  - 定义了对象群体的逻辑结构,包括属性和操作
  - 系统运行时,类作为产生对象的模版,在物理层面是不存在的

- **对象:**
  - 系统运行的时候必须为每个需要的对象分配内存、保存数据
  - 对象存在于物理层面,每个对象都有自己的数据空间(内存)
  - 所有对象共享同一块代码空间

- **消息:**
  - 对象之间的一种交流手段
  - 就像我们日常工作中的各种交流手段

- **所有相关对象的相互协作完成软件功能**

### 1.5.1 什么是面向对象的思考方式?
1. 观察到的一切都是对象
2. 定义: 在对世界进行观察建模的时候,把它们看成是由一系列相互交流相互影响的对象集
   - 软件开发的常用思维: 面向对象、面向过程
   - 面向过程: 流水线 面向对象: 篮球赛
   - 面向对象分析: OOA
   - 面向对象设计: OOD

### 1.6.1 面向对象方式的核心特征(一)
- **封装 (Encapsulation)**
  1. 隐藏了对象的实现细节
  2. 内部的状态不为其他对象所访问
  3. 对象的数据只通过接口访问
  - 要封装什么?
    1. 内部的不让人知道的
    2. 可以封装类的属性
    3. 可以封装类的方法

  - **规则:**
    - An object should only reveal the interfaces needed to interact with it. Detail not pertinent to the use of the object should be hidden from other objects. 
  - **建议:**
    - Getter and Setter

- **继承 (Inheritance)**
  - The basic principle is simple:
    - A class gets the state and behavior of another class and adds additional state and behaviour.

- **多态 (Polymorphism)**
  - 本意: 有多种形态
  - 当一个类从另一个类继承而来,多态使得子类可以替代父类
  - 消息接收方不需要知道消息接收方属于哪个子类
  - 同一类族的接受者可以按自己的方式处理消息
  - 使用指向父类的指针或者引用,能够调用子类的对象

### 1.7.1 面向对象方式的核心特征(二)
- **聚合/组合 (Aggregation/Composition)**
  - Inheritance is a "is-a" relationship
  - Aggregation is a "has-a" relationship
  - **Aggregation indicate that**
    - One object contains a set of other objects
    - 例如: A University is a collection of students, faculty, and courses
  - **Aggregation relationship is transitive**
    - if A contains B and B contains C, then A contains C
  - **Aggregation relationship are asymmetric**
    - if A contains B, but does not B contain A
  - **A variant of aggregation is composition which adds the property of existence dependency**
    - 组合强调: 整体控制生命
    - if A composes B, then if A is deleted, B is deleted
  - **Composition is a type of Strong aggregation**
    - ‘whole’ can control the life span of 'portion'

- **接口/实现 (Interface/Implementation)**
  - **对于软件系统**
    - 软件系统的内部是由大量的互相关联的类构成的
    - 当对其中一个类的局部进行修改的时候,不能影响其他类
  - **接口 (interface)**
    - describe how users of the class interact with the class
  - **实现 (Implementation)**
    - 完成接口所定义的功能,如类、构件等完成的任务
    - 发电厂实现接口,TV依赖插座
    ![](/image/1.jpg)
    - 发电厂实现接口,TV依赖插座

- **抽象 (Abstraction)**
  - 抽象是一种思维方式,是一种对现实世界的简化和理解
  - 例如: 人、狗、猫,抽象成动物
  - **抽象与具体的比较: 你要去飞机场,做出租车去**
    1. A: 师傅请送我去机场.
    2. B: 师傅!走!左拐,执行,右拐!!!.....
    - (A是抽象的,不需要知道具体的细节.)

### 2.1.1 UML序言
#### 1.1
#### 1.2 建立复杂的模型
#### 1.3 模型的定义
- **建模 (modeling)**
  1. 重要的研发成果常常产自类比 (analogy)
  2. 把不太理解的东西和一些已经较为理解、且十分类似的东西做比较,可以对这些不太理解的东西产生更深刻的理解,叫做**建模**
- **模型 (model)**
  1. 建模产生的结果就是模型,模型是对现实的简化、对事物的一种抽象
  2. 模型可以帮助人们更好的了解事物的本质,抓住问题要害
  3. 在模型中,人们总是剔除那些与问题无关的、非本质的东西,从而使得模型与真实的实体更加简单、易于把握

#### 1.4 建模的目的
- 因为不能完整的理解一个复杂的系统,所以要对他建模
- 为了更好的理解正在开发的系统
- 建模的四个目的
  1. 帮助我们按照需要对系统进行可视化
  2. 帮助我们详细说明系统的结构和行为
  3. 给出了一个知道我们构造系统的模版
  4. 对我们的决策进行文档化

#### 1.5 建模的四项基本原理
1. 选择要创建什么模型
2. 每一种模型可以在不同的精度级别下表示
3. 最好的模型是与现实相关的
4. 单个模型是不充分的,对每一个重要的系统最好用一组几乎独立的模型处理

#### 1.6 UML: Unified Modeling Language
#### 1.7 什么是UML?
#### 1.8 UML的概念模型
![](/image/2.jpg)
![](/image/3.jpg)   
![](/image/4.jpg)

### 2.2.1 用例(用况)模型
#### 2.1 参与者 (Actor)
- **参与者为人:** ![](/image/5.jpg)
- **参与者为一个系统:** ![](/image/6.jpg)
  - 代表位于系统之外和系统进行交互的一类事物(人、物、其他的软件子系统)
  - 通过它,可以对软件系统与外界发生的交互进行分析和描述
  - 通过它,可以了解客户希望软件系统提供哪些功能

#### 2.2 用例 (Use Case)
- 定义: 系统为响应参与者引发的一个事件而执行的一系列的处理/动作,而这些处理应该为参与者产生一种有价值的结果.
- 这些动作:
  1. 不但应该包含正常情况下的各种动作序列
  2. 而且应包含对非正常情况时软件系统的动作系列的描述, Exception/Alternate
![](/image/7.jpg)

#### 2.3 寻找用例
- 1.参与者希望系统提供什么功能
- 2.系统是否存储和检索信息
- 3.当系统改变状态时,是否通知参与者
- 4.是否存在影响系统的外部事件,是哪个参与者通知系统这些外部事件
- 5.哪个参与者触发了活动
**每个用例都有一个名称:**
  - 短小精悍的动名词,如:取钱,存钱

#### 2.4 用例图中的关系
- **关联关系**
  - 1. 用例之间的关系
  - 2. 用例之间的关系是一种关联关系
  - 3. 用例之间的关系是一种依赖关系(extend)
  - 4. 用例之间的关系是一种泛化关系:如下订单和网上下订单
  - 5. 用例之间的关系是一种包含关系(include)
#### 2.5用例描述
![](/image/8.jpg)
#### 2.6用例模型 Usecase Model
- 用例模型包括:
  - 系统边界
  - 参与者
  - 用例
  - 用例图
  - 用例描述
### 2.3.1 活动图
#### 3.1 活动图的定义:
- **活动图描述了在一个过程中,顺序的/并行的活动及其之间的关系**
- **活动图是定点和弧的集合**
![](/image/9.jpg)
#### 3.2 活动图的元素
![](/image/10.jpg)

### 2.4.1 类图
#### 4.1 类图的定义
#### 4.2 类图的元素
![](/image/11.jpg)
#### 4.3 类图:问题的引出?
- 1.有多少个类
- 2.每个类需要定义多少属性
- 3.每个类需要定义多少操作?
- 4.类之间的关系
- 5.类之间的信息交互,如何完成复杂功能的?
#### 4.4 UML中类的表示
- **类的图形表示**
![](/image/12.jpg)
#### 4.5 类元素的命名
- 类的命名
    - 类名中每个词的第一个字母通常要大写
- 操作的命名
    - 操作名 除第一个词之外的每个词的第一个字母要大写
    - 例如:selectCourse()
- 属性的命名
    - 属性名 除第一个单词之外的每个词的第一个字母要大写
    - 例如:courseName
#### 4.6 关联关系的修饰
![](/image/13.jpg)
- 多重性Multiplicity
![](/image/14.jpg)
- 聚合/组合
![](/image/15.jpg)
#### 4.7关联类:Association class
- Association class is an association that is also a class,and consists of the class,association the dashed line
  - It may have attributes,operations and relationships
  - You can use an association class when there is exactly one unique link between any pair of objects at any point in the time
  - If a pair of objects may have many links to each other at a given point in time,then you reify the relationship by replacing it with a normal class
#### 4.8 案例
![](/image/16.jpg)
### 2.5.1 顺序图
- 交互图
- 通信图
#### 5.1 问题的提出?
![](/image/17.jpg)
#### 5.2 相关概念
- 交互
  - 对象之间为实现某一功能而必须实施的协作过程、动态行为,称为交互
- 消息
  - 对象间的协作与交流表现为一个对象以某种方式启动另一个对象的活动,这种交流载UML被定义为消息
- 顺序图的建模元素
  - 对象或角色
  - 参与者
  - 消息
- 交互图
#### 5.3 交互的基本概念 -- 消息
- 同步消息
- 异步消息
#### 5.4 顺序图:交互图的一种
- 关于操作:operation
![](/image/18.jpg)
#### 5.5 代码和顺序图的映射
![](/image/19.jpg)
### 2.6.1 通信图
- 通信图强调对象之间的结构关系
- 顺序图强调 随着时间的推移,各对象是如何交互的
#### 6.1 通信图
![](/image/20.jpg)
#### 6.2 通信图和顺序图的区别
### 2.7.1 状态图
#### 7.1 问题的引出
![](/image/21.jpg)
#### 7.2 状态图的基本概念
- 状态(state)
  - 是对象的生命期中的一个条件或状况
  - 在此期间,对象可以响应事件、执行某活动
  - 例如 灯 有几个状态
- 状态机(state machine)
  - 是一种行为
  - 说明对象在它的生命期中,响应事件所经历的状态序列 以及他们对每个事件的响应
- 状态图(state diagram,state Chart):
  - 状态及可以用状态图来可视化
  - 状态图显示了一个状态及,它强调从状态到状态的控制流
- 状态有以下几个部分组成
  - 名称(name)
    - 每个单词首字母大写
  - 进入/退出动作(entry/exit action)
  - 内部迁移(internal transition)
  - 子状态(substate)
  - 延迟事件(deferred event)
- 事件(event)
    - 是对一个在时间和空间上占有一定位置的有意义的事物的描述
      - 在状态及的语境中,一个时间是一个激励的发生,它能够出发一个状态迁移
    - UML对四种时间进行建模
      - 参量变化 change event
      - 信号signal(异步)
      - 信号call(同步)
      - 时间事件time event
        - 时间时间 是表示一段时间的推移
          - 用关键字after 后面跟着事件表达式
          - 用关键字at 表示某个绝对时间点上发生的时间事件
        - 变化事件 表示状态的一个变化或某些条件得到满足的事件
          - 用关键字when后跟一个布尔表达式,当条件满足,则引发变化事件
- 迁移Transition
  - 在状态A,发生事件并满足一定条件,转到状态B
  - 一个迁移由5部分组成
    - 源状态 Source state
    - 事件触发器 event trigger(触发事件名称)
    - 触发条件 guard condition
    - 效应(effect)(或者,迁移动作)
      - 可执行的动作
    - 目标状态
- 特殊的迁移
    - 自身迁移 self transition
    - 内部迁移 internal transition

#### 7.3 状态图的建模元素

![](/image/22.jpg)
#### 7.4 理解状态图

#### 7.5 状态图建模

- 建模步骤
  - 1.选择对象及视点
  - 2.定义对象在生命周期内可能存在的状态
  - 3.在每种状态下可接受的事件以及将要转去的新状态
#### 7.6 比较状态图与交互图、活动图

![](/image/23.jpg)
### 3.1.1 面向对象分析与设计概览

#### OOAD Overview
![](/image/24.jpg)
![](/image/25.jpg)
- 课程的关键Key importance
    - 通用职责分配模式
    - Follows GRASP principle
      - General Responsibilities Assignment Software Patterns
- What is implement
- What is deployment
- Relationship of the Analysis and Design
  - “do the right thing(Analysis),and do the thing right(design)”
