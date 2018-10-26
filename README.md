独立门锁服务的文件结构

    jre----------------------运行环境，目前采用1.6

    lib----------------------依赖包文件，包括自己编写的接口包也得放进

    logs---------------------日志，根据log4j，可自行配置

    resources----------------动态库文件存放目录

    doorcard.properties------门锁的常用配置文件

    log4j.properties---------日志配置

    mutex.lock---------------共享占有文件通道

    server.properties--------独立服务端配置，设置服务超时等参数

    启动门卡接口.bat---------启动程序。



重点是lib目录下的几个自己开发包：

    ItfHandlerUtils---------制定的所有接口类型的方法规范，不用修改，源码可参考
	
	https://github.com/tq835465605/ItfHandlerUtils

    DoorCard_Server---------整个接口服务的主框架代码，不用修改，源码可参考
	
	https://github.com/tq835465605/DoorCard_Server

    Chuangjia---------------需要自己编写，根据不同门锁，开发不同的类型，源码可参考
	
	https://github.com/tq835465605/ChuangJia


类加载逻辑是采用spi加载模式。

门锁类别的服务端只需要自己写类似ChuangJia的源码即可
