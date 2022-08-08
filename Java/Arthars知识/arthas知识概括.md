<!--
 * @Author: MrDeng
 * @Date: 2022-08-06 15:51:18
 * @LastEditTime: 2022-08-07 08:43:08
 * @LastEditors: dengjuming
 * @Description: arthas基本使用总结
 * @FilePath: /advanced-learning/spring/Arthars知识/arthas知识概括.md
-->

一、基本整理
- jvm知识点
  - 新生代
    - 首先对象在Eden区，如果Eden区满了，但是晋升条件不足，就进入 s0，如果s0满了就去s1
    - 对象每经历一次Minor GC，年龄加1
    - 晋升年龄阈值，MaxTenuringThreshold，默认值 15次
    - gc名称：Minor Gc
    - 算法方式：复制算法
  - 老年代
    - 新生代经历N次Gc后，仍然存活，就会被放到老年代
    - gc名称：Full Gc
    - 算法方式：标记-清理或标记-整理算法
  - 持久代
    - 主要存放元数据，例如：Class、Method的元信息，该区域划分对垃圾回收影响不大
- 进行调优
  - 记录好日志；
  - 对程序做好性能监控；
  - 根据日志和性能监控数据修改程序；
  - 使用专业工具通过不同的JVM参数进行压测并获得最佳配置。
