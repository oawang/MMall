# 2018年的最后一天，我为自己筹划一件大事

> 前方图片高能，加载不出来需要多次刷新等待

![image](http://bloghello.oursnail.cn/wallpaper.jpg)

## 前言



一直以来都是学习慕课的实战视频，虽然也跟着做出了一些东西，但是思路都是别人提供好的，脱离了老师，我一直在问自己一个问题：**能不能独立地按照自己的思路做出一些东西来？**

带着这个想法，我想，做一个开源项目对于我来说还是很遥远，但是，我想从改造现有项目开始，逐步开启个人独立开发的序幕。

在去年，即2017年年底，我在慕课上学习了这两门课程：

![https://coding.imooc.com/class/96.html](http://bloghello.oursnail.cn/scfs1-1.png)

![https://coding.imooc.com/class/96.html](http://bloghello.oursnail.cn/scfs1-2.png)

第一期项目实现了比较简单的电商业务，整合SSM，并且部署到云端。

第二期实现了tomcat集群，配合redis实现分布式session，还有一些定时任务、redis分布式锁、maven环境隔离的一些东西。

整体感觉是：一期实现业务，二期对于一期的提高不是太大，跟分布式无太大关系，仅仅实现了单点登陆和分布式session存储而已。

个人感觉下一期的课程应该是springCloud的分布式改造，进行服务拆分和治理。所以，在整合这两个课程的基础上用springCloud进行微服务治理。


对于微服务的学习，我主要是学习了慕课网这门课程：


![https://coding.imooc.com/class/177.html](http://bloghello.oursnail.cn/scfs1-3.png)

这个课程业务极其简单，就是一个天气预报功能，作者的目的就是忽略业务干扰，急速入门微服务。整理的笔记：[swgBook-github](https://github.com/sunweiguo/swgBook/tree/master/spring-cloud-weather-action)


在码码在线这个平台，学习了SpringCloud微服务组件，加深了对微服务组件的理解。
![www.coder520.com](http://bloghello.oursnail.cn/scfs1-4.png)

由于引入微服务必然是为了应对高并发场景，所以在码码在线这个平台上学习了分布式电商实战码码购：[mama-buy笔记](https://github.com/sunweiguo/mama-buy)

这个实战比较有深度，现在还在消化中，所以，对于电商实战的改造，我将借鉴这个实战里面的一些思想。

鉴于高并发场景，秒杀就是终极体现，所以在慕课网上学习了：

![image](http://bloghello.oursnail.cn/scfs1-5.png)

服务端的优化主要是通过redis的内存标记+预减库存+MQ异步下单实现。


在最后，我花一天时间简单过了一遍廖师兄改造微信点餐项目的实现思路，最后他使用`docker`+`rancher`这两个工具实现容器化和对容器的管理。没有具体去做：

![image](http://bloghello.oursnail.cn/scfs1-6.png)

经历了这一年的洗礼，当然不仅仅以上内容的学习，中间跨过了秋招，个人也成长了许多。嗯，就是这样...

在有了以上的基础之后，我觉得我可以自己尝试去对电商项目改造一番了。虽然这个文章也没人看，但是我期待一下自己的表现吧！如果完成了，就将改造的过程整理一下。加油！

## 项目进展

- [x] 2018/12/31 完成了聚合工程的创建、Eureka服务注册中心、spring cloud config+gitHub+spring cloud bus（rabbitMQ）实现配置自动刷新--tagV1.0
- [x] 2018/12/31 将Eureka注册中心(单机)和配置中心部署到服务器上，这比较固定，所以先部署上去，以后本地就直接用这两个即可，对配置进行了一点点修改
- [ ] 2018/12/31 关于配置的自动刷新，用postman发送post请求是可以的，但是用github webhook不行，不知道是不是这个版本的问题
- [x] 2018/12/31 用户模块的逻辑实现,首先增加了一些pom文件的支持，整合mybatis，测试数据库都通过，下面就可以真正去实现业务代码了
- [x] 2019/1/1 完成用户注册、登陆、校验用户名密码有效性这个三个接口，在注册这个接口，增加一个ZK分布式锁来防止在高并发场景下出现用户名或邮箱重复问题

## 项目详细描述

待续...

## 项目启动

## 项目复原笔记