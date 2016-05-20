# ncae-doc-tomcat
#### 功能描述

本模板用于通过寄云 PaaS 平台，在您的私有 / 公有云快速搭建 Tomcat 应用运行环境；简化您的程序代码的上传配置流程；根据负载及系统资源使用情况，自动伸缩应用节点的数量，轻松实现自动运维。

#### 操作步骤

1. 指定您的云账户信息；
2. 指定运行应用环境的主机配置信息；
3. 指定您的程序代码获取路径；（目前支持通过 GitHub 项目路径获取，和通过 URL 获取 war/zip/tar.gz 源码包）  
  https://github.com/neucloud-ncae/ncae-example-tomcat.git  
  http://neucloud.oss-cn-beijing.aliyuncs.com/softwares/ncae/ncae-example-tomcat.war  
  http://neucloud.oss-cn-beijing.aliyuncs.com/softwares/ncae/ncae-example-tomcat-master.zip
4. 指定您程序后端数据库的连接信息：数据库地址、数据库库名、数据库用户、数据库密码；（此步骤可选，这些选项默认为空值）
5. 执行部署操作；
6. 部署执行成功后，根据平台提供的方式登录服务器，完成您所上传应用的后续配置。
7. 根据实例详情下的访问地址进行访问。


#### 常见问题

##### 如何配置数据库连接？

您之前所填写的数据库连接信息，都在应用服务器中以环境变量的形式进行了映射，其对应关系：
> 数据库地址：DB_ADDR  
数据库库名：DB_NAME  
数据库用户：DB_USER  
数据库密码：DB_PASSWORD  

##### Tomcat管理员帐号密码？

>帐号：tomcat  
密码：tomcat  
配置文件：/usr/local/apache-tomcat-7.0.56/conf/tomcat-users.xml

##### 程序目录？

项目被放置于 /usr/local/apache-tomcat-7.0.56/webapps/ 路径下，请您自行根据项目的路径结构调整相关配置。


