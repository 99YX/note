

# spring

## 第一章 IOC技术

### 1.1 IOC 概念

  由容器进行 控制反转，创建对象，对象属性赋值。

### 1.2 IOC 优点

​     解耦合

### 1.3 创建对象方式

​     反射，new ,序列化，容器创建，动态代理

### 1.4 配置文件

![屏幕截图 2022-07-13 155506](C:\Users\26414\Desktop\日常学习\图片\屏幕截图 2022-07-13 155506.png)

![屏幕截图 2022-07-14 153428](C:\Users\26414\Desktop\日常学习\图片\屏幕截图 2022-07-14 153428.png)

### 1.5 创建对象的时间

在创建容器的时候，就会调用无参数的构造方法，完成对象的创建。由几个bean,就有几个对象

### 1.6 spring 当中的方法

```java
//定义字符串名，方便获取xml文件
String  xml="spring.xml";
//创建容器，将bean加载到容器中
ApplicationContext applicationContext=new ClassPathXmlApplicationContext(xml);
//创建对象 ,强制转换
UserService userServiceImpl =  (UserService)applicationContext.getBean("UserServiceImpl");
//调用方法
userServiceImpl.testAPP();

//获取对象的个数
int beanDefinitionCount = applicationContext.getBeanDefinitionCount();
System.out.println("-----个数------"+beanDefinitionCount);
//获取对象的名字
String[] beanDefinitionNames = applicationContext.getBeanDefinitionNames();
System.out.println("-----名字------"+beanDefinitionNames[0]);
```

### 1.7 属性注入

简单类型：基本类型和字符串

![属性赋值](C:\Users\26414\Desktop\日常学习\图片\属性赋值.png)

引用类型:

![引用类型赋值](C:\Users\26414\Desktop\日常学习\图片\引用类型赋值.png)



```java
@Test
public void springTest()
{
    //定义字符串名，方便获取xml文件
    String  xml="spring.xml";
    //创建容器，将bean加载到容器中
    ApplicationContext applicationContext=new ClassPathXmlApplicationContext(xml);
    //创建对象 ,强制转换
    UserService userServiceImpl =  (UserService)applicationContext.getBean("UserServiceImpl");
    //调用方法
    userServiceImpl.testAPP();

    //获取对象的个数
    int beanDefinitionCount = applicationContext.getBeanDefinitionCount();
    System.out.println("-----个数------"+beanDefinitionCount);
    //获取对象的名字
    String[] beanDefinitionNames = applicationContext.getBeanDefinitionNames();
    System.out.println("-----名字------"+beanDefinitionNames[0]);

    //获取student 对象
    Student student = (Student) applicationContext.getBean("Student");

    System.out.println(student);
}
```

```java
代码结果
我是抽象方法
-----个数------3
-----名字------UserServiceImpl
Student{name='yanxin', age=23, school=School{name='南京大学', address='学府路'}}
```

### 1.8 自动注入

![引用类型规则1](C:\Users\26414\Desktop\日常学习\图片\引用类型规则1.png)

![引用类型规则2](C:\Users\26414\Desktop\日常学习\图片\引用类型规则2.png)

### 1.8 多个配置文件

![多个配置文件](C:\Users\26414\Desktop\日常学习\图片\多个配置文件.png)

![通配符](C:\Users\26414\Desktop\日常学习\图片\通配符.png)

### 1.9 注解使用

component 注解

![Component注解](C:\Users\26414\Desktop\日常学习\图片\Component注解.png)

在配置文件当中配置组件扫描器

```java
<beans  <!-- 命名空间前缀，用前缀可以表示命名空间 -->
xmlns:context="http://www.springframework.org/schema/context"
  
xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd

http://www.springframework.org/schema/context

https://www.springframework.org/schema/context/spring-context.xsd"

   
     <!-- 声明组件扫描器 context前缀 component-scan标签（英文组件扫描的意思） -->
    <context:component-scan base-package="包路径"/>
   
 </beans>
```

