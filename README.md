# Pager CMS

Pager CMS是一款完全**基于云服务的次世代建站工具**，它可以帮助网站开发商降低开发部署成本，提升网站安全性，以及网站终端用户体验。

## Pager CMS概要

### 项目背景

当前针对企业或者个人用户的建站方式主要有以下几种：
- 完全自主开发：包括网站的前端和后端
- 使用CMS系统针对页面进行高度定制化
- 完全使用云服务，比如阿里云建站

针对这三种方案，现有的解决方案优缺点如下：
| 方案 | 优点 | 缺点 |
| --- | --- | --- |
| 自主开发 | 针对特殊需求特殊定制 | 开发时间长，成本高 |
| CMS | 可以满足绝大部分需求，可以针对页面进行高度定制化 | 现有CMS系统多为PHP，容易被攻击，需要开发商自己部署，用户体验差，运维风险高（数据丢失），针对部分特殊需求（比如微信公众号同步）暂时解决方案比较少 |
| 云服务 | 开发成本低，不需要运维，可靠性高，不用担心被攻击 | 基本没有什么定制化的空间，只能简单针对页面定制，价格偏贵，没有数据的控制权 |

这三个方案里面，其中自主开发，完全是对项目进行定制，其实无法做成产品做大来推广。
云服务这种方案，基本被头部厂商，比如阿里，腾讯等把控，没有什么入场机会。
CMS这种方案，之所以能够成为产品，是因为目前国内有大量的中小企业从事建站服务，这样的开发商为他们的客户开发页面高度定制化的网站，必须使用能够针对页面进行高度定制化的CMS系统来开发。
针对这种方案，可以做出比市场上现有产品要好的产品和服务，逐渐去推广。

### 项目契机
当前国内建站最多的CMS系统DedeCMS针对所有用户收费，一个网站5800，很多老网站大量往其他平台，比如WordPress，帝国，pboot等CMS转移。
然而，这些PHP的平台依然无法解决CMS建站中的一些问题
容易被攻击：PHP很多还停留在5.x，本身就容易被攻击，很多建站的企业还疏于更新源程序（或者本身源程序被魔改过，要处理冲突也没法去改）
运维成本高：PHP本身要部署在服务器上，开发商要自己去买服务器买流量或者带宽，有的CMS还依赖数据库，还要有专门的人来管服务器和数据库，做好定期备份
终端用户体验差：因为成本的限制，这种网站，基本都是单服务器，没法保证高可用性，和访问链路的通畅，终端用户访问的时候打开速度不理想。
针对这一现状，本项目，以下暂定成为Pager CMS，简称Pager，拟定开发一款软件即服务（以下简称SaaS）的CMS，改CMS具有以下特征：

- 开发商不用自行购买服务器和数据库，只用买Pager的建站资源
- Pager尽量使用模板生成静态页面，直接把页面部署到CDN，提升用户体验
- 特殊需求比如留言板等需要后端服务的功能，通过集约化的微服务，面向所有终端用户提供服务
- Pager提供在线编辑和开发工具，开发商无需在本地调试，降低开发环境搭建和维护成本
- Pager提供模板商城，开发商可以挑选半成品模板直接建站（类似AB模板网）

### 收费模式
Pager支持两种收费模式，一种就是SaaS，买软件服务，第二种就是卖授权，然后自己部署（self hosted）或者我们来帮助部署。
这点类似于Github的官网版和企业self host自建版，针对这两个模式

- SaaS
  - 卖模板
  - 建站工具：每一个网站的建站工具收取相应费用，或者工具免费
  - 存储费用
  - 流量费用，也可以按带宽付费？？
- self hosted
  - 按年来付软件使用授权
  - 部署费用
  - 运维费用

### 用户群体
用户群体主要有以下四大类

| 用户 | 权限 | 说明 |
| --- | --- | --- |
| 终端用户 | 访问网页，访问微服务（比如提交留言板等）| 用户访问存在CND上生成的静态页面网站，用户访问各个功能的微服务（比如留言板），提交留言板的时候直接提交请求到留言板的微服务，请求带有网站的id |
| 网站使用者（企业或个人） | 访问CMS系统，访问微服务（比如查看留言板等） | 网站使用者可以访问CMS来设置网站的文章和内容，能设置的部分由网站开发者指定 |
| 网站开发商 | 访问CMS系统，添加用户，编辑模板，发布网页 | 网站开发商可以创建网站项目，添加用户和权限，编辑网页的模板，指定网站使用者可以编辑的内容 |
| 模板开发商 | 访问CMS系统，创建编辑模板，分享模板	 |  |


## Pager CMS功能文档

- 文章列表
- 文章分页
- 文章详情
