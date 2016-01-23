# phpinstall
Centos6.6下安装php
一、安装mysql 

#yum -y install mysql mysql-server mysql-devel 

配置mysql开机启动服务 

#chkconfig --add mysqld (在服务清单中添加mysql服务) 

#chkconfig mysqld on (设置mysql服务随开机启动) 

#service mysqld start (启动mysql服务) 

二、安装PHP 

#yum -y install php 

#service httpd restart (重启apache) 

#vi /var/www/html/index.php 
<?php 
phpinfo(); 
?> 
保存退出，用IE访问http://youdomain.com/ 如果输出了phpinfo信息说明你的php安装成功了。 

三、安装php的相关组件 

#yum search php (搜索php相关的组件) 

#yum -y install php-mysql php-gd php-imap php-ldap php-odbc php-pear php-xml php-xmlrpc 

安装完成后重启apache服务 

#service httpd restart 
