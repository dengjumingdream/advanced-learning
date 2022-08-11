<!--
 * @Author: MrDeng
 * @Date: 2022-08-11 14:31:05
 * @LastEditTime: 2022-08-11 16:09:34
 * @LastEditors: dengjuming
 * @Description: 
 * @FilePath: /advanced-learning/Java/微服务架构/README.md
-->
一、微服务架构问题
    1.java搭建微服务
      - https://blog.csdn.net/wufaliang003/article/details/79464737
      - https://blog.csdn.net/buchengbugui/article/details/109511356
    2.面试会问什么
      - 微服务架构是如何运作的？
      - 单体应用、SOA 和微服务架构有什么区别？
      - 什么是 Spring Cloud？
      - Spring Cloud 解决了哪些问题？
      - 你能否给出关于 Rest 和微服务的要点？REST 是啥
    3.构成
      - 负载均衡器
      - Dubbo：阿里提供的微服务系统的协调者
        - 身份：
          - 服务提供者
          - 服务消费者
          - 注册中心
        - 流程：
          - 将dubbo包引入项目
          - 项目启动，dubbo将项目需要发布的服务、以及IP和端口发送给注册中心
          - 与此同时，dubbo还会扫描当前项目所需引用的服务，向注册中心请求这些服务所在的IP和端口
          - 正常运行后。当系统A调用系统B服务的时候，A就会和B建立一条RPC通信，然后再调用B上的服务
      - 容器化部署：docker
      - 自动化构建：Jenkins使用

二、微服务架构如何运作？
    - 客户端：来自不同设备的不同用户发送请求。
    - 身份提供商：验证用户或客户身份并颁发安全令牌
    - API网关：处理客户端请求
    - 静态内容：容纳所有系统的内容
    - 管理：在节点上平衡服务并识别故障
    - 服务发现：查找微服务之间通信路径的指南。
    - 内容交付网络：代理服务器及其数据中心的分布式网络。
    - 远程服务：启用驻留在 IT 设备网络上的远程访问信息。

三、网关整理
    - Nacos
    - spring cloud

四、Nacos 整理

五、spring cloud整理

六、项目搭建项目