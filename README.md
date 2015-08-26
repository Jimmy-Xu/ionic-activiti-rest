## source

### ionic

Ref: http://ccoenraets.github.io/ionic-tutorial

	git clone https://github.com/ccoenraets/ionic-tutorial.git

### activiti-rest

Ref: https://github.com/Activiti/Activiti/tree/master/modules/activiti-webapp-rest2

	git clone https://github.com/Activiti/Activiti.git


## usage

### 运行activiti-webapp-rest2

1、安装依赖

下载并安装 Apach Tomcat 7.0
下载并安装jdk 1.7


2、导入项目到Intellij IDEA
Intellij IDEA中import maven项目(选中pom.xml) Activiti-activiti-5.18.0\modules\activiti-webapp-rest2

3、Intellij IDEA的Run Configuration中，创建Tomcat Server
Deployment的Application context 设置为/activiti-rest

4、修改配置，以支持跨域
修改Activiti-activiti-5.18.0\modules\activiti-webapp-rest2\src\main\webapp\WEB-INF\web.xml，增加CORSFilter的配置

修改Activiti-activiti-5.18.0\modules\activiti-webapp-rest2\pom.xml
增加cors-filter-2.4.jar和java-property-utils-1.9.1.jar的配置

5、Run

6、测试
curl -s --header "Authorization:Basic a2VybWl0Omtlcm1pdA==" http://localhost:8080/activiti-rest/service/identity/users/


### 运行ionic-tutorial

cd conference
ionic serve

点Login，用户名密码都为kermit，浏览器console里，能看到后端返回的数据就表示成功
