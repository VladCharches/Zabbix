MTN.*NIX.11 Zabbix
---

***Student***: [Uladzislau Charches](https://upsa.epam.com/workload/employeeView.do?employeeId=4060741400038705754#emplTab=general)

# Zabbix_Task3


**Screenshots**


![1](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/1.png)

![2](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/2.png)

![3](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/3.png)

![4](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/4.png)

![5](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/5.png)

![6](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/6.png)

![7](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/7.png)

![8](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/8.png)

![9](https://github.com/VladCharches/Zabbix/blob/Task3/Screens/9.png)

1. Yum install Javajdk Tomcat and webapps 

3. To install Tomcat  Jmx parameters with Jmxgateway I added to server.xml 

<Listener className="org.apache.catalina.mbeans.JmxRemoteLifecycleListener" rmiRegistryPortPlatform="12345" rmiServerPortPlatform="12346" />

3. Edited tomcat.conf  JAVA_OPTS="${JAVA_OPTS} -Djava.rmi.server.hostname=IP of agent -Dcom.sun.management.jmxremote -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.ssl=false"

also I downdloaded wget https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.70/bin/extras/catalina-jmx-remote.jar
to /usr/share/tomcat/lib and start tomcat service

4. On server:
    
yum install zabbix-java-gateway

nano /etc/zabbix/zabbix_server.conf

- JavaGateway=127.0.0.1

- JavaGatewayPort=10052

- StartJavaPollers=5 

After:

service zabbix-server restart

service zabbix-java-gateway start
