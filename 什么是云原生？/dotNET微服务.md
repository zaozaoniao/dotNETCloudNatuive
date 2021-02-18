前文传送门：
 - [什么是云原生？](https://www.cnblogs.com/JulianHuang/p/14375725.html)
 - [现代云原生设计理念](https://www.cnblogs.com/JulianHuang/p/14377177.html)
 
### Microservices

微服务是构建现代应用程序的一种流行的体系结构样式，云原生系统拥抱微服务。  

微服务是由一组(使用共享结构交互的、独立的小块服务)搭建的分布式集，具有以下特征：
- 在大型的领域上下文中，每个微服务实现特定的业务功能
- 每个微服务都自主开发的，且可以独立部署
- 每个微服务都独立封装了自己的数据存储技术（SQL，NoSQL）和编程平台。
- 每一个微服务都运行在独立进程，并使用标准的通信协议(例如HTTP/HTTPS、WebSocket或AMQP)与其他进程进行通信。
- 它们一起组成一个应用程序。

下图对比单体与微服务应用:  
> 请注意，单体应用由分层架构组成，在单个进程中执行，通常使用关系型数据库。  
但是，微服务方法将功能分为包含逻辑和数据的独立服务，每个微服务都托管自己的数据存储。  

![](https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/media/monolithic-vs-microservices.png)

微服务依然遵守"十二要素应用"中的One Codebase, One Application”原则。
> 每个微服务存储在独立代码仓库，通过版本管理进行跟踪，可以部署到多个环境。

###  Why microservices?
微服务提供了敏捷性。  

上一段落，我们已经对比了单体和微服务，我们看到了一些明显的好处：  

-  每个微服务都有自治的生命周期，可以独立演进、多频次部署。   
你不必等待发布窗口即可部署新功能或更新，你可以只更新复杂应用的一小部分区域，减少破坏整个系统的风险。  

-  每个微服务都可以独立扩展。  
不需要以应用整体为单位扩展，而仅扩展那些需要更多处理能力或网络带宽的微服务，这种细粒度的伸缩方法提供更好的控制力和成本优势。

学习微服务的最佳指南是《.NET Microservices: Architecture for Containerized .NET Applications》，这本书深入探讨了微服务设计和架构，它是微服务实践https://github.com/dotnet-architecture/eShopOnContainers的阅读搭档。

### Developing microservices
可以使用任何现代开发平台来创建微服务。    

微软.NET平台是一个绝佳的选择，免费、开源，内置许多功能以简化微服务开发。 .NET是跨平台的，可以在Windows、macOS和大多数Linux上构建和运行应用程序。  

.NET的性能很高，在TechEmpower组织的性能基准测试中，.NET相当优秀。  

.NET由Microsoft和.NET社区在GitHub上维护。

