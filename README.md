# .NETCORE.HighConcurrentArchitecture

一个基础的.NET CORE 轻量级高并发服务端结构
上手简单易用无门槛

实际使用请根据系统业务情况合理修改 日志和单元测试根据喜好自行完善

联系作者:290330505@qq.com

使用第三方软件

https://dev.mysql.com/downloads/
https://www.rabbitmq.com/
https://redis.io/

https://github.com/2881099/csredis
https://github.com/StackExchange/Dapper

https://github.com/travist/jsencrypt

20191023
--更新至.NET CORE3.0 
新增自定义授权策略
新增数据库创建脚本

主要包括JWTTOKEN的验证实现

RSA加密传输

权限中间件

RabbitMQ队列和Mysql数据库连接池

连接池不会每次请求都创建数据库或MQ连接，最多只会创建指定数量的连接，当连接不可用或丢失，将会重新创建连接，并在调用以后重置为可用状态，进入空闲队列以供其它请求使用,并不会释放。

采用Dapper访问Mysql

采用Redis作为读取缓存

采用RabbitMQ和独立后台进行MySQL写入

Redis缓存实现 RedisCore内部自带连接池

数据同步服务
运行

cd dir

dotnet restore  //获取依赖

dotnet build    //编译  

dotnet run      //运行
 

