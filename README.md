# simple-screenSHOT-to-PRD-quickstart
## 1. 得到页面截图
 - selenium或者puppeteer都可以截图。

## 2. 页面截图转功能描述
```
请描述上面功能截图的内容
```

## 3. 页面功能描述转PRD文档
```
后续我将提供给你一个页面功能描述，请帮我转化为覆盖PRD文档，主要内容覆盖：
1. 功能需求
 - 功能列表
 - 功能名称
 - 功能描述
 - 用户故事
 - 接口描述
 - 优先级

2. 系统架构
 - 技术架构图
 - 系统组件
 - 数据流图
 - 数据库设计

---------------
{}
```

## 4. PRD转接口设计定义
```
根据以下描述，返回一个表格，表格里每一行包含以下6列：接口用途、请求方式（GET｜POST）、接受参数、request案例、成功时reponse、失败时response

------------
{}
```

## 5. PRD转数据库设计定义
```
根据以下描述，返回一个表格，表格里每一行包含以下3列：表名、字段名、生成的SQL语句

------------
数据库设计
用户表（users）

用户ID（user_id）
手机号码（phone）
邮箱地址（email）
密码（password）
第三方平台标识（platform）
第三方认证信息（auth_info）
登录记录表（login_records）

记录ID（record_id）
用户ID（user_id）
登录时间（login_time）
登录方式（login_method）
```
