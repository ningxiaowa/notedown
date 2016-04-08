#常用Linux命令
1. 远程登录Linux服务器  
  $ ssh root@123.57.55.74
2. Centos  
  $ yum update //更新  
  $ yum -y install mariadb* //安装mysql数据库  
  $ systemctl start mariadb.service  
  $ systemctl enable mariadb.service  
  $ mysql_secure_installation //mysql安全设置  
  //新建mysql远程用户  
  CREATE USER 'angel'@'%' IDENTIFIED BY 'Angel@2015';  
  GRANT ALL PRIVILEGES ON *.* TO 'angel'@'%'; ##第一个*是指全部数据库, 可以指定某一个  
  flush privileges;  
3. 安装jdk  
进入oracle java官网寻找最新的JDK地址，在以下代码中url替换最新的jdk地址。  
//没办法直接通过wget下载，需要cookie  
wget --no-check-certificate --no-cookies --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com" "http://download.oracle.com/otn-pub/java/jdk/7u15-b03/jdk-7u15-linux-x64.rpm"  
  $ yum install jdk-7u15-linux-x64.rpm  
4. 修改权限  
  $ chmod -R 777 aaa.tar.gz  
5. 解压  
  $ tar -xzvf aaa.tar.gz  
6. tomcat  
  $ catalina run  
webapp的根目录(CATALINA_HOME)为:/usr/local/Cellar/tomcat/7.0.33/libexec/webapps/ROOT/