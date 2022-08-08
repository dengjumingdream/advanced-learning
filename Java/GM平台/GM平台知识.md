<!--
 * @Author: MrDeng
 * @Date: 2022-07-29 10:43:30
 * @LastEditTime: 2022-08-04 11:42:16
 * @LastEditors: dengjuming
 * @Description: GM平台后端知识整理
 * @FilePath: /advanced-learning/spring/GM平台知识.md
-->

一、注解
  - EnableSwagger2
    - 引入swagger，通过注解生成对应文档。
  - SpringBootApplication(集成了三个注解)
    - ComponentScan：
      - 用来自动扫描被这些注解注释的类，最终生成ioc容器里的bean；
      - 默认扫描范围 root package子包下边，还可自定义扫描位置；
    - EnableAutoConfiguration
      - springboot自动化配置的核心注解，通过Import注解，动态加载所需的bean
    - SpringBootConfiguration
      - 和Configuration注解一样，都是用来声明这是配置类；
  - Import
    - 将类导入springIoc容器中
    - 导入@Configuration注解的配置类
    - 声明一个bean
  - TomcatConfiguration
    - 导入TomcatConfiguration配置类，通过该类实现多接口访问项目；

二、spring 四大注解
  - Service
    - 该注解主要针对于业务逻辑层（service层）
  - Repository
    - 该注解主要针对于数据访问层的（Dao，持久化层）
  - Component
    - 该注解不属于任何层，当该类不知道属于以上三类的那一类时可以使用该注解。
  - Controller
    - 该注解主要针对于控制器层（servlet层 ，Controller层）

三、Springboot内置容器
  - Jettey容器
  - Tomcat容器
  - undertow容器

四、启动流程
  - 加载初始化参数
  - 加载容器并启动

五、springIOC容器
  - 解耦各业务对象间依赖关系的对象绑定方式；
  - beanFactory和ApplicationContext；
  - 对Bean进行实例化、装配和管理
  - 基本属性 - BeanDefinition（元属性）
    - 类全名
    - Bean的行为配置元素：作用域、生命周期
    - 其他Bean的引用，依赖项
    - 其他配置，例如：连接池的连接数配置等等

六、aop切面
  - aop的应用场景：
    -  监控方法运行时间 （监控性能）
    -  权限控制
    -  缓存优化 （第一次调用查询数据库，将查询结果放入内存对象， 第二次调用， 直接从内存对象返回，不需要查询数据库 ）

七、shrio权限管理
 - 权限管理模型
 - shrio和 Security区别
   - shrio是Apache提供的
   - Security是spring的亲儿子，全家桶里头的
   - 其他没啥区别
 - 详解
   - Subject
   - SecurityManager
   - Realm

八、数据持久化
 - mybatis-plus

九、redis管理
 - 用户token管理
 - saveLog功能管理
 - pip管道管理
 - jedis控制


十、代码模板
 - 结合mybatis-plus构建前后端代码，通过实体表构建代码

十一、arthas使用
 - 调优
 - 查看具体类
 - 查看堆栈等等
 - agent探针

十二、高并发压测(jmeter)

十三、netty压测工具

十四、gitlab使用
 - gitCZ代码规范
 - pipline使用
 - runner使用
 - mvn私有源

十五、vue.js功能
 - 前端的那几样东西，react也是的
 - 路由功能
 - 生命周期
 - store

十六、webpack打包
 - 打包优化等等
 - cdn

十七、loader
 - 高级语法处理
 - less、css等等处理

十八、es6

十九、nrm、nvm等等处理

二十、首页优化

二十一、nginx配置

二十二、mysql处理

二十三、网关分发rabbitMQ处理
