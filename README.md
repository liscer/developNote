配置记录
eclipse4.7 Tomcat7 1.1创建Dynamic Web项目修改output目录为/WebRoot/WEB-INF/classes,因为reloadable:如果这个属性设为true，tomcat服务器在运行状态下会监视在WEB-INF/classes和WEB-INF/lib目录下class文件的改动，如果监测到有class文件被更新的，服务器会自动重新加载Web应用。
1.2Tomcat的server.xml配置文件不是Tomcat的安装根目录conf中,是由eclipse指定,在工程目录/Servers/Tomcat v7.0 Server at localhost-config/server.xml
1.3run as server 相当于在/Servers/Tomcat v7.0 Server at localhost-config/server.xml中添加 
<Valve className="org.apache.catalina.valves.AccessLogValve" directory="logs" pattern="%h %l %u %t &quot;%r&quot; %s %b" prefix="localhost_access_log." suffix=".txt"/>
      <Context docBase="huihui" path="/huihui" reloadable="true" source="org.eclipse.jst.jee.server:huihui"/></Host>
    </Engine>
