# Async-后端Java组内部考核接口文档

此接口文档仅用于Async-后端Java组内部考核使用

## 1.成员列表查询

### 基本信息

请求路径：/merbers

请求方式：GET

接口描述：该接口用于实验室成员信息查询

### 请求参数：

无

### 响应数据

参数格式:application/json

参数说明:

|  参数名   |  类型   | 是否必须 | 备注                         |
| :-------: | :-----: | :------: | ---------------------------- |
|   code    | String  |   必须   | 响应码，1代表成功，0代表失败 |
|    msg    | String  |  非必须  | 提示信息                     |
|   name    | String  |  非必须  | 成员昵称                     |
|    sex    | String  |  非必须  | 性别                         |
|    id     | String  |  非必须  | id                           |
|   grade   | String  |  非必须  | 成员年级                     |
|  college  | String  |  非必须  | 成员学院                     |
|   major   | String  |  非必须  | 成员专业                     |
|   admin   | boolean |  非必须  | 成员是否为管理员             |
| arrearage | boolean |  非必须  | 成员是否欠费                 |
|   money   | double  |  非必须  | 成员欠费金额                 |
|   seat    | boolean |  非必须  | 成员是否有固定座位           |
| location  | String  |  非必须  | 成员固定座位号               |
| password  | String  |  非必须  | 成员密码                     |

### 响应数据案例：

成功响应案例：

~~~json
{
  "code": "1",
  "msg": "success",
  "members": [
    {
      "id": "1",
      "name": "张三",
      "sex": "男",
      "grade": "大二",
      "college": "计算机学院",
      "major": "软件工程",
      "admin": true,
      "arrearage": false,
      "money": 0.0,
      "seat": true,
      "location": "09"
    },
    {
      "id": "2",
      "name": "李四",
      "sex": "女",
      "grade": "大三",
      "college": "化学学院",
      "major": "化学工程",
      "admin": false,
      "arrearage": true,
      "money": 50.0,
      "seat": false,
      "location": "null"
    }
  ]
}
~~~

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "查询失败"
}

~~~

## 2.实验室信息查询

### 基本信息

请求路径：/labs

请求方式：GET

接口描述：该接口用于实验室信息的查询

### 请求参数：

无

### 响应数据

参数格式：application/json

参数说明:

|   参数名   |     类型     | 是否必须 | 备注                         |
| :--------: | :----------: | :------: | ---------------------------- |
|    code    |    number    |   必须   | 响应码，1代表成功，0代表失败 |
|    msg     | StringString |  非必须  | 提示信息                     |
|    name    |    String    |  非必须  | 实验室名称                   |
|  welcome   |    String    |  非必须  | 实验室登录欢迎语             |
|   money    |    double    |  非必须  | 实验室资金                   |
|  activity  |  activity[]  |  非必须  | 实验室活动                   |
| seatRemain |     int      |  非必须  | 实验室剩余座位               |
|    bill    |    bill[]    |  非必须  | 实验室账单                   |

### 响应数据案例：

成功响应案例：

~~~json
{
  "code": 1,
  "msg": "success",
  "name": "异步开发实验室",
  "welcome": "欢迎登录异步开发实验室管理人员信息管理系统",
  "money": 10000.0,
  "activity": [
    {
      "id": 1,
      "name": "活动1",
      "description": "活动1的描述"
    },
    {
      "id": 2,
      "name": "活动2",
      "description": "活动2的描述"
    }
  ],
  "seatRemain": 20,
  "bill": [
    {
      "id": 1,
      "amount": 50.0,
      "description": "账单1的描述"
    },
    {
      "id": 2,
      "amount": 100.0,
      "description": "账单2的描述"
    }
  ]
}
~~~

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "查询失败"
}

~~~

## 3.活动信息查询

### 基本信息

请求路径：/activities

请求方式：GET

接口描述：该接口用于活动信息的查询

### 请求参数：

无

### 响应数据

参数格式：application/json

参数说明：

|    参数名    |  类型  | 是否必须 |             备注             |
| :----------: | :----: | -------- | :--------------------------: |
|     code     | number | 必须     | 响应码，1代表成功，0代表失败 |
|     msg      | String | 非必须   |           提示信息           |
|     name     | String | 非必须   |           活动名称           |
|   creator    | String | 非必须   |          活动创建人          |
| creationTime | String | 非必须   |         活动创建时间         |
| introduction | String | 非必须   |         活动活动简介         |
|  startTime   | String | 非必须   |         活动开始时间         |
|   endTime    | String | 非必须   |         活动结束时间         |

### 响应数据案例：

成功响应案例：

~~~json
{
  "code": 1,
  "msg": "success",
  "data": {
    "name": "活动名称",
    "creator": "活动创建人",
    "creationTime": "活动创建时间",
    "introduction": "活动活动简介",
    "startTime": "活动开始时间",
    "endTime": "活动结束时间"
  }
}
~~~

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "查询失败"
}

~~~

## 4.座位信息查询

### 基本信息

请求路径：/seats

请求方式：GET

接口描述:该接口用于座位信息的查询

### 请求参数：

无

### 响应数据

参数格式：application/json

参数说明：

|  参数名   |  类型   | 是否必须 |           信息类型           |
| :-------: | :-----: | -------- | :--------------------------: |
|   code    | number  | 必须     | 响应码，1代表成功，0代表失败 |
|    msg    | String  | 非必须   |           提示信息           |
| location  | String  | 非必须   |           座位位置           |
| available | boolean | 非必须   |         座位是否空闲         |
|   owner   | String  | 非必须   |          座位持有人          |
|  ownerId  | String  | 非必须   |        座位持有人学号        |

### 响应数据案例：

成功响应案例：

~~~json
{
  "code": 1,
  "msg": "success",
  "location": "06",
  "available": false,
  "owner": "张三",
  "ownerId": "2021122001"
}
~~~

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "查询失败"
}

~~~

## 5.流水信息查询

### 基本信息

请求路径：/bills

请求方式；GET

接口描述：该接口用于流水信息的查询

### 请求参数：

请求数据样例：

~~~shell
/bills
~~~

### 响应数据

参数格式：application/json

参数说明：

| 参数名 |  类型  | 是否必须 |             备注             |
| :----: | :----: | -------- | :--------------------------: |
|  code  | number | 必须     | 响应码，1代表成功，0代表失败 |
|  msg   | String | 非必须   |           提示信息           |
|  date  | String | 非必须   |         流水变动时间         |
| issue  | String | 非必须   |           流水事件           |
| amount | double | 非必须   |           流水金额           |
| remain | double | 非必须   |        变动后剩余资金        |

### 响应数据案例：

成功响应案例：

~~~json
{
  "code": 1,
  "msg": "success",
  "date": "2023-05-11",
  "issue": "购买活动奖品",
  "amount": 100.0,
  "remain": 500.0
}
~~~



失败响应案例：

~~~json
{
  "code": 0,
  "msg": "查询失败"
}

~~~



## 6.欠费信息查询

### 基本信息

请求路径：/debts

请求方式：GET

接口描述：该接口用于欠费信息的查询

### 请求参数：

请求数据样例：

~~~shell
/debts?id=20222123095
~~~

### 响应数据

参数格式：application/json

参数说明：

| 参数名  |  类型   | 是否必须 |             备注             |
| :-----: | :-----: | -------- | :--------------------------: |
|  code   | number  | 必须     | 响应码，1代表成功，0代表失败 |
|   msg   | String  | 非必须   |           提示信息           |
|  data   | Object  | 非必须   |           欠费日期           |
|  issue  | String  | 非必须   |           欠费事件           |
|  money  | double  | 非必须   |           欠费金额           |
|  owner  | String  | 非必须   |          欠费人姓名          |
| ownerId | String  | 非必须   |          欠费人学号          |
| handIn  | boolean | 非必须   |           是否补交           |

### 响应数据案例：

成功响应势力：

~~~json
{
  "code": 1,
  "msg": "success",
  "data": {
    "date": "2023-05-11",
    "issue": "实验室用水",
    "money": 100.0,
    "owner": "张三",
    "ownerId": "20222123095",
    "handIn": false
  }
}

~~~

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "查询失败"
}

~~~

## 7.删除成员

### 基本信息

请求路径：/members/{id}

请求方式：DELETE

接口描述：该接口用于删除指定ID的成员

### 请求参数：

id：成员ID（路径参数）

请求参数样例：

~~~html
/members/20220810**
~~~

### 响应数据

参数格式：该接口用于删除指定ID的实验室成员

参数说明：

| 参数名 |  类型  | 是否必须 |
| :----: | :----: | :------: |
|  code  | String |   必须   |
|  msg   | String |  非必须  |
|  data  | object |  非必须  |

### 响应数据案例：

成功响应案例：

~~~json
{    
    "code":1,    
    "msg":"success",    
    "data":null
}
~~~

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "删除失败"
}

~~~



## 8.修改成员

### 基本信息

请求路径：/merbers

请求方式：PUT

接口描述

### 请求参数：

id：成员ID（路径参数）

### 响应数据

参数格式:该接口用于修改指定ID的实验室成员

参数说明:

|  参数名   |  类型   | 是否必须 | 备注                         |
| :-------: | :-----: | :------: | ---------------------------- |
|   code    | String  |   必须   | 响应码，1代表成功，0代表失败 |
|    msg    | String  |  非必须  | 提示信息                     |
|   name    | String  |  非必须  | 成员昵称                     |
|    sex    | String  |  非必须  | 性别                         |
|    id     | String  |  非必须  | id                           |
|   grade   | String  |  非必须  | 成员年级                     |
|  college  | String  |  非必须  | 成员学院                     |
|   major   | String  |  非必须  | 成员专业                     |
|   admin   | boolean |  非必须  | 成员是否为管理员             |
| arrearage | boolean |  非必须  | 成员是否欠费                 |
|   money   | double  |  非必须  | 成员欠费金额                 |
|   seat    | boolean |  非必须  | 成员是否有固定座位           |
| location  | String  |  非必须  | 成员固定座位号               |
| password  | String  |  非必须  | 成员密码                     |

请求数据案例：

~~~json
{
  "code": "1",
  "name": "张三",
  "sex": "男",
  "id": "2",
  "grade": "大二",
  "college": "计算机科学与技术",
  "major": "软件工程",
  "admin": false,
  "arrearage": false,
  "money": 0.0,
  "seat": true,
  "location": "02",
  "password": "********"
}
~~~

响应数据样例：

~~~json
{
    "code":1,
    "msg":"success",
    "data":null
}
~~~



失败响应案例：

~~~json
{
  "code": 0,
  "msg": "修改失败"
}

~~~

## 9.添加成员

### 基本信息

请求路径：/merbers

请求方式：POST

接口描述：该接口用于添加指定ID的实验室成员

### 请求参数：

application/json

参数说明:

|  参数名   |  类型   | 是否必须 | 备注               |
| :-------: | :-----: | :------: | ------------------ |
|   name    | String  |  非必须  | 成员昵称           |
|    sex    | String  |  非必须  | 性别               |
|    id     | String  |  非必须  | id                 |
|   grade   | String  |  非必须  | 成员年级           |
|  college  | String  |  非必须  | 成员学院           |
|   major   | String  |  非必须  | 成员专业           |
|   admin   | boolean |  非必须  | 成员是否为管理员   |
| arrearage | boolean |  非必须  | 成员是否欠费       |
|   money   | double  |  非必须  | 成员欠费金额       |
|   seat    | boolean |  非必须  | 成员是否有固定座位 |
| location  | String  |  非必须  | 成员固定座位号     |
| password  | String  |  非必须  | 成员密码           |

请求数据案例：

~~~json
{
  "name": "张三",
  "sex": "男",
  "id": "2",
  "grade": "大一",
  "college": "计算机科学与技术",
  "major": "软件工程",
  "admin": false,
  "arrearage": false,
  "money": 0.0,
  "seat": true,
  "location": "02",
  "password": "********"
}
~~~

成功响应样例

~~~json
{
    "code":1,
    "msg":"success",
    "data":null
}
~~~

| 名称 | 类型   | 是否必须 | 备注                         |
| ---- | ------ | -------- | ---------------------------- |
| code | number | 必须     | 响应码，1代表成功，0代表失败 |
| msg  | string | 非必须   | 提示信息                     |
| data | object | 必须     | 返回的数据                   |

失败响应案例：

~~~json
{
  "code": 0,
  "msg": "修改失败"
}

~~~

## 10. 登录

### 基本信息

> 请求路径：/login
>
> 请求方式：POST
>
> 接口描述：该接口用于登录系统，登录完毕后，系统下发Cookie或JWT令牌。 



### 请求参数

参数格式：application/json

参数说明：

| 名称     | 类型   | 是否必须 | 备注 |
| -------- | ------ | -------- | ---- |
| id       | String | 必须     | 学号 |
| password | String | 必须     | 密码 |

请求数据样例：

```json
{
	"id": "20220810**",
    "password": "123456"
}
```



### 响应数据

参数格式：application/json

参数说明：

| 名称 | 类型   | 是否必须 | 默认值 | 备注                        | 其他信息 |
| ---- | ------ | -------- | ------ | --------------------------- | -------- |
| code | number | 必须     |        | 响应码, 1 成功 ; 0  失败    |          |
| msg  | string | 非必须   |        | 提示信息                    |          |
| data | string | 必须     |        | 返回的数据 ,Cookie/ jwt令牌 |          |



响应数据样例：

```json
{
  "code": 1,
  "msg": "success",
  "data": "eyJhbGciOiJIUzI1NiJ9.eyJuYW1lIjoi6YeR5bq4IiwiaWQiOjEsInVzZXJuYW1lIjoiamlueW9uZyIsImV4cCI6MTY2MjIwNzA0OH0.KkUc_CXJZJ8Dd063eImx4H9Ojfrr6XMJ-yVzaWCVZCo"
}
```



> 如果检测到用户未登录，则会返回如下固定错误信息：
>
> ```json
> {
> 	"code": 0,
> 	"msg": "NOT_LOGIN",
> 	"data": null
> }
> ```

## 11.发布内部活动

### 基本信息：

> 请求路径：/activities
>
> 请求方式：POST
>
> 接口描述：该接口用于发布内部活动信息 

### 请求参数：

application/json

参数说明：

|    参数名    |  类型  | 是否必须 |  信息类型  |
| :----------: | :----: | -------- | :--------: |
|     name     | String | 非必须   |  活动名称  |
|   creator    | String | 非必须   | 活动创建人 |
| creationTime | String | 非必须   |  创建时间  |
| introduction | String | 非必须   |  活动简介  |
|  startTime   | String | 非必须   |  开始时间  |
|   endTime    | String | 非必须   |  结束时间  |

请求数据样例：

~~~json
{
    "name":"讲座"，
    "creator":"立本",
    "creationTime":"2023-05-26",
    "introduction":"活动简历概述",
    "startTime":"2023-05-26"，
    "endTime":"2023-05-26"
    
}
~~~

成功响应样例：

~~~json
{
    "code":1,
    "msg":"success",
    "data":null
}
~~~

| 名称 | 类型   | 是否必须 | 备注                         |
| ---- | ------ | -------- | ---------------------------- |
| code | number | 必须     | 响应码，1代表成功，0代表失败 |
| msg  | string | 非必须   | 提示信息                     |
| data | object | 必须     | 返回的数据                   |

失败响应案例：

~~~json
{
    "code":0,
    "msg":"fail",
}
~~~

## 12.上传活动证明

### 基本信息：

> 请求路径：/upload
>
> 请求方式：POST
>
> 接口描述：该接口用于上传活动证明

### 请求参数：

application/json

参数说明：

| 参数名 | 类型 | 是否必须 | 信息类型 |
| :----: | :--: | -------- | :------: |
| image  | file | 是       |   图片   |

成功响应样例：

~~~json
{
    "code":1,
    "msg":"success",
    "data":"https://asynclab-activity-032154/certify.jpg"
}
~~~

| 名称 | 类型   | 是否必须 | 备注                           |
| ---- | ------ | -------- | ------------------------------ |
| code | number | 必须     | 响应码，1代表成功，0代表失败   |
| msg  | string | 非必须   | 提示信息                       |
| data | object | 非必须   | 返回的数据，上传图片的访问路径 |

失败响应案例：

~~~json
{
    "code":0,
    "msg":"fail",
}
~~~

## 13.上传缴费项目

### 基本信息：

> 请求路径：/payments
>
> 请求方式：POST
>
> 接口描述：该接口用于上传缴费项目

### 请求参数：

application/json

参数说明：

|  参数名  |  类型  | 是否必须 |
| :------: | :----: | :------: |
|  issue   | String |  非必须  |
| debtorId | String |  非必须  |
|   date   | String |  非必须  |
|  amount  | double |  非必须  |

请求数据样例：

~~~json
{
    "issue":"缴费项名称",
    "debtorId":"20220810**"，
    "date":"2023-6-01",
    "amount":1000.0
}
~~~

成功响应样例：

~~~json
{
    "code":1,
    "msg":"success",
    "data":null
}
~~~

| 名称 | 类型   | 是否必须 | 备注                         |
| ---- | ------ | -------- | ---------------------------- |
| code | number | 必须     | 响应码，1代表成功，0代表失败 |
| msg  | string | 非必须   | 提示信息                     |
| data | object | 必须     | 返回的数据                   |

失败响应案例：

~~~json
{
    "code":0,
    "msg":"fail",
}
~~~

