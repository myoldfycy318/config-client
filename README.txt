resource文件需要配置为bootstrap.yml



其配置文件bootstrap.properties：

spring.application.name=config-client
spring.cloud.config.label=master
spring.cloud.config.profile=dev
spring.cloud.config.uri= http://localhost:8888/
server.port=8881

spring.cloud.config.label 指明远程仓库的分支
spring.cloud.config.profile

dev开发环境配置文件
test测试环境
pro正式环境
spring.cloud.config.uri= http://localhost:8888/ 指明配置服务中心的网址。

===============================================
http://localhost:8881/hi
client调用接口hi的时候，传给server的数据就是配置文件里面的name，profile，可以这么理解：
http://localhost:8881/hi = http://localhost:8888/config-client/dev