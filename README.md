本次是在docker中进行安装
参考的安装博客如下所示
https://www.yuque.com/u552836/rospxv/ehz3l

# ranger
python2.7
安装在ubuntu系统的docker环境下
在ranger-admin中
#此参数表示数据库脚本单独执行
setup_mode=SeparateDBA

#数据库类型
DB_FLAVOR=MYSQL
#连接mysql的jar包所在位置
SQL_CONNECTOR_JAR=/u01/app/apache-hive-2.3.4-bin/lib/mysql-connector-java-5.1.47.jar

db_root_user=root
db_root_password=输入密码
db_host=10.200.4.117
db_name=ranger
db_user=root
db_password=输入密码

#设置Ranger里面的用户密码
rangerAdmin_password=输入密码
rangerTagsync_password=输入密码
rangerUsersync_password=输入密码
keyadmin_password=输入密码

#禁用audit审计，如需开启，需安装solr
#audit_store=solr
#audit_solr_urls=
#audit_solr_user=
#audit_solr_password=
#audit_solr_zookeepers=
#***********禁用audit审计，如需开启，需安装solr这步很关键，一直访问不到可视化界面

#**********在安装过程中，./set_globals.sh这步很关键，没有这步出现很奇怪的报错
接着，运行set_globals.sh

# ./set_globals.sh 
usermod: no changes
[2019/11/27 21:54:32]:  [I] Soft linking /etc/ranger/admin/conf to ews/webapp/WEB-INF/classes/conf
