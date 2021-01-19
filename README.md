## 开发工具 
IntelliJ IDEA 2020.2.2 x64
## 开发环境				

| JAVA |Maven | Mysql |SpringBoot | redis |RabbitMQ|
|--|--|--|--|--|--|
|15 | 3.2.2 | 5.5 | 1.5.9 | 3.2 |3.7.14|

## 部署说明

1. 下载代码 git clone https://github.com/bjtuql/miaosha
2. 安装redis、mysql、rabbitmq、java等环境
3. 在navicate中运行sql文件夹下的sql文件
4. 项目导入idea
5. 到src/main/resources下的application.properties下修改你的数据库链接用户名与密码，主要是mysql数据库和redis数据库
6. 启动前，检查配置 application.properties 中相关redis、mysql、rabbitmq地址
7. ![image-20210119194223558](C:\Users\mujou\AppData\Roaming\Typora\typora-user-images\image-20210119194223558.png)
8. 在数据库秒杀商品表里面设置合理的秒杀开始时间与结束时间
9. 登录地址：http://localhost:8080/login/to_login
10. 商品秒杀列表地址：http://localhost:8080/goods/to_list

## 项目描述
1. 使用分布式Seesion，可以让多台服务器可以响应。
2. 使用redis做缓存提高访问速度和并发量，减少数据库压力。
3. 使用页面静态化，缓存页面至浏览器，前后端分离降低服务器压力。
4. 使用消息队列完成异步下单，提升用户体验，削峰和降流。
5. 安全性优化：双重md5密码校验，秒杀接口地址的隐藏，接口限流防刷，数学公式验证码。

**项目说明文档在docs文件夹里面**

