## Async-后端Java组内部考核方案

这个项目将作为Async异步开发实验室内部**Java方向**的内部考核，考核截止时间为**8月20日**。

### 项目简介

在这个项目中，你们将要完成一个简单的实验室管理系统的后端。

主要目的是为实验室提供一个内部的**人员信息管理系统**，方便实验室人员的管理，实验室资金流动的管理，以及提供给内部人员更加便利的消息渠道。

为了更有利于数据的存储和管理，建议使用**数据库**储存信息

本项目将作为实验室内部**Java方向**的内部考核，考核截止时间为**8月20日**。

### 技术栈（任选一个完成此项目均可）:

* Servlet、JDBC
* SpringBoot + MyBatis
* SSM

**拦截器**：

* Struts2
* Interceptor

**数据库**：

* MySQL

### 项目要求

#### 管理员：

**功能**：

* 实现实验室成员信息的CRUD
* 分配固定座位
* 发布内部活动信息
* 上传活动证明
* 上传缴费项目

#### **成员：**

**功能**：

* 查询个人信息
* 查询活动
* 缴费信息查询



#### 人员信息类（member.class)

对于**实验室所有成员的信息**应具有以下规范：

|  参数名   |  类型   |    信息类型    |
| :-------: | :-----: | :------------: |
|   name    | String  |      姓名      |
|    sex    | String  |      性别      |
|    id     | String  |      学号      |
|   grade   | String  |      年级      |
|  college  | String  |      学院      |
|   major   | String  |      专业      |
|   admin   | boolean |   是否管理员   |
| arrearage | boolean |    是否欠费    |
|   money   | double  |    欠费金额    |
|   seat    | boolean | 是否有固定座位 |
| location  | String  |  固定座位位置  |
| password  | String  |      密码      |



#### 实验室类（lab.class)：

记录实验室的常规信息

|   参数名   |    类型    |    信息类型    |
| :--------: | :--------: | :------------: |
|    name    |   String   |   实验室名称   |
|  welcome   |   String   | 登录页面欢迎语 |
|   money    |   double   |   实验室资金   |
|  activity  | activity[] |   实验室活动   |
| seatRemain |    int     |    剩余座位    |
|    bill    |   bill[]   |    流水查看    |



#### 活动类（activity.class）：

记录实验室活动的常规信息

|    参数名    |  类型  | 信息类型 |
| :----------: | :----: | :------: |
|     name     | String | 活动名称 |
|   creator    | String |  创建人  |
| creationTime | String | 创建时间 |
| introduction | String | 活动简介 |
|  startTime   | String | 开始时间 |
|   endTime    | String | 结束时间 |



#### 座位类（seat.class)

记录实验室座位的信息，为选座和座位信息查询提供信息

|  参数名   |  类型   |  信息类型  |
| :-------: | :-----: | :--------: |
| location  | String  |  座位位置  |
| available | boolean |  是否空闲  |
|   owner   | String  |   持有人   |
|  ownerId  | String  | 持有人学号 |



#### 流水类（bill.class)

记录实验室资金的流水，仅**管理员**有权限查询流水的日期，事件，金额等信息

| 参数名 |  类型  |    信息类型    |
| :----: | :----: | :------------: |
|  date  | String |  流水变动时间  |
| issue  | String |    流水事件    |
| amount | double |    流水金额    |
| remain | double | 变动后剩余资金 |



#### 欠费信息类（arrearage.class)

| 参数名  |  类型   |  信息类型  |
| :-----: | :-----: | :--------: |
|  date   | String  |  欠费日期  |
|  issue  | String  |  欠费事件  |
|  money  | double  |  欠费金额  |
|  owner  | String  | 欠费人姓名 |
| ownerId | String  | 欠费人学号 |
| handIn  | boolean |  是否补交  |

#### 缴费信息类（payment.class)

| 参数名  |  类型   |  信息类型  |
| :-----: | :-----: | :--------: |
|  date   | String  |  发起日期  |
|  issue  | String  |  缴费事件  |
|  money  | double  |  缴费金额  |
| debtorId| String  |  缴费学号  |

#### 前后端交互

* 根据前端接口文档实现该项目的功能

#### Web拦截器的使用

* 登录验证，判断用户是否登录。
* 权限验证，判断用户是否有权限访问资源
