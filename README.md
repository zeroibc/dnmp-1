# dnmp
怀着忐忑的心情上传了我的第一个github项目
刚接触Docker没多久，这个练手的 希望大家多多指教

在此之前先要了解docker一些基本用法 我学习docker的记录：https://jlmvp.cn/

首先确保你安装了docker和docker-compse以及git

# 开始
1、将项目clone到本地
![Image text](https://github.com/MichealJl/dnmp/blob/master/1.jpg)

2、进入dnmp将env-example 重命名为.env

3、配置env中你所需要设置的环境变量
![Image text](https://github.com/MichealJl/dnmp/blob/master/2.jpg)

4、在docker-compose.yml目录 执行docker-compose config 你可以看到完整配置信息
![Image text](https://github.com/MichealJl/dnmp/blob/master/3.jpg)

5、执行docker-compose up -d  （额。。安装php的那些扩展挺慢的 你可以酌情 修改php目录下的Dockerfile，等用的到那些扩展的时候 再装）
![Image text](https://github.com/MichealJl/dnmp/blob/master/4.jpg)

安装成功之后显示如下
![Image text](https://github.com/MichealJl/dnmp/blob/master/5.jpg)

6、修改nginx的配置文件 nginx/conf.d/default.conf
![Image text](https://github.com/MichealJl/dnmp/blob/master/6.jpg)

![Image text](https://github.com/MichealJl/dnmp/blob/master/7.jpg)

![Image text](https://github.com/MichealJl/dnmp/blob/master/8.jpg)

![Image text](https://github.com/MichealJl/dnmp/blob/master/9.jpg)

7、重启nginx服务

8、在你的项目目录下创建index.php 输出phpinfo(); 
![Image text](https://github.com/MichealJl/dnmp/blob/master/10.jpg)

执行 

ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';

flush privileges;
