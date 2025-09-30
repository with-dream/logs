# kotlin大纲

Kotlin-Study/\
├── 一、学习准备\
│ ├── Kotlin 简介与应用场景\
│ │ ├── Kotlin 语言发展历史\
│ │ ├── Kotlin 与 Java 对比\
│ │ └── Kotlin 在 Android、后端、跨平台中的应用\
│ ├── 开发环境\
│ │ ├── IntelliJ IDEA、Android Studio\
│ │ ├── Gradle Kotlin DSL\
│ │ └── Ktor 项目初始化\
│ └── 运行机制\
│ ├── Kotlin 编译流程\
│ ├── Kotlin 与 JVM 字节码\
│ └── Kotlin/Native 与 Kotlin/JS 概览\
│\
├── 二、Kotlin 基础语法\
│ ├── 变量与数据类型\
│ │ ├── val / var\
│ │ ├── 类型推断\
│ │ └── 基本类型与字符串模板\
│ ├── 控制流\
│ │ ├── if 表达式\
│ │ ├── when 表达式\
│ │ └── for / while 循环\
│ ├── 函数\
│ │ ├── 默认参数与命名参数\
│ │ ├── 单表达式函数\
│ │ └── 可变参数 vararg\
│ └── 包与可见性修饰符\
│\
├── 三、面向对象与类\
│ ├── 类与对象\
│ │ ├── 主构造函数与次构造函数\
│ │ ├── 属性与字段\
│ │ └── data class 与解构声明\
│ ├── 继承与多态\
│ │ ├── open / final / abstract\
│ │ ├── 接口与默认实现\
│ │ └── sealed class\
│ ├── 对象与单例\
│ │ ├── object 关键字\
│ │ ├── 伴生对象\
│ │ └── object 表达式（匿名对象）\
│ └── 委托\
│ ├── 类委托 by\
│ ├── 属性委托（lazy、observable）\
│ └── 自定义委托\
│\
├── 四、函数式编程\
│ ├── 高阶函数\
│ │ ├── 函数类型\
│ │ ├── Lambda 表达式\
│ │ └── 内联函数 inline\
│ ├── 扩展与运算符重载\
│ │ ├── 扩展函数与属性\
│ │ ├── 中缀表达式 infix\
│ │ └── 运算符重载 operator\
│ └── Kotlin 标准函数\
│ ├── let、apply、run、also、with\
│ └── scope functions 的应用场景\
│\
├── 五、集合与泛型\
│ ├── Kotlin 集合框架\
│ │ ├── 不可变集合 List/Set/Map\
│ │ ├── 可变集合 MutableList/MutableSet/MutableMap\
│ │ └── 集合操作符（map、filter、reduce、fold）\
│ ├── 泛型\
│ │ ├── 泛型类与泛型函数\
│ │ ├── 型变：out、in\
│ │ └── 星投影 \*\
│ └── 序列（Sequence）\
│ ├── 惰性求值\
│ └── 与集合的对比\
│\
├── 六、空安全与类型系统\
│ ├── 可空类型与安全调用\
│ │ ├── ?\
│ │ ├── ?. 与 ?:\
│ │ └── !!\
│ ├── lateinit 与 lazy\
│ ├── 智能类型转换\
│ ├── 类型别名 typealias\
│ └── 内联类与值类 value class\
│\
├── 七、协程与并发\
│ ├── 协程基础\
│ │ ├── 挂起函数 suspend\
│ │ ├── 协程作用域 CoroutineScope\
│ │ └── Job 与取消\
│ ├── 协程调度\
│ │ ├── Dispatchers.Default、IO、Main\
│ │ └── withContext 切换线程\
│ ├── Flow\
│ │ ├── 冷流与热流\
│ │ ├── 中间操作与终止操作\
│ │ └── SharedFlow、StateFlow\
│ └── 通道（Channel）\
│ ├── 发送与接收\
│ ├── 缓冲通道\
│ └── Select 表达式\
│\
├── 八、反射与元编程\
│ ├── Kotlin 反射\
│ │ ├── KClass、KCallable\
│ │ ├── 获取属性与方法\
│ │ └── 调用成员\
│ ├── 注解与注解处理\
│ │ ├── Kotlin 注解定义\
│ │ ├── APT 与 KAPT\
│ │ └── Kotlin Symbol Processing（KSP）\
│ └── Kotlin 编译器插件\
│ ├── 编译器前端与中间表示 IR\
│ ├── 编译器插件开发入门\
│ └── 常见插件示例\
│\
├── 九、性能与优化\
│ ├── 内存管理\
│ │ ├── JVM 上的 Kotlin 内存模型\
│ │ └── Kotlin/Native 的内存管理\
│ ├── 协程性能优化\
│ │ ├── 调度器选择\
│ │ ├── 背压与取消\
│ │ └── 缓冲优化\
│ └── 性能分析工具\
│ ├── JMH\
│ ├── Android Profiler\
│ └── LeakCanary\
│\
└── 十、安全与规范\
├── 代码规范\
│ ├── Kotlin 官方 Coding Conventions\
│ ├── Ktlint\
│ └── Detekt\
├── Android 安全\
│ ├── ProGuard 与 R8\
│ ├── Keystore\
│ └── 安全存储\
└── 常见漏洞防护\
├── SQL 注入\
├── XSS\
└── CSRF
