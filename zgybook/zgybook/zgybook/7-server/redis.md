# redis

## 预配环境  
1. linux环境
> 安装及配置  
```
# /usr/local路径，解压
tar -zvxf redis-6.2.6.tar.gz
# /usr/local路径，修改文件夹
mv redis-6.2.6 /usr/local/redis
# /usr/local/redis路径，编译
make
# /usr/local/redis路径，安装
make PREFIX=/usr/local/redis install


# /usr/local/redis路径，编辑redis.conf文件
1、将bind 127.0.0.1 -::1注释
2、protected-mode yes 改为 no
3、daemonize no 改为 yes
```

具体参考：[https://www.cnblogs.com/hunanzp/p/12304622.html](https://www.cnblogs.com/hunanzp/p/12304622.html)

> 开机自启脚本
```
cp /usr/local/redis/utils/redis_init_script /etc/init.d/redis
vi /etc/init.d/redis

修改redis-server、redis-cli、redis.conf路径
开头!sh后添加注释
# chkconfig: 2345 90 10
# description: Redis is a persistent key-value database

# /etc/init.d/路径下
chmod +x /etc/init.d/redis
chkconfig --add redis
chkconfig redis on

service autojar.sh start/stop
```

具体参考：[https://developer.aliyun.com/article/789869](https://developer.aliyun.com/article/789869)

2. win10环境
更新中...
## **相关介绍**  
介绍redis的内容  
## **相关资源**  
runoob资源网：[https://www.runoob.com/redis/redis-tutorial.html](https://www.runoob.com/redis/redis-tutorial.html) 

```





