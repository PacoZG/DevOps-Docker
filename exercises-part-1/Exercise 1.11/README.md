# Commands used

```bash
$ docker build . -t exer-1-11
```

```bash
$ docker run -p 3000:8080 exer-1-11
```

## result:
```
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.1.3.RELEASE)

2022-05-02 06:55:24.027  INFO 1 --- [           main] c.d.dockerexample.DemoApplication        : Starting DemoApplication v1.1.3 on 5dd39aa4f98e with PID 1 (/usr/src/app/target/docker-example-1.1.3.jar started by root in /usr/src/app)
2022-05-02 06:55:24.028  INFO 1 --- [           main] c.d.dockerexample.DemoApplication        : No active profile set, falling back to default profiles: default
2022-05-02 06:55:24.714  INFO 1 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8080 (http)
2022-05-02 06:55:24.735  INFO 1 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2022-05-02 06:55:24.735  INFO 1 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.16]
2022-05-02 06:55:24.745  INFO 1 --- [           main] o.a.catalina.core.AprLifecycleListener   : The APR based Apache Tomcat Native library which allows optimal performance in production environments was not found on the java.library.path: [/usr/lib/jvm/java-1.8-openjdk/jre/lib/aarch64/server:/usr/lib/jvm/java-1.8-openjdk/jre/lib/aarch64:/usr/lib/jvm/java-1.8-openjdk/jre/../lib/aarch64:/usr/java/packages/lib/aarch64:/lib:/usr/lib]
2022-05-02 06:55:24.790  INFO 1 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2022-05-02 06:55:24.790  INFO 1 --- [           main] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 733 ms
2022-05-02 06:55:24.918  INFO 1 --- [           main] o.s.s.concurrent.ThreadPoolTaskExecutor  : Initializing ExecutorService 'applicationTaskExecutor'
2022-05-02 06:55:25.000  INFO 1 --- [           main] o.s.b.a.w.s.WelcomePageHandlerMapping    : Adding welcome page template: index
2022-05-02 06:55:25.117  INFO 1 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
2022-05-02 06:55:25.119  INFO 1 --- [           main] c.d.dockerexample.DemoApplication        : Started DemoApplication in 1.304 seconds (JVM running for 1.545)
2022-05-02 06:55:32.705  INFO 1 --- [nio-8080-exec-1] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring DispatcherServlet 'dispatcherServlet'
2022-05-02 06:55:32.705  INFO 1 --- [nio-8080-exec-1] o.s.web.servlet.DispatcherServlet        : Initializing Servlet 'dispatcherServlet'
2022-05-02 06:55:32.708  INFO 1 --- [nio-8080-exec-1] o.s.web.servlet.DispatcherServlet        : Completed initialization in 3 ms
```

## result in broswer:
![Success](./browser-result.png)