# test-spring-boot-starter
1.自定义spring-boot-start步骤:
  1、创建一个maven工程，
      非官方的自定义spring-boot starter命名规范{name}-spring-boot-starter
  2、引入必要的依赖
      Maven配置文件引入：
      <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-autoconfigure</artifactId>
            <version>2.0.0.RELEASE</version>
          </dependency>
          <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-configuration-processor</artifactId>
            <version>2.0.0.RELEASE</version>
            <optional>true</optional>
          </dependency>
      </dependencies>    
   3、自定义自己的Properties类
   4、编写starter核心服务类  
   5、编写自动配置类
   6、src/main/resources/META-INF/spring.factories
     手动创建META-INF/spring.factories,配置
     org.springframework.boot.autoconfigure.EnableAutoConfiguration=\
     com.jt.PersonServiceAutoConfiguration
