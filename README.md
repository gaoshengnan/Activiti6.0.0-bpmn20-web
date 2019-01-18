# Activiti6.0.0工作流引擎的web程序设计器

### 一、流程设计器环境搭建步骤

1. 首先在[Activiti](https://www.activiti.org/)官网下载activiti6.0.0
2. 然后下载[Tomcat8.0.53](http://mirror.bit.edu.cn/apache/tomcat/)
3. 最后把activiti-6.0.0/wars/activiti-admin.war 和 activiti-6.0.0/wars/activiti-app.war放到tomcat的webapp目录下

### 二、Activiti6.0.0-bpmn20-web
Activiti6.0.0-bpmn20-web是我搭建好的Web流程设计器环境，可以直接clone项目到本地启动，就可以在线设计工作流引擎流程图，命令如下：

> git clone https://github.com/gaoshengnan/Activiti6.0.0-bpmn20-web.git

拉下代码之后打开Terminal，启动Tomcat
<div align="left"><img src="/picture/startTomcat.png" height="180" width="500" >

> 访问[http://localhost:8080/activiti-admin](http://localhost:8080/activiti-admin)，用户名 username：admin   |  密码 password：admin
<div align="left"><img src="/picture/loginAdmin.png" height="300" width="600" >

> 这里默认的Server port是9999，修改端口号为8080，设置app的密码为test
<div align="left"><img src="/picture/updatePortPass.png" height="350" width="530" >

> 并点击【Check Activiti Rest endpoint】测试一下
<div align="left"><img src="/picture/check.png" height="240" width="600" >


> 然后访问[http://localhost:8080/activiti-app](http://localhost:8080/activiti-app)，用户名 username：admin | 密码 password：test
<div align="left"><img src="/picture/loginApp.png" height="370" width="750" >

> 现在可以开始设计流程图了～～～

<div align="left"><img src="/picture/appMain.png" height="230" width="800" >
<div align="left"><img src="/picture/bpmn.png" height="460" width="950" >



### 默认h2数据库改成mysql数据库
activiti默认配置h2的数据库，当重新启动Tomcat，设计好的流程图就被清空，可以配置成自己的mysql数据库，修改这个路径下的配置：

> apache-tomcat-8.0.53/webapps/activiti-app/WEB-INF/classes/META-INF/activiti-app/activiti-app.properties
  
<div align="left"><img src="/picture/data.png" height="300" width="550" >

> 注意：切换时如果出现问题可以查看这片故障排查记录[记录ActivitiWeb流程设计器从h2转成mysql线上故障排查
](http://seina.top/2019/01/17/activitiWebH2ToMysql/)


