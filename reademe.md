# Tomcat8 源码注释

## idea配置
1.添加VM options:
```
-Dcatalina.home=catalina-home
-Dcatalina.base=catalina-home
-Djava.endorsed.dirs=catalina-home/endorsed
-Djava.io.tmpdir=catalina-home/temp
-Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager
-Djava.util.logging.config.file=catalina-home/conf/logging.properties
-Duser.language=en
-Duser.region=EN
```
2.org.apache.catalina.startup.ContextConfig  第778行加上如下代码
```
778: context.addServletContainerInitializer(new JasperInitializer(),null);
```
## tomcat的启动过程：
org.apache.catalina.startup.Bootstrap

### 2.1.static 静态代码块

### 2.2.main 方法