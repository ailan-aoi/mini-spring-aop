# mini-spring-aop

手写的迷你 IoC 和 AOP。扫描注解生成 Bean，再用 JDK 或 CGLIB 代理套上拦截器链。

写于 2020 年，用来对照 Spring 里「容器怎么建对象、切面怎么包住方法」。

## 里面有什么

- 注解：`@Component`、`@Bean`、`@Autowired`、`@Qualifier`
- `BeanFactory`：按包名扫描，`getObject` 取出实例，并可挂上 `MethodIntercepter`
- `JDKProxy` / `CGLibProxy`：两种代理
- `IntercepterChain`：把多个拦截器串起来

源码在 `mini-spring-aop/src`，包名 `com.mec.aop`。目录是当时的 Eclipse 工程，依赖放在 `src/libs`（含 cglib）。

## 状态

学习代码，Java 包名和实现按最初上传的样子保留。仓库曾用名 `easySpringAop`，旧地址会重定向到这里。
