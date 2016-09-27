MTN.*NIX.11 Zabbix
---

***Student***: [Uladzislau Charches](https://upsa.epam.com/workload/employeeView.do?employeeId=4060741400038705754#emplTab=general)

# Zabbix_Task1

My additional files: 

[Vagrantfile](Vagrantfile)

[provision.yml](provision.yml)

[main.yml](roles/zabbix/tasks/main.yml)

**Command for zabbix_sender**
zabbix_sender -z 127.0.0.1 -s "Zabbix server" -k "system.cpu.load[percpu,avg1]" -o 234 -vv

**Command for zabbix get**

zabbix_get -s 127.0.0.1 -p 10050 -k system.swap.size[,pfree]

zabbix_get -s 127.0.0.1 -p 10050 -k system.cpu.util[,system]


![1](https://github.com/VladCharches/Zabbix/blob/Task1/screens/1.png)
![2](https://github.com/VladCharches/Zabbix/blob/Task1/screens/2.png)
![3](https://github.com/VladCharches/Zabbix/blob/Task1/screens/3.png)
![4](https://github.com/VladCharches/Zabbix/blob/Task1/screens/4.png)
![4.2](https://github.com/VladCharches/Zabbix/blob/Task1/screens/4-2.png)
![5](https://github.com/VladCharches/Zabbix/blob/Task1/screens/5.png)
![7](https://github.com/VladCharches/Zabbix/blob/Task1/screens/7.png)
![8](https://github.com/VladCharches/Zabbix/blob/Task1/screens/8.png)
