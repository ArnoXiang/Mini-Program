## PHP后台restful服务实现方案与PHP开发框架调研报告

REST（英文：Representational State Transfer，简称REST) ， 直译为表现层状态转移，或者表述性状态转移；Rest 指的是一组架构约束条件和原则，是web服务的一种架构风格，一种设计风格，是一种思想；同时Rest不是针对某一种编程语言的。

**本质：**一种软件架构风格 

**核心：**面向资源设计的API在制作微信小程序的过程中，后台服务的实现是至关重要的一环。本文将探讨如何使用PHP语言实现RESTful服务，并简要介绍几种流行的PHP开发框架。

## PHP后台RESTful服务实现方案

RESTful架构风格的Web API称为RESTful API，它定义了资源的三个基本方面：

- 资源的地址（URI）

- 传输的资源类型（如JSON、XML）

- 资源的操作（如POST、GET、PUT或DELETE方法）


在PHP语言中，我们可以不依赖任何框架来创建RESTful服务。例如，可以通过.htaccess文件和PHP脚本来处理HTTP请求，并返回相应的资源。
一个简单的RESTful服务类可能包含获取所有资源列表和获取单个资源的方法。此外，还需要一个基类来处理HTTP状态码和响应头。

## 常见的PHP开发框架

PHP框架提供了一套工具和库，以便更快速、更规范地开发应用程序。以下是几种常见的PHP框架：

**Laravel:** Laravel是一个开源的PHP框架，适用于开发复杂的Web应用程序。它提供了丰富的功能，如路由、会话、缓存和身份验证，以及数据迁移、MVC架构支持等。

**CodeIgniter**: CodeIgniter是一个轻量级的PHP框架，以其小巧和简单易学而著称。它提供了快速的性能和强大的错误处理能力，适合初学者和小型项目3。

**Symfony**: Symfony是一个成熟的PHP框架，适用于大型企业级项目。它遵循PHP和Web标准，提供了可重用的PHP组件，易于与其他库集成。

**Yii**: Yii是一个高性能的PHP框架，适用于各种Web应用程序。它提供了简单的安装过程和健壮的安全特性，适合于需要高度安全性的项目。

**Zend Framework**: Zend Framework是一个面向对象的框架，提供了高度的可定制性。它是构建复杂企业级应用程序的理想选择。

## PHP后台restful服务实现方案：

# 设计概念和准则

符合REST设计风格的Web API称为RESTful API。它从以下三个方面资源进行定义：

直观简短的资源地址：URI，比如：http://example.com/resources/。
传输的资源：Web服务接受与返回的互联网媒体类型，比如：JSON，XML，YAM等。
对资源的操作：Web服务在该资源上所支持的一系列请求方法（比如：POST，GET，PUT或DELETE）。
以webService为例通俗解释。

非Rest设计，以往我们都会这么写：

http://localhost:8080/admin/getUser （查询用户）

http://localhost:8080/admin/addUser （新增用户）

http://localhost:8080/admin/updateUser （更新用户）

http://localhost:8080/admin/deleteUser （删除用户）

总结：以不同的URL（主要为使用动词）进行不同的操作。

Rest架构：

GET http://localhost:8080/admin/user （查询用户）

POST http://localhost:8080/admin/user （新增用户）

PUT http://localhost:8080/admin/user （更新用户）

DELETE http://localhost:8080/admin/user （删除用户）

总结：URL只指定资源，以HTTP方法动词进行不同的操作。用HTTP STATUS/CODE定义操作结果。

Restful：遵守了rest风格的web服务便可称为Restful。

常用的响应状态码 (httpCode)

| 状态码  | 描述 |
| ------------- | ------------- |
200 | 请求成功
201	| 创建成功
202 | 更新成功
400 | 无效请求
401 | 未授权
403 | 禁止访问
404 | 请求资源不存在
500 | 内部错误

请求方式

【GET】 /users # 查询用户信息列表

【GET】 /users/1001 # 查看某个用户信息

【POST】 /users # 新建用户信息

【PUT】 /users/1001 # 更新用户信息(全部字段)

【PATCH】 /users/1001 # 更新用户信息(部分字段)

【DELETE】 /users/1001 # 删除用户信息

【PATCH】一般不用，用【PUT】

查询参数
RESTful API 接口应该提供参数，过滤返回结果。

【GET】 /{version}/{resources}/{resource_id}?offset=0&limit=20

响应参数
JSON格式（code、data、msg）

## 为什么需要Restful？
URL具有很强可读性的，具有自描述性， 对程序员友好

1. 规范化请求过程和返回结果

2. 资源描述与视图的松耦合

3. 可提供OpenAPI，便于第三方系统集成，提高互操作性

4. 提供无状态的服务接口，降低复杂度，可提高应用的水平扩展性

5. 不暴露内部代码结构，更安全


## 参考
- https://www.runoob.com/php/php-restful.html
- https://www.cnblogs.com/jackzhuo/p/12964474.html
- https://zhuanlan.zhihu.com/p/304449541
- https://zhuanlan.zhihu.com/p/142993304
- https://developer.aliyun.com/article/931504
- https://cloud.baidu.com/article/2920503
- https://blog.csdn.net/phpergod/article/details/92841998
- https://cloud.tencent.com/developer/article/2373874


在选择PHP框架时，需要考虑项目的规模、复杂性以及团队的经验。例如，Laravel适用于中大型项目，而CodeIgniter则更适合小型项目和初学者。

## 总结
PHP后台RESTful服务的实现可以不依赖框架，但使用框架可以提高开发效率和代码质量。同时在选择框架时，应根据项目需求和团队熟悉度来决定。
