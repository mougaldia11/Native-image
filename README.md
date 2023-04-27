# Native-image
J'ai essayé d'utiliser le plugin org.graalvm.buildtools:native-maven-plugin
La construction de l'image native a réussi sauf que j'arrive pas à exécuter l'exécutable.
j'ai la sortie ci-dessous :

'''

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::               (v2.7.11)

16:12:54.092 [main] INFO org.springframework.boot.SpringApplication - Starting application using Java 11.0.18 on WX-OR6211599 with PID 106310 (started by galaye in /home/galaye/demo)
16:12:54.098 [main] DEBUG org.springframework.boot.SpringApplication - Running with Spring Boot v2.7.11, Spring v5.3.27
16:12:54.102 [main] INFO org.springframework.boot.SpringApplication - No active profile set, falling back to 1 default profile: "default"
16:12:54.103 [main] DEBUG org.springframework.boot.SpringApplication - Loading source class com.example.helloworld.demo.DemoApplication
16:12:54.119 [main] DEBUG org.springframework.context.annotation.AnnotationConfigApplicationContext - Refreshing org.springframework.context.annotation.AnnotationConfigApplicationContext@3f05449e
16:12:54.122 [main] DEBUG org.springframework.beans.factory.support.DefaultListableBeanFactory - Creating shared instance of singleton bean 'org.springframework.context.annotation.internalConfigurationAnnotationProcessor'
16:12:54.129 [main] WARN org.springframework.context.annotation.AnnotationConfigApplicationContext - Exception encountered during context initialization - cancelling refresh attempt: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'org.springframework.context.annotation.internalConfigurationAnnotationProcessor': Instantiation of bean failed; nested exception is org.springframework.beans.BeanInstantiationException: Failed to instantiate [org.springframework.context.annotation.ConfigurationClassPostProcessor]: No default constructor found; nested exception is java.lang.NoSuchMethodException: org.springframework.context.annotation.ConfigurationClassPostProcessor.<init>()
16:12:54.134 [main] ERROR org.springframework.boot.SpringApplication - Application run failed
org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'org.springframework.context.annotation.internalConfigurationAnnotationProcessor': Instantiation of bean failed; nested exception is org.springframework.beans.BeanInstantiationException: Failed to instantiate [org.springframework.context.annotation.ConfigurationClassPostProcessor]: No default constructor found; nested exception is java.lang.NoSuchMethodException: org.springframework.context.annotation.ConfigurationClassPostProcessor.<init>()
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateBean(AbstractAutowireCapableBeanFactory.java:1334)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1232)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:582)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:542)
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:335)
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234)
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:333)
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:213)
        at org.springframework.context.support.PostProcessorRegistrationDelegate.invokeBeanFactoryPostProcessors(PostProcessorRegistrationDelegate.java:106)
        at org.springframework.context.support.AbstractApplicationContext.invokeBeanFactoryPostProcessors(AbstractApplicationContext.java:748)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:564)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:731)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:408)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:307)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1303)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1292)
        at com.example.helloworld.demo.DemoApplication.main(DemoApplication.java:11)
Caused by: org.springframework.beans.BeanInstantiationException: Failed to instantiate [org.springframework.context.annotation.ConfigurationClassPostProcessor]: No default constructor found; nested exception is java.lang.NoSuchMethodException: org.springframework.context.annotation.ConfigurationClassPostProcessor.<init>()
        at org.springframework.beans.factory.support.SimpleInstantiationStrategy.instantiate(SimpleInstantiationStrategy.java:83)
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateBean(AbstractAutowireCapableBeanFactory.java:1326)
        ... 16 common frames omitted
Caused by: java.lang.NoSuchMethodException: org.springframework.context.annotation.ConfigurationClassPostProcessor.<init>()
        at java.base@11.0.18/java.lang.Class.getConstructor0(DynamicHub.java:3349)
        at java.base@11.0.18/java.lang.Class.getDeclaredConstructor(DynamicHub.java:2553)
        at org.springframework.beans.factory.support.SimpleInstantiationStrategy.instantiate(SimpleInstantiationStrategy.java:78)
        ... 17 common frames omitted
'''
