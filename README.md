# Ansible 部署RabbitMQ 集群
# [源码出自Github项目alexey-medvedchikov/ansible-rabbitmq ](https://github.com/alexey-medvedchikov/ansible-rabbitmq)
### 该项目只支持集群部署，并做了以下改动：
* 根据定义的hosts组，动态生成集群
> 比如 你的hosts文件如下：  
[rabbitmq]  
sdevrmq01.example.com   
sdevrmq01.example.com  
sdevrmq01.example.com    
你的site.yml hosts指定组为  
hosts: rabbitmq   
那么次roles将以该组主机建立集群，并且选择集群中的第一台机器作为master节点。 
