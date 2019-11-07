# ch01 概述与基础知识

## Web应用工作原理

* 客户端把请求发送到服务器端的Web应用程序，Web应用程序接收请求后进行相关处理，并把客户端请求的资源以文本、图片、网页等形式返回到客户端。
* 由于解析HTML文件一般为浏览器，所以将这种架构称为B/S架构(Browser/Server)。

## Web应用的特点

* 发送到集中部署，无需安装客户端程序。
* 集中管理，业务逻辑在服务段进行维护。
* 数据共享，所有客户端访问同一服务器。
* 更强大的平台无关性，不必关心客户端的软硬件平台。

## HTTP

* URL(Uniform Resource Location)
    1. 语法1：protocol://[host.]domain[:port][/context][/resource][?query=string]

    2. 语法2：protocol://IP address [:port][/context][/resource][?query=string]

* 请求
    1. 方法-URI-协议/版本
    2. 请求头
    3. 请求正文

* 请求类型
    1. GET：获取资源
    2. POST：传输实体文本
    3. PUT：传输文件
    4. DELETE：删除资源或文件
    5. HEAD：获取响应报文头部
    6. OPTIONS：询问支持的方法
    7. TRACE：追踪路径

* 响应
    1. 协议-状态码-描述
    2. 响应头-信息
    3. 响应正文

* 状态码
    |HTTP状态码|含义|
    |:-------:|:--:|
    |200|请求成功|
    |201|请求成功并在服务器上创建新资源|
    |202|请求被接受，但未处理完成|
    |204|请求成功，但未发布任何新内容|
    |404|请求的资源不可用|
    |500|服务器发生内部错误|
    |501|服务器不支持完成请求所需功能
    |503|服务器过载，不能对请求进行服务|

## Web开发平台

* java
* .NET
* php

## XML(eXtensible Markup Language)可扩展标记语言

* XML语法规范
    1. XML规范将一个XML文档分为序言和文档元素两个部分。
    2. 序言部分包含XML声明、注释和文档类型定义等；文档元素部分则包含元素、子元素、属性和文本等。
    3. XML声明：XML声明必须是文档的第一行。

* 根元素
    1. 每个XML文档有且只有一个根元素。
    2. 根元素是一个完全包含文档中其他所有元素的元素。

* 元素
    1. 一个元素由开始标记、结束标记、可选属性和可选文本组成。

* 格式
    1. 必须有声明语句
    2. 有且仅有一个根元素
    3. 大小写敏感、属性值用引号、标记成对、空标记关闭。。。

* 有效的XML文档——格式良好+符合DTD或Scheme

* DTD(文档定义类型)
    1. DTD文档包括：
        >1.元素(ELEMENT)的定义则。
        >2.元素之间的关系规则
        >3.属性(ATTLIST)的定义规则
        >4.可使用的实体(ENTITY)和符号(NOTATION)规则

    2. DTD与XML的关系
        >1.类与对象
        >2.数据库表结构与数据记录

    3. 为什么需要DTD
        >1.不同组织的人可以使用一个通用DTD用来交换数据。
        >2.应用程序可以使用一个标准DTD校验从外部世界接受来的XML数据是否有效。

* DTD缺点
    1. DTD不遵守XML语法，导致写XML文档时用一种语法，写DTD时又用另外一种语法；
    2. DTD数据类型有限，不可扩展，不支持命名空间。

* Schema
    1. Schema基于XML语法，所以可以使用解析XML的工具解析Schema文件；
    2. Schema扩充了数据类型，还支持元素的集成和属性组等。

* JDBC

# ch02 Servlet基础

## Servlet基本概率

* Java Servlet 是运行在 Web 服务器或应用服务器上的程序，它是作为来自 Web 浏览器或其他 HTTP 客户端的请求和 HTTP 服务器上的数据库或应用程序之间的中间层。

## Servlet API

* javax.servlet：定义Servlet和Servlet容器之间契约的类和接口；
* javax.servlet.http: 定义基于HTTP协议的Servlet的类和接口
* javax.servlet.annotation: Servlet、Filter、Listener等接口的注解定义
* javax.servlet.descriptor: 一些配置信息的类型定义。

## javax.servlet包

* Servlet技术的核心是javax.servlet.Servlet接口，所有的Servlet类必须直接或间接的实现Servlet接口。
* Servlet容器负责加载和调和具体的Servlet类，每一个类型的Servlet类只能有一个实例。

## Servlet的生命周期

* 包括加载、实例化、处理客户端请求和销毁。
* 该生命周期有javax.servlet.Servlet接口的init、service、destory方法实现。

# ch03 JSP

## JSP基本概念

* JSP：用Servlet来编写Web应用，导致服务端代码过于繁琐和复杂，将Servlet中的静态部分和动态部分分开来编写，同时提供类似HTML的写法，这就是JSP。

* JSP是一种建立在Servlet规范提供的功能之上的动态网页技术。

* JSP文件在用户第一次请求时，会被编译成Servlet，然后由这个Servlet处理用户的请求。

* JSP可以看成是运行时的Servlet。
