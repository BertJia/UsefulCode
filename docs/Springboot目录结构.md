# src.main
一、代码层结构
## java
### com.atticwind.demo
 顶级域名.公司.项目
#### Application.java
1. 启动类(Application.java)推荐放在根目录com.atticwind.demo包下
#### domain
2. 实体类(domain)
    A: com.atticwind.demo.domain(jpa项目)
    B: com.atticwind.demo.pojo(mybatis项目)
#### mapper
3. 数据接口访问层(Dao)
    A: com.atticwind.demo.repository(jpa项目)
    B: com.atticwind.demo.mapper(mybatis项目)
#### service
4. 数据服务接口层(Service)推荐：com.atticwind.demo.service
##### impl
5. 数据服务实现层(Service Implements)推荐：com.atticwind.demo.service.impl
#### controller
6. 前端控制器层(Controller)推荐：com.atticwind.demo.controller
#### utils
7. 工具类库(utils)推荐：com.atticwind.demo.utils
#### config
8. 配置类(config)推荐：com.atticwind.demo.config
#### dto
9. 数据传输对象(dto)推荐：com.atticwind.demo.dto
   数据传输对象(Data Transfer Object)用于封装多个实体类(domain)之间的关系，不破坏原有的实体类结构
#### vo 
10. 视图包装对象(vo)推荐：com.atticwind.demo.vo
    视图包装对象(View Object)用于封装客户端请求的数据，防止部分数据泄露(如：管理员ID)，保证数据安全，不破坏   原有的实体类结构
## resources
二、资源目录结构
### application.properties
1. 项目配置文件：resources/application.properties
### static
2. 静态资源目录：resources/static/
   用于存放html、css、js、图片等资源
### templates
3. 视图模板目录：resources/templates/
   用于存放jsp、thymeleaf等模板文件
### logback-spring.xml
### _mapper_
_4. mybatis映射文件：resources/mapper/(mybatis项目)_
_5. mybatis配置文件：resources/mapper/config/(mybatis项目)_
