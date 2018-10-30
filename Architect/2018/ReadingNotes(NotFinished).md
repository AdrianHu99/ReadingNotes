http://www.infoq.com/cn/minibooks/architect-201810?utm_source=minibooks_about_architect&utm_medium=link&utm_campaign=architect



1. JEP 328: Flight Recorder(JFR) - JFR 是一套集成进入JDK和JVM内部的事件机制框架，通过良好的架构和设计的框架，硬件层面的极致优化，生产环境的广泛验证，
它可以做到极致的可靠和低开销。
我们可以随时主动开启JFR 进行特定诊断，也可以让系统长期运行JFR。
    - 对锁竞争、阻塞、延迟，JVM GC、SafePoint等领域，进行细粒度分析；
    - 深入JIT Compiler内部，全面把握热点方法、内联、逆优化等等；
    - JFR 提供了标准的JAVA API，可以与各种层面进行定制、集成，为复杂的企业应用栈或者复杂的分布式应用，提供ALL-IN-ONE的解决方案。
    
2. JEP 331：Low-Overhead Heap Profiling
高效了解在JAVA堆上都进行了哪些对象分配，是诊断内存问题的基本出发点之一。


3. KVS 数据库  ANNA 1.0
http://db.cs.berkeley.edu/jmh/papers/anna_ieee18.pdf
https://zhuanlan.zhihu.com/p/34603927
https://github.com/fluent-project/fluent/tree/master/kvs
https://arxiv.org/pdf/1809.00089.pdf

4. !!!架构师如何判断技术演进的方向
基于业务发展阶段进行判断，这也是为什么架构师必须具备业务理解能力的原因。不同的行业业务发展路径、轨迹、模式不一样，架构师必须能够基于行业发展和企业自身
情况做出准确判断。

5. Kubernetes
设计不应针对故障，而应该针对恢复

