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

## 6. 数据到数据库
### 创建数据库的SQL语句

```sql
-- 创建用户表
CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    phone VARCHAR(20),
    email VARCHAR(50),
    password VARCHAR(255),
    platform VARCHAR(20),
    auth_info TEXT
);

-- 创建登录记录表
CREATE TABLE login_records (
    record_id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    login_time DATETIME,
    login_method VARCHAR(20),
    FOREIGN KEY (user_id) REFERENCES users(user_id)
);
```

### 插入数据到数据库的SQL语句

```sql
-- 插入数据到用户表
INSERT INTO users (phone, email, password, platform, auth_info) VALUES 
('1234567890', 'user1@example.com', 'password1', 'wechat', 'auth_info1'),
('0987654321', 'user2@example.com', 'password2', 'qq', 'auth_info2'),
('1122334455', 'user3@example.com', 'password3', 'wechat', 'auth_info3');

-- 插入数据到登录记录表
INSERT INTO login_records (user_id, login_time, login_method) VALUES 
(1, '2024-05-23 10:00:00', 'password'),
(2, '2024-05-23 10:05:00', 'password'),
(3, '2024-05-23 10:10:00', 'password'),
(1, '2024-05-23 10:15:00', 'wechat'),
(2, '2024-05-23 10:20:00', 'qq');
```

这两组SQL语句分别创建了所需的数据库表并插入了一些示例数据。


### 复杂平台进行分析
```
从第一性原理看，一个收款支付系统包含哪些主要模块
从第一性原理看，一个联盟营销系统包含哪些主要模块
从第一性原理看，一个即时通讯系统包含哪些主要模块
从第一性原理看，一个风控引擎系统包含哪些主要模块
从第一性原理看，一个新闻推荐系统包含哪些主要模块
从第一性原理看，一个电子商务系统包含哪些主要模块
从第一性原理看，一个物流履约系统包含哪些主要模块
从第一性原理看，一个多人在线娱乐开放世界系统包含哪些主要模块
从第一性原理看，一个基础游戏引擎系统包含哪些主要模块
```
